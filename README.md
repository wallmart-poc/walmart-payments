# walmart-payments · Payment Service

Payment authorization gRPC service. Simulates credit card charge processing within the checkout flow, returning a transaction ID on success.

## Stack
- **Language:** Node.js 20
- **Framework:** gRPC (`@grpc/grpc-js`)

## API
Implements `PaymentService` from `demo.proto`:
- `Charge(ChargeRequest) → ChargeResponse` — validates card details and returns a transaction UUID

No real payment processor is called — charges are simulated for demo purposes.

## Running locally
```bash
npm install
node index.js
```
Service listens on port `50051` by default (`PAYMENT_SERVICE_PORT`).

## Dependencies
None — standalone service, no outbound calls to other internal services.
