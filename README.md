<!--- CARD BEGIN --->

![DNB-Hugo/AUDITOR](.github/github-card-dark.png#gh-dark-mode-only)
![DNB-Hugo/AUDITOR](.github/github-card-light.png#gh-light-mode-only)

<!--- CARD END --->

# GoHugo Component / Auditor

This module is a GoHugo component that adds auditing tools to your development website and not thought for use in a live deployment. It is work in progress.

[![Codacy Badge](https://app.codacy.com/project/badge/Grade/7361e712444841f2b4fcddfe25873130)](https://www.codacy.com/gh/davidsneighbour/hugo-auditor/dashboard)

## Headers CT

See [CT.css](https://github.com/csswizardry/ct) for details. Enable this feature only on development setup to see information about optimisation approaches for your header tag order.

```toml
[params.dnb.auditor]
ct = true
```

then add somewhere in the foooter of your base template:

```gotemplate
{{- partialCached "ct/ct.html" . -}}
```

## Create a JSON file with list of all created URLs

Add output type to `outputs` section in your config:

```toml
home = [..., "dnblinklist" ]
```

After creation of the site there is a JSON file available at `/links.json` ([http://localhost:1313/links.json](http://localhost:1313/links.json)) containing all created links.
