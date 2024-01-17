---
title: test dynamic metadata
keep-md: true
---




::: {#2dc5d4ac .cell execution_count=2}
``` {.python .cell-code}
import random
variant = int(random.random() * 3) + 1
opts = {}
opts["is_email_variant_" + str(variant)] = True
quarto_metadata(**opts)
```

::: {.cell-output .cell-output-display .cell-output-markdown execution_count=2}

---
is_email_variant_3: true
---


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

