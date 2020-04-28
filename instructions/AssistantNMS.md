## Assistant for No Man's Sky - API Instructions

### [Web Documentation](https://api.nmsassistant.com)

### Access levels
- Public Basic
  - Easy to use endpoints that return data related to No Man's Sky
- Public Advanced
  - Public endpoints that are more focused on data surrounding the Assistant for No Man's Sky apps
- Authenticated
  - Endpoints that require a logged in AssistantNMS user

_You can change your access level in the top right of the [Documentation](https://api.nmsassistant.com)_

### Authentication
#### You will need an AssistantNMS Account. You can send an email to [support@nmsassistant.com](mailto:support@nmsassistant.com) requesting one.

All the endpoints that require Authentication need a JWT token to be passed in the `Authorization` header. 
To get a JWT token you must first send a `POST` request to /Auth

#### How to get the JWT Token
Your username and password must be in the following format `Username:Password`.
That string must then be base64 encoded and passed in the `Authorization` header with the prefix `Basic `.

For example: The username 'fred' and password 'bob' would be encoded from `fred:bob` to `ZnJlZDpib2I=` and then placed in the request as `Authorization: Basic ZnJlZDpib2I=`
