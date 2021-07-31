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
		],
		"plugins": [
			[
				"@semantic-release/commit-analyzer",
				{
					"preset": "angular",
					"releaseRules": [
						{"type": "refactor", "release": false},
						{"type": "style", "release": "patch"},
						{"scope": "no-release", "release": false},
						{"scope": "cli", "release": "patch"},
						{"scope": "patch", "release": "patch"}
					]
				}
			],
			"@semantic-release/release-notes-generator",
			"@semantic-release/npm",
			"@semantic-release/github"
		]
	}
}
```

## Other Actions

-   [actions/create-release](https://github.com/actions/create-release)
-   [action-gh-release](https://github.com/softprops/action-gh-release)
-   [release-tag](https://github.com/yyx990803/release-tag)
