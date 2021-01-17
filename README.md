# EZ-linter

## Settings

1. Copy server/settings.example.js to server/settings.js and change values to match your MongoDB and Github OAuth settings.

### Recommended database setup

- Database name: ez-linter
- Collection name for eslintrc files: configs

## Endpoints

- `POST /api/user/config`: add config to database if not already present and adds configId to list of user's saved configs. Return configId in body of response as {configId: '<configId>'}
- `DELETE /api/user/config`: remove config from user list of saved configs
- `GET /api/user/savedconfigs`: get user's list of saved config ids. Returned in body of response as {configs: configs[]}
- `GET /api/config/:id`: returns eslintrc config from database. If id is not found, returns status 404.
