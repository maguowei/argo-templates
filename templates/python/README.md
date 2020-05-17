# Argo Template Python

```yaml
apiVersion: argoproj.io/v1alpha1
kind: Workflow
metadata:
  generateName: python-script-
spec:
  entrypoint: python
  arguments:
    parameters:
    - name: code
      value: |
        import requests
        r = requests.get("https://www.v2ex.com/api/topics/hot.json")
        print(r.json())
  templates:
  - name: python
    inputs:
      parameters:
      - name: code
    script:
      image: argotemplate/python:sha-404822e
      command: [python]
      source: "{{inputs.parameters.code}}"
```
