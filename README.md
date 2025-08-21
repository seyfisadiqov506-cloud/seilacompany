import React from "react";
import { motion } from "framer-motion";
import { Gift, Sparkles, Instagram, Phone, Mail, Store, MapPin, ArrowRight } from "lucide-react";
import { Button } from "@/components/ui/button";
import { Card, CardContent, CardHeader, CardTitle } from "@/components/ui/card";

// Seila Company — Landing Page (AZ)
// - Dil: Azərbaycan dili
// - Tailwind + shadcn/ui + Framer Motion
// Qeydlər:
//   • LOGO, şəkillər və linklərdəki placeholder-ləri real məlumatlarla əvəz edin.
//   • Kontaktlar bölməsində Instagram və e‑poçt realdır (@seilagifts, seyfi.sadiqov506@gmail.com).
//   • İstəsəniz, bu faylı Next.js/React layihəsinə bir komponent kimi əlavə edə bilərsiniz.

const NAV = {
  about: "Haqqımızda",
  gifts: "Seila Gifts",
  catalog: "Kataloq",
  contact: "Əlaqə",
};

const COPY = {
  brand: "Seila Company",
  tagline: "Xüsusi anlar üçün kreativ həllər",
  heroTitle: "Yadda qalan ideyalar, real nəticələr",
  heroSubtitle:
    "*Seila Gifts* markası altında unikal hədiyyələr, fərdiləşdirilmiş kompozisiyalar və işıqlı dekorlarla anlarınızı daha dəyərli edirik.",
  ctaPrimary: "WhatsApp-la yazın",
  ctaSecondary: "Kataloqa baxın",
  aboutTitle: "Şirkət haqqında",
  aboutText:
    "Seila Company — müasir ideyaları və kreativ həlləri birləşdirən brenddir. Missiyamız sadə əşyaları yaddaqalan təəssürata çevirmək, müştərilərimizə fərdiləşdirilmiş hədiyyələr və estetik təqdimat təklif etməkdir.",
  giftsTitle: "Seila Gifts",
  giftsText:
    "Fərdi çərçivələr (LED effektlə), adınıza özəlləşdirilən qutular, minimalist dekor setləri və tədbirlər üçün işıqlı installyasiyalar – hər biri sizin üslubunuza uyğun hazırlanır.",
  catalogTitle: "Populyar məhsullar",
  contactTitle: "Əlaqə",
  addressLabel: "Ünvan",
  address: "Bakı, Azərbaycan",
  phoneLabel: "Telefon",
  emailLabel: "E‑poçt",
  igLabel: "Instagram",
  footer: `© ${new Date().getFullYear()} Seila Company. Bütün hüquqlar qorunur.`,
};

const PRODUCTS = [
  {
    title: "AutoLuxe LED Çərçivə",
    desc: "Dinamik işıq effektləri və fərdiləşdirmə ilə premium çərçivə.",
    image:
      "https://images.unsplash.com/photo-1526318472351-c75fcf070305?q=80&w=1600&auto=format&fit=crop",
  },
  {
    title: "Fərdi Hədiyyə Qutusu",
    desc: "Ad, tarix və mesajla tam fərdiləşdirilmiş dizayn.",
    image:
      "https://images.unsplash.com/photo-1480554840075-1b2dc6e3a3f1?q=80&w=1600&auto=format&fit=crop",
  },
  {
    title: "Minimalist Dekor Seti",
    desc: "Evdə və ofisdə estetik atmosfer üçün seçilmiş elementlər.",
    image:
      "https://images.unsplash.com/photo-1519710164239-da123dc03ef4?q=80&w=1600&auto=format&fit=crop",
  },
];

export default function SeilaLandingAZ() {
  return (
    <div className="min-h-screen bg-white text-gray-900">
      {/* Header / Navbar */}
      <header className="sticky top-0 z-40 bg-white/70 backdrop-blur border-b">
        <div className="max-w-6xl mx-auto px-4 h-16 flex items-center justify-between">
          <div className="flex items-center gap-2 font-semibold">
            <Sparkles className="h-5 w-5" /> {COPY.brand}
          </div>
          <nav className="hidden md:flex items-center gap-6 text-sm">
            <a href="#about" className="hover:text-gray-600">{NAV.about}</a>
            <a href="#gifts" className="hover:text-gray-600">{NAV.gifts}</a>
            <a href="#catalog" className="hover:text-gray-600">{NAV.catalog}</a>
            <a href="#contact" className="hover:text-gray-600">{NAV.contact}</a>
          </nav>
          <div className="flex items-center gap-2">
            <a
              href="#contact"
              className="inline-flex items-center gap-2 text-sm px-3 py-2 rounded-2xl border hover:bg-gray-50"
            >
              <Phone className="h-4 w-4" /> {COPY.ctaPrimary}
            </a>
          </div>
        </div>
      </header>

      {/* Hero */}
      <section className="relative overflow-hidden">
        <div className="max-w-6xl mx-auto px-4 py-20 grid md:grid-cols-2 gap-8 items-center">
          <motion.div initial={{ opacity: 0, y: 24 }} animate={{ opacity: 1, y: 0 }} transition={{ duration: 0.5 }}>
            <h1 className="text-3xl md:text-5xl font-bold leading-tight">
              {COPY.heroTitle}
            </h1>
            <p className="mt-4 text-base md:text-lg text-gray-600" dangerouslySetInnerHTML={{ __html: COPY.heroSubtitle }} />
            <div className="mt-8 flex flex-wrap gap-3">
              <Button asChild className="rounded-2xl h-11 px-5">
                <a href="#contact" className="inline-flex items-center gap-2">
                  {COPY.ctaPrimary} <ArrowRight className="h-4 w-4" />
                </a>
              </Button>
              <Button asChild variant="outline" className="rounded-2xl h-11 px-5">
                <a href="#catalog">{COPY.ctaSecondary}</a>
              </Button>
            </div>
          </motion.div>
          <motion.div initial={{ opacity: 0, scale: 0.98 }} animate={{ opacity: 1, scale: 1 }} transition={{ duration: 0.5, delay: 0.1 }}>
            <div className="aspect-[4/3] w-full rounded-3xl overflow-hidden shadow">
              <img
                alt="Seila Gifts hero"
                src="https://images.unsplash.com/photo-1516387938699-a93567ec168e?q=80&w=1600&auto=format&fit=crop"
                className="w-full h-full object-cover"
              />
            </div>
          </motion.div>
        </div>
      </section>

      {/* About */}
      <section id="about" className="border-t">
        <div className="max-w-6xl mx-auto px-4 py-16 grid md:grid-cols-2 gap-8 items-start">
          <div>
            <h2 className="text-2xl md:text-3xl font-semibold">{COPY.aboutTitle}</h2>
            <p className="mt-4 text-gray-600">{COPY.aboutText}</p>
          </div>
          <div className="grid grid-cols-2 gap-4">
            {[1, 2, 3, 4].map((i) => (
              <div key={i} className="rounded-2xl overflow-hidden border">
                <img
                  alt={`Gallery ${i}`}
                  src={`https://picsum.photos/seed/seila-${i}/600/420`}
                  className="w-full h-40 object-cover"
                />
              </div>
            ))}
          </div>
        </div>
      </section>

      {/* Seila Gifts */}
      <section id="gifts" className="border-t bg-gray-50">
        <div className="max-w-6xl mx-auto px-4 py-16">
          <div className="flex items-center gap-2 mb-6">
            <Gift className="h-5 w-5" />
            <h2 className="text-2xl md:text-3xl font-semibold">{COPY.giftsTitle}</h2>
          </div>
          <p className="text-gray-600 max-w-3xl">{COPY.giftsText}</p>
        </div>
      </section>

      {/* Catalog */}
      <section id="catalog" className="border-t">
        <div className="max-w-6xl mx-auto px-4 py-16">
          <h2 className="text-2xl md:text-3xl font-semibold mb-8">{COPY.catalogTitle}</h2>
          <div className="grid md:grid-cols-3 gap-6">
            {PRODUCTS.map((p, idx) => (
              <Card key={idx} className="rounded-3xl overflow-hidden">
                <CardHeader>
                  <CardTitle className="text-lg">{p.title}</CardTitle>
                </CardHeader>
                <CardContent>
                  <div className="rounded-2xl overflow-hidden border">
                    <img alt={p.title} src={p.image} className="w-full h-48 object-cover" />
                  </div>
                  <p className="mt-3 text-sm text-gray-600">{p.desc}</p>
                  <div className="mt-4">
                    <Button asChild variant="outline" className="w-full rounded-2xl">
                      <a href="#contact">Sifariş et</a>
                    </Button>
                  </div>
                </CardContent>
              </Card>
            ))}
          </div>
        </div>
      </section>

      {/* Contact */}
      <section id="contact" className="border-t bg-gray-50">
        <div className="max-w-6xl mx-auto px-4 py-16 grid md:grid-cols-2 gap-8">
          <div>
            <h2 className="text-2xl md:text-3xl font-semibold mb-6">{COPY.contactTitle}</h2>
            <ul className="space-y-4 text-sm">
              <li className="flex items-center gap-3"><MapPin className="h-4 w-4" /> <span><strong>{COPY.addressLabel}:</strong> {COPY.address}</span></li>
              <li className="flex items-center gap-3"><Phone className="h-4 w-4" /> <span><strong>{COPY.phoneLabel}:</strong> —</span></li>
              <li className="flex items-center gap-3"><Mail className="h-4 w-4" /> <span><strong>{COPY.emailLabel}:</strong> <a className="underline" href="mailto:seyfi.sadiqov506@gmail.com">seyfi.sadiqov506@gmail.com</a></span></li>
              <li className="flex items-center gap-3"><Instagram className="h-4 w-4" /> <span><strong>{COPY.igLabel}:</strong> <a className="underline" href="https://instagram.com/seilagifts" target="_blank" rel="noreferrer">@seilagifts</a></span></li>
            </ul>
            <div className="mt-6 flex gap-3">
              <Button asChild className="rounded-2xl">
                <a href="#" aria-label="WhatsApp">WhatsApp</a>
              </Button>
              <Button asChild variant="outline" className="rounded-2xl">
                <a href="mailto:seyfi.sadiqov506@gmail.com">E‑poçt yazın</a>
              </Button>
            </div>
          </div>

          <div className="grid grid-cols-2 gap-4">
            {["https://images.unsplash.com/photo-1545235617-9465d2a55698?q=80&w=1600&auto=format&fit=crop",
              "https://images.unsplash.com/photo-1600721391666-c1b2a23c367b?q=80&w=1600&auto=format&fit=crop",
              "https://images.unsplash.com/photo-1503602642458-232111445657?q=80&w=1600&auto=format&fit=crop",
              "https://images.unsplash.com/photo-1503602642458-232111445657?q=80&w=1600&auto=format&fit=crop"].map((src, i) => (
              <div key={i} className="rounded-2xl overflow-hidden border aspect-[4/3]">
                <img alt={`Contact ${i+1}`} src={src} className="w-full h-full object-cover" />
              </div>
            ))}
          </div>
        </div>
      </section>

      {/* Footer */}
      <footer className="border-t">
        <div className="max-w-6xl mx-auto px-4 py-10 text-sm text-gray-600 flex items-center justify-between">
          <span>{COPY.footer}</span>
          <span className="flex items-center gap-2"><Store className="h-4 w-4" /> Seila Gifts</span>
        </div>
      </footer>
    </div>
  );
}
