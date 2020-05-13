# Python Stack 

This React stack is based in the this [one](https://github.com/appsody/stacks/blob/master/incubator/nodejs/README.md)

This one modifies the Dockerfiles to add React support and install IBM Carbon Design libraries.

1. Create the base template to modify over:

```console 
foo@bar:~$ appsody stack create react-stack --copy incubator/nodejs
```
2. Modify the Docker files to change the Node.js base image with the one that supports React and add IBM Carbon Libraries: 
- [image/project/Dockerfile](https://github.com/chechuironman/kabanero-react-stack/blob/master/image/project/Dockerfile) 
- [image/Dockerfile-stack](https://github.com/chechuironman/kabanero-react-stack/blob/master/image/Dockerfile-stack)
3. Modify the [stack.yaml](https://github.com/chechuironman/kabanero-react-stack/blob/master/stack.yaml) file with the info of teh new stack.
4. Package the satck:

```console 
foo@bar:~$ appsody stack package
```

5. Validate the stack:

```console 
foo@bar:~$ stack vallidate
```

6. Add the stack to the stack hub:

```console 
foo@bar:~$ appsody stack add-to-repo chechu-repo --release-url https://github.com/chechuironman/kabanero-stacks/releases/latest/download
```

In my Kabanero stack hub you can see instructions on how to expose the files to your OpenShift instance:

[https://github.com/chechuironman/kabanero-stacks](https://github.com/chechuironman/kabanero-stacks)
