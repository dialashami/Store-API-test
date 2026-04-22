
# Store API Test

Automated REST API tests for the [Fake Store API](https://fakestoreapi.com), written in C# using NUnit. Built as part of a QA internship assignment covering both manual and automated testing.

---

## Project Structure

```
Assignment#4/
├── Helpers/
│   └── ApiClient.cs        # HTTP client wrapper (GET requests, response reading)
├── Models/
│   └── Cart.cs             # Cart and CartProduct deserialization models
├── Tests/
│   └── CartApiTests.cs     # NUnit test class with 3 test cases
```

---

## API Under Test

| Property | Value |
|---|---|
| URL | `https://fakestoreapi.com/carts/5` |
| Method | `GET` |
| Response Format | JSON |

---

## Test Cases

| Test | Description | Expected Result |
|---|---|---|
| `Verify_StatusCode_Is200` | Sends a GET request and checks the HTTP status | `200 OK` |
| `Verify_CartId_Is5_InTheBody` | Deserializes the response and checks the cart ID | `id == 5` |
| `Verify_Cart_Contains_AtLeast1Product` | Checks the products array is present and non-empty | `products.Count > 0` |

All 3 tests pass. Total run time: ~947 ms.

---

## Prerequisites

- [.NET SDK](https://dotnet.microsoft.com/download) (6.0 or later)
- NUnit 3
- Newtonsoft.Json (Json.NET)

Install dependencies via NuGet:

```bash
dotnet add package NUnit
dotnet add package NUnit3TestAdapter
dotnet add package Microsoft.NET.Test.Sdk
dotnet add package Newtonsoft.Json
```

---

## Running the Tests

```bash
cd Assignment#4
dotnet test
```

To see console output (test logs) during the run:

```bash
dotnet test --logger "console;verbosity=detailed"
```

---

## Manual Testing

Manual tests were performed using **Postman** prior to automation. The test plan (STP) document covers:

- **TC-01** — Verify status code is 200
- **TC-02** — Verify response body contains `"id": 5`
- **TC-03** — Verify `products` array contains at least one item

All manual tests passed with the expected JSON response.

---

## Notes

- The `ApiClient` uses a 10-second request timeout.
- `[OneTimeSetUp]` and `[OneTimeTearDown]` manage the client lifecycle — the `HttpClient` is created once per test run and properly disposed after.
- The `Accept: application/json` header is set on every request.
