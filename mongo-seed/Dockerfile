FROM mongo:4.4

COPY . .
# CMD mongoimport --uri 'mongodb://root:rootcinecus@ecommerce_mongo:27017/ecommerce?authSource=admin' --collection stocks --type json --file /stocks.json --jsonArray;
CMD mongoimport --uri 'mongodb://root:rootcinecus@ecommerce_mongo:27017/ecommerce?authSource=admin' --collection products --type json --file /products.json --jsonArray;\
mongoimport --uri 'mongodb://root:rootcinecus@ecommerce_mongo:27017/ecommerce?authSource=admin' --collection stocks --type json --file /stocks.json --jsonArray;