# Generating the immich client for new versions
1. Install openapi-generator-cli: `npm install -g @openapitools/openapi-generator-cli`
2. Navigate to repo root folder
3. Update [immich-openapi-specs.json](./immich-openapi-specs.json) to the latest version from -> https://raw.githubusercontent.com/immich-app/immich/refs/heads/main/open-api/immich-openapi-specs.json
4. Run `npx @openapitools/openapi-generator-cli generate -i .\immich-openapi-specs.json -g python -o ./ --global-property apis,models,modelDocs=false,apiDocs=false,apiTests=false,modelTests=false -p packageName=immich_api_client`