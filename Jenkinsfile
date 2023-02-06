podTemplate(yaml: """
apiVersion: v1
kind: Pod
metadata:
  labels:
    openjdk-11: "true"
  annotations:
spec:
  containers:
  - name: jdk11
    image: openjdk:11
    command:
    - cat
    tty: true
"""
) {
    node(POD_LABEL) {
      container('jdk11') {
        sh "java -version"
      }
    }
}
