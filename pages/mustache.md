# mustache

> `mustache` is the reference implementation of the mustache spec
> More information: <https://mustache.github.io/>.

- Apply the data in `data.yml` to the template defined in `template.mustache`

`mustache data.yml template.mustache`

- Pipe the data through STDIN and process the template defined in `template.mustache`

cat data.yml | mustache - template.mustache

- Typical template:

```
Hello {{name}}
You have just won {{value}} dollars!

```

- Render a list:

### data.yml
```
{
  "repo": [
    { "name": "resque" },
    { "name": "hub" },
    { "name": "rip" }
  ]
}
```

### template.mustache
```
{{#repo}}
  <b>{{name}}</b>
{{/repo}}
```


