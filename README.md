# Boris Bikes

- Boris Bikes challenge

## Motivation

- TDD pair programming challenge in the first week of Makers.

## Code style

- Test-driven development
- Pair programming with a different cohort member daily. Visit credits to view those that contributed.

## Screenshots

## Tech/framework used

- VS Code
- GitHub

## Built with

- Ruby

## Installation

- Provide step by step series of examples and explanations about how to get a development env running.
- rspec
- bundle

## Tests

- The fist test was written to determine if rspec works
- Test whether methods exist
- Test whether the bike is released
- Test whether the bike can be docked
- Test whether fail works when dock empty or dock full

## How to use?

## If people like your project they’ll want to learn how they can use it. To do so include step by step guide to use your project.

#### Challenge 2 : From User Stories to Domain Model

User stories

| User Story   | As a User              | I want to                                                               | So that I can                                        |
| ------------ | ---------------------- | ----------------------------------------------------------------------- | ---------------------------------------------------- |
| User Story 1 | As a person            | I'd like a docking station to release a bike.                           | So that I can use a bike                             |
| User Story 2 | As a person            | I'd like to see if a bike is working.                                   | So that I can use a good bike                        |
| User Story 3 | As a system maintainer | I'd like docking stations not to accept more bikes than their capacity. | So that I can control the distribution of bikes      |
| User Story 4 | As a system maintainer | I want a docking station to have a default capacity of 20 bikes.        | So that So that I can plan the distribution of bikes |

| Objects         |     Messages |
| :-------------- | -----------: |
| person          |              |
| docking station | release bike |
| bike            |     working? |

#### Visual Representation of how objects communicate

docking_station --> release_bike --> bike --> person
person --> working? ---> use_bike

#### Challenge 3: From a Domain Model to a Feature Test

From irb run:

3.0.0 :001 > docking_station = DockingStation.new created this error:

Result: NameError (uninitialized constant DockingStation)

#### Challenge 4: Errors are good

**Type of Error:** NameError
**File path:** /Users/username/.rvm/rubies/ruby-3.0.0/bin/irb:11:in '<main>'
**Line Number:** 1
**What does it mean?** It means that the name is undefined, we have not defined our class yet
**How to solve it?** Define the class DockingStation in the application file

#### Challenge 5: From Feature Tests to Unit Tests

Task: write a failing unit test which would give you a similar error message to the feature test we ran from irb previously.

To complete this step, we perform the following:

- Initialise RSpec within your project
- Create a new spec file for your DockingStation object
- Set up the spec file to describe a DockingStation
- Run RSpec from the Command Line

#### Challenge 6: Passing your first Unit Test

Created a new file inside lib directory for DockingStation class, and defined the class. Used 'require <file>' to link the file to the spec file.

#### Challenge 7: Back to the feature

Run the following feature_test from Irb:

3.0.0 :003 > docking_station.release_bike

Error: NoMethodError (undefined method `release_bike' for #<DockingStation:0x00007fb9fca8f490>)

**'what is the error telling me to do next?'**

To define 'release_bike' method inside my newly created DockingStation class so we can use it with its instances

#### Challenge 8: Back to the unit

Now we repeat the cycle again:

1. We run feature test from the command line
2. We write a unit test for the unit of behavior, in this case, release_bike method, in our spec file (Note: this is a failing test, and it will fail in the same way as our feature test).
3. Then we make our unit test pass by adding the simplest code possible - in this case, by defining our release_bike method inside the DockingStation class.

#### Challenge 9: Building a bike

Again, follow these steps

1. Feature test the bike object to see if it is running, i.e, run bike = docking_station.release_bike from irb, which gives us nil. Then run bike.working?, which will give us error message.
2. Read the following error message:
   NoMethodError (undefined method `working?' for nil:NilClass)

_What does it tell us?_

That our bike object does not exist - it is nil!

3. Create a spec file with the unit test describing the Bike class and run it

4. Make it pass in the simplest way possible by changing the code in our newly created application file (i.e. bike.rb)

## Credits

- Maria Valero
- Jenny Bell
- Dewald Viljoen
