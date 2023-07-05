## CORRECCIONES

---

**1 - En el create:**  **`src/controllers/car.controllers.js`** 

    const {quantity, productId} = req.body

Las constantes definidas en la destructuracion, vienen del req, no del res

---
  **2 - `src/controllers/purchase.controllers.js`** 

No uso la **instancia** car, si no el **model** Car para destruir el registro

    await Car.destroy({where:{userId}})

  ---
   **3 - `src/tests/product.test.js`** 
    
En el **test de get** espero que la longitud del array recibido sea 1, no 2