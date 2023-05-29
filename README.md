# KubeProject Tilt

This is the repository that contains the Tiltfile for the entire Kube Project.

The only thing that is not constructed by Tilt is the face recognition service.
Letting Tilt build that on every run would be massively ineffective because the
dlib takes minutes to build and install.

Caveat: The current Python Libraries face recognition might not be perfect in
large images.

## How to use it:

Create a kind cluster by running:

```
kind create cluster --config kind_test_cluster.yaml
```

This will create some volumes for the kind cluster which we'll use later to drop in images into.

Checkout all the three services next to this one:

```
git clone git@github.com:kube-project/face-recognition-service.git
git clone git@github.com:kube-project/receiver-service.git
git clone git@github.com:kube-project/image-processor-service.git
git clone git@github.com:kube-project/frontend-service.git
```

Once the cluster is running, simply run:

```
tilt up
```

If everything went fine, when opening the tilt dashboard you should see lots of greens.
