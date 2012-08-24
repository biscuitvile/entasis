entasis
-------

Entasis provides a few neat methods for building a basic class. Handy for models without a database.

Example:

    class Person < Entasis::Base
      attributes :name, :age, :city

      def age=(years)
        @age = years.to_i
      end
    end

    hilda = Person.new(:name => 'Hilda', :age => '23', :city => 'Berlin')
    hilda.attribute_names # => ["name", "age", "city"]
    hilda.attributes      # => {"name"=>"Hilda", "age"=>23, "city"=>"Berlin"}
    anon = Person.new
    anon.valid?           # => false
    anon.errors           # => {:name=>["can't be blank"]}>


Note on Patches/Pull Requests
-----------------------------

* Fork the project.
* Make your feature addition or bug fix.
* Add tests for it. This is important so I don't break it in a  future version unintentionally.
* Commit, do not mess with rakefile, version, or history.
* Send me a pull request.


Author
------

Ingemar Edsborn (ingemar@xox.se)


Copyright
---------

Copyright (c) 2010 Ingemar Edsborn. See LICENSE for details
