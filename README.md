<!DOCTYPE html>
<html lang="pt">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Naturaltech & Bio Brazil Fair 2025 - Bilheteria</title>
  <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="bg-green-50 text-gray-800">
  <!-- Lang Switcher -->
  <div class="fixed top-4 right-4 z-50">
    <button type="button" onclick="switchLang('pt')" class="mx-1 px-2 py-1 border rounded bg-white text-sm">PT</button>
    <button type="button" onclick="switchLang('en')" class="mx-1 px-2 py-1 border rounded bg-white text-sm">EN</button>
  </div>

  <!-- Banner -->
  <header class="relative h-64 w-full overflow-hidden">
    <img src="https://images.unsplash.com/photo-1542838687-7183a53647bb?auto=format&fit=crop&w=1470&q=80" alt="Naturaltech Fair" class="absolute inset-0 w-full h-full object-cover opacity-80" />
    <div class="absolute inset-0 bg-green-900 bg-opacity-40 flex items-center justify-center">
      <h1 class="text-white text-4xl md:text-5xl font-bold text-center px-4"
          data-pt="Naturaltech & Bio Brazil Fair 2025"
          data-en="Naturaltech & Bio Brazil Fair 2025">
        Naturaltech & Bio Brazil Fair 2025
      </h1>
    </div>
  </header>

  <!-- Countdown -->
  <div class="text-center bg-green-200 py-4 font-semibold text-green-900 text-xl" id="countdown"></div>

  <!-- Intro -->
  <main class="text-center mt-10">
    <h2 class="text-3xl font-bold mb-4 text-green-700" 
        data-pt="Bilheteria para a Naturaltech & Bio Brazil Fair 2025"
        data-en="Ticketing for Naturaltech & Bio Brazil Fair 2025">
      Bilheteria para a Naturaltech & Bio Brazil Fair 2025
    </h2>
    <p class="mb-6 text-lg"
       data-pt="Garanta sua entrada para o maior evento de produtos naturais da América Latina."
       data-en="Secure your entry to the largest natural products event in Latin America.">
      Garanta sua entrada para o maior evento de produtos naturais da América Latina.
    </p>
  </main>

  <!-- À propos -->
  <section class="bg-white py-10 px-6 md:px-20">
    <h2 class="text-3xl font-bold text-green-700 mb-6" data-pt="Sobre o Evento" data-en="About the Event">Sobre o Evento</h2>
    <p class="text-lg mb-4"
       data-pt="A Naturaltech & Bio Brazil Fair é a maior feira de produtos naturais, orgânicos e sustentáveis da América Latina..."
       data-en="Naturaltech & Bio Brazil Fair is Latin America's largest event for natural, organic and sustainable products...">
      A Naturaltech & Bio Brazil Fair é a maior feira de produtos naturais, orgânicos e sustentáveis da América Latina...
    </p>
    <p class="text-lg font-semibold text-green-800"
       data-pt="Participe e conecte-se com um futuro mais saudável e sustentável!"
       data-en="Join us and connect with a healthier, more sustainable future!">
      Participe e conecte-se com um futuro mais saudável e sustentável!
    </p>
  </section>

  <!-- Tickets -->
  <section class="py-12 px-6 md:px-20 bg-green-100">
    <h2 class="text-3xl font-bold text-green-800 mb-8" data-pt="Escolha seu ingresso" data-en="Choose your ticket">Escolha seu ingresso</h2>
    <div class="grid md:grid-cols-3 gap-8">
      <div class="bg-white p-6 rounded shadow text-center">
        <h3 class="text-xl font-bold mb-2" data-pt="Passaporte 2 dias" data-en="2-Day Pass">Passaporte 2 dias</h3>
        <p class="text-green-700 font-bold text-lg mb-4">R$ 40</p>
        <button type="button" onclick="openForm('Passaporte 2 dias', '40')" class="bg-green-600 text-white px-4 py-2 rounded" data-pt="Comprar" data-en="Buy">Comprar</button>
      </div>
      <div class="bg-white p-6 rounded shadow text-center">
        <h3 class="text-xl font-bold mb-2" data-pt="Passaporte 3 dias" data-en="3-Day Pass">Passaporte 3 dias</h3>
        <p class="text-green-700 font-bold text-lg mb-4">R$ 60</p>
        <button type="button" onclick="openForm('Passaporte 3 dias', '60')" class="bg-green-600 text-white px-4 py-2 rounded" data-pt="Comprar" data-en="Buy">Comprar</button>
      </div>
      <div class="bg-white p-6 rounded shadow text-center">
        <h3 class="text-xl font-bold mb-2" data-pt="VIP" data-en="VIP">VIP</h3>
        <p class="text-green-700 font-bold text-lg mb-4">R$ 100</p>
        <button type="button" onclick="openForm('VIP', '100')" class="bg-green-600 text-white px-4 py-2 rounded" data-pt="Comprar" data-en="Buy">Comprar</button>
      </div>
    </div>
  </section>

  <!-- Formulaire -->
  <div id="buyForm" class="hidden fixed top-0 left-0 w-full h-full bg-black bg-opacity-60 flex items-center justify-center z-40">
    <div class="bg-white p-6 rounded shadow-xl w-96">
      <h2 class="text-xl font-bold mb-4" data-pt="Formulário de Compra" data-en="Purchase Form">Formulário de Compra</h2>
      <form action="https://formspree.io/f/xxxxxxx" method="POST">
        <label class="block mb-2 font-semibold" data-pt="Nome completo" data-en="Full Name">Nome completo</label>
        <input name="nome" type="text" class="w-full border p-2 mb-4" required />

        <label class="block mb-2 font-semibold" data-pt="Email" data-en="Email">Email</label>
        <input name="email" type="email" class="w-full border p-2 mb-4" required />

        <label class="block mb-2 font-semibold" data-pt="Tipo de ingresso" data-en="Ticket Type">Tipo de ingresso</label>
        <input name="tipo" type="text" id="ticketType" class="w-full border p-2 mb-4" readonly />

        <label class="block mb-2 font-semibold" data-pt="Preço (R$)" data-en="Price (R$)">Preço (R$)</label>
        <input name="preco" type="text" id="ticketPrice" class="w-full border p-2 mb-4" readonly />

        <input type="hidden" name="_subject" value="Nova compra de ingresso" />

        <p class="text-sm text-green-700 mt-2 mb-4" data-pt="Você receberá os dados para pagamento via PIX após o envio." data-en="You will receive PIX payment details after submission.">
          Você receberá os dados para pagamento via PIX após o envio.
        </p>

        <div class="flex justify-end space-x-2">
          <button type="button" onclick="closeForm()" class="bg-gray-300 px-4 py-2 rounded" data-pt="Cancelar" data-en="Cancel">Cancelar</button>
          <button type="submit" class="bg-green-600 text-white px-4 py-2 rounded" data-pt="Enviar" data-en="Submit">Enviar</button>
        </div>
      </form>
    </div>
  </div>

  <!-- Footer -->
  <footer class="bg-green-900 text-green-100 text-center py-4 mt-16">
    <p data-pt="Evento: Naturaltech & Bio Brazil Fair 2025 | Data: 11-14 de junho de 2025 | Local: Anhembi Exhibition Center, São Paulo"
       data-en="Event: Naturaltech & Bio Brazil Fair 2025 | Date: June 11-14, 2025 | Location: Anhembi Exhibition Center, São Paulo">
      Evento: Naturaltech & Bio Brazil Fair 2025 | Data: 11-14 de junho de 2025 | Local: Anhembi Exhibition Center, São Paulo
    </p>
  </footer>

  <!-- JavaScript -->
  <script>
    function openForm(type, price) {
      document.getElementById('buyForm').classList.remove('hidden');
      document.getElementById('ticketType').value = type;
      document.getElementById('ticketPrice').value = price;
    }

    function closeForm() {
      document.getElementById('buyForm').classList.add('hidden');
    }

    function switchLang(lang) {
      document.querySelectorAll('[data-pt]').forEach(el => {
        if (el.dataset[lang]) {
          el.innerText = el.dataset[lang];
        }
      });
      localStorage.setItem('preferredLang', lang);
    }

    function updateCountdown() {
      const countdownEl = document.getElementById('countdown');
      const eventDate = new Date('2025-06-11T09:00:00');
      const now = new Date();
      const diff = eventDate - now;

      if (diff <= 0) {
        countdownEl.innerText = localStorage.getItem('preferredLang') === 'en' ? "The event has started!" : "O evento já começou!";
        return;
      }

      const days = Math.floor(diff / (1000 * 60 * 60 * 24));
      const hours = Math.floor((diff / (1000 * 60 * 60)) % 24);
      const minutes = Math.floor((diff / (1000 * 60)) % 60);
      const seconds = Math.floor((diff / 1000) % 60);

      countdownEl.innerText = (localStorage.getItem('preferredLang') === 'en' ? "Countdown to event: " : "Contagem regressiva para o evento: ") +
        `${days}d ${hours}h ${minutes}m ${seconds}s`;
    }

    window.addEventListener('DOMContentLoaded', () => {
      const preferredLang = localStorage.getItem('preferredLang') || (navigator.language.slice(0, 2) === 'en' ? 'en' : 'pt');
      switchLang(preferredLang);
      updateCountdown();
      setInterval(updateCountdown, 1000);
    });
  </script>
</body>
</html>
