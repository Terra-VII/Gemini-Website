'use client';

import React, { useState, useEffect } from 'react';
import Image from 'next/image';
import { 
  Shield, 
  Navigation, 
  Radio, 
  MapPin, 
  Compass, 
  ChevronRight, 
  Sliders, 
  Calendar, 
  Users, 
  CheckCircle, 
  Menu, 
  X, 
  Info,
  HelpCircle,
  Mail,
  Camera,
  BookOpen
} from 'lucide-react';

export default function TerraVIIMasterPage() {
  const [activeTab, setActiveTab] = useState<'home' | 'about' | 'philosophy' | 'expeditions' | 'dossier' | 'gallery' | 'journal' | 'booking' | 'contact' | 'faq'>('home');
  const [altitude, setAltitude] = useState(13700);
  const [selectedHotspot, setSelectedHotspot] = useState<number | null>(0);
  const [isVettingOpen, setIsVettingOpen] = useState(false);
  const [mobileMenuOpen, setMobileMenuOpen] = useState(false);

  // Vetting Form State
  const [vettingStep, setVettingStep] = useState(1);
  const [formData, setFormData] = useState({
    route: 'Tawang & Beyond',
    experience: 'Intermediate Off-Road',
    altitudeReadiness: 'Yes',
    name: '',
    email: '',
    phone: ''
  });

  // Hotspots for Mechanical Dissection
  const hotspots = [
    { id: 0, label: 'SATELLITE MESH', title: 'Garmin InReach Telemetry', desc: 'Continuous satellite positioning & SOS uplink in zero-cellular border zones.' },
    { id: 1, label: 'PARAMEDIC CHASE', title: '4x4 Medical Redundancy', desc: 'Dedicated chase vehicle carrying compressed oxygen and emergency trauma kit within 5 minutes.' },
    { id: 2, label: 'HIGH-CLEARANCE SUSPENSION', title: 'Terrain-Tuned Travel', desc: 'Re-valved long-travel suspension designed for slate drops and unpaved riverbed crossings.' }
  ];

  // FAQ Items
  const faqs = [
    { q: 'Why is each convoy strictly capped at 8 riders?', a: 'Zero crowd friction. Eight machines stay nimble across narrow alpine switchbacks, landslides, and river crossings where large groups get stranded.' },
    { q: 'What riding experience is required?', a: 'Riders must have solid intermediate off-road experience, confidence on loose gravel/slate, and physical readiness for 13,000+ FT altitude endurance.' },
    { q: 'What medical safety support is provided?', a: 'Every expedition is flanked by a dedicated 4x4 paramedic chase vehicle equipped with medical-grade oxygen canisters, trauma kits, and satellite SOS channels.' }
  ];

  return (
    <div className="bg-[#030303] text-[#E5E5E5] min-h-screen font-sans selection:bg-[#8C734B] selection:text-black relative">
      
      {/* ------------------------------------------------------------- */}
      {/* GLOBAL HEADER                                                */}
      {/* ------------------------------------------------------------- */}
      <header className="fixed top-0 left-0 right-0 z-50 bg-[#030303]/85 backdrop-blur-md border-b border-white/5 px-6 md:px-12 py-4 flex items-center justify-between">
        
        {/* Dedicated Uncropped Raw Logo Slot */}
        <button onClick={() => setActiveTab('home')} className="relative flex items-center h-12 w-48 text-left">
          <div className="flex items-center space-x-3">
            <div className="w-9 h-9 border border-[#8C734B]/40 rounded-full flex items-center justify-center font-mono text-xs text-[#8C734B] tracking-widest">
              VII
            </div>
            <div>
              <span className="font-heading tracking-[0.25em] text-[#E5E5E5] text-sm uppercase block font-bold">
                TERRA VII
              </span>
              <span className="font-mono text-[9px] text-stone-500 tracking-widest uppercase block">
                LAND OF THE SEVEN
              </span>
            </div>
          </div>
        </button>

        {/* Desktop Navigation */}
        <nav className="hidden lg:flex items-center space-x-6 font-mono text-xs tracking-widest text-stone-400">
          <button onClick={() => setActiveTab('about')} className={`hover:text-[#8C734B] transition-colors uppercase ${activeTab === 'about' ? 'text-[#8C734B]' : ''}`}>ABOUT</button>
          <button onClick={() => setActiveTab('philosophy')} className={`hover:text-[#8C734B] transition-colors uppercase ${activeTab === 'philosophy' ? 'text-[#8C734B]' : ''}`}>PHILOSOPHY</button>
          <button onClick={() => setActiveTab('expeditions')} className={`hover:text-[#8C734B] transition-colors uppercase ${activeTab === 'expeditions' ? 'text-[#8C734B]' : ''}`}>EXPEDITIONS</button>
          <button onClick={() => setActiveTab('gallery')} className={`hover:text-[#8C734B] transition-colors uppercase ${activeTab === 'gallery' ? 'text-[#8C734B]' : ''}`}>GALLERY</button>
          <button onClick={() => setActiveTab('journal')} className={`hover:text-[#8C734B] transition-colors uppercase ${activeTab === 'journal' ? 'text-[#8C734B]' : ''}`}>JOURNAL</button>
          <button onClick={() => setActiveTab('faq')} className={`hover:text-[#8C734B] transition-colors uppercase ${activeTab === 'faq' ? 'text-[#8C734B]' : ''}`}>FAQ</button>
          <button onClick={() => setActiveTab('contact')} className={`hover:text-[#8C734B] transition-colors uppercase ${activeTab === 'contact' ? 'text-[#8C734B]' : ''}`}>COMMAND</button>
        </nav>

        {/* Clearance Vetting CTA */}
        <div className="flex items-center space-x-4">
          <button 
            onClick={() => setIsVettingOpen(true)} 
            className="px-5 py-2.5 bg-[#8C734B] hover:bg-[#A3875B] text-black font-mono text-xs tracking-widest uppercase font-semibold transition-all shadow-lg"
          >
            CLAIM SEAT
          </button>

          <button onClick={() => setMobileMenuOpen(!mobileMenuOpen)} className="lg:hidden p-2 text-stone-300">
            {mobileMenuOpen ? <X size={20} /> : <Menu size={20} />}
          </button>
        </div>
      </header>

      {/* Mobile Drawer Navigation */}
      {mobileMenuOpen && (
        <div className="fixed inset-0 z-40 bg-[#030303] pt-28 px-8 flex flex-col space-y-6 font-mono text-sm text-stone-300 lg:hidden border-b border-white/10">
          <button onClick={() => { setActiveTab('home'); setMobileMenuOpen(false); }} className="text-left border-b border-white/5 pb-2">01 / HOME</button>
          <button onClick={() => { setActiveTab('about'); setMobileMenuOpen(false); }} className="text-left border-b border-white/5 pb-2">02 / ABOUT</button>
          <button onClick={() => { setActiveTab('philosophy'); setMobileMenuOpen(false); }} className="text-left border-b border-white/5 pb-2">03 / PHILOSOPHY</button>
          <button onClick={() => { setActiveTab('expeditions'); setMobileMenuOpen(false); }} className="text-left border-b border-white/5 pb-2">04 / EXPEDITIONS</button>
          <button onClick={() => { setActiveTab('gallery'); setMobileMenuOpen(false); }} className="text-left border-b border-white/5 pb-2">05 / GALLERY</button>
          <button onClick={() => { setActiveTab('journal'); setMobileMenuOpen(false); }} className="text-left border-b border-white/5 pb-2">06 / JOURNAL</button>
          <button onClick={() => { setActiveTab('faq'); setMobileMenuOpen(false); }} className="text-left border-b border-white/5 pb-2">07 / FAQ</button>
          <button onClick={() => { setActiveTab('contact'); setMobileMenuOpen(false); }} className="text-left border-b border-white/5 pb-2">08 / COMMAND</button>
        </div>
      )}

      {/* ------------------------------------------------------------- */}
      {/* REALTIME TELEMETRY ALTIMETER (FIXED)                          */}
      {/* ------------------------------------------------------------- */}
      <div className="fixed right-6 bottom-12 z-30 hidden md:flex flex-col items-end font-mono text-xs text-[#8C734B] bg-[#030303]/90 p-4 border border-white/10 backdrop-blur-md">
        <span className="text-[10px] text-stone-500 tracking-widest uppercase">REALTIME TELEMETRY</span>
        <div className="flex items-baseline space-x-1 mt-1">
          <span className="text-2xl font-bold text-[#E5E5E5]">{altitude.toLocaleString()}</span>
          <span className="text-stone-400">FT</span>
        </div>
        <span className="text-[9px] text-[#D03B2B] mt-1 tracking-widest uppercase">SELA PASS PASSAGE</span>
      </div>

      {/* ------------------------------------------------------------- */}
      {/* MAIN VIEW SYSTEM                                              */}
      {/* ------------------------------------------------------------- */}
      <div className="pt-28">

        {/* HOMEPAGE: 5 NARRATIVE CHAPTERS */}
        {activeTab === 'home' && (
          <main className="max-w-7xl mx-auto px-6 md:px-12 space-y-32">
            
            {/* CHAPTER I: SILENCE BEFORE ENGINE */}
            <section className="min-h-[85vh] flex flex-col justify-center border-b border-white/10 pb-20">
              <span className="font-mono text-xs text-[#8C734B] tracking-[0.3em] uppercase flex items-center space-x-2">
                <MapPin size={12} className="text-[#D03B2B]" />
                <span>27.5860° N, 91.8594° E — ARUNACHAL PRADESH</span>
              </span>
              <h1 className="font-heading text-5xl md:text-8xl uppercase tracking-widest mt-6 leading-none">
                THE UNPAVED <br /><span className="text-[#8C734B]">FRONTIER</span>
              </h1>
              <p className="mt-8 text-stone-400 max-w-xl text-sm leading-relaxed font-light">
                We do not run commercial tours. We field tactical platoons of eight riders into the unmapped, high-altitude passes of Northeast India.
              </p>
              <div className="mt-12 flex flex-wrap gap-4">
                <button 
                  onClick={() => setIsVettingOpen(true)}
                  className="px-8 py-4 bg-[#8C734B] hover:bg-[#A3875B] text-black font-mono text-xs tracking-widest uppercase font-semibold transition-all shadow-lg"
                >
                  CLAIM COHORT SEAT
                </button>
                <button 
                  onClick={() => setActiveTab('dossier')}
                  className="px-8 py-4 border border-white/20 hover:border-[#8C734B] font-mono text-xs tracking-widest uppercase text-stone-300 transition-all"
                >
                  INSPECT DOSSIER
                </button>
              </div>
            </section>

            {/* CHAPTER II: ELEVATION ASCENT */}
            <section className="py-16 border-b border-white/10 space-y-12">
              <div className="flex flex-col md:flex-row justify-between items-start md:items-end gap-6">
                <div>
                  <span className="font-mono text-xs text-[#8C734B] tracking-widest uppercase">CHAPTER II / ASCENT</span>
                  <h2 className="font-heading text-3xl md:text-5xl uppercase tracking-widest mt-2">VERTICAL ELEVATION</h2>
                </div>
                <div className="font-mono text-xs text-stone-400">
                  SCRUB ELEVATION: 
                  <input 
                    type="range" 
                    min="3200" 
                    max="15200" 
                    value={altitude} 
                    onChange={(e) => setAltitude(Number(e.target.value))} 
                    className="ml-3 accent-[#8C734B]"
                  />
                </div>
              </div>

              <div className="grid grid-cols-1 md:grid-cols-3 gap-6 font-mono text-xs">
                <div className="bg-white/5 p-6 border-l-2 border-[#8C734B] space-y-2">
                  <span className="text-stone-500">3,200 FT — MEGHALAYA</span>
                  <h4 className="font-heading text-lg text-[#E5E5E5]">SUBTROPICAL GORGES</h4>
                  <p className="text-stone-400 font-sans text-xs">Wet gravel trails, rainforest river crossings, chassis mud armor testing.</p>
                </div>
                <div className="bg-white/5 p-6 border-l-2 border-[#8C734B] space-y-2">
                  <span className="text-stone-500">8,900 FT — DIRANG VALLEY</span>
                  <h4 className="font-heading text-lg text-[#E5E5E5]">HIGH-ALTITUDE PINE</h4>
                  <p className="text-stone-400 font-sans text-xs">Loose slate switchbacks, thinning air, technical engine carburetor tuning.</p>
                </div>
                <div className="bg-white/5 p-6 border-l-2 border-[#D03B2B] space-y-2">
                  <span className="text-[#D03B2B]">13,700 FT — SELA PASS</span>
                  <h4 className="font-heading text-lg text-[#E5E5E5]">FROZEN RIDGE LINE</h4>
                  <p className="text-stone-400 font-sans text-xs">Sub-zero granite drops, snapping prayer flags, complete high-altitude solitude.</p>
                </div>
              </div>
            </section>

            {/* CHAPTER III: MECHANICAL DISSECTION */}
            <section className="py-16 border-b border-white/10 space-y-8">
              <span className="font-mono text-xs text-[#8C734B] tracking-widest uppercase">CHAPTER III / TACTICAL MACHINE</span>
              <h2 className="font-heading text-3xl md:text-5xl uppercase tracking-widest">ENGINEERED FOR THE UNPAVED</h2>

              <div className="grid grid-cols-1 lg:grid-cols-3 gap-8 items-center bg-white/5 p-8 border border-white/10">
                <div className="space-y-4 lg:col-span-1">
                  {hotspots.map((hs) => (
                    <button
                      key={hs.id}
                      onClick={() => setSelectedHotspot(hs.id)}
                      className={`w-full text-left p-4 border transition-all font-mono text-xs ${selectedHotspot === hs.id ? 'border-[#8C734B] bg-[#8C734B]/10 text-[#E5E5E5]' : 'border-white/10 text-stone-500 hover:text-stone-300'}`}
                    >
                      <span className="block text-[10px] text-[#8C734B] mb-1">SPEC 0{hs.id + 1}</span>
                      <span className="font-bold uppercase tracking-wider block">{hs.label}</span>
                    </button>
                  ))}
                </div>

                <div className="lg:col-span-2 p-6 border-l border-white/10 space-y-4">
                  <span className="font-mono text-xs text-[#D03B2B] tracking-widest uppercase">MECHANICAL DETAIL</span>
                  <h3 className="font-heading text-2xl uppercase tracking-wider">{hotspots[selectedHotspot || 0].title}</h3>
                  <p className="text-stone-400 text-sm leading-relaxed">{hotspots[selectedHotspot || 0].desc}</p>
                </div>
              </div>
            </section>

            {/* CHAPTER IV: THE 8-RIDER PACT */}
            <section className="py-16 border-b border-white/10 grid grid-cols-1 md:grid-cols-3 gap-12">
              <div className="space-y-2">
                <span className="font-mono text-xs text-[#8C734B]">01 / CAPACITY CAP</span>
                <h3 className="font-heading text-xl">8 RIDERS MAXIMUM</h3>
                <p className="text-xs text-stone-400 leading-relaxed font-light">Zero crowd friction. Complete convoy mobility across technical cliffside ledges.</p>
              </div>
              <div className="space-y-2">
                <span className="font-mono text-xs text-[#8C734B]">02 / CHASE VEHICLE</span>
                <h3 className="font-heading text-xl">PARAMEDIC & OXYGEN</h3>
                <p className="text-xs text-stone-400 leading-relaxed font-light">Dedicated 4x4 support carrying medical-grade oxygen canisters and trauma equipment.</p>
              </div>
              <div className="space-y-2">
                <span className="font-mono text-xs text-[#8C734B]">03 / SAT COMMS</span>
                <h3 className="font-heading text-xl">GARMIN MESH UPLINK</h3>
                <p className="text-xs text-stone-400 leading-relaxed font-light">Realtime satellite tracking across zero-cellular Himalayan border sectors.</p>
              </div>
            </section>

          </main>
        )}

        {/* VIEW: ABOUT */}
        {activeTab === 'about' && (
          <main className="max-w-7xl mx-auto px-6 md:px-12 py-12 space-y-12">
            <span className="font-mono text-xs text-[#8C734B] tracking-widest uppercase">ABOUT TERRA VII</span>
            <h1 className="font-heading text-4xl md:text-6xl uppercase tracking-widest">WE DO NOT RUN TOURS</h1>
            <p className="text-stone-300 max-w-2xl text-sm leading-relaxed">
              TERRA VII was forged to reclaim high-altitude motorcycle expeditions from commercial tourism. We operate strictly as exclusive 8-rider platoons, combining high-altitude logistics, paramedic redundancy, and local monastic respect.
            </p>
          </main>
        )}

        {/* VIEW: PHILOSOPHY */}
        {activeTab === 'philosophy' && (
          <main className="max-w-7xl mx-auto px-6 md:px-12 py-12 space-y-12">
            <span className="font-mono text-xs text-[#8C734B] tracking-widest uppercase">OPERATIONAL PHILOSOPHY</span>
            <h1 className="font-heading text-4xl md:text-6xl uppercase tracking-widest">TRANSFORMATION OVER TURISM</h1>
            <blockquote className="border-l-2 border-[#8C734B] pl-6 text-xl font-heading text-stone-300">
              "The mountain does not care about your titles. High air humbles everyone equally."
            </blockquote>
          </main>
        )}

        {/* VIEW: EXPEDITIONS CATALOG */}
        {activeTab === 'expeditions' && (
          <main className="max-w-7xl mx-auto px-6 md:px-12 py-12 space-y-12">
            <span className="font-mono text-xs text-[#8C734B] tracking-widest uppercase">EXPEDITIONS CATALOG</span>
            <h1 className="font-heading text-4xl md:text-6xl uppercase tracking-widest">MASTER ROUTES</h1>

            <div className="grid grid-cols-1 md:grid-cols-2 gap-8">
              <div className="bg-white/5 p-8 border border-white/10 space-y-4">
                <span className="font-mono text-xs text-[#D03B2B]">ROUTE 01 — FLAGSHIP</span>
                <h3 className="font-heading text-2xl uppercase">TAWANG & BEYOND</h3>
                <p className="text-xs text-stone-400">12 Days / 13,700 FT Max / Arunachal Pradesh</p>
                <div className="flex justify-between items-center pt-4 border-t border-white/10">
                  <span className="font-mono text-sm text-[#8C734B]">₹285,000</span>
                  <button onClick={() => setActiveTab('dossier')} className="font-mono text-xs underline text-stone-300">INSPECT DOSSIER</button>
                </div>
              </div>

              <div className="bg-white/5 p-8 border border-white/10 space-y-4 opacity-75">
                <span className="font-mono text-xs text-stone-500">ROUTE 02 — ADVANCED</span>
                <h3 className="font-heading text-2xl uppercase">THE NAGALAND FRONTIER</h3>
                <p className="text-xs text-stone-400">10 Days / Dense Jungle & Dirt Passes</p>
                <div className="flex justify-between items-center pt-4 border-t border-white/10">
                  <span className="font-mono text-sm text-stone-500">SEASON COHORT FULL</span>
                  <span className="font-mono text-xs text-stone-500">WAITLIST ONLY</span>
                </div>
              </div>
            </div>
          </main>
        )}

        {/* VIEW: EXPEDITION DOSSIER */}
        {activeTab === 'dossier' && (
          <main className="max-w-7xl mx-auto px-6 md:px-12 py-12 space-y-12">
            <div className="flex justify-between items-end border-b border-white/10 pb-6">
              <div>
                <span className="font-mono text-xs text-[#8C734B] uppercase">TACTICAL DOSSIER #01</span>
                <h1 className="font-heading text-4xl md:text-6xl uppercase tracking-widest mt-2">TAWANG & BEYOND</h1>
              </div>
              <div className="text-right font-mono">
                <span className="text-xs text-stone-500 block">INVESTMENT</span>
                <span className="text-2xl text-[#8C734B]">₹285,000</span>
              </div>
            </div>

            <div className="grid grid-cols-1 md:grid-cols-2 gap-4 font-mono text-xs">
              <div className="bg-white/5 p-4 border-l-2 border-[#8C734B]">DAY 01–03: GUWAHATI → DIRANG (3,000 FT → 4,900 FT)</div>
              <div className="bg-white/5 p-4 border-l-2 border-[#8C734B]">DAY 04–06: SELA PASS CROSSING → TAWANG MONASTERY (13,700 FT)</div>
              <div className="bg-white/5 p-4 border-l-2 border-[#D03B2B]">DAY 07–09: BUM LA PASS & HIGH LAKES (15,200 FT)</div>
              <div className="bg-white/5 p-4 border-l-2 border-[#8C734B]">DAY 10–12: DESCENT VIA BOMDILA TO BASE COMMAND</div>
            </div>
          </main>
        )}

        {/* VIEW: GALLERY */}
        {activeTab === 'gallery' && (
          <main className="max-w-7xl mx-auto px-6 md:px-12 py-12 space-y-12">
            <span className="font-mono text-xs text-[#8C734B] tracking-widest uppercase">SPATIAL MEDIA ARCHIVE</span>
            <h1 className="font-heading text-4xl md:text-6xl uppercase tracking-widest">FIELD ARCHIVE</h1>
            <div className="grid grid-cols-1 md:grid-cols-3 gap-4">
              <div className="h-64 bg-white/5 border border-white/10 p-4 font-mono text-xs text-stone-500 flex items-end">FRAME 01 / SELA FOG</div>
              <div className="h-64 bg-white/5 border border-white/10 p-4 font-mono text-xs text-stone-500 flex items-end">FRAME 02 / MONASTERY DAWN</div>
              <div className="h-64 bg-white/5 border border-white/10 p-4 font-mono text-xs text-stone-500 flex items-end">FRAME 03 / SLATE DESCENT</div>
            </div>
          </main>
        )}

        {/* VIEW: JOURNAL */}
        {activeTab === 'journal' && (
          <main className="max-w-7xl mx-auto px-6 md:px-12 py-12 space-y-12">
            <span className="font-mono text-xs text-[#8C734B] tracking-widest uppercase">FIELD DISPATCHES</span>
            <h1 className="font-heading text-4xl md:text-6xl uppercase tracking-widest">JOURNAL LOGS</h1>
            <article className="bg-white/5 p-8 border border-white/10 space-y-3">
              <span className="font-mono text-xs text-[#D03B2B]">LOG 084 — BUM LA SECTOR</span>
              <h3 className="font-heading text-xl uppercase">CROSSING THE SLATE AT 15,000 FEET</h3>
              <p className="text-xs text-stone-400 font-light">"When oxygen drops by 40%, every throttle movement becomes deliberate..."</p>
            </article>
          </main>
        )}

        {/* VIEW: BOOKING CLEARANCE */}
        {activeTab === 'booking' && (
          <main className="max-w-7xl mx-auto px-6 md:px-12 py-12 space-y-12">
            <span className="font-mono text-xs text-[#8C734B] tracking-widest uppercase">GATEKEEPER CLEARANCE</span>
            <h1 className="font-heading text-4xl md:text-6xl uppercase tracking-widest">CLAIM YOUR SEAT</h1>
            <p className="text-stone-400 text-sm max-w-xl">Complete the 4-step rider vetting process to submit your application to Base Command.</p>
            <button 
              onClick={() => setIsVettingOpen(true)}
              className="px-8 py-4 bg-[#8C734B] text-black font-mono text-xs tracking-widest uppercase font-semibold"
            >
              LAUNCH VETTING APPLICATION
            </button>
          </main>
        )}

        {/* VIEW: FAQ */}
        {activeTab === 'faq' && (
          <main className="max-w-7xl mx-auto px-6 md:px-12 py-12 space-y-12">
            <span className="font-mono text-xs text-[#8C734B] tracking-widest uppercase">FREQUENT INQUIRIES</span>
            <h1 className="font-heading text-4xl md:text-6xl uppercase tracking-widest">FIELD FAQ</h1>
            <div className="space-y-6 max-w-3xl">
              {faqs.map((f, i) => (
                <div key={i} className="bg-white/5 p-6 border border-white/10 space-y-2">
                  <h4 className="font-heading text-lg text-[#E5E5E5]">{f.q}</h4>
                  <p className="text-xs text-stone-400 font-light leading-relaxed">{f.a}</p>
                </div>
              ))}
            </div>
          </main>
        )}

        {/* VIEW: CONTACT COMMAND */}
        {activeTab === 'contact' && (
          <main className="max-w-7xl mx-auto px-6 md:px-12 py-12 space-y-12">
            <span className="font-mono text-xs text-[#8C734B] tracking-widest uppercase">DIRECT CHANNEL</span>
            <h1 className="font-heading text-4xl md:text-6xl uppercase tracking-widest">BASE COMMAND</h1>
            <div className="font-mono text-xs space-y-4 text-stone-400">
              <p>HEADQUARTERS: GUWAHATI / TAWANG SECTOR</p>
              <p>ENCRYPTION: SECURE SATELLITE MESH</p>
              <p>EMAIL: COMMAND@TERRAVII.COM</p>
            </div>
          </main>
        )}

      </div>

      {/* ------------------------------------------------------------- */}
      {/* VETTING MODAL (CLEARANCE FLOW)                                */}
      {/* ------------------------------------------------------------- */}
      {isVettingOpen && (
        <div className="fixed inset-0 z-50 bg-black/90 backdrop-blur-md flex items-center justify-center p-6">
          <div className="bg-[#030303] border border-white/20 p-8 max-w-xl w-full space-y-6 relative font-mono text-xs">
            <button 
              onClick={() => setIsVettingOpen(false)}
              className="absolute top-6 right-6 text-stone-400 hover:text-white"
            >
              <X size={18} />
            </button>

            <div>
              <span className="text-[10px] text-[#8C734B] tracking-widest block">STEP 0{vettingStep} OF 04</span>
              <h3 className="font-heading text-2xl uppercase tracking-wider text-[#E5E5E5] mt-1">RIDER CLEARANCE VETTING</h3>
            </div>

            {vettingStep === 1 && (
              <div className="space-y-4">
                <label className="block text-stone-400">SELECT EXPEDITION COHORT</label>
                <select 
                  value={formData.route}
                  onChange={(e) => setFormData({...formData, route: e.target.value})}
                  className="w-full bg-white/5 border border-white/10 p-3 text-[#E5E5E5]"
                >
                  <option value="Tawang & Beyond">TAWANG & BEYOND (OCTOBER COHORT)</option>
                  <option value="Cloud Kingdom">THE CLOUD KINGDOM (NOVEMBER COHORT)</option>
                </select>
                <button onClick={() => setVettingStep(2)} className="w-full py-3 bg-[#8C734B] text-black font-semibold uppercase">NEXT: RIDING PROFILE</button>
              </div>
            )}

            {vettingStep === 2 && (
              <div className="space-y-4">
                <label className="block text-stone-400">OFF-ROAD EXPERIENCE LEVEL</label>
                <select 
                  value={formData.experience}
                  onChange={(e) => setFormData({...formData, experience: e.target.value})}
                  className="w-full bg-white/5 border border-white/10 p-3 text-[#E5E5E5]"
                >
                  <option value="Intermediate">INTERMEDIATE (GRAVEL & SLATE CONFIDENT)</option>
                  <option value="Advanced">ADVANCED (TECHNICAL ENDURO/ALPINE)</option>
                </select>
                <button onClick={() => setVettingStep(3)} className="w-full py-3 bg-[#8C734B] text-black font-semibold uppercase">NEXT: MEDICAL READINESS</button>
              </div>
            )}

            {vettingStep === 3 && (
              <div className="space-y-4">
                <label className="block text-stone-400">HIGH-ALTITUDE ENDURANCE ACKNOWLEDGEMENT (13,000+ FT)</label>
                <button 
                  onClick={() => setVettingStep(4)}
                  className="w-full py-3 bg-[#8C734B] text-black font-semibold uppercase"
                >
                  CONFIRM MEDICAL READINESS
                </button>
              </div>
            )}

            {vettingStep === 4 && (
              <div className="space-y-4">
                <input 
                  type="text" 
                  placeholder="FULL RIDER NAME"
                  value={formData.name}
                  onChange={(e) => setFormData({...formData, name: e.target.value})}
                  className="w-full bg-white/5 border border-white/10 p-3 text-[#E5E5E5]"
                />
                <input 
                  type="email" 
                  placeholder="EMAIL ADDRESS"
                  value={formData.email}
                  onChange={(e) => setFormData({...formData, email: e.target.value})}
                  className="w-full bg-white/5 border border-white/10 p-3 text-[#E5E5E5]"
                />
                <button 
                  onClick={() => {
                    alert('Application Submitted to Base Command.');
                    setIsVettingOpen(false);
                    setVettingStep(1);
                  }}
                  className="w-full py-3 bg-[#8C734B] text-black font-semibold uppercase"
                >
                  SUBMIT TO BASE COMMAND
                </button>
              </div>
            )}
          </div>
        </div>
      )}

      {/* ------------------------------------------------------------- */}
      {/* GLOBAL FOOTER                                                 */}
      {/* ------------------------------------------------------------- */}
      <footer className="border-t border-white/10 bg-[#030303] py-12 px-6 md:px-12 mt-32">
        <div className="max-w-7xl mx-auto flex flex-col md:flex-row justify-between items-center text-xs font-mono text-stone-500 gap-4">
          <div>
            <span className="text-[#8C734B] font-bold">TERRA VII</span> — BASE COMMAND GUWAHATI / TAWANG
          </div>
          <div>
            ALL RIGHTS RESERVED © 2026 TERRA VII EXPEDITIONS
          </div>
        </div>
      </footer>

    </div>
  );
}
