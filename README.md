import React from "react"; import { Card, CardContent } from "@/components/ui/card"; import { Button } from "@/components/ui/button"; import { Input } from "@/components/ui/input"; import { Textarea } from "@/components/ui/textarea";

const properties = [ { id: 1, address: "54 North St, Douglas, MA 01516", price: "$589,900", bedrooms: 3, bathrooms: 2, size: "1,788 sqft", lot: "0.63 acre", description: "Charming single-family home with spacious interiors and a beautiful yard.", image: "https://via.placeholder.com/400x250" }, { id: 2, address: "21 Elm St, Worcester, MA 01609", price: "$475,000", bedrooms: 4, bathrooms: 3, size: "2,100 sqft", lot: "0.50 acre", description: "Modern colonial-style home in the heart of Worcester with newly renovated kitchen.", image: "https://via.placeholder.com/400x250" }, { id: 3, address: "102 Main St, Andover, MA 01810", price: "$749,000", bedrooms: 5, bathrooms: 4, size: "3,000 sqft", lot: "1 acre", description: "Elegant estate with large living spaces and a spacious backyard ideal for entertaining.", image: "https://via.placeholder.com/400x250" } ];

export default function SoniaConnollyRealEstate() { return ( <div className="p-6"> <h1 className="text-4xl font-bold mb-6">Sonia Connolly Real Estate</h1> <p className="mb-10 text-lg text-gray-600">Your Trusted Partner in Massachusetts Real Estate</p>

<div className="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6 mb-12">
    {properties.map((property) => (
      <Card key={property.id} className="rounded-2xl shadow-md">
        <img
          src={property.image}
          alt={property.address}
          className="w-full h-48 object-cover rounded-t-2xl"
        />
        <CardContent className="p-4">
          <h2 className="text-xl font-semibold mb-2">{property.address}</h2>
          <p className="text-lg text-green-600 font-bold mb-2">{property.price}</p>
          <p className="text-sm text-gray-600 mb-1">
            {property.bedrooms} Beds | {property.bathrooms} Baths | {property.size} | Lot: {property.lot}
          </p>
          <p className="text-sm text-gray-500 mb-4">{property.description}</p>
          <Button>View Details</Button>
        </CardContent>
      </Card>
    ))}
  </div>

  <div className="max-w-xl mx-auto p-6 bg-white rounded-2xl shadow-md">
    <h2 className="text-2xl font-bold mb-4">Contact Sonia Connolly</h2>
    <p className="mb-4 text-gray-600">Have a question? Get in touch via the form below or message on <a href="https://www.facebook.com/share/16LmAneaAU/" target="_blank" className="text-blue-600 underline">Facebook</a>.</p>
    <form className="space-y-4">
      <Input type="text" placeholder="Your Name" required />
      <Input type="email" placeholder="Your Email" required />
      <Textarea placeholder="Your Message" rows={5} required />
      <Button type="submit">Send Message</Button>
    </form>
  </div>
</div>

); }

