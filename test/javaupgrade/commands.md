1. clone https://github.com/peterborkuti/movie-info-service into `/test/javaupgrade`
2. run `az login --device-code`
3. run test
```shell
node ./dist/simulationMain.js --external-scenarios ./test/javaupgrade --parallelism 1 --sidebar -n 1 --disable-tools=get_errors --install-extension={YOUR_VSIX_PATH} --model claude-3.7-sonnet --in-extension-host --scenario-workspace-folder --verbose --output ./test/javaupgrade/out/$(date +%Y-%m-%d-%H%M)simulator_output  --skip-cache
```