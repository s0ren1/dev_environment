### Complete docker buildx template

    docker buildx build --progress=tty --pull --platform linux/amd64,linux/arm64 \
    --cache-from=[]:cache \
    --cache to=type=registry,ref=[]:cache,mode=max  \
    --push 
    --tag []:latest --target main . -f Dockerfile.ci
	



### Standard commands for building apps
    docker buildx stop
    docker buildx create --use --name mybuilder
    
    docker buildx build \
    --cache-from type=registry,ref=s0ren1/go-hello-world:cache \
    --cache-to   type=registry,ref=s0ren1/go-hello-world:cache,mode=max \
    --push --tag s0ren1/go-hello-world:build --target build . -f dockerfile.multi

    docker buildx build \
    --cache-from type=registry,ref=s0ren1/go-hello-world:cache \
    --cache-to   type=registry,ref=s0ren1/go-hello-world:cache,mode=max \
    --push --tag s0ren1/go-hello-world:app --target app . -f dockerfile.multi