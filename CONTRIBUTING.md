Contributing guidelines
=======================

- Issue reporting
- Code submissions
- Code style
- License agreement

Issue reporting
---------------

PROJECT is officially hosted on GitHub at https://github.com/USER/PROJECT.  
Please report all issues to the [issue tracker](https://github.com/USER/PROJECT/issues)

Code submissions
----------------

PROJECT follows the [git flow](http://nvie.com/posts/a-successful-git-branching-model/) model.  
Read more about the workflow for a [pull request](https://help.github.com/articles/using-pull-requests).

Fork it
-------

Fork the project https://github.com/USER/PROJECT/fork into your GitHub account

```
$ git clone git@github.com:USER/PROJECT.git
$ git remote add upstream https://github.com/USER/PROJECT
```

Make your contribution
----------------------

```
$ git checkout develop
$ git checkout -b feature-branch
$ git add <the files you modified>
$ git push origin feature-branch
```

Try your best to make great commit messages.  
Check out [better commits](http://web-design-weekly.com/2013/09/01/a-better-git-commit) and use `git add -p`.

Submit your pull request through GitHub
---------------------------------------

Select the branch on your fork, click the green PR button and submit it.

Keep your fork updated
----------------------

You should do this before making any commits and after your PR has been accepted.
```
$ git checkout develop
$ git fetch upstream
$ git rebase upstream/develop
$ git push origin develop
```

License agreement
-----------------

By contributing you agree that these contributions are your own
(or approved by your employer) and you grant a full, complete, irrevocable
copyright license to all users and developers of the project, present and
future, pursuant to the license of the project.