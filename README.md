# Back-end: 
## Person api:
- getPersonList: GET /api/persons/search/findByQuery
- getPerson: GET /api/persons/$id
- updatePerson: PATCH /api/persons/$id + person data in body
- createPerson: POST /api/persons + person data in body
- deletePerson: DELETE /api/persons/$id

## Supplier api:
- getSupplierList: GET /api/suppliers/search/findByQuery
- getSupplier: GET /api/supplier/$id
- updateSupplier: PATCH /api/supplier/$id + supplier data in body
- createSupplier: POST /api/suppliers + supplier data in body
- deleteSupplier: DELETE /api/suppliers/$id

>NOTE: I wasn't able to retrieve the suppplier's id through the api, so i created a workaround in front end to get the supplier ids. 
What i did was to get the supplier id from the entity's _links.self.href field and distribute it wherever needed for the CRUD operations.

# Front-end:

To prepare UI for production run: `npm run build` 
Then deploy the dist folder contents to the web root of a web server (NGINX, Apache etc).