---
title: test conditional emails using dynamic metadata
keep-md: true
# format: email
email-preview: true
---


::: {.cell}

```{.r .cell-code}
# Pick variant
variant <- sample(1:3, 1)
```
:::

::: {.cell}

```{.r .cell-code}
# write metadata as yaml
#| output: asis
cat(
  "---",
  paste0("is_email_variant_",variant,": true"),
  "---",
  sep = "\n"
)
```

::: {.cell-output .cell-output-stdout}
```
---
is_email_variant_3: true
---
```
:::
:::



::: {.email}

::: {.content-visible when-meta="is_email_variant_1"}
::: {.subject}
subject 1
:::
:::

::: {.content-visible when-meta="is_email_variant_2"}
::: {.subject}
subject 2
:::
:::

::: {.content-visible when-meta="is_email_variant_3"}
::: {.subject}
subject 3
:::
:::

::: {.email-scheduled}
True
:::

::: 