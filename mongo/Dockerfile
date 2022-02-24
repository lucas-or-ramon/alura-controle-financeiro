FROM bitnami/mongodb:5.0

COPY expenditure.json /expenditure.json
COPY revenue.json /revenue.json

CMD mongoimport --host mongodb --db finance --collection revenue --drop --type json --file /revenue.json --jsonArray && \
    mongoimport --host mongodb --db finance --collection expenditure --drop --type json --file /expenditure.json --jsonArray