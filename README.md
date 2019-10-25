### devpi
---
https://github.com/devpi/devpi

http://doc.devpi.net/latest/

```py
// client/devpi/test.py

def setenv_devpi(hub, env, osturl, packageurl, packagemd5):
  if not packagemd5:
    packagemd5 = ""
  if sys.version_info[0] < 3:
    posturl = posturl.encode("utf8")
    packageurl = packageurl.encode("utf8")
    packagemd5 = packagemd5.encode("utf8")
  env["DEVPI_POSTURL"] = posturl.encode("utf8")
  env["DEVPI_PACKAGEURL"] = packageurl.encode("utf8")
  env["DEVPI_PACKAGEMD5"] = (packagemd5 or "").encode("utf8")
  for name in env:
    if name.startswith("DEVPI"):
      hub.debug("setenv_devpi %s %s", name, env[name])

class DevIndex:





```

```
```

```
```

