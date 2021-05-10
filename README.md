# Precheck
Code for Precheck project website, live at https://crsuzh.github.io/Precheck/.

## HOWTO

## Preparation
- The software hugo can be installed using brew. If brew is not installes in OS X, install homebrew first.

```
brew install hugo
```

- Create a local copy of the website were changes will be made.

```
git clone --recurse-submodules git@github.com:crsuzh/SwissRN.git
```

or

```
git clone --recurse-submodules https://github.com/crsuzh/SwissRN.git
```

## Editing website

- Checkout last version with `git pull`

- Global settings are in `config.yaml` as well as the menu items. See folder `content` additonal pages.

- Start local webserver to see changes, assuming project folder is names Precheck.
```
cd Precheck
hugo server
```

Page can be seen at http://localhost:1313/.

## Images

Images are in the folder `content/img`. Examples for correct paths are:
- For `config.toml` use `./img/logo.jpg`.
- Für other pagets in `content` use path `./../img/image.jpg`

## Publish webpage

- Run the command `hugo`. Die full webpage is created in the folder `docs`. To start from scratch, the two folders `docs` and `ressources` can be deleted when necessary (e.g. for a total cleanup when something is not working), as these folder and their content are always recreated with `hugo`. 

```
cd SwissRN
hugo
```

- Check what files have changed.

```
git status
```

- Publish website in `docs` and changes in `content` or other files.

```
git add --all docs
git add config.toml
git commit -m "my comment about the changes made."
git push
```

Now changes are online.
