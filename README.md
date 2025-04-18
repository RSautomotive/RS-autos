import React from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { Input } from "@/components/ui/input";
import { Star } from "lucide-react";

export default function HomePage() {
  return (
    <main className="p-4 md:p-8 space-y-12">
      {/* Hero Section */}
      <section className="grid md:grid-cols-2 gap-6 items-center">
        <div>
          <h1 className="text-4xl font-bold mb-4">Quality Used Cars in Somerset</h1>
          <Button className="text-lg">View Stock</Button>
        </div>
        <div className="bg-gray-300 rounded-xl h-64 md:h-80"></div>
      </section>

      {/* Search & Filter */}
      <section className="space-y-4">
        <h2 className="text-2xl font-semibold">Search & Filter</h2>
        <div className="grid grid-cols-1 md:grid-cols-4 gap-4">
          <Input placeholder="Make / Model" />
          <Input placeholder="Price Range" />
          <Input placeholder="Mileage" />
          <Button>Search</Button>
        </div>
      </section>

      {/* Featured Vehicles */}
      <section className="space-y-4">
        <h2 className="text-2xl font-semibold">Featured Vehicles</h2>
        <div className="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-4">
          {[1, 2, 3].map((vehicle) => (
            <Card key={vehicle} className="rounded-2xl shadow-md">
              <div className="bg-gray-200 h-40 rounded-t-2xl"></div>
              <CardContent className="p-4">
                <h3 className="text-lg font-semibold">Vehicle Title</h3>
                <p className="text-gray-600">£X,XXX</p>
              </CardContent>
            </Card>
          ))}
        </div>
      </section>

      {/* Info Blocks */}
      <section className="grid grid-cols-1 md:grid-cols-3 gap-6">
        <Card className="rounded-2xl shadow-sm">
          <CardContent className="p-4">
            <h3 className="text-xl font-semibold mb-2">Sell or Part-Exchange</h3>
            <p>Quick and easy trade-in process to get your next vehicle.</p>
          </CardContent>
        </Card>

        <Card className="rounded-2xl shadow-sm">
          <CardContent className="p-4">
            <h3 className="text-xl font-semibold mb-2">Finance</h3>
            <p>Flexible finance options available through trusted partners.</p>
          </CardContent>
        </Card>

        <Card className="rounded-2xl shadow-sm">
          <CardContent className="p-4">
            <h3 className="text-xl font-semibold mb-2">Customer Reviews</h3>
            <p>We’re proud of our 5-star customer satisfaction rating.</p>
            <div className="flex space-x-1 mt-2">
              {[...Array(5)].map((_, i) => (
                <Star key={i} size={16} className="text-yellow-500" />
              ))}
            </div>
          </CardContent>
        </Card>
      </section>

      {/* Footer */}
      <footer className="text-center text-sm text-gray-500 pt-10 border-t mt-10">
        <p>Privacy Policy | Terms & Conditions | Returns & Warranty Info</p>
        <div className="mt-2">© 2025 RS Automotive Ltd</div>
      </footer>
    </main>
  );
}
