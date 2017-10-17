# Deploy (Staging)
1. SSH to server. Check if your IP added to the inbound rules of the security group on AWS.
2. Navigate to the root folder of the project
3. Git pull
4. Run `yarn` to make sure packages are installed
5. Run `yarn build-staging`
6. Run `pm2 status` see if `scheduler` is running. If `scheduler` is running, run `pm2 gracefulReload all`. If not, run `pm2 start pm2/staging.json`.

# Deploy (Production)
1. SSH to server. Check if your IP added to the inbound rules of the security group on AWS.
2. Navigate to the root folder of the project
3. Git pull and checkout the corresponding release branch
4. Run `yarn` to make sure packages are installed
5. Run `yarn build-prod`
6. Run `pm2 status` see if `scheduler` is running. If `scheduler` is running, run `pm2 gracefulReload all`. If not, run `pm2 start pm2/prod.json`.
