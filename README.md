# KubeProject Tilt

This is the repository that contains the Tiltfile for the entire Kube Project.

The only thing that is not constructed by Tilt is the face recognition service.
Letting Tilt build that on every run would be massively ineffective because the
dlib takes minutes to build and install.

Caveat: The current Python Libraries face recognition might not be perfect in
large images.