# Ugly list pattern

There are several ways to construct lists, this is one of the uglier ones

## The Problem

We want to construct a list in a way that's not readily available using other filters.

For example, this is an output from a router listing images in the router's flash.

```yaml
router_output: |
  1 -rw- 68468172 Dec 1 2008 23:12:00 +00:00 c800-universalk9-mz.SPA.153-3.M4.bin
  9 -rw- 95947248 Sep 2 2020 19:42:52 +00:00 c800-universalk9-mz.SPA.157-3.M4a.bin
  8 -rw- 95947248 Sep 2 2020 19:42:52 +00:00 c800-universalk9-mz.SPA.157-3.M4b.bin
```

and we want to extract the image names at the end of the listing. 

You can do it with one of the lines, individually

```yaml
- name: extract the image name from one line
  debug:
    msg: "{{ router_output.split()[2] }}
```

output
```

```


