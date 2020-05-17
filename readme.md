#### Structure of personal portfolio

This personal portfolio project hosts, or displays, many other projects.

#### Everytime a project is added, must manually update

1. in ~/package.json: `"start": "npm run build --prefix client/projects/<project name>"`
2. in ~/package.json: `"heroku-postbuild": "npm i --prefix=client/projects/<project name> && npm run build --prefix=client/projects/<project name>"`
3. in ~/client/projects/\<project name\>/package.json: `"homepage": "/projects/<project name>"`
4. in ~/client/root/src/components/sections/projectsSection: edit allCardDetails.js. Add photo to ~/client/root/public
5. Change all absolute paths (non react-router) to relative paths("./" or no slash at all. just a "/" is absolute). Add \<base href="%PUBLIC_URL%/"\> to index.html
6. If using react router, add basename=/homepage to BroswerRouter

#### issues that may be improvable

- For manual updates 1, 2 and 3: Create an array containing project names, and all areas are automatically updated based on this array
