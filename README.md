# telelian

hugo를 사용하여 github에 홈페이지를 만들려면 2개의 저장소가 필요하다.

- hugo 컨텐츠 관리용: https://github.com/iamlow/telelian
- 홈페이지 저장소: https://github.com/iamlow/telelian-gh-pages

## Install Hugo on mac

```sh
brew update
brew install hugo
```

### To verify 

```sh
hugo version
```

## Make a homepage

### Create a new site

```sh
hugo new site telelian
```

### Add a theme

```sh
cd telelian
git init
git submodule add https://github.com/devcows/hugo-universal-theme.git themes/hugo-universal-theme
cp -rf themes/hugo-universal-theme/exampleSite/* .
```

### Customize the theme

Open up config.toml in a text editor

### Run test

```sh
hugo server
```

### Set up repository

```sh
git add *
git commit
git remote add origin git@github.com:iamlow/telelian.git
```

#### For gh-pages

```sh
git submodule add -b master git@github.com:iamlow/telelian-gh-pages.git public
```

#### Push a repository

```sh
git push -u origin master
```

## Deploy

```sh
hugo
```

## References

- https://sabzil.org/hugo/
