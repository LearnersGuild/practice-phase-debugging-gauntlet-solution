# Solution to Learners Guild Debugging Gauntlet

## Links

[Learners Guild Debugging Gauntlet Challenge Repo](https://github.com/LearnersGuild/practice-phase-debugging-gauntlet)

## Bugs to Fix

- `views/partials/footer.ejs`
  - refers to wrong .js file name (script.js instead of pets.js)

- `actions/getOwnersByPetId.js`
  - query uses wrong column name (o.id instead of o.owner_id)

- `routes/pets.js`
  - imports nonexistent function from actions index.js (getOwnersById instead of getOwnersByPetId)
  - getting petId from wrong object (req.query instead of req.params)
  - getOwnersBy(Pet)Id does not have argument passed (should have petId argument passed)

- `public/pets.js`
  - onclick event listener attached to wrong class (.pet instead of .pet-name)
  - petOwnerDiv identified by class instead of id
  - .pet-name onclick arrow function doesn't bind "this" (needs to be non-arrow function)
  - fetch does not use `.then(response => response.json())` to transform stream response body into object