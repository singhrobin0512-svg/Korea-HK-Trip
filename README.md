
export default function TravelDashboard() {
  const koreaDays = [
    {
      day: 'Day 1 • Seoul Arrival',
      title: 'Airport → Trang Blue Hotel → Myeongdong',
      commute: 'AREX + Metro • KRW 11,000 approx',
      walk: 'Moderate',
      wow: 'Myeongdong Night Market',
      food: ['Egg Bread', 'Korean Corn Dogs', 'Street BBQ'],
      timeline: [
        'Land at ICN around 4:25 PM',
        'Buy T-Money + eSIM at airport',
        'AREX to Seoul Station',
        'Metro/taxi to Gwanak-gu hotel',
        'Evening at Myeongdong street market'
      ]
    },
    {
      day: 'Day 2 • Palace + Cafes',
      title: 'Gyeongbokgung → Bukchon → Cafe Onion',
      commute: 'Metro Line 3',
      walk: 'Heavy',
      wow: 'Hanok village rooftops',
      food: ['Tosokchon Samgyetang', 'London Bagel Museum'],
      timeline: [
        'Reach Gyeongbokgung before 10 AM',
        'Bukchon Hanok Village photos',
        'Cafe Onion Anguk',
        'Insadong cultural street',
        'Return by evening'
      ]
    },
    {
      day: 'Day 3 • Nami Island',
      title: 'Nami + Rail Bike Experience',
      commute: 'ITX Train + Ferry',
      walk: 'Moderate',
      wow: 'Tree-lined cinematic island',
      food: ['Nami cafes', 'Korean ramen'],
      timeline: [
        'Early departure from Seoul',
        'Nami Island ferry',
        'Gangchon Rail Bike',
        'Sunset return to Seoul'
      ]
    }
  ];

  const hkDays = [
    {
      day: 'Day 9 • Hong Kong Arrival',
      title: 'Electronics Shopping Day',
      commute: 'A21 Bus + MTR',
      walk: 'Moderate',
      wow: 'Victoria Harbour skyline',
      food: ['Yat Lok Roast Goose', 'Bubble tea'],
      timeline: [
        'Land in Hong Kong',
        'Check-in Ramada TST',
        'Visit Sim City electronics market',
        'Ladies Market + Sneaker Street',
        'Star Ferry at night'
      ]
    },
    {
      day: 'Day 10 • Disneyland',
      title: 'Relaxed Disneyland Day',
      commute: 'MTR Disneyland Line',
      walk: 'Heavy',
      wow: 'Night fireworks',
      food: ['Disney snacks', 'Character dining'],
      timeline: [
        'Leave before 9 AM',
        'Fantasyland rides',
        'Parade viewing',
        'Night castle show'
      ]
    }
  ];

  const cards = [
    { title: 'Weather', value: '18°C–31°C', desc: 'Carry umbrella + light jacket' },
    { title: 'Best eSIM', value: 'Airalo / Nomad', desc: 'Install before departure' },
    { title: 'Walking Load', value: '8K–18K steps', desc: 'Comfortable shoes essential' },
    { title: 'Budget Style', value: 'Premium Smart Budget', desc: 'Metro-first planning' }
  ];

  return (
    <div className="min-h-screen bg-slate-950 text-white">
      <div className="bg-gradient-to-r from-blue-700 via-purple-700 to-pink-700 p-10 rounded-b-[40px] shadow-2xl">
        <div className="max-w-7xl mx-auto">
          <h1 className="text-5xl font-bold mb-4">Asia Premium Interactive Travel Planner</h1>
          <p className="text-xl text-slate-100 max-w-3xl">
            Seoul • Busan • Hong Kong • Macau • Electronics Shopping • Cafes • Family Travel
          </p>

          <div className="grid md:grid-cols-4 gap-4 mt-8">
            {cards.map((card, i) => (
              <div key={i} className="bg-white/10 backdrop-blur-lg rounded-3xl p-5 border border-white/10 shadow-xl">
                <h3 className="text-sm uppercase tracking-wide text-slate-300">{card.title}</h3>
                <div className="text-2xl font-bold mt-2">{card.value}</div>
                <p className="text-sm text-slate-300 mt-2">{card.desc}</p>
              </div>
            ))}
          </div>
        </div>
      </div>

      <div className="max-w-7xl mx-auto p-6 space-y-12">

        <section>
          <div className="flex items-center justify-between mb-6">
            <h2 className="text-4xl font-bold">🇰🇷 South Korea Timeline</h2>
            <div className="text-slate-400">22 May → 30 May</div>
          </div>

          <div className="grid gap-6">
            {koreaDays.map((item, idx) => (
              <div key={idx} className="bg-slate-900 border border-slate-800 rounded-[28px] overflow-hidden shadow-2xl hover:scale-[1.01] transition-all">
                <div className="grid lg:grid-cols-3 gap-0">
                  <div className="bg-gradient-to-br from-blue-700 to-purple-700 p-8">
                    <div className="text-sm text-blue-100">{item.day}</div>
                    <h3 className="text-3xl font-bold mt-2">{item.title}</h3>

                    <div className="mt-6 space-y-3 text-sm">
                      <div>🚇 {item.commute}</div>
                      <div>🚶 Walking: {item.walk}</div>
                      <div>📸 Wow Factor: {item.wow}</div>
                    </div>
                  </div>

                  <div className="lg:col-span-2 p-8">
                    <div className="grid md:grid-cols-2 gap-8">
                      <div>
                        <h4 className="text-xl font-semibold mb-4">Timeline</h4>
                        <div className="space-y-4">
                          {item.timeline.map((t, i) => (
                            <div key={i} className="flex gap-3 items-start">
                              <div className="w-3 h-3 rounded-full bg-blue-500 mt-2"></div>
                              <div className="text-slate-300">{t}</div>
                            </div>
                          ))}
                        </div>
                      </div>

                      <div>
                        <h4 className="text-xl font-semibold mb-4">Food & Cafes</h4>
                        <div className="flex flex-wrap gap-3">
                          {item.food.map((f, i) => (
                            <div key={i} className="px-4 py-2 rounded-full bg-slate-800 border border-slate-700 text-sm">
                              {f}
                            </div>
                          ))}
                        </div>

                        <div className="mt-8 p-5 rounded-2xl bg-slate-800 border border-slate-700">
                          <div className="text-sm text-slate-400">Money Saving Tip</div>
                          <div className="mt-2">Use convenience stores like CU & GS25 for breakfast combos and drinks.</div>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            ))}
          </div>
        </section>

        <section>
          <div className="flex items-center justify-between mb-6">
            <h2 className="text-4xl font-bold">🇭🇰 Hong Kong + Macau</h2>
            <div className="text-slate-400">30 May → 3 June</div>
          </div>

          <div className="grid gap-6">
            {hkDays.map((item, idx) => (
              <div key={idx} className="bg-slate-900 border border-slate-800 rounded-[28px] overflow-hidden shadow-2xl hover:scale-[1.01] transition-all">
                <div className="grid lg:grid-cols-3 gap-0">
                  <div className="bg-gradient-to-br from-pink-700 to-orange-600 p-8">
                    <div className="text-sm text-orange-100">{item.day}</div>
                    <h3 className="text-3xl font-bold mt-2">{item.title}</h3>

                    <div className="mt-6 space-y-3 text-sm">
                      <div>🚇 {item.commute}</div>
                      <div>🚶 Walking: {item.walk}</div>
                      <div>📸 Wow Factor: {item.wow}</div>
                    </div>
                  </div>

                  <div className="lg:col-span-2 p-8">
                    <div className="grid md:grid-cols-2 gap-8">
                      <div>
                        <h4 className="text-xl font-semibold mb-4">Timeline</h4>
                        <div className="space-y-4">
                          {item.timeline.map((t, i) => (
                            <div key={i} className="flex gap-3 items-start">
                              <div className="w-3 h-3 rounded-full bg-pink-500 mt-2"></div>
                              <div className="text-slate-300">{t}</div>
                            </div>
                          ))}
                        </div>
                      </div>

                      <div>
                        <h4 className="text-xl font-semibold mb-4">Food & Shopping</h4>
                        <div className="flex flex-wrap gap-3">
                          {item.food.map((f, i) => (
                            <div key={i} className="px-4 py-2 rounded-full bg-slate-800 border border-slate-700 text-sm">
                              {f}
                            </div>
                          ))}
                        </div>

                        <div className="mt-8 p-5 rounded-2xl bg-slate-800 border border-slate-700">
                          <div className="text-sm text-slate-400">Pro Shopping Tip</div>
                          <div className="mt-2">Compare 3–4 electronics stores in Sim City before buying DJI or Insta360 products.</div>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            ))}
          </div>
        </section>

        <section className="grid lg:grid-cols-3 gap-6">
          <div className="bg-slate-900 border border-slate-800 rounded-3xl p-6">
            <h3 className="text-2xl font-bold mb-4">📱 Essential Apps</h3>
            <ul className="space-y-3 text-slate-300">
              <li>Naver Maps</li>
              <li>Kakao Metro</li>
              <li>Papago Translate</li>
              <li>MTR Mobile</li>
              <li>Klook</li>
            </ul>
          </div>

          <div className="bg-slate-900 border border-slate-800 rounded-3xl p-6">
            <h3 className="text-2xl font-bold mb-4">🎒 Carry Essentials</h3>
            <ul className="space-y-3 text-slate-300">
              <li>Universal Adapter</li>
              <li>Compact Umbrella</li>
              <li>Comfortable Sneakers</li>
              <li>Power Bank</li>
              <li>Medicine Pouch</li>
            </ul>
          </div>

          <div className="bg-slate-900 border border-slate-800 rounded-3xl p-6">
            <h3 className="text-2xl font-bold mb-4">💸 Money Saving Hacks</h3>
            <ul className="space-y-3 text-slate-300">
              <li>Use metro over taxis</li>
              <li>Book Disney/Peak via Klook</li>
              <li>Use tax refund counters</li>
              <li>Buy snacks from convenience stores</li>
            </ul>
          </div>
        </section>

      </div>
    </div>
  );
}
