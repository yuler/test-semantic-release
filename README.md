# test-semantic-release

[@yuler/test-semantic-release](https://npm.im/@yuler/test-semantic-release)

## Tech Stack

-   [semantic-release](https://github.com/semantic-release/semantic-release)

```json
{
	"release": {
		"branches": [
			"+([0-9])?(.{+([0-9]),x}).x",
			"master",
			"main",
			"next",
			"next-major",
			{
				"name": "next",
				"channel": "next"
			},
			{
				"name": "beta",
				"prerelease": true
			},
			{
				"name": "alpha",
				"prerelease": true
			}
		]
	}
}
```

## Other Actions

-   [actions/create-release](https://github.com/actions/create-release)
-   [action-gh-release](https://github.com/softprops/action-gh-release)
-   [release-tag](https://github.com/yyx990803/release-tag)
