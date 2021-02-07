# add-release-channel
This action adds a release channel to your package.json version

## Inputs

### `releaseChannel`

**Required** The name of the release channel you wanna set. Default `"alpha"`.

### `buildNumber`

**Optional** Specify a build number. This number can be generated by your own script or just a date. Default `"null"`.

## Outputs

### `releaseChannel`

Get the complete output of you package.json `version`. Depending if you used the build number parameter this will look like:
`"version": "1.2.1-[releaseChannel]-[buildNumber]"`

## Example usage

```
uses: felix-schaipp/add-release-channel@main
with:
  releaseChannel: "beta"
  buildNumber: 0402042021 # hhddmmyyyy use a date as the build number
```
