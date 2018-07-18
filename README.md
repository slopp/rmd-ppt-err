This repository is a reprex of an issue with R Markdown rendering powerpoint.

To reproduce:

1. Render `ppt.Rmd` directly. An image is produced.
2. Render `generate.Rmd` which, in turn, calls `render('ppt.Rmd')`. 

*Expected*: The `ppt`  output to be the same in case 1 and 2.

*Error*: The `ppt` output in case 2 does not in include any chunk outputs.

*Impact*: This bug prevents a critical RSC use case, which is deploying an RMD that creates a PPT as an artifact to attach to an email.

