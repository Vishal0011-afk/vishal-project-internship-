# vishal-project-internship-
#internship project 
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>PORT1 - Deliver Anything, Anywhere</title>
  <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="bg-white text-gray-900">

  <header class="bg-blue-600 p-4 text-white">
    <div class="max-w-6xl mx-auto flex justify-between items-center">
      <h1 class="text-2xl font-bold">PORT1</h1>
      <nav class="space-x-4">
        <a href="#services" class="hover:underline">Services</a>
        <a href="#query" class="hover:underline">Raise a Query</a>
        <a href="#contact" class="hover:underline">Contact</a>
      </nav>
    </div>
  </header>

  <section class="bg-blue-50 py-20 text-center">
    <h2 class="text-4xl font-bold mb-4">Deliver Anything, Anywhere</h2>
    <p class="text-lg mb-6">Book mini trucks, bikes & more in minutes.</p>
    <a href="#query" class="bg-blue-600 text-white px-6 py-3 rounded-xl hover:bg-blue-700">Raise a Query</a>
  </section>

  <section id="services" class="py-16 max-w-6xl mx-auto">
    <h3 class="text-3xl font-bold text-center mb-8">Our Services</h3>
    <div class="grid md:grid-cols-3 gap-6">
      <div class="bg-white shadow-md p-6 rounded-xl">
        <h4 class="text-xl font-semibold mb-2">Bike Deliveries</h4>
        <p>Fast and efficient small item transport.</p>
      </div>
      <div class="bg-white shadow-md p-6 rounded-xl">
        <h4 class="text-xl font-semibold mb-2">Mini Trucks</h4>
        <p>Perfect for intra-city medium goods movement.</p>
      </div>
      <div class="bg-white shadow-md p-6 rounded-xl">
        <h4 class="text-xl font-semibold mb-2">LCVs</h4>
        <p>Large-scale logistics made simple.</p>
      </div>
    </div>
  </section>

  <section id="query" class="bg-gray-100 py-16">
    <div class="max-w-2xl mx-auto">
      <h3 class="text-3xl font-bold text-center mb-8">Raise a Delivery Query</h3>
      <form id="queryForm" class="space-y-4 bg-white p-6 rounded-xl shadow-md">
        <input type="text" name="pickup" placeholder="Pickup Location" required class="w-full border p-2 rounded" />
        <input type="text" name="drop" placeholder="Drop Location" required class="w-full border p-2 rounded" />
        <input type="text" name="goods" placeholder="Type of Goods" class="w-full border p-2 rounded" />
        <input type="text" name="weight" placeholder="Weight & Dimensions" class="w-full border p-2 rounded" />
        <input type="text" name="vehicle" placeholder="Preferred Vehicle Type" class="w-full border p-2 rounded" />
        <input type="datetime-local" name="datetime" required class="w-full border p-2 rounded" />
        <input type="text" name="name" placeholder="Your Name" required class="w-full border p-2 rounded" />
        <input type="email" name="email" placeholder="Email" required class="w-full border p-2 rounded" />
        <input type="tel" name="phone" placeholder="Phone Number" required class="w-full border p-2 rounded" />
        <button type="submit" class="w-full bg-blue-600 text-white py-2 rounded hover:bg-blue-700">Submit</button>
        <p id="status" class="text-center text-green-600 mt-4 hidden">Thanks! We'll get in touch shortly.</p>
      </form>
    </div>
  </section>

  <section id="contact" class="py-16 text-center">
    <h3 class="text-3xl font-bold mb-4">Need Help?</h3>
    <p class="mb-4">Check <a href="https://docs.google.com/spreadsheets/d/1abc123def456/edit?usp=sharing" target="_blank" class="text-blue-600 underline">this Google Sheet</a> or contact us below.</p>
    <p>📞 +91-7303503765 | 📧 support@port1.com</p>
    <p>📱 <a href="https://wa.me/7303503765" target="_blank" class="text-green-600 underline">Chat on WhatsApp</a></p>
  </section>

  <footer class="bg-blue-600 text-white text-center py-4">
    &copy; 2025 PORT1. All Rights Reserved.
  </footer>

  <script>
    const form = document.getElementById('queryForm');
    const status = document.getElementById('status');
    form.addEventListener('submit', async (e) => {
      e.preventDefault();
      const data = new FormData(form);
      const response = await fetch("https://script.google.com/macros/s/AKfycbx7H3-2gP6CJIXDJNkCxkMX8A67Uw4AlD5pKZmsLjpP8RRmC4lg-pc4LhRU24GbL5P61w/exec", {
        method: "POST",
        body: data
      });
      if (response.ok) {
        form.reset();
        status.classList.remove('hidden');
      }
    });
  </script>
</body>
</html>
