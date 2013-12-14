# s3-buildpack

This is an experimental Heroku buildpack that uploads your static site to S3.

## Usage

1. Go set up a [static website S3 bucket](https://console.aws.amazon.com/s3/home?region=us-east-1).
1. Put an index.html file in the root of your app.
1. Configure stuff:

```
heroku labs:enable buildpack-env-arg # this will go away soon
heroku config:set \
  BUILDPACK_URL=https://github.com/zeke/s3-buildpack \
  S3_BUCKET=foo \
  S3_ACCESS_KEY_ID=bar \
  S3_SECRET_ACCESS_KEY=baz
```

There is no step 4.