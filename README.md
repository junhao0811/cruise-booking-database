# 🚢 Cruise Booking Database

A relational database designed from scratch for a cruise line company, taken all the way from business requirements to a working **Oracle SQL** schema.

---

## 🗺️ What it models

| Area | Tables |
|---|---|
| Fleet | `SHIP`, `CABIN`, `OPERATOR` |
| Voyages | `CRUISE`, `CRUISE_ITINERARY`, `PORT`, `COUNTRY` |
| Bookings | `PASSENGER`, `MANIFEST` (which passenger is in which cabin on which cruise), `ADDRESS` |

It captures real-world rules: ships with multiple cabin classes, multi-stop itineraries across ports and countries, passengers travelling with a guardian, and cabins that may or may not be booked.

---

## 🛠️ Design process

1. **Assumptions:** documented business rules and edge cases ([`docs/assumptions.pdf`](./docs/assumptions.pdf))
2. **Conceptual model:** entity-relationship diagram of the domain ([`docs/conceptual_model.pdf`](./docs/conceptual_model.pdf))
3. **Normalisation:** forms taken step by step from UNF → 1NF → 2NF → 3NF ([`docs/normalisation.pdf`](./docs/normalisation.pdf))
4. **Logical model:** full relational model with keys and relationships ([`docs/logical_model.pdf`](./docs/logical_model.pdf))
5. **Schema:** Oracle DDL with primary keys, foreign keys and check constraints ([`sql/schema.sql`](./sql/schema.sql))

The editable model is in [`data-modeler/`](./data-modeler) and opens in **Oracle SQL Developer Data Modeler**.

---

## 🚀 Run it

In Oracle (SQL Developer, SQLcl or SQL\*Plus):
```sql
@sql/schema.sql
```
[`sql/schema_output.txt`](./sql/schema_output.txt) shows the expected output.

## 🛠️ Tech
Oracle SQL · ER modelling · normalisation · Oracle SQL Developer Data Modeler
