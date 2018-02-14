# Override-console

Will override console so that it will also show line number. This is especially useful in Cloudwatch because Cloudwatch does not provide this :(?

## installing

```
npm i @alfredwesterveld/override-console
```

## Usage
But inside Lambda handler I use it like:
```
exports.handler = function(event, context, callback) {
    require('@alfredwesterveld/override-console');
    // console.log('start lambda') => Not needed but used in example below
````

Then in Cloudwatch it would output something like:
```
	start lambda - /var/task/index.js:53:17
```

## Acknowledgement

Many thanks to:
- idbehold: https://stackoverflow.com/a/42929881/11926
- Dmitry Druganov: https://stackoverflow.com/a/47296370/11926