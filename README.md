# Precheck
Code for Precheck project website, live at https://crsuzh.github.io/Precheck/.

## HOWTO

## Preparation
- The software hugo can be installed using brew. If brew is not installed in OS X, install homebrew first.

```
brew install hugo
```

- Create a local copy of the website were changes will be made.

```
git clone --recurse-submodules git@github.com:crsuzh/Precheck.git
```

or

```
git clone --recurse-submodules https://github.com/crsuzh/Precheck.git
```

## Editing website

- Checkout last version with `git pull`

- Global settings are in `config.yaml` as well as the menu items. See folder `content` additional pages and posts. The content of the front page is in `layouts/lists.html`

- Start the local webserver to see changes, assuming the project folder is named Precheck.
```
cd Precheck
hugo server
```

Page can be seen at http://localhost:1313/Precheck/.

## Images

Images are in the folder `static/img`. Examples for correct paths are:
- For other pages in `content` use path `../images/logo_uzh.png`

## Publish webpage

- Run the command `hugo`. The full webpage is created in the folder `public`. However, a copy of this folders needs to be created named `docs` (requirement by GitHub pages). (Do not simply replace delete the old docs folder, but rather update all the documents from public into `docs`, otherwise you will lose the CNAME file.)

```
cp -a public docs
```

To start building from scratch, the folders `docs`, `public` and `ressources` can safely be deleted when necessary (e.g. for a total cleanup when something is not working). These folders and their content will always be recreated with the command `hugo`.

```
cd Precheck
hugo
```

- Check what files have changed.

```
git status
```

- Publish website in `docs` with `git`. Do not forget to also submit all other changes as well.

```
git add --all docs
git add config.yaml
git commit -m "my comment about the changes made."
git push
```

Now changes are online and can be seen after a few minutes.
