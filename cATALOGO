import React, { useState } from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Input } from "@/components/ui/input";
import { Button } from "@/components/ui/button";
import { motion } from "framer-motion";

const productsMock = [
  {
    id: 1,
    name: "Coxinha Tradicional",
    price: "R$ 7,00",
    image: "https://via.placeholder.com/400x400",
    category: "Salgados Fritos",
    description: "Coxinha de frango cremosa e crocante",
  },
  {
    id: 2,
    name: "Risoles de Presunto e Queijo",
    price: "R$ 6,50",
    image: "https://via.placeholder.com/400x400",
    category: "Salgados Fritos",
    description: "Risoles recheado com presunto e queijo",
  },
  {
    id: 3,
    name: "Enroladinho de Salsicha",
    price: "R$ 6,00",
    image: "https://via.placeholder.com/400x400",
    category: "Salgados Assados",
    description: "Enroladinho macio com salsicha de qualidade",
  },
  {
    id: 4,
    name: "Esfiha de Carne",
    price: "R$ 5,50",
    image: "https://via.placeholder.com/400x400",
    category: "Salgados Assados",
    description: "Esfiha aberta recheada com carne temperada",
  },
  {
    id: 5,
    name: "Bolinha de Queijo",
    price: "R$ 6,50",
    image: "https://via.placeholder.com/400x400",
    category: "Salgados Fritos",
    description: "Bolinha crocante recheada com queijo derretido",
  },
];

export default function CatalogoSite() {
  const [search, setSearch] = useState("");

  const filteredProducts = productsMock.filter((p) =>
    p.name.toLowerCase().includes(search.toLowerCase())
  );

  return (
    <div className="min-h-screen bg-gray-50 p-6">
      <div className="max-w-6xl mx-auto">
        {/* Header */}
        <div className="mb-8 flex flex-col md:flex-row md:items-center md:justify-between gap-4">
          <div>
            <h1 className="text-3xl font-bold">Catálogo de Salgados</h1>
            <p className="text-gray-600">Confira nossos salgados disponíveis</p>
          </div>

          <div className="flex gap-2 w-full md:w-80">
            <Input
              placeholder="Buscar salgado..."
              value={search}
              onChange={(e) => setSearch(e.target.value)}
            />
          </div>
        </div>

        {/* Products Grid */}
        <div className="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
          {filteredProducts.map((product) => (
            <motion.div
              key={product.id}
              initial={{ opacity: 0, y: 20 }}
              animate={{ opacity: 1, y: 0 }}
              transition={{ duration: 0.3 }}
            >
              <Card className="rounded-2xl shadow-md hover:shadow-xl transition">
                <CardContent className="p-4">
                  <img
                    src={product.image}
                    alt={product.name}
                    className="w-full h-60 object-cover rounded-xl mb-4"
                  />

                  <h2 className="text-xl font-semibold mb-1">
                    {product.name}
                  </h2>

                  <p className="text-gray-500 text-sm mb-2">
                    {product.category}
                  </p>

                  <p className="text-gray-700 text-sm mb-3">
                    {product.description}
                  </p>

                  <div className="flex items-center justify-between">
                    <span className="text-lg font-bold">
                      {product.price}
                    </span>

                    <Button>Comprar</Button>
                  </div>
                </CardContent>
              </Card>
            </motion.div>
          ))}
        </div>
      </div>
    </div>
  );
}
