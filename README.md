# Kernel headers intermediary repo

Selects `qti_kernel_headers` repo based on kernel version so that multiple
versions can live inside on AOSP tree.

Needs following changes:

```make
$(call soong_config_set,qti_kernel_headers,version,6.6)
```

`common-headers` needs to rename the module name from `qti_kernel_headers` to
`qti_kernel_headers_6.6` (based on version).
