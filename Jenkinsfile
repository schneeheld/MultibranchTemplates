podTemplate(yaml: """
apiVersion: v1
kind: Pod
metadata:
  labels:
    openjdk-17: "true"
  annotations:
spec:
  containers:
  - name: maven-jdk17
    image: maven:3.8.5-openjdk-17
    command:
    - cat
    tty: true
"""
) {
    node(POD_LABEL) {
      container('maven-jdk17') {
        sh "java -version"
      }
    }
}
