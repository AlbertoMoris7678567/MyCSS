{
  "name": "p5.js Web Editor",
  "description": "The p5.js Web Editor is an in-browser editor for creative coding, specifically for writing p5.js sketches.",
  "repository": "https://github.com/processing/p5.js-web-editor",
  "logo": "https://p5js.org/assets/img/p5js.svg",
  "keywords": ["processing", "p5js", "p5.js"],
  "addons": [
    {
      "plan": "mongolab:sandbox",
      "as": "MONGO"
    },
    {
      "plan": "mailgun:starter",
      "as": "MAILGUN"
    }
  ],
  "env": {
    "API_URL": {
      "value": "/editor"
    },
    "AWS_ACCESS_KEY": {
      "description": "AWS Access Key",
      "value": "placeholder"
    },
    "AWS_SECRET_KEY": {
      "description": "AWS Secret Key",
      "value": "placeholder"
    },
    "AWS_REGION": {
      "description": "AWS Region for the S3_BUCKET",
      "value": "placeholder"
    },
    "EMAIL_SENDER": {
      "description": "The sending email address for transactional emails.",
      "value": "no-reply@mydomain.com"
    },
    "EMAIL_VERIFY_SECRET_TOKEN": {
      "description": "A secret key for...? Not sure where used.",
      "generator": "secret"
    },
    "EXAMPLE_USER_EMAIL": {
      "description": "The email address for the account holding the default Example sketches",
      "value": "examples@p5js.org"
    },
    "EXAMPLE_USER_PASSWORD": {
      "value": "hellop5js"
    },
    "GG_EXAMPLES_EMAIL": {
      "description": "The email address for the account holding the Generative Design Example sketches",
      "value": "benedikt.gross@generative-gestaltung.de"
    },
    "GG_EXAMPLES_PASS": {
      "value": "generativedesign"
    },
    "GG_EXAMPLES_USERNAME": {
      "value": "generative-design"
    },
    "GITHUB_ID": {
      "description": "The GitHub Client Id for sign in with GitHub support",
      "value": "placeholder"
    },
    "GITHUB_SECRET": {
      "description": "The GitHub Client Secret",
      "value": "placeholder"
    },
    "GOOGLE_ID": {
      "description": "The Google Client Id for sign in with Google support",
      "value": "placeholder"
    },
    "GOOGLE_SECRET": {
      "description": "The Google Client Secret",
      "value": "placeholder"
    },
    "NODE_ENV": {
      "value": "production"
    },
    "S3_BUCKET": {
      "desription": "Name of the S3 bucket for asset storage",
      "value": "placeholder"
    },
    "S3_BUCKET_URL_BASE": {
      "description": "S3 bucket URL base",
      "required": false
    },
    "SESSION_SECRET": {
      "description": "A secret key for verifying the integrity of signed cookies.",
      "generator": "secret"
    }
  },
  "scripts": {
    "postdeploy": "MONGO_URL=$MONGO_URI MAILGUN_KEY=$MAILGUN_API_KEY npm run fetch-examples:prod"
  }
}
