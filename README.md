# Object Relations Code Challenge

For this assignment, we'll be working with an Uber-style domain. We have three models - Driver, Customer, and trip. For our purposes, a Driver has many trips, a Customer has many trips, and Driver - Customer is a many to many relationship.

If you are not sketching out your domain, and thinking about single source of truth, you are doing it wrong :(


## Notes

Your goal is to build out all of the methods listed in the deliverables. Do your best to follow Ruby best practices. For example, use higher-level array methods such as `map`, `select`, and `find` when appropriate in place of `each`

We've provided you with a console that you can use to test your code. To enter a console session, run `ruby tools/console.rb`. You'll be able to test out the methods that you write here.


## Deliverables

Build the following methods on the customer class
+ Customer.all
  + should return all of the customers
+ Customer.find_by_name(name)
  + given a string of a full name, returns the first customer whose full name matches
+ Customer.find_all_by_first_name(name)
  + given a string of a first name, returns an array containing all customers with that first name
+ Customer.all_names
  + should return an array of all of the customer full names
+ Customer.trips
  + should return all of the customer's trips
+ Customer.drivers
  + should return all of the drivers the customer has ridden with
+ Customer#request_trip(driver, distance)
  + given a distance and a driver, creates a new trip and associates it with that customer and that driver
  + distance should be represented by a number

Build out the following methods on the Trip class

+ Trip.all
  + returns all of the trips
+ Trip#customer
  + returns the customer for that given trip
+ Trip#driver
  + returns the driver for that given trip
+ Trip#distance
  + returns the distance for that given trip

Build out the following methods on the Driver class

+ Driver.all
  + returns an array of all drivers
+ Driver.find_by_name(name)
  + given a string of driver name, returns the first driver that matches
+ Driver#trips
  + returns an array of all trips for that driver
+ Driver#mileage
  + returns an the sum total distance of all the trips the driver has made
