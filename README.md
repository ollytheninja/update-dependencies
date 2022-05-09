# Update Dependencies

Pinning dependencies is easy, ensuring there is a process to update those pins in a controlled manner is hard.

This repo contains some documentation and helper scripts for updating dependencies automatically.

## Python Dependencies

I love the `pip-compile` utility the `pip-tools` package.
It allows you to write simple (unpinned) dependencies to `requirements.in`, then run pip-compile which generates a `requirements.txt` with all the dependencies pinned.

You then reference requirements.txt in all your build scripts as usual.

`github-action-pip.yaml` is a workflow I use to ensure that I'm notified of dependencies that need updating, but allows me to have full control of when and if those updates happen!
