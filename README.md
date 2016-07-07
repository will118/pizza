# Shell script for tracking Dominos UK

![pizza](https://github.com/will118/pizza/raw/master/pizza.gif)
(In the actual script a dot is 10seconds)


When you click track pizza on the website the URL has a base64 encoded string in the URL.

```
./pizza.sh MTU3MTI1MjU5fDY5ZjlhOTYyLWVhOGUtNGRhZi04MTI2LTIyYmVjODVmZDhkYg==
```
For those interested it decodes to:
```
157125259|69f9a962-ea8e-4daf-8126-22bec85fd8db
```

I think the first number is the store id, but I haven't checked.

Anyway the Dominos tracker updates too slowly, and doesn't have any info about when it transitioned from state to state.

So I made a node script which piped stuff into `toilet` and would check every n seconds.

I thought it'd be nice to have one that didn't have any dependencies, so I (hacked together a shell script,) hardcoded some toilet outputs in and only used basic shell stuff (i.e. no bash/zsh as far as I know).
