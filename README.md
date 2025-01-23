---

### **Exercice 1 : Base de données NoSQL pour la gestion de stock**

Pour répondre à cet exercice, vous devez fournir une structure JSON qui répond aux critères listés. Voici une proposition avec une explication :

#### **Structure JSON**
```json
{
  "stores": {
    "store_id_1": {
      "products": {
        "barcode_1": {
          "name": "Product Name",
          "quantity": 100,
          "expiration_dates": [
            "2025-12-31",
            "2026-01-15"
          ],
          "reservations": [
            {
              "customer_id": "customer_1",
              "quantity": 2,
              "reservation_date": "2025-01-20"
            },
            {
              "customer_id": "customer_2",
              "quantity": 1,
              "reservation_date": "2025-01-21"
            }
          ]
        },
        "barcode_2": {
          "name": "Another Product",
          "quantity": 50,
          "expiration_dates": ["2026-06-30"],
          "reservations": []
        }
      }
    },
    "store_id_2": {
      "products": {
        "barcode_1": {
          "name": "Product Name",
          "quantity": 200,
          "expiration_dates": ["2025-12-15"],
          "reservations": []
        }
      }
    }
  }
}
```

#### **Explications**
1. **Hiérarchie des données :**
   - Les magasins sont identifiés par un `store_id`.
   - Chaque magasin contient une liste de produits identifiés par leur code-barres unique (`barcode`).

2. **Gestion des stocks :**
   - Chaque produit a une propriété `quantity` qui indique le nombre d'unités en stock.
   - Les dates d'expiration sont gérées sous forme de tableau (`expiration_dates`).

3. **Multi-magasin :**
   - La structure est organisée par magasin, permettant de gérer les mêmes produits dans plusieurs magasins.

4. **Réservations :**
   - Une réservation est un objet dans un tableau `reservations` contenant les informations sur le client, la quantité réservée et la date de réservation.

---

![image](https://github.com/user-attachments/assets/c08be92c-9371-4f21-b35e-139fa79802be)

