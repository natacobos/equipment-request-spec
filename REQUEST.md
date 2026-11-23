# Request from the retail operations team

"Our stores lose time when equipment breaks. Today a store employee emails the IT service desk, the
email gets lost, nobody knows if it was approved, and a broken scanner can stay broken for two weeks.
We want a simple way to ask for a replacement and to see where each request is."

## What we know

- About 300 stores. Store employees use a shared tablet or their phone, usually standing at the counter.
  They need to send a request in under a minute: which store, which equipment (scanner, receipt printer,
  card reader, tablet), what is wrong, and a photo if they have one.
- The store manager approves every request. Requests for equipment that costs more than $500 also need
  the regional manager's approval. Finance says this limit may change next quarter.
- Store employees and managers must see only their own store's requests. Regional managers see every
  store in their region. The IT team sees everything and wants to filter and report on requests.
- Once approved, a ticket must be created in the IT service desk system through its REST API. The API
  needs a Microsoft Entra ID sign-in with an app registration (a technical user with a client secret).
- The service desk system is down for maintenance every Sunday night. No approved request may be lost.
- There are three environments: development, test and production. Each one uses a different service
  desk address (a test service desk in development and test, the real one in production).
