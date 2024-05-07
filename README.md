# podspec-operator
1. Install go 1.21
2. Install operator-sdk compatible with go
https://sdk.operatorframework.io/docs/building-operators/golang/installation/
3. mkdir podspec-operator
4. cd podspec-operator
5. operator-sdk init --domain=example.com --repo=podspec-operator
6. operator-sdk create api --group=example --version=v1 --kind=PodSpec
7. Update api/v1/podspec_types.go
input fields
Status fields
8. make generate
9. make manifest
10. Update internal/controller/podspec_controller.go
Reconciler function to create the pod
Annotation to create the role with pod create permission
11. make manifest
12. make docker-build docker-push
13. make deploy
14. Create sample crd


