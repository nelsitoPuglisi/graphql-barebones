# OL GraphQL Onboarding Project
Please create a new repository and use this codebase to get your application development started.

# Commands
* `yarn start:dev` USE THIS FOR LOCAL DEVELOPMENT. It will start the server and watch for every change made in the code. This way you don't have to rebuild everytime you change something.
* `yarn build` transpile our typescript source into javascript in the `build/` folder
* `yarn start` build and then start the server
* `yarn test` runs the tests with jest.

# Requirements
A few rules that you need to consider when iterating through the requirements:
* Do TDD
* And more TDD
* And even more TDD
* Force yourself to write the test first
* Create the following kinds of tests: unit, integration (these should use mocked/stubbed data), e2e (these should use a Database that you can teardown and recreate before each test). Respect the test pyramid.
* Design your application applying Clean Architecture, Clean Code and Sandro Mancuso's IDD principles.

# Important
If you have limited time to complete this training, please skip Iterations 0 and 1 and start directly with Iteration 2. If you have time please complete Iterations 0 and 1 too.

## Iteration 0
* Add docker to the project to start the server and a database of your preference. Make it in a way that you can start both the server and database in one command.
* Set up CI pipelines to make sure all the tests pass and that the typescript code is valid. Configure the repo so no one can push directly to master and every change needs to be added via a Merge Request. 

## Iteration 1
* Create a signup mutation that returns a response containing a JWT
* Create a login query that returns a response containing a JWT

## Iteration 2
* Register at https://developers.themoviedb.org/ and get an API key
* Create a `tvShows` query that accepts a `title` parameter. Use themoviedb.org API to search for the first page of TV Shows based on the `title` parameter and return the results. Return the following information from a TV Show: title, firstAirDate, voteAvg. API documentation: https://developers.themoviedb.org/3/search/search-tv-shows

## Iteration 3
* Create a `movies` query that accepts a `title` parameter. Use themoviedb.org API to search for the first page of Movies based on the `title` parameter and return the results. Return the following information from a movie: title, releaseDate, voteAvg. API documentation: https://developers.themoviedb.org/3/search/search-movies

# Iteration 4
* Restrict access to authenticated users: create a GraphQL Directive that can be applied to a query or mutation and have that directive validate that only authorized users can use them. Apply this directive to the queries created in Iteration 2 and 3.

# Iteration 5
Add a new query named `seasons` under the `tvShows` query. When a client requests for the seasons of a tv show you can use this API to fetch the data: https://developers.themoviedb.org/3/tv-seasons/get-tv-season-details

# Iteration 6
Add a new query `credits` under `movies`. When a client requests for the credits of a movie you can use this API to fetch the data: https://developers.themoviedb.org/3/movies/get-movie-credits. Make sure to only return the first 10 crew and cast members.

# Iteration 7
Add pagination to your `tvShows` and `movies` queries.# graphql-barebones
