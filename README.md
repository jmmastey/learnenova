LevelUpRails [![codebeat badge](https://codebeat.co/badges/db618adb-34dc-48d0-9536-5c18391e89ef)](https://codebeat.co/projects/github-com-jmmastey-level_up)
=========

An app to store and verify training material for engineers on the [Rails Prime Stack](http://words.steveklabnik.com/rails-has-two-default-stacks). Currently hosted at http://leveluprails.com.

Your Help Wanted
---------------
Hey there. If you're reading this, I'd welcome and appreciate your contributions on the project. Even if you feel like you're not ready to contribute to an open source repo. If that's the case for you, open up a new issue and we'll find something that works for your skill level. You're not an impostor, and we're here to help.

Getting Started
---------------

Clone the repo, bundle install, create db, run rake to test. Deploy at will.
There is a Procfile provided for foreman. Feel free to create a `.env` file
for the environment. Some content modules may not be stored in source control
for competitive purposes.

    bundle install
    bundle exec rake db:{setup,seed}
    foreman start

Proprietary Content Support
---------------------------

LevelUp now supports proprietary courses for users from organizations. While the intention is to share as much as possible, it's useful to have one platform that also covers internal projects. the production site uses private gems with Rails Engines to mount the additional content. Users, courses, and categories can all have organization flags on them, which render them invisible to anyone outside those orgs.

Update Certificate
------------------
Cert provided by LetsEncrypt. Update as follows:

    sudo certbot certonly --manual
    heroku config:set LETS_ENCRYPT_CODE=some_value
    sudo heroku certs:update /etc/letsencrypt/live/leveluprails.com-0001/fullchain.pem /etc/letsencrypt/live/leveluprails.com-0001/privkey.pem

Contributing
------------

Contributions are very welcome. Fork, fix, submit pulls.

Contribution is expected to conform to the [Contributor Covenant](https://github.com/jmmastey/level_up/blob/master/CODE_OF_CONDUCT.md).

Credits
-------

See [the humans file](public/humans.txt) for information on helpful humans.

Some icons are used via the Noun Project. We bought a license but here's attribution anyway, because we like them:
- [Map](https://thenounproject.com/term/map/96666/), by Lloyd Humphreys, DK
- [Quiz](https://thenounproject.com/term/quiz/117740/), by carlos sarmento
- [Books](https://thenounproject.com/term/books/137857/), by Jakub Čaja
- [Signpost](https://thenounproject.com/term/signpost/116372/), by Creative Stall

License
-------

This software is released under the [MIT License](https://github.com/jmmastey/level_up/blob/master/MIT-LICENSE).
