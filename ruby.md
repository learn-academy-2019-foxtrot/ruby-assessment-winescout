# ASSESSMENT 4: INTRO TO RUBY
## Interview Practice Questions

Answer the following questions. First, without external resources. Challenge yourself to answer from memory. Then, research the question to expand on your answer. Even if you feel you have answered the question completely on your own there is always something more to learn.   

1. In what ways are JavaScript and Ruby similar? In what ways are they different?

  Your answer:
  
  Similar:  OO (both can be programmed functionally as well (javascript moreso))
  Similar: interpreted rather than compiled
  Similar: Dynamic
  Similar: We use frameworks in both (React, Rails)
  
  Difference:  Js optimized for Browser
  Difference: Speed doing certian task
  Difference: Js has const, let, var
  


  Researched answer:



2. What is a hash?

  Your answer:
  
  Key value pair collection
  Used to store collection of grouped information.
  represent objects
  
  
  bike = {
    number_of_tires: 2,
    number_of_inflated_tires: 1,
    rides: [
      {
        day: "January 1st.",
        city: "Portland, OR"
      },
      {
        day: "January 2nd.",
        city: "Corvalis, OR"
      }
    ]
  }

  Researched answer:



3. What is the testing framework used in Ruby? Describe the process of setting up the testing environment.

  Your answer:
  rspec, 
  minitest (if you're old school)

  Researched answer:
  gem install rspec
  
  (In Rails)
  rails new BikeTireBlowout -T  (the -T means no testing, so we can add our own)
  gem install rspec-rails
  rails generate rspec:install


Note::::
We use this to create a new rails app
rails new BikeTireBlowout -T --database=postgresql
- OR -
rails new BikeTireBlowout -T -d postgresql

Those are the same, and just mean use Postgres as the DB for this project, otherwise you'll get SQlite3, which is awesome, but not as awesome as Postgres.


4. Name three possible relationships between objects?

  Your answer:
  has_one
  
  has_many
  has_many :through
  
  belong_to
  is_a


  class Person
    has_many :hands
    has_many :fingers, through: :hands
  end
  
  class Hand
    has_many :fingers
  end
  
  class Finger
    belongs_to :hand
    
    def initialize
      # This is an instance variable.  It is available across methods
      # in an instance of Finger.
      @ring_finger_has_ring = false
    end
    
    def put_a_ring_on_it
      @ring_finger_has_ring = true
    end
  end
  
  
  
  Researched answer:



5. What is an instance variable? How is it different from other variables in Ruby?

  Your answer:

  Researched answer:
  See above



6. Ruby has a great community and tons of free resources to help you learn. [Here](https://www.ruby-lang.org/en/documentation/)is a list of great resources. Below are a few popular ones:
- [Interactive Ruby Tutorial](http://tryruby.org/levels/1/challenges/0)
- [Why's (poigniant) Guide to Ruby](http://poignant.guide/book/chapter-1.html): comics, anecdotes, and microscopic canaries
- [Ruby in 20 Min](https://www.ruby-lang.org/en/documentation/quickstart/)
- [Ruby Style Guide](https://rubystyle.guide/)

Choose one of these resources and look through the material for 10-15 min. List three new things you learned about Ruby:

1) . Been around since 1991

2) . Symbols are elegant, and beautiful

3) . Comments on first line indicated to shell instructions.  use Ruby interpreter for example, or linting

4) . __FILE__ . refers to file it is execute in

5) Array comparrison is off the chain.  [1,2,3] | [1,4] == [1,2,3,4]

6) Class.instance_methods

7) Why Not gem.  It makes uncertiany certianly fun.



7. STRETCH: What are blocks, procs, and lambdas?

  Your answer:
  
  do 
    puts "this is a block"
  end

  { 
    puts "this is also a block"
  }
  
  lambda:
  ->(input){ puts "This is a proc #{input}" }
  # input is a variable passed in
  
  proc:
  Proc.new {|input| puts "this is a lambda #{input}" }
  
  
  Researched answer:
