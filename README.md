# Sample Media (VOD) App

This is a sample media app to demonstrate media functionality in the context of a Progressive Web App.

## Follow along

The build of this site is being cataloged on YouTube as part of the
[Chrome Developers Developer Diary](https://www.youtube.com/playlist?list=PLNYkxOF6rcIBykcJ7bvTpqU7vt-oey72J) series.

## Running the site locally

1. Clone the repo
1. `cd sample-media-pwa`
1. `npm install`

### Setting up some secrets.

Once the entire internet has been cloned into your `node_modules` folder you'll need to create
`src/config`, into which you will need to place a couple of files: `oauth.js` and `session.js`.
These are files which contain secrets and keys, so you can either
[create the appropriate values](https://cloud.google.com/nodejs/getting-started/authenticate-users),
or you can put some placeholder info in:

```json
// oauth.js
module.exports = {
  clientID: 'lolztehclientid',
  clientSecret: 'suchhiddenmanysecretwow',
  callbackURL: 'http://localhost:8080/auth/google/callback',
  accessType: 'offline'
};
```

```json
// session.js
module.exports = {
  resave: false,
  saveUninitialized: false,
  secret: 'totallyasecret',
  signed: true,
  memcacheURL: 'localhost:11211'
};
```

Finally, with that done you should be able to run: `npm run dev`.

Fair warning, though: the videos (which can only be described as huge) are not included in the repo,
so again you'll need to make some placeholder content for those.