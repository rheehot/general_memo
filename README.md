# Git memo
##### Set always commit for merge
```
$ git config --global --add merge.ff false
```

##### Remove all untracked files and folders
```
$ git clean -fd
```

##### Change previous commit history
```
$ git rebase -i --root
$ git commit --amend
$ git rebase --continue
```

##### Check git log graph
```
$ git log --graph --oneline
```

# Rails memo
##### Rails new default option set
- postgresql default database / not using minitest / skip coffee auto generating
```
# ~/.railsrc
--database=postgresql
-T
--skip-coffee
```

##### After rails new with postgresql
```
$ rails db:create
$ rails db:migrate
```

##### After setting back-end environment, check working
$ curl -H "Content-Type: application/json" -X POST -d '{"username":"1st_user","password":"foobar"}' http://localhost:3001/login

$ curl -H "Content-Type: application/json" -X POST -d '{"username":"2nd_user","password":"foobar"}' http://localhost:3001/login

##### Push heroku
```
$ heroku git:remote -a [name of heroku app]
$ heroku run rails db:migrate
$ heroku run rails db:seed
```

##### Rubocop code style check
- Choose the option one of this below
```
$ rubocop -x
$ rubocop --auto-correct
```

- Make exception
```
$ rubocop --auto-gen-config  
```

##### Postgresql restart
```
$ sudo service postgresql restart
```

##### Server restart
```
$ ps -aef | grep rails    
$ kill -9 [pID]   
```

##### Rails console save error
```
> p.errors.messages
```

##### Heroku rails app image not showing
- config > environments > production.rb
```
config.assets.compile = true
config.assets.digest = true
```

##### heroku server reset
```
$ heroku pg:reset DATABASE
```

##### Haml
- [tutorial](http://haml.info/tutorial.html)

##### Nested form
- with stimulus

##### Active Storage
- [tutorial](shorturl.at/ehOX2)

##### Rails 6 connect bootstrap
- [tutorial](https://www.youtube.com/watch?v=bn9arlhfaXc)

# General memo
##### Get some dummy texts
```
https://hipsum.co
```

# CSS memo
##### gradient picker
- https://uigradients.com

##### css 3 generator
- https://css3generator.com/

##### float with clearfix
```
<div class="clearfix">
  <div class="float-left">
  </div>
</div>

.clearfix:after {
   content: ".";
   visibility: hidden;
   display: block;
   height: 0;
   clear: both;
}
```
