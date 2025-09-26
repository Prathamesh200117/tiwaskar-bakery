import React from "react";

// Full Menu Page for Tiwaskar's Bakery House
// Step 2: After homepage, now categories with items & prices

export default function TiwaskarMenu() {
  const menu = {
    Cookies: [
      { name: "Peanut Butter (100 gm)", price: "₹130" },
      { name: "Choco Chip (150 gm)", price: "₹120" },
      { name: "Badam Pistachio (150 gm)", price: "₹140" },
      { name: "Whole Wheat (200 gm)", price: "₹160" },
      { name: "Coconut (200 gm)", price: "₹125" },
      { name: "Tuti Fruti (200 gm)", price: "₹110" },
    ],
    "Tea Cakes": [
      { name: "Tuti Fruity (150 gm)", price: "₹140" },
      { name: "Chocolate (150 gm)", price: "₹150" },
      { name: "Banana Cake", price: "₹250" },
      { name: "Pineapple (150 gm)", price: "₹140" },
      { name: "Blueberry (150 gm)", price: "₹190" },
      { name: "English Tea Cake (150 gm)", price: "₹180" },
    ],
    Brownies: [
      { name: "Chocolate Brownie (3 pcs)", price: "₹135" },
      { name: "Almond Brownie (2 pcs)", price: "₹145" },
      { name: "Walnut Brownie (2 pcs)", price: "₹155" },
      { name: "Brownie Cupcake (4 pcs)", price: "₹100" },
    ],
    Baklava: [
      { name: "Dry Fruit Mix (150 gm)", price: "₹300" },
      { name: "Dry Fruit Square (200 gm)", price: "₹360" },
      { name: "Dry Fruit Tart (180 gm)", price: "₹310" },
      { name: "Chocolate (150 gm)", price: "₹320" },
      { name: "Pistachio (150 gm)", price: "₹400" },
    ],
    Muffins: [
      { name: "Choco-Chip (4 pcs)", price: "₹70" },
      { name: "Blueberry (4 pcs)", price: "₹120" },
      { name: "Red Velvet (4 pcs)", price: "₹95" },
      { name: "Apple (4 pcs)", price: "₹90" },
      { name: "Tuti Fruti (4 pcs)", price: "₹65" },
      { name: "Chocolate (4 pcs)", price: "₹60" },
    ],
    Bread: [
      { name: "Lavash (150 gm)", price: "₹200" },
      { name: "Sourdough Bread", price: "₹550" },
    ],
    Cakes: [
      { name: "Tuti Fruity (S)", price: "₹135 onwards" },
      { name: "Chocolate (S)", price: "₹140 onwards" },
      { name: "Mixed Dry Fruit (S)", price: "₹170 onwards" },
      { name: "Pineapple (S)", price: "₹145 onwards" },
      { name: "Blueberry (S)", price: "₹180 onwards" },
      { name: "Chocolate Brownie Cake", price: "₹220 onwards" },
    ],
    Croissants: [
      { name: "Butter", price: "₹150" },
      { name: "Chocolate", price: "₹170" },
    ],
  };

  return (
    <div className="min-h-screen bg-gradient-to-b from-white to-amber-50 text-gray-800">
      <header className="bg-white shadow sticky top-0 z-30">
        <div className="max-w-6xl mx-auto px-6 py-4 flex items-center justify-between">
          <h1 className="text-xl font-semibold">Tiwaskar's Bakery House</h1>
          <a
            href="https://wa.me/918830457234"
            target="_blank"
            rel="noreferrer"
            className="inline-block bg-amber-500 text-white px-4 py-2 rounded-xl shadow"
          >
            Order Now
          </a>
        </div>
      </header>

      <section className="max-w-6xl mx-auto px-6 py-12">
        <h2 className="text-3xl font-bold mb-8">Our Menu</h2>
        {Object.entries(menu).map(([category, items]) => (
          <div key={category} className="mb-12">
            <h3 className="text-2xl font-semibold mb-4 border-b pb-2 border-amber-200">
              {category}
            </h3>
            <div className="grid sm:grid-cols-2 md:grid-cols-3 gap-6">
              {items.map((item) => (
                <div
                  key={item.name}
                  className="bg-white rounded-lg p-5 shadow flex flex-col justify-between"
                >
                  <div>
                    <h4 className="font-semibold">{item.name}</h4>
                    <p className="text-sm text-gray-500 mt-1">Chef's Special</p>
                  </div>
                  <div className="mt-4 flex items-center justify-between">
                    <div className="text-lg font-bold">{item.price}</div>
                    <a
                      href={`https://wa.me/918830457234?text=I%20want%20to%20order%20${encodeURIComponent(
                        item.name
                      )}`}
                      target="_blank"
                      rel="noreferrer"
                      className="inline-block bg-amber-600 text-white px-3 py-2 rounded-lg"
                    >
                      Order
                    </a>
                  </div>
                </div>
              ))}
            </div>
          </div>
        ))}
      </section>

      <footer className="bg-white py-8 border-t mt-12">
        <div className="max-w-6xl mx-auto px-6 text-center text-gray-600">
          <p>Tiwaskar's Bakery House • Amravati</p>
          <p>Phone / WhatsApp: <a href="tel:+918830457234" className="text-amber-600">8830457234</a></p>
        </div>
      </footer>
    </div>
  );
}
