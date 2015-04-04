# Travis Elixir PLT Generator

Generate PLTs for your Elixir project, so you can run Dialyzer on Travis without
slowing your builds down.

Unless you have specific requirements, you should use these prebuilt PLTs over
here:
<https://github.com/danielberkompas/travis_elixir_plts>

## Usage
You must have an Amazon S3 account with a valid bucket name. Make sure that the
bucket was created in the "US Standard" region, or you'll encounter errors.

1. Fork this repository.
2. Set the following ENV vars for your fork on Travis:

```
ARTIFACTS_KEY=<AWS S3 Access Key>
ARTIFACTS_SECRET=<AWS S3 Access Secret>
ARTIFACTS_BUCKET=<AWS S3 Bucket Name>
```

3. Enable builds for your fork on Travis.
4. Watch your PLTs flow into a `travis_elixir_plts` folder in your bucket.

You can build for different combinations of Elixir and OTP by editing the
`.travis.yml` file.
