# Get Involved

The goal of PPB is to be a learning tool. Building games can be complex, and
PPB should make that complexity approachable for new developers. It is also
open to developers of all skill levels for contribution and improvement.

This guide will include steps experienced developers may not need explanation
for, it's target audience is new developers not used to contribution.

## Before You Begin

1. Read the [README][readme].
2. Read the [Code of Conduct][coc].
   - All contributors must abide by the current code of conduct.
   - The current code of conduct is the [Contributor's Covenant][covenant].
3. Familiarize yourself with this guide!

## I've Never Coded Before

`ppb` doesn't include tools to get you from a proper zero to running.
Check out something like [Automate the Boring Stuff][auto] or ask a
teacher for a resource to learn with.

## I Don't Know How To Start

The best place to start is to build something with `ppb`! Joining the
community of developers who are using it and asking questions is a great
place to start. Read the tutorials written by ppb and others, and keep
notes: any time you do something that feels rough or seems to be harder
than you'd like, take a note!

## I Don't Like How This Works

After you're comfortable using `ppb` it's time to join the discussions.
We try to keep discussions public on github, and label any issue meant
to be a discussion with the [discussion label][discuss]. Your opinion
matters, and you might notice something no one else has. If you don't
like what it's like to use `ppb`, talk about it with us, and we can try
to find a solution together.

## I Found A Bug

Good news: You already know where the issue tracker is, report your bug
by adding a [new issue][issues] to the github page! Your report should
focus on the problem: What broke? What didn't work the way you expected?
How did you expect it to work?

In addition to that, we'll want to know how you got there: A link to
your code, any packages you used with ppb, and a stack trace if there is
one! Definitely remember to get the python version with `python --version`.

Label it with the label `bug` and one of the contributors will get to it
soon!

## I Have A Suggestion

Same as with bugs, head on over to the [issue tracker][issues] and
write up an issue describing what you want to improve, and how you'd do
it.

Remember to consider the [goals and principles of ppb][goals]. We want
to leave enough for people to explore on their own, but solve enough of
the hard problems that they're free to do that.

## I Want To Code

Thanks for considering code contributions! The [new contributor label][new contributor]
is a collection of issues we believe are suitable for people new to PPB.
You are welcome to work on any issue you would like, we just think those
are a good starting place for those that are unfamiliar with the code base.

You need to [fork ppb][fork]. This creates a copy of the ppb repository under
your GitHub account. You'll push changes there and create a pull request (PR) to
the main ppb repository once your contribution is ready.

Then you need to clone the repository and set up a Python virtual environment
(sometimes referred to as "venv" or "virtualenv"). This is where you'll install
ppb's dependencies, as well as ppb itself in "editable mode". Editable mode
means that as you make changes to ppb, you don't need to reinstall it in order
for Python to "see" those changes.

Replace `{username}` in the `clone` command below with your GitHub username.

```
git clone https://github.com/{username}/pursuedpybear
cd pursuedpybear
git remote add upstream https://github.com/ppb/pursuedpybear
python3 -m venv .venv
source .venv/bin/activate
pip install --upgrade -r requirements-tests.txt
pip install --editable .
```

The `git clone` command created a "git remote" pointing at your fork. The
`git remote` command added another remote called "upstream" with points to the
official ppb repository.

Editors like VS Code or PyCharm know how to use the `.venv` automatically. If
you open a new terminal though, you'll need to activate it again with the
`source .venv/bin/activate` command.

Find a ticket your like, such as one labeled [new contributor][]. Create a
branch off of `canon` with a descriptive label, such as a word that summarizes
the change.

```
git switch -c my-fix canon
```

Now get to work! Some tickets have detailed instructions: A maintainer
mapped out the needs and wrote some instructions. Others are more open.
Start working, try to solve the problem. If you get stuck, ask
questions in your open PR. The maintainers and active contributors are
here to help.

You can add your name, and optionally email and social media link, to
the [`CONTRIBUTORS.md` file][contributors] as part of your first PR.

Once you've made some changes, push them to a branch on your fork:

```
git push origin my-fix
```

Go to the ppb repository, the pull requests tab, and click the green
"New pull request" button. There are two dropdowns, the left is the
target, "canon", and on the right select your branch. Reference the
issue your PR is addressing in the body, like `fixes #{issue}`, and 
describe the change a bit. Make a [draft pull request][draftpr] or
include "WIP" in the title.

You can keep working and pushing more commits. As you work, you can make
sure the tests pass by running `pytest`. It was installed as part of
installing `requirements-tests.txt` above.

```
pytest
```

Tests for a lot of supported platforms will also be run as you push
commits to your PR. If any fail, you can click to see the logs and what
error came up.

Once you think it's ready, press the "Ready for review" button on your draft PR,
or remove "WIP" from the title. Now someone senior in the project will
review. They'll either ask for changes or approve your PR. If you need
to make changes, commit to your branch and push it up and it'll update
the PR. Your reviewer will look again later.

If you got accepted, your PR will make it into the project soon! Only a
maintainer can merge your PR, so you'll need to wait. They may ask for
some final changes. Same rules as before: Push new changes to your
branch and things will be updated.

## Can I Review

You're always welcome to review other PRs! Just use the comment function
unless you're told you can block PRs. The people doing the "official"
review will take your comments into consideration. If you actively
provide reviews, you'll be told to add your name to
[CONTRIBUTORS][contributors] as a reviewer!

## Can I Contribute Without Code?

There's so much else that needs to be done besides fixing `ppb`'s code.
We need documentation. Docstrings or [the docs folder][docs] are
available to be added to. Our test suite could use some love. In the
end you contribute to `ppb` by being part of its community.

[auto]: https://automatetheboringstuff.com "Automate the Boring Stuff"
[coc]: https://github.com/ppb/.github/blob/canon/CODE_OF_CONDUCT.md "Code of Conduct"
[contributors]: https://github.com/ppb/pursuedpybear/blob/canon/CONTRIBUTORS.md "Contributors"
[covenant]: http://contributor-covenant.org/ "Contributor's Covenant"
[discuss]: https://github.com/ppb/pursuedpybear/issues?q=is%3Aissue+is%3Aopen+label%3Adiscussion "PPB Discussions"
[docs]: https://github.com/ppb/pursuedpybear/tree/canon/docs "PPB Docs"
[draftpr]: https://github.blog/2019-02-14-introducing-draft-pull-requests/ "Introducing draft pull requests"
[fork]: https://help.github.com/articles/fork-a-repo/ "Fork a repo"
[goals]: https://ppb.dev/#guiding-principles "PPB Goals"
[issues]: https://github.com/ppb/pursuedpybear/issues "PPB Issues"
[new contributor]: https://github.com/ppb/pursuedpybear/labels/new%20contributor "Issues labeled New Contributor"
[projects]: https://github.com/orgs/ppb/projects "PPB Projects"
[readme]: https://github.com/ppb/pursuedpybear/blob/canon/README.md "PPB README"
