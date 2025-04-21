export default function HomePage() { return ( <main className="flex flex-col items-center justify-center p-4 space-y-10 relative"> {/* Botón de volver */} <button onClick={() => window.history.back()} className="fixed top-4 left-4 bg-gray-800 text-white px-3 py-1 rounded-full shadow-lg z-50" > ← Volver </button>

{/* Logo principal */}
  <section className="w-full max-w-xs">
    <img
      src="/mnt/data/file-AcuQ2PLoqudtNVCgHfr8c5"
      alt="Roots and Routes Costa Rica Vacations Logo"
      className="w-full object-contain"
    />
  </section>

  {/* Imagen alusiva a la variedad de productos */}
  <section className="w-full max-w-6xl">
    <img
      src="/mnt/data/A_high-resolution_digital_photograph_collage_showc.png"
      alt="Costa Rica experiencia completa: transporte, alojamiento, tours"
      className="w-full rounded-2xl shadow"
    />
  </section>

  {/* Encabezado principal */}
  <section className="w-full text-center space-y-4">
    <h1 className="text-4xl font-bold">Roots and Routes Costa Rica Vacations</h1>
    <p className="text-xl">Transport, Car Rentals, Lodging, Guided. All-in-One.</p>
    <div className="flex justify-end w-full max-w-5xl mt-4">
      <select className="border p-2 rounded">
        <option value="es">Español</option>
        <option value="en">English</option>
      </select>
    </div>
    <div className="flex flex-wrap justify-center gap-4 mt-6">
      <button className="bg-blue-500 text-white px-4 py-2 rounded-2xl shadow">Reservar Transporte</button>
      <button className="bg-green-500 text-white px-4 py-2 rounded-2xl shadow">Alquilar Carro</button>
      <button className="bg-orange-500 text-white px-4 py-2 rounded-2xl shadow">Buscar Hospedaje</button>
      <button className="bg-red-500 text-white px-4 py-2 rounded-2xl shadow">Explorar Tours</button>
    </div>
  </section>

  {/* Servicios principales */}
  <section className="w-full max-w-5xl grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6">
    {[
      { title: "Transporte Privado", desc: "Traslados seguros entre destinos y aeropuertos." },
      { title: "Renta de Carro", desc: "Compará y reservá tu vehículo ideal para explorar." },
      { title: "Alojamiento", desc: "Casas vacacionales y hoteles verificados por nosotros." },
      { title: "Tours Guiados", desc: "Aventura, naturaleza y cultura en los mejores destinos." },
    ].map((s, i) => (
      <div key={i} className="border rounded-2xl p-4 shadow hover:shadow-lg transition">
        <h3 className="text-xl font-semibold mb-2">{s.title}</h3>
        <p>{s.desc}</p>
        <button className="mt-4 text-blue-600 underline">Reservar</button>
      </div>
    ))}
  </section>

  {/* Paquetes destacados */}
  <section className="w-full max-w-4xl text-center mt-10">
    <h2 className="text-2xl font-bold mb-4">Paquetes Completos</h2>
    <p className="mb-4">Itinerarios armados para que solo te preocupes por disfrutar.</p>
    <div className="bg-gray-100 p-4 rounded-2xl">
      <h3 className="text-lg font-semibold">7 días Arenal + Monteverde</h3>
      <p>Incluye transporte, alojamiento y tours. Desde $850 por persona.</p>
      <button className="mt-2 text-blue-600 underline">Ver más</button>
    </div>
  </section>

  {/* Quiénes somos */}
  <section className="w-full max-w-3xl mt-10 text-center">
    <h2 className="text-2xl font-bold mb-2">¿Quiénes Somos?</h2>
    <p className="mb-4">Somos una empresa costarricense dedicada a ofrecer experiencias turísticas completas y personalizadas. ¡Viví Costa Rica con nosotros!</p>
    <div className="flex justify-center gap-4">
      <a href="#" className="text-blue-600 underline">Instagram</a>
      <a href="#" className="text-blue-600 underline">Facebook</a>
      <a href="#" className="text-blue-600 underline">WhatsApp</a>
    </div>
  </section>

  {/* Testimonios */}
  <section className="w-full max-w-4xl mt-10 text-center">
    <h2 className="text-2xl font-bold mb-4">Testimonios</h2>
    <div className="grid grid-cols-1 md:grid-cols-2 gap-6">
      {[
        {
          name: "Emily (USA)",
          text: "Roots and Routes made our trip stress-free. The service was amazing from start to finish!"
        },
        {
          name: "Luis (España)",
          text: "Una experiencia inolvidable. Todo bien coordinado, desde el carro hasta las actividades."
        }
      ].map((t, i) => (
        <div key={i} className="border rounded-2xl p-4 shadow">
          <p className="italic">“{t.text}”</p>
          <p className="mt-2 font-semibold">– {t.name}</p>
        </div>
      ))}
    </div>
  </section>

  {/* Formulario de contacto */}
  <section className="w-full max-w-xl mt-10 text-center">
    <h2 className="text-2xl font-bold mb-2">Contáctanos</h2>
    <p className="mb-4">¿Tenés preguntas? Escribinos y con gusto te ayudamos.</p>
    <form className="flex flex-col space-y-3">
      <input type="text" placeholder="Nombre" className="border p-2 rounded" />
      <input type="email" placeholder="Correo" className="border p-2 rounded" />
      <textarea placeholder="Mensaje" className="border p-2 rounded" rows="3" />
      <button className="bg-blue-500 text-white py-2 rounded-2xl">Enviar</button>
    </form>
  </section>
</main>

); }

