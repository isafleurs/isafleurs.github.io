#Isafleurs blog
Bloggin platform with [Ghost](https://ghost.org/) deployed with [Buster](https://github.com/axitkhurana/buster/) 

Blog code is maintained on a bitbucket repo.



##Running the project locally
Run `npm start` to start ghost

Open `http://localhost:2368`

Admin is located here : `http://localhost:2368/admin`


##Setup buster

We use buster to deploy to github pages.

`setup buster --gh-repo=<github-repo-url>`

This will create a git repo inside `your/site/static`. This is where buster will generate all your ghost static files before getting push to `<github-repo-url>` on branch master.


`add-domain isafleurs.ca`

 Adds CNAME file with custom domain name as required by Github Pages.

##Deploy


`buster generate --domain=http://127.0.0.1:2368`

Ghost port is generally `2368` but you can change this to fit your needs.

`buster deploy`

Buster push the newly generated content to remote branch `master`.

*Make sure that a CNAME is located in static folder. Github pages needs it to find your blog. It should contain a single line with this : `isafleurs.ca`*

Note: Changes can take up to 10 minutes to show up. So don't panic just yet.
