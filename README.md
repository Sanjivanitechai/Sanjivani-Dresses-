import React from "react"; import { Card, CardContent } from "@/components/ui/card"; import { Button } from "@/components/ui/button"; import { PhoneCall, MapPin, ShoppingCart } from "lucide-react";

export default function SanjeevaniDresses() { return ( <div className="min-h-screen bg-gradient-to-br from-blue-50 to-blue-100 p-6 font-sans"> <header className="text-center py-6"> <img
src="https://chat.openai.com/images/logo-placeholder.png"
alt="Sanjivani Dresses Logo"
className="mx-auto h-24 w-24 rounded-full mb-4"
/> <h1 className="text-4xl font-bold text-blue-800">Sanjivani Dresses</h1> <p className="text-lg text-blue-600 mt-2 italic"> "Smart Schoolwear, Sensible Prices!" — Where Quality Meets Affordability for Every Student </p> </header>

<section className="grid grid-cols-1 md:grid-cols-2 gap-6 items-center max-w-6xl mx-auto">
    <div className="space-y-4">
      <h2 className="text-2xl font-semibold text-blue-700">Our Features</h2>
      <ul className="list-disc list-inside text-blue-700 text-base">
        <li>Reasonable prices for all dress types</li>
        <li>Work with perfection and neat finishing</li>
        <li>Instant response to customer complaints</li>
        <li>Available anytime for support and queries</li>
      </ul>
      <Button className="mt-4 bg-blue-700 hover:bg-blue-800">
        <ShoppingCart className="mr-2" /> Shop Now
      </Button>
    </div>

    <img
      src="https://images.unsplash.com/photo-1602810311224-e74c6c0f84f0?auto=format&fit=crop&w=800&q=80"
      alt="School Uniforms"
      className="rounded-2xl shadow-lg"
    />
  </section>

  <section className="my-12 max-w-6xl mx-auto">
    <h2 className="text-2xl font-semibold text-center text-blue-700 mb-6">Dress Gallery</h2>
    <div className="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-4">
      {["/mnt/data/gallery1.jpg", "/mnt/data/gallery2.jpg", "/mnt/data/gallery3.jpg", "/mnt/data/gallery4.jpg"].map((src, index) => (
        <Card key={index} className="bg-white shadow-xl rounded-2xl">
          <CardContent className="p-4">
            <img
              src={src}
              alt={`Dress ${index + 1}`}
              className="rounded-xl mb-2"
            />
            <p className="text-blue-700 font-semibold">Design #{index + 1}</p>
          </CardContent>
        </Card>
      ))}
    </div>
  </section>

  <section className="bg-blue-200 py-8 px-4 rounded-2xl max-w-4xl mx-auto text-center">
    <h2 className="text-2xl font-bold text-blue-800">Contact Us</h2>
    <p className="text-blue-700 mt-2">
      <MapPin className="inline-block mr-2" /> Prabhat Colony, near Gandhi School, Kalali Road, JMT
    </p>
    <p className="text-blue-700 mt-2">
      <PhoneCall className="inline-block mr-2" /> +91 99311 61872, +91 91424 60235
    </p>
    <Button className="mt-4 bg-blue-700 hover:bg-blue-800">Get in Touch</Button>
  </section>

  <footer className="mt-12 text-center text-blue-600 text-sm">
    &copy; 2025 Sanjeevani Dresses. All rights reserved.
  </footer>
</div>

); }

