/* =========================================================
   OFFERVIEW – IA MODULES (OFICIAL)
   Archivo: offerview-ia-modules.js
   Autor: OfferView
   Descripción:
   Módulos de IA base para búsqueda, recomendación,
   tendencias y monetización.
   ========================================================= */

/* =========================================================
   1️⃣ OFFERVIEW AI SEARCH
   Analiza intención de búsqueda del usuario
   ========================================================= */
const OfferViewAISearch = {
  analyze(query) {
    return {
      query,
      intent: this.detectIntent(query),
      keywords: query.toLowerCase().split(" "),
      createdAt: new Date().toISOString()
    };
  },

  detectIntent(query) {
    const q = query.toLowerCase();
    if (q.includes("oferta") || q.includes("barato")) return "DEALS";
    if (q.includes("comprar")) return "BUY";
    if (q.includes("tienda")) return "STORE";
    if (q.includes("vuelo") || q.includes("hotel")) return "TRAVEL";
    return "SEARCH";
  }
};

/* =========================================================
   2️⃣ OFFERVIEW AI RECOMMENDER
   Recomienda tiendas según interés del usuario
   ========================================================= */
const OfferViewAIRecommender = {
  recommend(interests = []) {
    if (interests.includes("gaming"))
      return ["Steam", "Epic Games", "GameStop"];

    if (interests.includes("moda"))
      return ["Zara", "H&M", "Shein"];

    if (interests.includes("tecnologia"))
      return ["Amazon", "Newegg", "Samsung"];

    if (interests.includes("viajes"))
      return ["Booking", "Expedia", "Airbnb"];

    return ["Amazon", "AliExpress", "Mercado Libre"];
  }
};

/* =========================================================
   3️⃣ OFFERVIEW AI TRENDS
   Tendencias simuladas (luego API real)
   ========================================================= */
const OfferViewAITrends = {
  getTodayTrends() {
    return [
      "Ofertas Amazon hoy",
      "Zapatillas Nike en descuento",
      "Juegos PC baratos",
      "Vuelos baratos 2025"
    ];
  }
};

/* =========================================================
   4️⃣ OFFERVIEW AI MONETIZATION
   Decide enlaces afiliados inteligentes
   ========================================================= */
const OfferViewAIMonetization = {
  affiliateLinks: {
    Amazon: "https://www.amazon.com/?tag=offerview",
    AliExpress: "https://www.aliexpress.com/?aff=offerview",
    Booking: "https://www.booking.com/?aid=offerview"
  },

  getAffiliate(store) {
    return this.affiliateLinks[store] || null;
  }
};

/* =========================================================
   EXPORT GLOBAL (para uso en index.html)
   ========================================================= */
window.OfferViewAI = {
  search: OfferViewAISearch,
  recommend: OfferViewAIRecommender,
  trends: OfferViewAITrends,
  monetize: OfferViewAIMonetization
};
