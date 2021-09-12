# Chandler's Bike Map

```sh
for file in rides/*; do mv $file rides/$(xq -r '.gpx.metadata.time | split("T")[0]' < $file).gpx; done
```

```sh
python -c 'import os, json; print(json.dumps([f"rides/{r}" for r in sorted(os.listdir("rides"))]))'
```
