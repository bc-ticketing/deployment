FROM mhart/alpine-node:10
RUN npm install -g ganache-cli
ADD . /
EXPOSE 8545
CMD sh -c "ganache-cli --h 0.0.0.0 --port ${GANACHE_PORT} --db ganache_db --mnemonic '${MNEMONIC}' -a ${ACCOUNTS} --defaultBalanceEther ${INITIAL_BALANCE}"