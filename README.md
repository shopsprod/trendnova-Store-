# export default function TrendNovaStore() {
  const categories = ['Gaming', 'Tech', 'Lifestyle', 'Accessoires'];
  const products = [
    {
      name: 'Mini Projecteur LED',
      price: '39,99€',
      oldPrice: '59,99€',
      badge: 'Best Seller',
      image: 'https://images.unsplash.com/photo-1516321318423-f06f85e504b3?q=80&w=1200&auto=format&fit=crop',
      description: 'Transforme n’importe quelle pièce en cinéma.'
    },
    {
      name: 'Écouteurs Bluetooth Pro',
      price: '24,99€',
      oldPrice: '44,99€',
      badge: 'Promo',
      image: 'https://images.unsplash.com/photo-1505740420928-5e560c06d30e?q=80&w=1200&auto=format&fit=crop',
      description: 'Son premium et autonomie longue durée.'
    },
    {
      name: 'Lampe RGB Gaming',
      price: '19,99€',
      oldPrice: '34,99€',
      badge: 'Viral',
      image: 'https://images.unsplash.com/photo-1525547719571-a2d4ac8945e2?q=80&w=1200&auto=format&fit=crop',
      description: 'Ambiance gaming moderne et personnalisable.'
    },
    {
      name: 'Montre Connectée Fit+',
      price: '49,99€',
      oldPrice: '79,99€',
      badge: 'Nouveau',
      image: 'https://images.unsplash.com/photo-1523275335684-37898b6baf30?q=80&w=1200&auto=format&fit=crop',
      description: 'Suivi sport, notifications et design élégant.'
    }
  ];

  return (
    <div className="min-h-screen bg-black text-white font-sans">
      {/* Header */}
      <header className="flex items-center justify-between px-8 py-6 border-b border-gray-800 sticky top-0 bg-black/90 backdrop-blur z-50">
        <div className="flex items-center gap-3">
          <div className="w-12 h-12 rounded-2xl bg-white text-black flex items-center justify-center font-black text-2xl">
            T
          </div>
          <div>
            <h1 className="text-2xl font-bold">TrendNova</h1>
            <p className="text-gray-400 text-sm">Produits tendances</p>
          </div>
        </div>

        <nav className="hidden md:flex gap-8 text-gray-300 font-medium">
          <a href="#home" className="hover:text-white transition">Accueil</a>
          <a href="#products" className="hover:text-white transition">Produits</a>
          <a href="#about" className="hover:text-white transition">À propos</a>
          <a href="#contact" className="hover:text-white transition">Contact</a>
        </nav>

        <button className="bg-white text-black px-5 py-2 rounded-xl font-semibold hover:scale-105 transition">
          Panier
        </button>
      </header>

      {/* Hero */}
      <section id="home" className="px-8 py-24 text-center max-w-6xl mx-auto">
        <div className="inline-block px-4 py-2 rounded-full bg-white/10 border border-white/10 mb-6">
          Boutique tendance 2026
        </div>

        <h2 className="text-5xl md:text-7xl font-black leading-tight mb-6">
          Les meilleurs produits
          <br />
          du moment
        </h2>

        <p className="text-gray-400 text-lg max-w-2xl mx-auto mb-10">
          Découvrez une sélection moderne de gadgets, accessoires et produits viraux à prix accessibles.
        </p>

        <div className="flex gap-4 justify-center flex-wrap">
          <button className="bg-white text-black px-8 py-4 rounded-2xl font-bold hover:scale-105 transition">
            Acheter maintenant
          </button>

          <button className="border border-gray-700 px-8 py-4 rounded-2xl hover:bg-white hover:text-black transition">
            Voir les produits
          </button>
        </div>
      </section>

      {/* Features */}
      <section className="grid md:grid-cols-3 gap-6 px-8 pb-20 max-w-6xl mx-auto">
        <div className="bg-zinc-900 rounded-3xl p-8 border border-zinc-800">
          <h3 className="text-2xl font-bold mb-3">Livraison rapide</h3>
          <p className="text-gray-400">Produits expédiés directement chez vos clients.</p>
        </div>

        <div className="bg-zinc-900 rounded-3xl p-8 border border-zinc-800">
          <h3 className="text-2xl font-bold mb-3">Paiement sécurisé</h3>
          <p className="text-gray-400">Transactions sécurisées et simples.</p>
        </div>

        <div className="bg-zinc-900 rounded-3xl p-8 border border-zinc-800">
          <h3 className="text-2xl font-bold mb-3">Produits viraux</h3>
          <p className="text-gray-400">Les tendances TikTok et réseaux sociaux.</p>
        </div>
      </section>

      {/* Products */}
      <section className="px-8 pb-10 max-w-7xl mx-auto">
        <div className="flex gap-4 flex-wrap justify-center">
          {categories.map((category, index) => (
            <button
              key={index}
              className="px-6 py-3 rounded-2xl border border-zinc-700 hover:bg-white hover:text-black transition"
            >
              {category}
            </button>
          ))}
        </div>
      </section>

      <section id="products" className="px-8 py-16 max-w-7xl mx-auto">
        <div className="flex items-center justify-between mb-12 flex-wrap gap-4">
          <div>
            <h2 className="text-4xl font-black mb-2">Nos Produits</h2>
            <p className="text-gray-400">Sélection premium et moderne.</p>
          </div>

          <button className="border border-gray-700 px-6 py-3 rounded-xl hover:bg-white hover:text-black transition">
            Voir tout
          </button>
        </div>

        <div className="grid sm:grid-cols-2 lg:grid-cols-4 gap-8">
          {products.map((product, index) => (
            <div
              key={index}
              className="bg-zinc-900 rounded-3xl overflow-hidden border border-zinc-800 hover:scale-[1.02] transition duration-300 relative"
            >
              <div className="absolute top-4 left-4 z-10 bg-white text-black px-4 py-1 rounded-full text-sm font-bold">
                {product.badge}
              </div>

              <img
                src={product.image}
                alt={product.name}
                className="w-full h-64 object-cover"
              />

              <div className="p-6">
                <h3 className="text-2xl font-bold mb-2">{product.name}</h3>
                <p className="text-gray-400 mb-4">{product.description}</p>

                <div className="flex items-center justify-between">
                  <div>
                    <span className="text-2xl font-black block">{product.price}</span>
                    <span className="text-gray-500 line-through text-sm">{product.oldPrice}</span>
                  </div>

                  <button className="bg-white text-black px-4 py-2 rounded-xl font-semibold hover:scale-105 transition">
                    Acheter
                  </button>
                </div>
              </div>
            </div>
          ))}
        </div>
      </section>

      {/* Trust Section */}
      <section className="px-8 py-20 max-w-6xl mx-auto grid md:grid-cols-3 gap-8">
        <div className="bg-zinc-900 p-8 rounded-3xl border border-zinc-800">
          <h3 className="text-3xl font-black mb-4">+5000</h3>
          <p className="text-gray-400">Clients satisfaits</p>
        </div>

        <div className="bg-zinc-900 p-8 rounded-3xl border border-zinc-800">
          <h3 className="text-3xl font-black mb-4">24/7</h3>
          <p className="text-gray-400">Support client</p>
        </div>

        <div className="bg-zinc-900 p-8 rounded-3xl border border-zinc-800">
          <h3 className="text-3xl font-black mb-4">100%</h3>
          <p className="text-gray-400">Paiement sécurisé</p>
        </div>
      </section>

      {/* About */}
      <section id="about" className="px-8 py-24 max-w-5xl mx-auto text-center">
        <h2 className="text-5xl font-black mb-6">Pourquoi TrendNova ?</h2>

        <p className="text-gray-400 text-lg leading-relaxed">
          TrendNova sélectionne les produits les plus populaires et utiles du marché.
          Notre objectif est d’offrir une boutique simple, rapide et moderne avec les meilleures tendances du web.
        </p>
      </section>

      {/* Newsletter */}
      <section className="px-8 pb-24">
        <div className="max-w-4xl mx-auto bg-white text-black rounded-[40px] p-12 text-center">
          <h2 className="text-4xl font-black mb-4">Rejoins la communauté</h2>

          <p className="mb-8 text-gray-700">
            Reçois les nouveaux produits et offres exclusives.
          </p>

          <div className="flex flex-col md:flex-row gap-4 justify-center">
            <input
              type="email"
              placeholder="Votre email"
              className="px-6 py-4 rounded-2xl border border-gray-300 w-full md:w-96"
            />

            <button className="bg-black text-white px-8 py-4 rounded-2xl font-bold hover:scale-105 transition">
              S’inscrire
            </button>
          </div>
        </div>
      </section>

      {/* Footer */}
      <footer id="contact" className="border-t border-zinc-800 px-8 py-12 text-center text-gray-500">
        <div className="flex justify-center gap-6 mb-8 flex-wrap text-sm">
          <a href="#" className="hover:text-white transition">Livraison</a>
          <a href="#" className="hover:text-white transition">CGV</a>
          <a href="#" className="hover:text-white transition">Politique de retour</a>
          <a href="#" className="hover:text-white transition">Confidentialité</a>
          <a href="#" className="hover:text-white transition">Contact</a>
        </div>
        <div className="flex items-center justify-center gap-3 mb-4">
          <div className="w-10 h-10 rounded-2xl bg-white text-black flex items-center justify-center font-black text-xl">
            T
          </div>
          <h3 className="text-2xl font-bold text-white">TrendNova</h3>
        </div>

        <p>© 2026 TrendNova — Tous droits réservés.</p>
      </footer>
    </div>
  );
}