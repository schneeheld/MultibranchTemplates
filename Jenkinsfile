podTemplate(yaml: """
apiVersion: v1
kind: Pod
metadata:
  labels:
    openjdk-8: "true"
  annotations:
spec:
  containers:
  - name: jdk8
    image: openjdk:8u131-alpine
    command:
    - cat
    tty: true
"""
) {
    node(POD_LABEL) {
      container('jdk8') {
        sh "java -version"
      }
    }
}
