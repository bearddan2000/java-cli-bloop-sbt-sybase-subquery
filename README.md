# java-cli-bloop-sbt-sybase-subquery

## Description
Creates a small database table
called `dog`. This table, `dog`, has been normalized to 3NF.
Two new tables have been added, `breedLookup` and `colorLookup`.
Creates a new table `dog_expanded` that joins
`dog`, `breedLookup` and `colorLookup`. Added clustered indexes on
`dog`.breedId and `dog`.colorId and a non-clustered index for
`dog_expanded`.id. Turned `dog_expanded` into a view with an
implicit index on `dog_expanded`.id. Using a subquery with the aggregate function
COUNT, create a new view `breed_count`. 

Compiled and ran from build server `bloop`.

# Build note
Dependencies must be compatable with jdk8 or less.

## Tech stack
- bloop
- java
- bloop-sbt
  - log4j
  - sybase driver

## Docker stack
- hseeberger/scala-bloop-sbt:11.0.2-oraclelinux7_1.3.5_2.12.10
- mariadb:latest

## To run
`sudo ./install.sh -u`

## To stop
`sudo ./install.sh -d`

## For help
`sudo ./install.sh -h`

## Credit
https://github.com/htorun/dbtableprinter