# code-llama-server

- Run the code-llama-2 LLM in Openshift
- Requires a worker node with NVIDIA GPU support

- Create the Openshift application
```
oc new-app python~https://github.com/bkoz/code-llama-server
```

- Expose the Gradio service as a route.
```
oc create route edge code-llama-server --service=code-llama-server --insecure-policy='Redirect'
```
