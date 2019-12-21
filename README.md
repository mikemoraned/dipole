# dipole
a small personal learning project for Go

## Intent

I am quite skeptical of the general applicability of Go i.e. I don't think it's a good general-purpose programming language. However, I believe it is useful for particular areas e.g. integrating with Kubernetes.

The intent of this project is to use Go for something it is likely good at to see how well it handles it, as well as using this to get more direct experience of the language and ecosystem, to see if this changes my mind.

## Application

The idea, which I think may not be new, but which fits this purpose, is to automatically sync up updown.io checks with ingress resources.

Steps:
* (x) contact updown.io API and list all current checks for my account
* (x) contact k8s API and list all ingresses for an example cluster of mine
* (x) map current ingresses to existing updown.io checks, and show what is different
* (x) make above run in k8s and log differences
* (x) add updown.io Go CLI which allows creation of new checks
* (x) extend above to a controller which adds new checks automatically, if new ingresses found
* (x) extend above to a controller which removes checks created by this tool, if ingress disappears
