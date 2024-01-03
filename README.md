# animal_data_vet
We are going to create a file owner.rb which defines the Owner class with attributes @name and @animals. That attribute @animals is what holds the relationship and to manage it we will also create a method add_animals to add animals to it. So this class ends up looking like this

# Upcoming improvements:

- `Improve the app to include more fields`.
- `Buying of medicines`
- `Permission of owners to keep pets`
- `Create a Kanel`
- `Preserve DATA`
- `Unit tests`

require "./animal.rb"
require "./dog.rb"
require "./spider.rb"
require "./owner.rb"
require "./visit.rb"
require "./vet.rb"

dog = Dog.new("black", "Rax")
spider = Spider.new(85, "Bob")

vet_maria = Vet.new("Maria", "New York")
vet_john = Vet.new("John", "San Francisco")

visit_1 = Visit.new("2017-12-22", dog, vet_maria)
visit_2 = Visit.new("2017-12-31", dog, vet_maria)

dog.visits.count
dog.visits.map { |visit| visit.date }
vet_john.visits.count
vet_maria.visits.count
vet_maria.visits.map { |visit| visit.animal.name }

visit_3 = Visit.new("2017-11-11", spider, vet_john)
visit_4 = Visit.new("2017-10-10", spider, vet_maria)

spider.visits.count
spider.visits.map { |visit| visit.date }
vet_john.visits.count
vet_john.visits.map { |visit| visit.animal.name }
vet_maria.visits.count
vet_maria.visits.map { |visit| visit.animal.name }
