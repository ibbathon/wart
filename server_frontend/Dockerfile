FROM node:16-alpine

# We want to build static files first, without using much space
WORKDIR /server_frontend
COPY . .
RUN npm install --quiet \
 && npm run build \
 && npm uninstall `ls node_modules`

# Next, install the actual server
RUN npm install -g serve

ENTRYPOINT ["./set_server_env.sh"]

CMD ["serve", "-s", "build"]
