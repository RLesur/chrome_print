# R Markdown HTML documents to PDF with Travis

In this repository, you will find a minimal example for generating a PDF using `pagedown::chrome_print(...)` with Travis.

1. Add in the `.travis.yml` configuration file:

```yml
addons:
  chrome: stable
```

2. Run the `pagedown::chrome_print()` function with the following options:

```r
pagedown::chrome_print("myfile.Rmd", extra_args = c("--disable-gpu", "--no-sandbox"), work_dir = ".chromedir")
```

