# Grav

**App Root:**

`apps/grav/`

Learn more [here](https://learn.getgrav.org/).

## Integration of design system Twig files

With the inclusion of the Grav plugin [twig-namespaces](https://github.com/phase2/grav-pl-starter/tree/master/app/user/plugins/twig-namespaces), Grav Twig templates in `~templates/` can \`

`,`

`, and`

`the Twig patterns within`source/\_patterns/\`. Similar to Drupal, including these patterns is done as follows:

```text
{% include "@organisms/path/to/file.twig" with {
  title: label,
  imageUrl: field_name.raw.path,
  largeCTA: true,
} %}
```

Configuration for Grav and additional docs can found in the `~README.md` file.

