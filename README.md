# Banking API Gateway — Apigee X Project

This is a secure API proxy built using **Apigee X** to simulate a real-world banking API gateway. It implements **OAuth 2.0 access token validation**, **custom error handling**, and **logging via ServiceCallout**.

---

## Features

- OAuth 2.0 token verification (`VerifyAccessToken`)
- Fault handling for `invalid_access_token` using `RaiseFault`
- Failure logging using `ServiceCallout` policy
- Secure base path: `/banking`
- Configured with ProxyEndpoint and TargetEndpoint routing

---

## 🧪 How It Works

1. Client requests a token using `client_id` and `client_secret` from Apigee's OAuth token endpoint.
2. Client calls the `/banking` endpoint with the token:

Authorization: Bearer <access_token>

3. Proxy validates the token using `OAuth-v20-1`.
4. If invalid:
- Logs the failure using `ServiceCallout`
- Returns a custom error using `Raise-Fault`
5. If valid, the request is routed to the backend.

---

## 🤝 Let's Connect

If you're a recruiter or fellow developer interested in API gateway design or Apigee development — feel free to connect!


