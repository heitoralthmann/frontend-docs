# Drupal

_For information on getting Drupal theming started in Particle, check the \[\_Drupal 8 Quickstart Guide_\]\(../getting-started/drupal-8.md\).\_

**App Root:**

`apps/drupal/`

**Templates**

`~templates/` - Drupal twig templates. These often will `include`, `embed`, or `extend` the Twig templates found in Pattern Lab like this:

\`

\`.

We keep the components in Pattern Lab "pure" and ignorant of Drupal's data model and use these templates to map the data between the two. Think of these as the Presenter templates in the [Model View Presenter](https://en.wikipedia.org/wiki/Model–view–presenter) approach. Also, Drupal Twig templates that have nothing to do with Pattern Lab go here.

## Drupal integration of design system Twig files

Drupal Twig templates in `~templates/` can \`

`,`

`, and`

`the Twig patterns within`source/\_patterns/\` folder. See the [Atomic Design and Namespaces](https://phase2.github.io/frontend-docs/apps/drupal/#atomic-design-and-namespaces) section above for details, but implementing an organism, for example, is pretty straightforward:

```text
{% include "@organisms/path/to/file.twig" with {
  title: label,
  imageUrl: field_name.raw.path,
  largeCTA: true,
} %}
```

\(Note: requires updating\) For a demonstration in a sample codebase of how exactly to integrate templates, see the [`drupal-lab`](https://github.com/phase2/drupal-lab) repo; in particular note how both a [node teaser template](https://github.com/phase2/drupal-lab/blob/master/web/themes/dashing/templates/content/node--article--teaser.html.twig) and a [views field template](https://github.com/phase2/drupal-lab/blob/master/web/themes/dashing/templates/views/views-view-fields--newspage--page.html.twig) in the Drupal `~templates/` folder can embed the [card template](https://github.com/phase2/drupal-lab/blob/master/web/themes/dashing/pattern-lab/source/_patterns/02-molecules/cards/card.twig) from Pattern Lab while formatting the data.

