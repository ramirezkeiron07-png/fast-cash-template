# fast-cash-template
import { Button } from "@/components/ui/button";
import { Card, CardContent } from "@/components/ui/card";
import { motion } from "framer-motion";

export default function BusinessWebsite() {
  return (
    <div className="min-h-screen bg-gray-50">
      {/* Hero Section */}
      <section className="bg-blue-600 text-white py-20 px-6 text-center">
        <motion.h1
          className="text-4xl md:text-5xl font-bold mb-4"
          initial={{ opacity: 0, y: -20 }}
          animate={{ opacity: 1, y: 0 }}
        >
          Your Business Name
        </motion.h1>
        <p className="max-w-xl mx-auto mb-6">
          We help customers with professional and reliable services.
        </p>
        <Button size="lg">Get a Free Quote</Button>
      </section>

      {/* Services */}
      <section className="py-16 px-6 max-w-6xl mx-auto">
        <h2 className="text-3xl font-bold text-center mb-10">Our Services</h2>
        <div className="grid md:grid-cols-3 gap-6">
          {["Service One", "Service Two", "Service Three"].map((service) => (
            <Card key={service} className="rounded-2xl shadow-sm">
              <CardContent className="p-6 text-center">
                <h3 className="text-xl font-semibold mb-2">{service}</h3>
                <p className="text-gray-600">
                  Short description of the service offered by the business.
                </p>
              </CardContent>
            </Card>
          ))}
        </div>
      </section>

      {/* About */}
      <section className="bg-white py-16 px-6">
        <div className="max-w-4xl mx-auto text-center">
          <h2 className="text-3xl font-bold mb-4">About Us</h2>
          <p className="text-gray-600">
            We are a trusted business providing high-quality services to our
            customers. Customer satisfaction is our top priority.
          </p>
        </div>
      </section>

      {/* Contact */}
      <section className="py-16 px-6 text-center">
        <h2 className="text-3xl font-bold mb-4">Contact Us</h2>
        <p className="mb-6">Email: business@email.com | Phone: (123) 456-7890</p>
        <Button>Contact Now</Button>
      </section>

      {/* Footer */}
      <footer className="bg-gray-900 text-gray-400 text-center py-4">
        © {new Date().getFullYear()} Your Business Name. All rights reserved.
      </footer>
    </div>
  );
}
