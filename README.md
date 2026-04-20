# SweetSafe.github.io
Discover mouthwatering dessert recipes specially crafted for people with diabetes. Low sugar, low carbs, but never low on flavor.

<style>
@import url('https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@600;700&family=Inter:wght@400;500;600&display=swap');
*{box-sizing:border-box;margin:0;padding:0}
:root{--teal:#0D9488;--teal-l:#14B8A6;--teal-d:#0a7870;--blue:#2563EB;--dark:#0f1923;--dark2:#1e293b;--gray:#64748b;--gray-l:#94a3b8;--border:#e2e8f0;--bg:#f8fafc;--white:#fff}
body{font-family:'Inter',sans-serif;color:var(--dark);background:var(--white);-webkit-font-smoothing:antialiased}
h1,h2,h3,.serif{font-family:'Cormorant Garamond',serif}

/* NAV */
nav{position:sticky;top:0;z-index:100;background:rgba(255,255,255,.96);backdrop-filter:blur(12px);border-bottom:1px solid var(--border);padding:0 2.5rem;height:68px;display:flex;align-items:center;justify-content:space-between}
.logo{display:flex;align-items:center;gap:10px;cursor:pointer;text-decoration:none;color:var(--dark)}
.logo-mark{width:38px;height:38px;background:linear-gradient(135deg,#0D9488,#2563EB);border-radius:12px;display:flex;align-items:center;justify-content:center;color:#fff;font-size:17px;flex-shrink:0}
.logo-name{font-family:'Cormorant Garamond',serif;font-size:22px;font-weight:700;letter-spacing:-.3px}
.nav-links{display:flex;gap:2rem}
.nl{background:none;border:none;font-size:14px;font-weight:500;color:var(--gray);cursor:pointer;font-family:'Inter',sans-serif;position:relative;padding:4px 0;transition:color .2s}
.nl::after{content:'';position:absolute;bottom:-2px;left:0;width:0;height:2px;background:var(--teal);border-radius:2px;transition:width .25s}
.nl:hover,.nl.active{color:var(--dark)}
.nl.active::after,.nl:hover::after{width:100%}
.nav-cta{background:var(--teal);color:#fff;border:none;padding:10px 22px;border-radius:10px;font-size:14px;font-weight:600;cursor:pointer;font-family:'Inter',sans-serif;transition:background .2s,transform .15s;letter-spacing:.1px}
.nav-cta:hover{background:var(--teal-d);transform:translateY(-1px)}

/* PAGES */
.page{display:none}
.page.active{display:block;animation:fadeUp .35s ease}
@keyframes fadeUp{from{opacity:0;transform:translateY(12px)}to{opacity:1;transform:translateY(0)}}

/* HERO */
.hero{padding:5rem 3rem 4.5rem;background:linear-gradient(150deg,#f0fffe 0%,#f0f8ff 45%,#f5f0ff 100%);display:flex;align-items:center;gap:4rem;overflow:hidden;position:relative}
.hero::before{content:'';position:absolute;top:-80px;right:-80px;width:400px;height:400px;background:radial-gradient(circle,rgba(13,148,136,.08),transparent 70%);border-radius:50%;pointer-events:none}
.hero-l{flex:1;max-width:520px;position:relative;z-index:1}
.hero-pill{display:inline-flex;align-items:center;gap:7px;background:rgba(13,148,136,.1);color:var(--teal-d);padding:7px 16px;border-radius:30px;font-size:13px;font-weight:600;margin-bottom:1.5rem;border:1px solid rgba(13,148,136,.2)}
.hero-h1{font-size:58px;line-height:1.05;margin-bottom:1.25rem;font-weight:700;letter-spacing:-1.5px;color:var(--dark)}
.hero-h1 em{color:var(--teal);font-style:normal}
.hero-sub{font-size:16px;color:var(--gray);line-height:1.75;margin-bottom:2.25rem;max-width:420px}
.hero-btns{display:flex;gap:.9rem;flex-wrap:wrap}
.btn-fill{background:var(--teal);color:#fff;border:none;padding:13px 26px;border-radius:10px;font-size:15px;font-weight:600;cursor:pointer;font-family:'Inter',sans-serif;display:flex;align-items:center;gap:8px;transition:background .2s,transform .15s}
.btn-fill:hover{background:var(--teal-d);transform:translateY(-2px)}
.btn-stroke{background:transparent;border:1.5px solid var(--teal);color:var(--teal);padding:12px 22px;border-radius:10px;font-size:15px;font-weight:600;cursor:pointer;font-family:'Inter',sans-serif;display:flex;align-items:center;gap:8px;transition:all .2s}
.btn-stroke:hover{background:var(--teal);color:#fff}
.hero-r{flex:1;max-width:490px;display:grid;grid-template-columns:1fr 1fr;gap:14px}
.hi{border-radius:18px;overflow:hidden;box-shadow:0 8px 32px rgba(0,0,0,.14)}
.hi img{width:100%;height:100%;object-fit:cover;display:block;transition:transform .4s}
.hi:hover img{transform:scale(1.04)}
.hi:nth-child(1){height:215px}.hi:nth-child(2){height:148px;margin-top:44px}.hi:nth-child(3){height:178px}.hi:nth-child(4){height:200px;margin-top:-32px}
.hero-stats{display:flex;gap:2rem;margin-top:2.25rem;padding-top:2rem;border-top:1px solid rgba(0,0,0,.07)}
.hstat-n{font-family:'Cormorant Garamond',serif;font-size:32px;font-weight:700;color:var(--teal);line-height:1}
.hstat-l{font-size:12px;color:var(--gray);margin-top:3px;font-weight:500}

/* FEATURES */
.features{padding:5.5rem 3rem;background:#fff}
.sec-eyebrow{font-size:12px;font-weight:700;letter-spacing:2px;text-transform:uppercase;color:var(--teal);margin-bottom:.9rem}
.sec-title{font-size:38px;font-weight:700;letter-spacing:-1px;margin-bottom:14px;max-width:500px}
.sec-sub{font-size:16px;color:var(--gray);line-height:1.7;max-width:520px;margin-bottom:3rem}
.feat-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:1.25rem}
.feat-card{border-radius:20px;padding:2.25rem 2rem;transition:transform .2s}
.feat-card:hover{transform:translateY(-3px)}
.fc-rose{background:#fff1f2;border:1px solid #fecdd3}
.fc-amber{background:#fffbeb;border:1px solid #fde68a}
.fc-teal{background:#f0fdfa;border:1px solid #99f6e4}
.feat-icon{width:56px;height:56px;border-radius:14px;margin-bottom:1.25rem;display:flex;align-items:center;justify-content:center;font-size:22px}
.fi-rose{background:#fb7185;color:#fff}
.fi-amber{background:#f59e0b;color:#fff}
.fi-teal{background:var(--teal);color:#fff}
.feat-card h3{font-size:16px;font-weight:600;margin-bottom:8px}
.feat-card p{font-size:13.5px;color:var(--gray);line-height:1.65}

/* RECIPE CARDS */
.rcard{background:#fff;border-radius:16px;overflow:hidden;box-shadow:0 1px 4px rgba(0,0,0,.06),0 4px 16px rgba(0,0,0,.06);transition:transform .25s,box-shadow .25s;cursor:pointer;border:1.5px solid transparent;position:relative}
.rcard:hover{transform:translateY(-5px);box-shadow:0 8px 32px rgba(0,0,0,.13)}
.rcard.highlighted{border-color:var(--teal-l)}
.rcard-img{position:relative;overflow:hidden}
.rcard-img img{width:100%;height:210px;object-fit:cover;display:block;transition:transform .4s}
.rcard:hover .rcard-img img{transform:scale(1.06)}
.card-overlay{position:absolute;inset:0;background:linear-gradient(to top,rgba(0,0,0,.45) 0%,transparent 55%)}
.badges{position:absolute;bottom:10px;left:10px;display:flex;gap:5px;z-index:2}
.badge{font-size:11px;font-weight:700;padding:4px 9px;border-radius:20px}
.b-red{background:#ef4444;color:#fff}
.b-amber{background:#f59e0b;color:#fff}
.cat-badge{position:absolute;top:10px;right:10px;background:rgba(255,255,255,.92);color:var(--dark2);font-size:11px;font-weight:600;padding:4px 10px;border-radius:20px;z-index:2;backdrop-filter:blur(4px)}
.rcard-body{padding:1.15rem 1.25rem 1.25rem}
.rcard-title{font-family:'Cormorant Garamond',serif;font-size:20px;font-weight:700;margin-bottom:6px;line-height:1.2;color:var(--dark)}
.rcard-title.accent{color:var(--teal)}
.rcard-desc{font-size:13px;color:var(--gray);line-height:1.55;margin-bottom:1rem;display:-webkit-box;-webkit-line-clamp:2;-webkit-box-orient:vertical;overflow:hidden}
.rcard-meta{display:flex;justify-content:space-between;align-items:center}
.meta-item{font-size:12.5px;color:var(--gray-l);display:flex;align-items:center;gap:4px;font-weight:500}
.divider-dot{width:3px;height:3px;background:var(--gray-l);border-radius:50%;margin:0 6px}

/* SECTION HEADERS */
.sec-header{display:flex;justify-content:space-between;align-items:flex-end;margin-bottom:2rem}
.view-all-btn{background:none;border:none;color:var(--teal);font-size:14px;font-weight:600;cursor:pointer;font-family:'Inter',sans-serif;display:flex;align-items:center;gap:5px;padding:8px 14px;border-radius:8px;transition:background .2s}
.view-all-btn:hover{background:rgba(13,148,136,.07)}

/* HOME SECTIONS */
.home-features{padding:5.5rem 3rem;background:#fff}
.home-featured{padding:3.5rem 3rem 5rem;background:var(--bg)}
.feat-recipes-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:1.5rem}

/* CTA SECTION */
.cta-section{padding:5.5rem 3rem;position:relative;overflow:hidden}
.cta-bg{position:absolute;inset:0;background:linear-gradient(135deg,#1d4ed8,#0D9488)}
.cta-bg::after{content:'';position:absolute;top:-60%;right:-10%;width:600px;height:600px;background:radial-gradient(circle,rgba(255,255,255,.07),transparent 60%);border-radius:50%;pointer-events:none}
.cta-inner{position:relative;z-index:1;text-align:center}
.cta-inner h2{font-family:'Cormorant Garamond',serif;font-size:46px;color:#fff;margin-bottom:14px;letter-spacing:-.5px;font-weight:700}
.cta-inner p{font-size:16px;color:rgba(255,255,255,.82);max-width:490px;margin:0 auto 2.5rem;line-height:1.7}
.btn-cta-white{background:#fff;color:#0a7870;border:none;padding:15px 36px;border-radius:10px;font-size:16px;font-weight:700;cursor:pointer;font-family:'Inter',sans-serif;display:inline-flex;align-items:center;gap:9px;transition:transform .2s,box-shadow .2s;box-shadow:0 4px 20px rgba(0,0,0,.15);letter-spacing:.1px}
.btn-cta-white:hover{transform:translateY(-2px);box-shadow:0 8px 30px rgba(0,0,0,.2)}

/* FOOTER */
footer{background:#0f1923;color:rgba(255,255,255,.65);padding:3.5rem 3rem 2rem}
.footer-grid{display:grid;grid-template-columns:2.2fr 1fr 1fr;gap:3rem;margin-bottom:2.5rem}
.flogo{display:flex;align-items:center;gap:10px;margin-bottom:1rem}
.flogo-mark{width:34px;height:34px;background:linear-gradient(135deg,#0D9488,#2563EB);border-radius:10px;display:flex;align-items:center;justify-content:center;font-size:15px}
.flogo-name{font-family:'Cormorant Garamond',serif;font-size:20px;font-weight:700;color:#fff}
.fdesc{font-size:13.5px;line-height:1.75;max-width:280px}
.footer-col h4{color:#fff;font-size:13px;font-weight:600;margin-bottom:1rem;letter-spacing:.5px;text-transform:uppercase}
.footer-col a{display:block;font-size:13px;color:rgba(255,255,255,.5);margin-bottom:8px;cursor:pointer;text-decoration:none;transition:color .2s}
.footer-col a:hover{color:#fff}
.footer-bottom{border-top:1px solid rgba(255,255,255,.08);padding-top:1.5rem;font-size:12.5px;color:rgba(255,255,255,.3)}

/* RECIPES PAGE */
.rpage{padding:3rem 3rem;min-height:600px}
.page-hdr{margin-bottom:2rem}
.page-hdr h1{font-size:38px;font-weight:700;letter-spacing:-1px;margin-bottom:6px}
.page-hdr p{color:var(--gray);font-size:15px}
.search-wrap{position:relative;margin-bottom:1.75rem;max-width:440px}
.search-wrap input{width:100%;border:1.5px solid var(--border);border-radius:12px;padding:12px 16px 12px 46px;font-size:14px;font-family:'Inter',sans-serif;color:var(--dark);outline:none;background:#fff;transition:border-color .2s,box-shadow .2s}
.search-wrap input:focus{border-color:var(--teal);box-shadow:0 0 0 3px rgba(13,148,136,.1)}
.search-icon{position:absolute;left:15px;top:50%;transform:translateY(-50%);color:var(--gray-l);font-size:16px;pointer-events:none}
.cat-tabs{display:flex;gap:8px;margin-bottom:2rem;flex-wrap:wrap}
.ct{background:#fff;border:1.5px solid var(--border);color:var(--gray);padding:8px 20px;border-radius:25px;font-size:13.5px;font-weight:500;cursor:pointer;font-family:'Inter',sans-serif;transition:all .2s}
.ct.active{background:var(--teal);border-color:var(--teal);color:#fff;box-shadow:0 2px 8px rgba(13,148,136,.3)}
.ct:hover:not(.active){border-color:var(--teal);color:var(--teal)}
.rgrid{display:grid;grid-template-columns:repeat(3,1fr);gap:1.5rem}
.no-results{grid-column:1/-1;text-align:center;padding:4rem;color:var(--gray)}
.no-results-icon{font-size:40px;margin-bottom:1rem}
.no-results h3{font-size:18px;font-weight:600;margin-bottom:6px;color:var(--dark2)}

/* DETAIL PAGE */
.dpage{padding:2.5rem 3rem;min-height:600px}
.back-btn{background:none;border:none;color:var(--teal);font-size:14px;font-weight:600;cursor:pointer;font-family:'Inter',sans-serif;display:flex;align-items:center;gap:6px;margin-bottom:2rem;padding:8px 14px;border-radius:8px;transition:background .2s}
.back-btn:hover{background:rgba(13,148,136,.08)}
.detail-grid{display:grid;grid-template-columns:1.1fr 1fr;gap:2.5rem;margin-bottom:2.5rem;align-items:start}
.detail-img{border-radius:18px;overflow:hidden;height:360px;box-shadow:0 8px 32px rgba(0,0,0,.15)}
.detail-img img{width:100%;height:100%;object-fit:cover}
.detail-info{}
.detail-cats{display:flex;gap:7px;margin-bottom:1rem;flex-wrap:wrap}
.d-tag{background:#f0fdfa;color:var(--teal-d);font-size:12px;font-weight:600;padding:5px 12px;border-radius:20px;border:1px solid rgba(13,148,136,.2)}
.detail-title{font-family:'Cormorant Garamond',serif;font-size:34px;font-weight:700;line-height:1.15;margin-bottom:10px;letter-spacing:-.5px}
.detail-desc{font-size:15px;color:var(--gray);line-height:1.7;margin-bottom:1.5rem}
.stats-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:10px;margin-bottom:1.25rem}
.stat-box{background:var(--bg);border-radius:12px;padding:13px 10px;text-align:center;border:1px solid var(--border)}
.stat-val{font-family:'Cormorant Garamond',serif;font-size:24px;font-weight:700;color:var(--teal)}
.stat-lbl{font-size:11px;color:var(--gray-l);margin-top:2px;font-weight:500;text-transform:uppercase;letter-spacing:.5px}
.content-grid{display:grid;grid-template-columns:1fr 1fr;gap:2.5rem}
.sec-h{font-size:16px;font-weight:700;margin-bottom:12px;color:var(--dark);border-bottom:2px solid var(--border);padding-bottom:8px}
.ingr-list{list-style:none}
.ingr-list li{padding:9px 0;border-bottom:1px solid var(--bg);font-size:14px;display:flex;align-items:center;gap:10px;color:var(--dark2)}
.ingr-dot{width:7px;height:7px;background:var(--teal);border-radius:50%;flex-shrink:0}
.steps-list{list-style:none}
.steps-list li{padding:10px 0;border-bottom:1px solid var(--bg);font-size:14px;line-height:1.65;display:flex;gap:12px;color:var(--dark2)}
.step-n{width:25px;height:25px;background:var(--teal);color:#fff;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:11.5px;font-weight:700;flex-shrink:0;margin-top:1px}
.tip-box{background:#f0fdfa;border-left:3px solid var(--teal);padding:13px 15px;border-radius:0 10px 10px 0;font-size:14px;color:#0f766e;line-height:1.65;margin-top:1rem}

/* CREATE PAGE */
.cpage{padding:3rem 3rem;min-height:600px}
.cpage-inner{max-width:660px}
.form-card{background:#fff;border:1px solid var(--border);border-radius:18px;padding:2.25rem;margin-bottom:1.5rem;box-shadow:0 2px 12px rgba(0,0,0,.05)}
.form-card-title{font-family:'Cormorant Garamond',serif;font-size:26px;font-weight:700;margin-bottom:6px;letter-spacing:-.3px}
.form-card-sub{font-size:14px;color:var(--gray);margin-bottom:1.75rem;line-height:1.65}
.flabel{font-size:13.5px;font-weight:600;margin-bottom:6px;display:block;color:var(--dark2)}
.fhint{font-size:13px;color:var(--gray-l);margin-bottom:10px}
textarea.fi{width:100%;border:1.5px solid var(--border);border-radius:12px;padding:13px 15px;font-size:14px;font-family:'Inter',sans-serif;color:var(--dark);resize:vertical;min-height:90px;outline:none;transition:border-color .2s,box-shadow .2s;background:#fff}
textarea.fi:focus{border-color:var(--teal);box-shadow:0 0 0 3px rgba(13,148,136,.1)}
.diet-opts{display:flex;gap:8px;flex-wrap:wrap;margin-bottom:1.75rem}
.dtag{background:var(--bg);border:1.5px solid var(--border);color:var(--gray);padding:7px 16px;border-radius:20px;font-size:13px;font-weight:500;cursor:pointer;font-family:'Inter',sans-serif;transition:all .2s}
.dtag.on{background:#f0fdfa;border-color:var(--teal);color:var(--teal)}
.gen-btn{width:100%;background:linear-gradient(135deg,var(--blue),var(--teal));color:#fff;border:none;padding:15px;border-radius:12px;font-size:16px;font-weight:700;cursor:pointer;font-family:'Inter',sans-serif;transition:opacity .2s,transform .15s;display:flex;align-items:center;justify-content:center;gap:9px;letter-spacing:.2px;box-shadow:0 4px 16px rgba(13,148,136,.3)}
.gen-btn:hover:not(:disabled){opacity:.92;transform:translateY(-1px)}
.gen-btn:disabled{opacity:.55;cursor:not-allowed;transform:none}
.spinner{width:19px;height:19px;border:2.5px solid rgba(255,255,255,.35);border-top-color:#fff;border-radius:50%;animation:spin .7s linear infinite;display:none}
@keyframes spin{to{transform:rotate(360deg)}}
.gen-out{display:none;background:#fff;border:1px solid var(--border);border-radius:18px;padding:2rem;box-shadow:0 2px 12px rgba(0,0,0,.05)}
.gen-name{font-family:'Cormorant Garamond',serif;font-size:28px;font-weight:700;margin-bottom:6px;letter-spacing:-.3px}
.gen-desc{font-size:14px;color:var(--gray);line-height:1.65;margin-bottom:1.5rem}
.gen-stats{display:grid;grid-template-columns:repeat(4,1fr);gap:10px;margin-bottom:1.75rem}
.gs{background:var(--bg);border-radius:10px;padding:12px;text-align:center;border:1px solid var(--border)}
.gs-v{font-family:'Cormorant Garamond',serif;font-size:22px;font-weight:700;color:var(--teal)}
.gs-l{font-size:11px;color:var(--gray-l);margin-top:2px;text-transform:uppercase;letter-spacing:.5px;font-weight:600}
.gen-grid{display:grid;grid-template-columns:1fr 1fr;gap:1.75rem}
.gen-sec-h{font-size:14px;font-weight:700;margin-bottom:10px;color:var(--dark);border-bottom:2px solid var(--border);padding-bottom:7px}
.gen-ingr-list{list-style:none}
.gen-ingr-list li{padding:8px 0;border-bottom:1px solid var(--bg);font-size:13.5px;color:var(--dark2);display:flex;align-items:flex-start;gap:9px}
.gen-steps-list{list-style:none}
.gen-steps-list li{padding:9px 0;border-bottom:1px solid var(--bg);font-size:13.5px;color:var(--dark2);line-height:1.6;display:flex;gap:10px}
.err-msg{background:#fef2f2;border:1px solid #fecaca;border-radius:10px;padding:13px 16px;font-size:14px;color:#dc2626;margin-top:1rem;display:none}
.loading-card{display:none;text-align:center;padding:2.5rem;background:#fff;border:1px solid var(--border);border-radius:18px}
.loading-dots{display:flex;gap:6px;justify-content:center;margin-bottom:1rem}
.ld{width:9px;height:9px;border-radius:50%;background:var(--teal);animation:bounce .9s infinite}
.ld:nth-child(2){animation-delay:.15s}.ld:nth-child(3){animation-delay:.3s}
@keyframes bounce{0%,100%{transform:translateY(0);opacity:.4}50%{transform:translateY(-7px);opacity:1}}

/* --- Added app features --- */

.step-progress{display:flex;align-items:center;justify-content:space-between;gap:10px;margin-bottom:.6rem;font-size:13px;color:var(--gray)}
.progress-track{height:8px;background:rgba(148,163,184,.2);border-radius:999px;overflow:hidden;flex:1;margin-bottom:.9rem}
.progress-fill{height:100%;border-radius:999px;background:linear-gradient(90deg,var(--teal),var(--blue));width:0%}
.step-toggle{border:none;background:none;color:var(--teal);font-size:12px;font-weight:700;cursor:pointer;padding:0;margin-right:4px}
.steps-list li.done{opacity:.78}
.steps-list li.done .step-n{background:#22c55e}

:root{
  --card:#ffffff;
  --soft:#f8fafc;
  --soft2:#eef2ff;
  --text-soft:#64748b;
}
body.dark-mode{
  --white:#0b1220;
  --bg:#0f172a;
  --dark:#e5eefb;
  --dark2:#cbd5e1;
  --gray:#94a3b8;
  --gray-l:#64748b;
  --border:#23314a;
  background:var(--white);
  color:var(--dark);
}
body.dark-mode nav{background:rgba(11,18,32,.92);border-bottom:1px solid #22324d}
body.dark-mode .rcard,body.dark-mode .form-card,body.dark-mode .gen-out,body.dark-mode .loading-card,body.dark-mode .stat-box,body.dark-mode .gs,body.dark-mode .search-wrap input{background:#0f172a;color:var(--dark);border-color:#22324d}
body.dark-mode .feat-card{filter:saturate(.95)}
body.dark-mode .feat-card,body.dark-mode .detail-img,body.dark-mode .hero,body.dark-mode .cta-section,body.dark-mode .home-featured,body.dark-mode .home-features,body.dark-mode .features,body.dark-mode .rpage,body.dark-mode .cpage{background:linear-gradient(180deg,rgba(255,255,255,.01),rgba(255,255,255,0))}
body.dark-mode .nav-cta,body.dark-mode .btn-fill,body.dark-mode .btn-cta-white,body.dark-mode .gen-btn,body.dark-mode .ct.active{box-shadow:none}
body.dark-mode .search-wrap input::placeholder{color:#7b8ba8}
body.dark-mode .rgrid .rcard,.feat-recipes-grid .rcard{border-color:#22324d}
body.dark-mode .meta-item,body.dark-mode .rcard-desc,body.dark-mode .sec-sub,body.dark-mode .page-hdr p,body.dark-mode .form-card-sub,body.dark-mode .fhint{color:#9aa9bd}
body.dark-mode .footer-col a{color:rgba(255,255,255,.68)}
body.dark-mode .footer-bottom{color:rgba(255,255,255,.38)}

.theme-toggle{background:none;border:1.5px solid var(--border);color:var(--dark);padding:9px 12px;border-radius:10px;font-size:15px;cursor:pointer;transition:transform .15s,background .2s;margin-right:.8rem}
.theme-toggle:hover{transform:translateY(-1px);background:rgba(13,148,136,.08)}
body.dark-mode .theme-toggle{border-color:#2b3d5c;color:#fff}

.filters-toolbar{display:grid;grid-template-columns:repeat(4,minmax(0,1fr));gap:.75rem;margin:0 0 1rem;align-items:end}
.filter-box{display:flex;flex-direction:column;gap:.45rem}
.filter-box label{font-size:12px;font-weight:700;letter-spacing:.2px;color:var(--gray)}
.filter-box select{border:1.5px solid var(--border);border-radius:12px;padding:11px 12px;font-size:14px;background:#fff;color:var(--dark);outline:none}
.filter-box select:focus{border-color:var(--teal);box-shadow:0 0 0 3px rgba(13,148,136,.1)}
body.dark-mode .filter-box select{background:#0f172a;color:var(--dark);border-color:#22324d}

.card-top-actions{position:absolute;top:10px;left:10px;right:10px;display:flex;justify-content:space-between;align-items:center;z-index:3;pointer-events:none}
.fav-btn{pointer-events:auto;background:rgba(255,255,255,.92);border:none;border-radius:999px;padding:7px 10px;font-size:13px;font-weight:700;cursor:pointer;backdrop-filter:blur(5px);box-shadow:0 4px 16px rgba(0,0,0,.08)}
.fav-btn.on{background:#fff1f2;color:#be123c}
body.dark-mode .fav-btn{background:rgba(15,23,42,.88);color:#fff;border:1px solid #22324d}
body.dark-mode .fav-btn.on{background:#3b0f1d;color:#ffb4c2}
.rating-chip{pointer-events:none;background:rgba(255,255,255,.92);border-radius:999px;padding:6px 9px;font-size:12px;font-weight:700;backdrop-filter:blur(5px)}
body.dark-mode .rating-chip{background:rgba(15,23,42,.88);border:1px solid #22324d}
.rating-chip span{color:#f59e0b}
.card-rating-row{display:flex;align-items:center;justify-content:space-between;gap:.5rem;margin-top:.65rem;font-size:12px;color:var(--gray)}
.card-rating-row .avg{font-weight:700;color:var(--dark)}

.detail-actions{display:flex;gap:.6rem;flex-wrap:wrap;margin:1rem 0 1rem}
.detail-actions .action-btn{border:1.5px solid var(--border);background:#fff;border-radius:12px;padding:10px 13px;font-size:13px;font-weight:700;cursor:pointer;color:var(--dark);transition:transform .15s,background .2s}
.detail-actions .action-btn:hover{transform:translateY(-1px);background:rgba(13,148,136,.07)}
body.dark-mode .detail-actions .action-btn{background:#0f172a;border-color:#22324d;color:var(--dark)}
body.dark-mode .detail-actions .action-btn:hover{background:rgba(20,184,166,.08)}

.detail-subgrid{display:grid;grid-template-columns:1fr 1fr;gap:1rem;margin-bottom:1.25rem}
.control-panel,.nutrition-panel,.shopping-panel,.timer-panel,.related-panel,.rating-panel{background:var(--bg);border:1px solid var(--border);border-radius:16px;padding:1rem}
.panel-h{font-size:13px;font-weight:800;letter-spacing:.4px;text-transform:uppercase;margin-bottom:.8rem;color:var(--gray)}
.servings-row{display:flex;align-items:center;justify-content:space-between;gap:.75rem;flex-wrap:wrap}
.servings-row select,.timer-panel input{border:1.5px solid var(--border);border-radius:10px;padding:10px 12px;background:#fff;color:var(--dark);font-family:'Inter',sans-serif}
body.dark-mode .servings-row select,body.dark-mode .timer-panel input{background:#0f172a;color:var(--dark);border-color:#22324d}

.clickable-ingr{cursor:pointer;transition:background .15s,border-color .15s}
.clickable-ingr:hover{background:rgba(13,148,136,.08)}
.clickable-ingr.added{background:rgba(13,148,136,.12)}
.shopping-list{list-style:none;display:grid;gap:.45rem;max-height:220px;overflow:auto;padding-right:.2rem}
.shopping-list li{display:flex;justify-content:space-between;gap:.5rem;align-items:center;background:#fff;border:1px solid var(--border);border-radius:10px;padding:8px 10px;font-size:13px}
body.dark-mode .shopping-list li{background:#0f172a;border-color:#22324d}
.list-actions{display:flex;gap:.5rem;flex-wrap:wrap;margin-top:.7rem}
.small-btn{border:1.5px solid var(--border);background:#fff;border-radius:10px;padding:8px 10px;font-size:12px;font-weight:700;cursor:pointer}
body.dark-mode .small-btn{background:#0f172a;color:var(--dark);border-color:#22324d}

.timer-display{font-family:'Cormorant Garamond',serif;font-size:30px;font-weight:700;color:var(--teal);letter-spacing:-.6px}
.timer-controls{display:flex;gap:.5rem;flex-wrap:wrap;margin-top:.6rem}

.rating-stars{display:flex;gap:.25rem;align-items:center;flex-wrap:wrap}
.rating-stars button{border:none;background:none;font-size:22px;cursor:pointer;padding:0;line-height:1;color:#d1d5db}
.rating-stars button.on{color:#f59e0b}
.rating-note{font-size:13px;color:var(--gray)}

.nutri-bars{display:grid;gap:.6rem}
.nutri-row{display:grid;grid-template-columns:72px 1fr 44px;gap:.6rem;align-items:center;font-size:13px}
.nutri-track{height:10px;border-radius:999px;background:rgba(148,163,184,.22);overflow:hidden}
.nutri-fill{height:100%;border-radius:999px;background:linear-gradient(90deg,var(--teal),var(--blue))}
.nutri-val{text-align:right;font-weight:700}

.related-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:1rem}
.related-grid .rcard-img img{height:150px}
.related-grid .rcard-title{font-size:18px}

@media print{
  nav, .home-features, .home-featured, .cta-section, footer, .back-btn, .detail-actions, .detail-subgrid, .related-panel, .search-wrap, .cat-tabs, .filters-toolbar, .theme-toggle{display:none !important;}
  .page{display:none !important;}
  #page-detail{display:block !important;}
  body{background:#fff !important;color:#000 !important;}
  .dpage{padding:0 !important;}
  .detail-grid{grid-template-columns:1fr !important;}
  .detail-img{height:260px !important;box-shadow:none !important;}
  .content-grid{grid-template-columns:1fr !important;}
  .nutrition-panel,.shopping-panel,.timer-panel,.rating-panel{break-inside:avoid;}
}


/* ===== Premium app shell upgrade ===== */
html { scroll-behavior: smooth; }
body {
  background:
    radial-gradient(circle at 12% 10%, rgba(20,184,166,.18), transparent 22%),
    radial-gradient(circle at 88% 8%, rgba(37,99,235,.16), transparent 24%),
    radial-gradient(circle at 50% 100%, rgba(168,85,247,.10), transparent 28%),
    linear-gradient(180deg, #f7fbff 0%, #eef4fb 46%, #f8fafc 100%);
  min-height: 100vh;
  overflow-x: hidden;
}
body::before, body::after {
  content: '';
  position: fixed;
  inset: auto;
  pointer-events: none;
  z-index: -1;
  filter: blur(30px);
  opacity: .55;
}
body::before {
  width: 420px; height: 420px; border-radius: 50%;
  left: -140px; top: 10vh;
  background: radial-gradient(circle, rgba(13,148,136,.22), transparent 70%);
}
body::after {
  width: 520px; height: 520px; border-radius: 50%;
  right: -180px; bottom: 8vh;
  background: radial-gradient(circle, rgba(37,99,235,.18), transparent 72%);
}
nav, footer, .hero, .home-features, .home-featured, .cta-section, .rpage, .cpage, .dpage {
  max-width: calc(100% - 28px);
  margin-left: auto;
  margin-right: auto;
}
nav {
  margin-top: 14px;
  border-radius: 24px;
  border: 1px solid rgba(148,163,184,.18);
  box-shadow: 0 24px 70px rgba(15,23,42,.08);
}
.logo-mark, .flogo-mark {
  box-shadow: 0 10px 28px rgba(13,148,136,.22);
}
.hero, .home-features, .home-featured, .cta-section, .rpage, .cpage, .dpage {
  border-radius: 30px;
  border: 1px solid rgba(148,163,184,.16);
  box-shadow: 0 24px 70px rgba(15,23,42,.06);
  background: rgba(255,255,255,.62);
  backdrop-filter: blur(18px);
}
.hero {
  min-height: 74vh;
  margin-top: 16px;
  padding: 4.6rem 3rem;
  position: relative;
  overflow: hidden;
  box-shadow: 0 30px 100px rgba(15,23,42,.10);
}
.hero::after {
  content: '';
  position: absolute;
  inset: 20px;
  border-radius: 26px;
  border: 1px solid rgba(255,255,255,.34);
  pointer-events: none;
}
.hero-h1 {
  font-size: clamp(3.8rem, 6vw, 6.4rem);
  letter-spacing: -2.4px;
}
.hero-sub {
  font-size: 17px;
  line-height: 1.8;
}
.hero-pill {
  box-shadow: 0 8px 30px rgba(13,148,136,.10);
  backdrop-filter: blur(16px);
}
.hero-btns .btn-fill,
.hero-btns .btn-stroke,
.btn-cta-white,
.nav-cta,
.gen-btn {
  border-radius: 16px;
}
.hero-r {
  filter: saturate(1.06);
}
.hi {
  box-shadow: 0 24px 50px rgba(15,23,42,.16);
  border: 1px solid rgba(255,255,255,.28);
}
.home-features, .home-featured, .rpage, .cpage, .dpage, .cta-section {
  padding: 3rem 2.5rem;
  margin-top: 18px;
}
.feat-grid, .feat-recipes-grid, .rgrid {
  gap: 1.25rem;
}
.feat-card, .rcard, .form-card, .gen-out, .loading-card, .detail-img, .stat-box, .gs, .control-panel, .nutrition-panel, .shopping-panel, .timer-panel, .related-panel, .rating-panel {
  border: 1px solid rgba(148,163,184,.16) !important;
  box-shadow: 0 18px 40px rgba(15,23,42,.06);
}
.feat-card, .rcard, .form-card, .gen-out, .loading-card, .detail-img, .stat-box, .gs {
  background: rgba(255,255,255,.8);
  backdrop-filter: blur(18px);
}
.feat-card {
  border-radius: 24px;
}
.rcard {
  border-radius: 24px;
  overflow: hidden;
  transition: transform .28s cubic-bezier(.2,.8,.2,1), box-shadow .28s ease, border-color .28s ease;
}
.rcard:hover {
  transform: translateY(-10px) scale(1.01);
  box-shadow: 0 28px 70px rgba(15,23,42,.14);
  border-color: rgba(20,184,166,.36) !important;
}
.rcard-img img { height: 232px; }
.card-top-actions { top: 12px; left: 12px; right: 12px; }
.badge, .cat-badge, .d-tag, .fav-btn, .rating-chip { backdrop-filter: blur(12px); }
.detail-grid { gap: 1.8rem; }
.detail-img {
  height: 420px;
  border-radius: 28px;
  overflow: hidden;
}
.detail-title { font-size: clamp(2.2rem, 4vw, 3.8rem); }
.detail-actions .action-btn,
.small-btn,
.theme-toggle,
.filter-box select,
.servings-row select,
.timer-panel input,
.search-wrap input {
  border-radius: 14px;
}
.detail-subgrid { gap: 1rem; }
.content-grid { gap: 1.4rem; }
.stats-grid { gap: 12px; }
.stat-box { border-radius: 18px; padding: 16px 10px; }
.step-n { box-shadow: 0 8px 18px rgba(13,148,136,.25); }
.filters-toolbar {
  position: sticky;
  top: 84px;
  z-index: 60;
  margin-bottom: 1.2rem;
  padding: 14px;
  background: rgba(255,255,255,.72);
  backdrop-filter: blur(18px);
  border-radius: 20px;
  border: 1px solid rgba(148,163,184,.16);
  box-shadow: 0 16px 40px rgba(15,23,42,.06);
}
.search-wrap input, .filter-box select, .servings-row select, .timer-panel input {
  background: rgba(255,255,255,.92);
}
.footer-grid { gap: 2.2rem; }
footer {
  margin-top: 18px;
  border-radius: 30px 30px 0 0;
}
body.dark-mode {
  background:
    radial-gradient(circle at 12% 10%, rgba(20,184,166,.16), transparent 24%),
    radial-gradient(circle at 88% 8%, rgba(37,99,235,.16), transparent 24%),
    linear-gradient(180deg, #07111f 0%, #0b1322 50%, #0f172a 100%);
}
body.dark-mode nav,
body.dark-mode .hero,
body.dark-mode .home-features,
body.dark-mode .home-featured,
body.dark-mode .cta-section,
body.dark-mode .rpage,
body.dark-mode .cpage,
body.dark-mode .dpage,
body.dark-mode footer {
  background: rgba(15,23,42,.78);
  border-color: rgba(51,65,85,.55);
}
body.dark-mode .rcard,
body.dark-mode .form-card,
body.dark-mode .gen-out,
body.dark-mode .loading-card,
body.dark-mode .detail-img,
body.dark-mode .stat-box,
body.dark-mode .gs,
body.dark-mode .filters-toolbar {
  background: rgba(15,23,42,.76) !important;
  border-color: rgba(51,65,85,.55) !important;
}
body.dark-mode .search-wrap input,
body.dark-mode .filter-box select,
body.dark-mode .servings-row select,
body.dark-mode .timer-panel input {
  background: rgba(15,23,42,.88);
  border-color: rgba(51,65,85,.6);
}
body.dark-mode .nav-cta,
body.dark-mode .btn-fill,
body.dark-mode .btn-cta-white,
body.dark-mode .gen-btn,
body.dark-mode .ct.active { box-shadow: none; }
body.dark-mode .rcard:hover { border-color: rgba(20,184,166,.34) !important; }
.toast {
  position: fixed;
  left: 50%;
  bottom: 24px;
  transform: translateX(-50%) translateY(18px);
  opacity: 0;
  padding: 12px 16px;
  border-radius: 999px;
  color: #fff;
  background: rgba(15,23,42,.92);
  border: 1px solid rgba(255,255,255,.12);
  z-index: 350;
  pointer-events: none;
  box-shadow: 0 18px 45px rgba(0,0,0,.22);
  transition: opacity .24s ease, transform .24s ease;
}
.toast.show { opacity: 1; transform: translateX(-50%) translateY(0); }
.mobile-dock {
  display: none;
}
@media (max-width: 980px) {
  nav { margin-top: 10px; padding: 0 .9rem; height: 62px; }
  .nav-links, .nav-cta { display: none; }
  .hero { min-height: auto; padding: 3rem 1.25rem; margin-top: 10px; }
  .hero-r { display: none; }
  .hero-h1 { font-size: clamp(3rem, 12vw, 4.6rem); }
  .home-features, .home-featured, .rpage, .cpage, .dpage, .cta-section { padding: 2rem 1.15rem; margin-top: 10px; border-radius: 22px; }
  .feat-grid, .feat-recipes-grid, .rgrid, .content-grid, .gen-grid, .detail-grid, .stats-grid, .gen-stats, .detail-subgrid { grid-template-columns: 1fr !important; }
  .filters-toolbar { position: static; }
  .sec-header { align-items: flex-start; gap: .5rem; }
  .detail-img { height: 280px; }
  .mobile-dock {
    display: flex;
    position: fixed;
    left: 10px;
    right: 10px;
    bottom: 10px;
    padding: 10px;
    gap: 8px;
    z-index: 320;
    border-radius: 22px;
    background: rgba(15,23,42,.82);
    backdrop-filter: blur(18px);
    border: 1px solid rgba(255,255,255,.12);
    box-shadow: 0 20px 50px rgba(0,0,0,.25);
  }
  .mobile-dock button {
    flex: 1;
    border: none;
    border-radius: 16px;
    padding: 10px 6px;
    font-size: 12px;
    font-weight: 700;
    color: #fff;
    background: rgba(255,255,255,.07);
  }
  .toast { bottom: 88px; }
}

</style>

<nav>
  <div class="logo" onclick="goPage('home')">
    <div class="logo-mark">🌿</div>
    <span class="logo-name">SweetSafe</span>
  </div>
  <div class="nav-links">
    <button class="nl active" data-page="home" onclick="goPage('home')">Home</button>
    <button class="nl" data-page="recipes" onclick="goPage('recipes')">Recipes</button>
    <button class="nl" data-page="create" onclick="goPage('create')">Create Recipe</button>
    <button class="nl" onclick="goPage('home')">About</button>
  </div>
  <button class="nav-cta" onclick="goPage('create')">Create Custom Recipe</button>
</nav>

<div class="mobile-dock" aria-label="Quick navigation">
  <button onclick="goPage('home')">Home</button>
  <button onclick="goPage('recipes')">Recipes</button>
  <button onclick="goPage('create')">Create</button>
  <button onclick="setTheme(theme==='dark'?'light':'dark')">Theme</button>
</div>
<div class="toast" id="toast" role="status" aria-live="polite"></div>

<!-- HOME -->
<div class="page active" id="page-home">
  <div class="hero">
    <div class="hero-l">
      <div class="hero-pill">❤️ Diabetes-Friendly Recipes</div>
      <h1 class="hero-h1">Delicious<br>Desserts,<br><em>Sugar-Free</em></h1>
      <p class="hero-sub">Discover mouthwatering dessert recipes specially crafted for people with diabetes. Low sugar, low carbs, but never low on flavor.</p>
      <div class="hero-btns">
        <button class="btn-fill" onclick="goPage('recipes')">Browse Recipes →</button>
        <button class="btn-stroke" onclick="goPage('create')">✦ Create Custom Recipe</button>
      </div>
      <div class="hero-stats">
        <div><div class="hstat-n">18+</div><div class="hstat-l">Recipes</div></div>
        <div><div class="hstat-n">&lt;8g</div><div class="hstat-l">Sugar per serving</div></div>
        <div><div class="hstat-n">AI</div><div class="hstat-l">Recipe builder</div></div>
      </div>
    </div>
    <div class="hero-r">
      <div class="hi"><img src="https://images.unsplash.com/photo-1533134242443-d4fd215305ad?auto=format&fit=crop&w=1200&q=80" alt="cheesecake" onerror="this.onerror=null;this.src=makeFallbackImage('Blueberry Cheesecake','No-Bake')"></div>
      <div class="hi"><img src="https://images.unsplash.com/photo-1606313564200-e75d5e30476c?auto=format&fit=crop&w=1200&q=80" alt="brownie" onerror="this.onerror=null;this.src=makeFallbackImage('Lemon Brownies','Baked')"></div>
      <div class="hi"><img src="https://images.unsplash.com/photo-1565958011703-44f9829ba187?auto=format&fit=crop&w=1200&q=80" alt="cake" onerror="this.onerror=null;this.src=makeFallbackImage('Strawberry Dessert','No-Bake')"></div>
      <div class="hi"><img src="https://images.unsplash.com/photo-1488477181946-6428a0291777?auto=format&fit=crop&w=1200&q=80" alt="parfait" onerror="this.onerror=null;this.src=makeFallbackImage('Berry Parfait','Quick & Easy')"></div>
    </div>
  </div>

  <div class="home-features">
    <div style="max-width:760px">
      <div class="sec-eyebrow">Why SweetSafe</div>
      <h2 class="sec-title">Built for people who love dessert<br>and manage their blood sugar</h2>
      <p class="sec-sub">We understand the challenges of managing diabetes while still wanting to enjoy life's sweet moments.</p>
    </div>
    <div class="feat-grid">
      <div class="feat-card fc-rose">
        <div class="feat-icon fi-rose">♥</div>
        <h3>Diabetes-Friendly</h3>
        <p>Every recipe is designed with blood sugar management in mind. Low glycemic, low sugar, maximum taste.</p>
      </div>
      <div class="feat-card fc-amber">
        <div class="feat-icon fi-amber">⏱</div>
        <h3>Quick &amp; Easy</h3>
        <p>Most recipes take under 30 minutes. Simple ingredients, clear instructions, delicious results every time.</p>
      </div>
      <div class="feat-card fc-teal">
        <div class="feat-icon fi-teal">✦</div>
        <h3>AI Recipe Creator</h3>
        <p>Tell us what ingredients you have, and our AI will create a custom diabetic-friendly recipe just for you.</p>
      </div>
    </div>
  </div>

  <div class="home-featured">
    <div class="sec-header">
      <div>
        <div class="sec-eyebrow">Most Popular</div>
        <h2 style="font-family:'Cormorant Garamond',serif;font-size:30px;font-weight:700;letter-spacing:-.5px">Featured Recipes</h2>
      </div>
      <button class="view-all-btn" onclick="goPage('recipes')">View All Recipes →</button>
    </div>
    <div class="feat-recipes-grid" id="featured-grid"></div>
  </div>

  <div class="cta-section">
    <div class="cta-bg"></div>
    <div class="cta-inner">
      <h2>Create Your Own Recipe</h2>
      <p>Have ingredients at home? Our AI-powered recipe creator will design a delicious, diabetes-friendly dessert based on what you already have in your kitchen.</p>
      <button class="btn-cta-white" onclick="goPage('create')">✦ Start Creating</button>
    </div>
  </div>

  <footer>
    <div class="footer-grid">
      <div>
        <div class="flogo"><div class="flogo-mark">🌿</div><span class="flogo-name">SweetSafe</span></div>
        <p class="fdesc">Discover mouthwatering dessert recipes specially crafted for people with diabetes. Low sugar, low carbs, but never low on flavor.</p>
      </div>
      <div class="footer-col">
        <h4>Recipes</h4>
        <a onclick="goPage('recipes')">Browse Recipes</a>
        <a onclick="goPage('create')">Create Recipe</a>
        <a onclick="goPage('home')">About</a>
      </div>
      <div class="footer-col">
        <h4>Categories</h4>
        <a onclick="goRecipes('No-Bake')">No-Bake</a>
        <a onclick="goRecipes('Quick & Easy')">Quick &amp; Easy</a>
        <a onclick="goRecipes('Chocolate')">Chocolate</a>
        <a onclick="goRecipes('Baked')">Baked</a>
      </div>
    </div>
    <div class="footer-bottom">© 2025 SweetSafe · Diabetes-Friendly Desserts · All rights reserved</div>
  </footer>
</div>

<!-- RECIPES PAGE -->
<div class="page" id="page-recipes">
  <div class="rpage">
    <div class="page-hdr">
      <h1>All Recipes</h1>
      <p>Browse our full collection of diabetes-friendly desserts</p>
    </div>
    <div class="search-wrap">
      <span class="search-icon">🔍</span>
      <input type="text" placeholder="Search by name, ingredient, or category..." id="search-input" oninput="filterRecipes()">
    </div>
    <div class="cat-tabs">
      <button class="ct active" data-cat="All" onclick="setCat('All')">All Recipes</button>
      <button class="ct" data-cat="No-Bake" onclick="setCat('No-Bake')">No-Bake</button>
      <button class="ct" data-cat="Quick & Easy" onclick="setCat('Quick & Easy')">Quick &amp; Easy</button>
      <button class="ct" data-cat="Chocolate" onclick="setCat('Chocolate')">Chocolate</button>
      <button class="ct" data-cat="Baked" onclick="setCat('Baked')">Baked</button>
    </div>
    <div class="rgrid" id="recipes-grid"></div>
  </div>
  <footer>
    <div class="footer-grid">
      <div><div class="flogo"><div class="flogo-mark">🌿</div><span class="flogo-name">SweetSafe</span></div><p class="fdesc">Diabetes-friendly desserts crafted with love.</p></div>
      <div class="footer-col"><h4>Navigate</h4><a onclick="goPage('home')">Home</a><a onclick="goPage('recipes')">Recipes</a><a onclick="goPage('create')">Create</a></div>
      <div class="footer-col"><h4>Categories</h4><a onclick="goRecipes('No-Bake')">No-Bake</a><a onclick="goRecipes('Chocolate')">Chocolate</a><a onclick="goRecipes('Baked')">Baked</a></div>
    </div>
    <div class="footer-bottom">© 2025 SweetSafe</div>
  </footer>
</div>

<!-- DETAIL PAGE -->
<div class="page" id="page-detail">
  <div class="dpage" id="detail-content"></div>
</div>

<!-- CREATE PAGE -->
<div class="page" id="page-create">
  <div class="cpage">
    <div class="cpage-inner">
      <div class="page-hdr" style="margin-bottom:1.75rem">
        <h1>AI Recipe Creator</h1>
        <p>Tell us what you have — we'll build the perfect dessert</p>
      </div>
      <div class="form-card">
        <div class="form-card-title">Your Ingredients</div>
        <p class="form-card-sub">List what you have at home and our AI will design a custom diabetes-friendly dessert recipe just for you.</p>
        <label class="flabel">What ingredients do you have?</label>
        <p class="fhint">Separate with commas — e.g. cream cheese, blueberries, almond flour, stevia</p>
        <textarea class="fi" id="ingredients-input" placeholder="e.g. Greek yogurt, raspberries, chia seeds, vanilla extract, stevia, almond flour..."></textarea>
        <div style="margin:1.25rem 0 .6rem"><label class="flabel">Dietary preferences</label></div>
        <div class="diet-opts">
          <button class="dtag" onclick="toggleTag(this)">Keto</button>
          <button class="dtag" onclick="toggleTag(this)">No-Bake</button>
          <button class="dtag" onclick="toggleTag(this)">Gluten-Free</button>
          <button class="dtag" onclick="toggleTag(this)">Dairy-Free</button>
          <button class="dtag" onclick="toggleTag(this)">High Protein</button>
          <button class="dtag" onclick="toggleTag(this)">Under 15 mins</button>
        </div>
        <button class="gen-btn" id="gen-btn" onclick="generateRecipe()">
          <span id="gen-btn-txt">✦ Generate My Recipe</span>
          <div class="spinner" id="gen-spinner"></div>
        </button>
        <div class="err-msg" id="err-msg"></div>
      </div>
      <div class="loading-card" id="loading-card">
        <div class="loading-dots"><div class="ld"></div><div class="ld"></div><div class="ld"></div></div>
        <p style="color:var(--gray);font-size:14px">Crafting your diabetes-friendly recipe…</p>
      </div>
      <div class="gen-out" id="gen-out"></div>
    </div>
  </div>
  <footer>
    <div class="footer-grid">
      <div><div class="flogo"><div class="flogo-mark">🌿</div><span class="flogo-name">SweetSafe</span></div><p class="fdesc">Diabetes-friendly desserts crafted with love.</p></div>
      <div class="footer-col"><h4>Navigate</h4><a onclick="goPage('home')">Home</a><a onclick="goPage('recipes')">Recipes</a></div>
      <div class="footer-col"><h4>Categories</h4><a onclick="goRecipes('No-Bake')">No-Bake</a><a onclick="goRecipes('Chocolate')">Chocolate</a></div>
    </div>
    <div class="footer-bottom">© 2025 SweetSafe</div>
  </footer>
</div>

<script>
const RECIPES=[
  {id:1,name:"Blueberry & Lemon Cheesecake",desc:"A fruity cheesecake with a lemon zing to it. Low sugar, high protein, and absolutely delicious.",sugar:"5g",carbs:"22.7g",time:15,cal:190,cat:"No-Bake",difficulty:"Easy",featured:true,rating:4.7,votes:128,img:"https://images.unsplash.com/photo-1533134242443-d4fd215305ad?auto=format&fit=crop&w=1400&q=80",nutrition:{sugar:5,carbs:22.7,protein:7,fat:13},ingredients:["200g low-fat cream cheese","1 tbsp lemon zest","2 tbsp stevia","½ cup fresh blueberries","1 tsp vanilla extract","6 almond flour crackers","1 tbsp coconut oil"],steps:["Crush almond crackers with melted coconut oil. Press into 4 ramekins and chill.","Beat cream cheese with stevia, lemon zest, and vanilla until smooth.","Spoon over bases, smooth tops. Add blueberries on top.","Chill for at least 1 hour before serving."],tip:"Use full-fat cream cheese for a richer texture without significantly increasing carbs."},
  {id:2,name:"Low Carb Lemon Brownies",desc:"Bright and tangy lemon brownies with only 3g net carbs. Perfect for satisfying your sweet tooth.",sugar:"0.5g",carbs:"3g",time:45,cal:145,cat:"Baked",difficulty:"Medium",featured:true,rating:4.6,votes:92,img:"https://images.unsplash.com/photo-1606313564200-e75d5e30476c?auto=format&fit=crop&w=1400&q=80",nutrition:{sugar:0.5,carbs:3,protein:6,fat:10},ingredients:["1 cup almond flour","2 eggs","¼ cup erythritol","3 tbsp lemon juice","1 tsp lemon zest","¼ cup melted butter","½ tsp baking powder","Pinch of salt"],steps:["Preheat oven to 175°C. Line a small baking pan with parchment.","Whisk eggs, erythritol, lemon juice and zest.","Stir in melted butter, then fold in almond flour, baking powder and salt.","Bake 22–25 minutes until golden. Cool before slicing."],tip:"Add a glaze of powdered erythritol and lemon juice for a bakery-style finish."},
  {id:3,name:"Strawberry Cheesecake Fluff",desc:"Creamy, fluffy, and packed with protein. Ready in just 5 minutes for a quick sweet treat.",sugar:"4g",carbs:"6g",time:5,cal:120,cat:"No-Bake",difficulty:"Easy",featured:true,rating:4.8,votes:166,img:"https://images.unsplash.com/photo-1565958011703-44f9829ba187?auto=format&fit=crop&w=1400&q=80",nutrition:{sugar:4,carbs:6,protein:8,fat:5},ingredients:["½ cup low-fat cream cheese","½ cup plain Greek yogurt","2 tbsp stevia","½ cup sliced strawberries","½ tsp vanilla extract","1 tbsp lemon juice"],steps:["Beat cream cheese until smooth. Blend in Greek yogurt and stevia.","Add vanilla and lemon juice. Mix until light and fluffy.","Fold in sliced strawberries gently.","Serve immediately or chill for up to 2 hours."],tip:"This doubles as a great dip for apple slices or almond crackers."},
  {id:4,name:"Chocolate Avocado Mousse",desc:"Rich, velvety chocolate mousse made with avocado. Zero refined sugar and ready in 10 minutes.",sugar:"3g",carbs:"8g",time:10,cal:180,cat:"No-Bake",difficulty:"Easy",featured:false,rating:4.5,votes:104,img:"https://images.unsplash.com/photo-1541783245831-57d6fb0926d3?auto=format&fit=crop&w=1400&q=80",nutrition:{sugar:3,carbs:8,protein:4,fat:15},ingredients:["2 ripe avocados","3 tbsp unsweetened cocoa","3 tbsp almond milk","3 tbsp monk fruit sweetener","1 tsp vanilla","Pinch of sea salt","Dark chocolate shavings"],steps:["Blend avocados until perfectly smooth.","Add cocoa, sweetener, vanilla and salt. Blend again.","Stream in almond milk until mousse-like.","Chill 20 min then top with chocolate shavings."],tip:"Riper avocados make for a creamier, richer mousse."},
  {id:5,name:"Chia Coconut Pudding",desc:"Creamy overnight pudding loaded with fiber and omega-3s. Prep in 5 minutes the night before.",sugar:"3g",carbs:"12g",time:5,cal:150,cat:"No-Bake",difficulty:"Easy",featured:false,rating:4.4,votes:71,img:recipeArt("Chia Coconut Pudding"),nutrition:{sugar:3,carbs:12,protein:5,fat:9},ingredients:["3 tbsp chia seeds","1 cup unsweetened coconut milk","2 tbsp stevia","½ tsp vanilla extract","Fresh mango or berries","1 tbsp toasted coconut flakes"],steps:["Whisk chia seeds, coconut milk, stevia and vanilla in a jar.","Stir again after 5 minutes to prevent clumping.","Cover and refrigerate overnight or at least 4 hours.","Top with fresh fruit and coconut flakes before serving."],tip:"For extra creaminess, blend half the pudding and stir back in."},
  {id:6,name:"Keto Peanut Butter Cups",desc:"Homemade sugar-free peanut butter cups that taste better than the real thing. Just 4 ingredients.",sugar:"1g",carbs:"4g",time:20,cal:165,cat:"No-Bake",difficulty:"Easy",featured:false,rating:4.9,votes:143,img:recipeArt("Keto Peanut Butter Cups"),nutrition:{sugar:1,carbs:4,protein:3,fat:12},ingredients:["100g 85% dark chocolate","¼ cup natural peanut butter","2 tbsp powdered erythritol","¼ tsp sea salt","Coconut oil for greasing"],steps:["Melt chocolate with 1 tsp coconut oil. Pour half into 8 mini muffin cups.","Freeze 5 minutes until firm.","Mix peanut butter with erythritol and salt.","Add PB to cups, top with remaining chocolate. Freeze 15 min."],tip:"Use almond or sunflower seed butter for a nut-free version."},
  {id:7,name:"Cinnamon Baked Pears",desc:"Warm baked pears with cinnamon and walnut crumble. Naturally sweet with no added sugar.",sugar:"8g",carbs:"15g",time:25,cal:95,cat:"Baked",difficulty:"Easy",featured:false,rating:4.3,votes:66,img:recipeArt("Cinnamon Baked Pears"),nutrition:{sugar:8,carbs:15,protein:2,fat:3},ingredients:["2 ripe firm pears, halved","½ tsp cinnamon","Pinch of nutmeg","1 tbsp chopped walnuts","1 tsp raw honey","½ tsp vanilla extract","2 tbsp water"],steps:["Preheat oven to 180°C. Place pears cut-side up in a baking dish.","Brush with cinnamon, nutmeg and vanilla mixture.","Add water to dish. Bake 20–22 minutes until tender.","Top with walnuts and a drizzle of honey. Serve warm."],tip:"Serve with a dollop of plain Greek yogurt for added protein."},
  {id:8,name:"Berry Yogurt Parfait",desc:"Layers of creamy yogurt, fresh berries, and crunchy low-carb granola. Indulgent yet guilt-free.",sugar:"6g",carbs:"14g",time:5,cal:140,cat:"Quick & Easy",difficulty:"Easy",featured:false,rating:4.6,votes:81,img:recipeArt("Berry Yogurt Parfait"),nutrition:{sugar:6,carbs:14,protein:9,fat:4},ingredients:["1 cup plain Greek yogurt (2%)","½ cup mixed berries","2 tbsp low-carb granola","1 tbsp stevia","½ tsp vanilla","1 tsp lemon zest"],steps:["Stir stevia, vanilla and lemon zest into yogurt.","Layer half the yogurt in a glass.","Add half the berries and all the granola.","Top with remaining yogurt and berries."],tip:"Skip the granola if prepping ahead — add fresh right before eating."},
  {id:9,name:"Dark Chocolate Bark",desc:"Shatteringly crisp dark chocolate bark with nuts and seeds. Under 2g sugar per piece.",sugar:"1.5g",carbs:"5g",time:20,cal:172,cat:"Chocolate",difficulty:"Easy",featured:false,rating:4.8,votes:107,img:recipeArt("Dark Chocolate Bark"),nutrition:{sugar:1.5,carbs:5,protein:3,fat:14},ingredients:["200g 90% dark chocolate","2 tbsp toasted almonds","2 tbsp pistachios","1 tbsp pumpkin seeds","1 tbsp dried raspberries","¼ tsp sea salt flakes"],steps:["Melt chocolate in a double boiler until smooth.","Spread onto parchment-lined tray in a thin layer.","Scatter nuts, seeds and raspberries over the top.","Sprinkle sea salt, refrigerate 30 min until firm, break into shards."],tip:"Store in an airtight container in the fridge for up to 3 weeks."},
  {id:10,name:"Almond Flour Shortbread",desc:"Buttery, melt-in-your-mouth shortbread cookies with just 5g net carbs. A guaranteed crowd-pleaser.",sugar:"2g",carbs:"5g",time:22,cal:98,cat:"Baked",difficulty:"Medium",featured:false,rating:4.4,votes:59,img:recipeArt("Dark Chocolate Bark"),nutrition:{sugar:2,carbs:5,protein:3,fat:8},ingredients:["2 cups almond flour","¼ cup erythritol (powdered)","¼ cup cold butter","1 egg yolk","1 tsp vanilla","Pinch of salt"],steps:["Preheat oven to 160°C. Line tray with parchment.","Mix almond flour, erythritol and salt. Cut in cold butter.","Add egg yolk and vanilla; mix until dough forms.","Roll 1cm thick, cut shapes. Bake 12–14 min until lightly golden."],tip:"These firm up as they cool — don't overbake or they'll turn dry."},
  {id:11,name:"Coconut Flour Mug Cake",desc:"A warm chocolate cake in 90 seconds. Single-serving, sugar-free, and perfect for late-night cravings.",sugar:"2g",carbs:"8g",time:5,cal:135,cat:"Quick & Easy",difficulty:"Easy",featured:false,rating:4.5,votes:88,img:recipeArt("Coconut Flour Mug Cake"),nutrition:{sugar:2,carbs:8,protein:5,fat:7},ingredients:["2 tbsp coconut flour","1 tbsp cocoa powder","2 tbsp erythritol","1 egg","2 tbsp almond milk","1 tbsp melted butter","¼ tsp baking powder","¼ tsp vanilla"],steps:["Add all dry ingredients to a large microwave-safe mug and stir.","Add egg, milk, butter and vanilla. Mix well with a fork.","Microwave 60–90 seconds until set but moist in centre.","Let stand 1 minute before eating."],tip:"Don't overmix — coconut flour turns dense very quickly."},
  {id:12,name:"Chocolate Chia Mousse",desc:"An ultra-creamy chocolate mousse made with chia and cocoa. High fiber, low carb, ready overnight.",sugar:"2g",carbs:"9g",time:10,cal:158,cat:"Chocolate",difficulty:"Medium",featured:false,rating:4.6,votes:93,img:recipeArt("Chocolate Chia Mousse"),nutrition:{sugar:2,carbs:9,protein:7,fat:6},ingredients:["4 tbsp chia seeds","1½ cups unsweetened almond milk","3 tbsp cocoa powder","3 tbsp monk fruit sweetener","1 tsp vanilla","Pinch of cayenne","Raspberries to top"],steps:["Blend almond milk, cocoa, sweetener and vanilla until smooth.","Stir in chia seeds. Wait 10 minutes, stir again.","Refrigerate at least 4 hours or overnight.","Blend until smooth and mousse-like before serving with raspberries."],tip:"The cayenne creates a subtle Mexican chocolate warmth — pairs beautifully with tart raspberries."},
  {id:13,name:"Ricotta Lemon Cups",desc:"Light, creamy ricotta whipped with lemon and a touch of honey. A 5-minute Italian-inspired dessert.",sugar:"4g",carbs:"9g",time:5,cal:155,cat:"Quick & Easy",difficulty:"Easy",featured:false,rating:4.4,votes:61,img:recipeArt("Ricotta Lemon Cups"),nutrition:{sugar:4,carbs:9,protein:8,fat:5},ingredients:["1 cup part-skim ricotta","1 tbsp lemon zest","1 tbsp lemon juice","2 tbsp stevia","½ tsp vanilla","Fresh mint and berries"],steps:["Beat ricotta with a hand mixer until smooth and creamy.","Add stevia, lemon zest, juice and vanilla. Mix 1 more minute.","Taste and adjust sweetness.","Spoon into glasses, top with berries and mint."],tip:"Whipping ricotta completely transforms the texture — never skip this step."},
  {id:14,name:"Sugar-Free Panna Cotta",desc:"Silky Italian panna cotta with vanilla and berry coulis. Elegant, low-carb and impressively easy.",sugar:"2g",carbs:"4g",time:15,cal:140,cat:"No-Bake",difficulty:"Medium",featured:false,rating:4.7,votes:84,img:recipeArt("Chocolate Chia Mousse"),nutrition:{sugar:2,carbs:4,protein:4,fat:14},ingredients:["2 cups heavy cream","3 tbsp erythritol","1½ tsp unflavored gelatin","2 tbsp cold water","1 tsp vanilla","Berry coulis to serve"],steps:["Bloom gelatin in cold water for 5 minutes.","Warm cream and erythritol until steaming — do not boil.","Remove from heat, stir in gelatin and vanilla until dissolved.","Pour into 4 ramekins, cool, then refrigerate 3+ hours."],tip:"Run a knife around the edge and flip onto a plate for restaurant-style presentation."},
  {id:15,name:"Keto Tiramisu Cups",desc:"Classic tiramisu reimagined — mascarpone, espresso, almond sponge with zero sugar. Truly indulgent.",sugar:"1g",carbs:"5g",time:30,cal:210,cat:"No-Bake",difficulty:"Medium",featured:false,rating:4.9,votes:117,img:recipeArt("Keto Tiramisu Cups"),nutrition:{sugar:1,carbs:5,protein:7,fat:16},ingredients:["250g mascarpone","2 eggs, separated","3 tbsp erythritol","1 tsp vanilla","1 shot espresso, cooled","Keto almond ladyfingers","Cocoa to dust"],steps:["Beat yolks with erythritol until pale. Fold in mascarpone and vanilla.","Whisk whites to stiff peaks. Fold into mascarpone mixture.","Dip ladyfingers briefly in espresso. Layer in glasses.","Top with cream, chill 2 hours, dust with cocoa."],tip:"Make it the night before — flavors deepen beautifully."},
  {id:16,name:"Banana Nice Cream",desc:"One-ingredient frozen banana ice cream with endless flavour variations. Naturally sweet, no added sugar.",sugar:"9g",carbs:"18g",time:5,cal:105,cat:"Quick & Easy",difficulty:"Easy",featured:false,rating:4.3,votes:97,img:recipeArt("Banana Nice Cream"),nutrition:{sugar:9,carbs:18,protein:1,fat:0.5},ingredients:["3 frozen ripe bananas","1 tsp vanilla","Pinch of cinnamon","Optional: 1 tbsp cocoa or ½ cup frozen mango"],steps:["Freeze sliced bananas for at least 4 hours.","Blend frozen bananas — first crumbly, then creamy.","Add vanilla and cinnamon, blend 30 more seconds.","Eat immediately for soft-serve or freeze 1 hour for scoopable."],tip:"Combine with frozen mango and lime zest for a tropical sorbet twist."},
  {id:17,name:"Coconut Energy Bites",desc:"Sweet, chewy no-bake bites packed with healthy fats and fiber. Ready in 15 minutes.",sugar:"2g",carbs:"6g",time:15,cal:115,cat:"No-Bake",difficulty:"Easy",featured:false,rating:4.5,votes:74,img:recipeArt("Coconut Energy Bites"),nutrition:{sugar:2,carbs:6,protein:3,fat:8},ingredients:["1 cup desiccated coconut","½ cup almond flour","3 tbsp coconut oil, melted","2 tbsp stevia","1 tsp vanilla","1 tbsp chia seeds","Pinch of salt"],steps:["Mix almond flour, coconut, chia, stevia and salt.","Add melted coconut oil and vanilla; stir until mixture clumps.","Roll into 12 even balls, pressing firmly.","Refrigerate 30 minutes. Store in fridge up to 2 weeks."],tip:"Roll in extra coconut or add sugar-free choc chips for variation."},
  {id:18,name:"Raspberry Almond Clafoutis",desc:"A French-inspired baked custard with almond flour and raspberries. Low carb and elegantly simple.",sugar:"3g",carbs:"7g",time:35,cal:148,cat:"Baked",difficulty:"Medium",featured:false,rating:4.6,votes:53,img:recipeArt("Raspberry Almond Clafoutis"),nutrition:{sugar:3,carbs:7,protein:5,fat:6},ingredients:["3 eggs","½ cup almond milk","¼ cup almond flour","3 tbsp erythritol","1 tsp vanilla","1 tbsp butter for the dish","1 cup fresh raspberries"],steps:["Preheat oven to 180°C. Butter a medium baking dish.","Whisk eggs, almond milk, flour, erythritol and vanilla.","Scatter raspberries in the dish, pour batter over evenly.","Bake 30–32 minutes until puffed and golden with a slight wobble."],tip:"Best eaten the day it is baked — still delicious cold though."}
];

const STORAGE_KEYS={favs:'sweetsafe-favs',ratings:'sweetsafe-ratings',shopping:'sweetsafe-shopping',theme:'sweetsafe-theme',steps:'sweetsafe-steps',timer:'sweetsafe-timer'};
let currentCat='All', currentSearch='', currentDifficulty='All', currentPrep='Any', currentCalories='Any', currentSort='Featured', prevPage='home';
let currentDetailId=null, currentScale=1, timerState={id:null, endAt:0, tick:null};
let favorites=new Set(loadJSON(STORAGE_KEYS.favs, []));
let ratings=loadJSON(STORAGE_KEYS.ratings, {});
let shoppingList=loadJSON(STORAGE_KEYS.shopping, []);
let stepState=loadJSON(STORAGE_KEYS.steps, {});
let theme=localStorage.getItem(STORAGE_KEYS.theme) || 'light';

function loadJSON(key, fallback){
  try{ const v=localStorage.getItem(key); return v ? JSON.parse(v) : fallback; }catch{return fallback;}
}
function saveJSON(key, value){ localStorage.setItem(key, JSON.stringify(value)); }
function escapeHTML(s){ return String(s).replace(/&/g,'&amp;').replace(/</g,'&lt;').replace(/>/g,'&gt;').replace(/"/g,'&quot;').replace(/'/g,'&#39;'); }
function recById(id){ return RECIPES.find(r=>r.id===id); }
function recipeRating(r){
  const user = ratings[r.id];
  if (typeof user === 'number') return {avg:user, votes:(r.votes||0)+1};
  return {avg:r.rating||4.5, votes:r.votes||0};
}
function recipeArt(title){
  const t = String(title).toLowerCase();
  const make = (bg1,bg2,body,accent,caption,art) => {
    const s = `
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 800">
        <defs>
          <linearGradient id="g" x1="0" y1="0" x2="1" y2="1">
            <stop offset="0%" stop-color="${bg1}"/>
            <stop offset="100%" stop-color="${bg2}"/>
          </linearGradient>
          <filter id="shadow" x="-20%" y="-20%" width="140%" height="140%"><feDropShadow dx="0" dy="18" stdDeviation="26" flood-color="#000" flood-opacity="0.22"/></filter>
        </defs>
        <rect width="1200" height="800" rx="42" fill="url(#g)"/>
        <circle cx="1020" cy="130" r="120" fill="rgba(255,255,255,0.10)"/>
        <circle cx="150" cy="120" r="85" fill="rgba(255,255,255,0.08)"/>
        <text x="110" y="120" fill="#fff" font-family="Inter,Arial,sans-serif" font-size="28" font-weight="700" opacity="0.92">SweetSafe</text>
        <text x="110" y="250" fill="#fff" font-family="Cormorant Garamond,Georgia,serif" font-size="66" font-weight="700">${body}</text>
        <text x="110" y="320" fill="rgba(255,255,255,0.88)" font-family="Inter,Arial,sans-serif" font-size="26" font-weight="500">${caption}</text>
        <g filter="url(#shadow)">${art}</g>
        <text x="110" y="715" fill="rgba(255,255,255,0.74)" font-family="Inter,Arial,sans-serif" font-size="20" font-weight="500">${accent}</text>
      </svg>`;
    return `data:image/svg+xml;charset=UTF-8,${encodeURIComponent(s)}`;
  };
  if (t.includes('chocolate chia mousse')) return make('#3f1d6a','#8b5cf6','Chocolate Chia Mousse','Cocoa chia dessert cups',`
      <rect x="355" y="320" width="160" height="275" rx="36" fill="rgba(255,255,255,0.92)"/>
      <rect x="365" y="390" width="140" height="180" rx="22" fill="#3b2b2f"/>
      <circle cx="425" cy="355" r="14" fill="#d97706"/><circle cx="455" cy="385" r="10" fill="#ef4444"/><circle cx="475" cy="365" r="12" fill="#7c3aed"/>
      <rect x="690" y="320" width="160" height="275" rx="36" fill="rgba(255,255,255,0.92)"/>
      <rect x="700" y="390" width="140" height="180" rx="22" fill="#3b2b2f"/>
      <circle cx="760" cy="355" r="14" fill="#d97706"/><circle cx="790" cy="385" r="10" fill="#ef4444"/><circle cx="810" cy="365" r="12" fill="#7c3aed"/>
    `);
  if (t.includes('dark chocolate bark')) return make('#111827','#4c1d95','Dark Chocolate Bark','Chocolate bark with nuts',`
      <path d="M360 470 L820 360 L760 610 L320 620 Z" fill="#2f1a1a"/>
      <path d="M395 500 L770 410 L730 585 L350 600 Z" fill="#4b2d2d" opacity="0.65"/>
      <circle cx="450" cy="475" r="22" fill="#fbbf24"/><circle cx="540" cy="440" r="18" fill="#a3e635"/><circle cx="625" cy="470" r="18" fill="#f97316"/><circle cx="705" cy="430" r="20" fill="#ef4444"/>
    `);
  if (t.includes('keto peanut butter cups')) return make('#5b3416','#a16207','Keto Peanut Butter Cups','Chocolate peanut butter cups',`
      <rect x="360" y="335" width="145" height="145" rx="72" fill="#3a2616"/>
      <rect x="380" y="355" width="105" height="105" rx="52" fill="#f59e0b"/>
      <rect x="560" y="305" width="145" height="145" rx="72" fill="#3a2616"/>
      <rect x="580" y="325" width="105" height="105" rx="52" fill="#f59e0b"/>
      <rect x="760" y="355" width="145" height="145" rx="72" fill="#3a2616"/>
      <rect x="780" y="375" width="105" height="105" rx="52" fill="#f59e0b"/>
    `);
  if (t.includes('cinnamon baked pears')) return make('#b45309','#f59e0b','Cinnamon Baked Pears','Warm pears with spice',`
      <ellipse cx="490" cy="505" rx="84" ry="112" fill="#b45309"/>
      <ellipse cx="490" cy="500" rx="65" ry="96" fill="#f59e0b" opacity="0.88"/>
      <rect x="485" y="355" width="10" height="52" rx="5" fill="#5b3416"/>
      <path d="M468 355 Q490 330 517 350 Q497 338 482 352Z" fill="#2f855a"/>
      <ellipse cx="650" cy="505" rx="84" ry="112" fill="#b45309"/>
      <ellipse cx="650" cy="500" rx="65" ry="96" fill="#f59e0b" opacity="0.88"/>
      <rect x="645" y="355" width="10" height="52" rx="5" fill="#5b3416"/>
      <path d="M628 355 Q650 330 677 350 Q657 338 642 352Z" fill="#2f855a"/>
    `);
  if (t.includes('chia coconut pudding')) return make('#0f766e','#22c55e','Chia Coconut Pudding','Creamy coconut chia jars',`
      <rect x="360" y="295" width="160" height="290" rx="56" fill="rgba(255,255,255,0.86)"/>
      <rect x="370" y="430" width="140" height="145" rx="28" fill="#d9d1c6" opacity="0.55"/>
      <circle cx="430" cy="390" r="6" fill="#6b7280"/><circle cx="460" cy="420" r="6" fill="#6b7280"/><circle cx="446" cy="452" r="6" fill="#6b7280"/>
      <rect x="690" y="295" width="160" height="290" rx="56" fill="rgba(255,255,255,0.86)"/>
      <rect x="700" y="430" width="140" height="145" rx="28" fill="#d9d1c6" opacity="0.55"/>
      <circle cx="760" cy="390" r="6" fill="#6b7280"/><circle cx="790" cy="420" r="6" fill="#6b7280"/><circle cx="776" cy="452" r="6" fill="#6b7280"/>
    `);
  if (t.includes('berry yogurt parfait')) return make('#7c3aed','#ec4899','Berry Yogurt Parfait','Layered berries and yogurt',`
      <rect x="355" y="310" width="155" height="285" rx="42" fill="rgba(255,255,255,0.88)"/>
      <rect x="365" y="470" width="135" height="115" rx="22" fill="#f472b6" opacity="0.70"/>
      <rect x="365" y="430" width="135" height="55" rx="12" fill="#e5e7eb" opacity="0.85"/>
      <rect x="365" y="390" width="135" height="45" rx="12" fill="#f9fafb" opacity="0.95"/>
      <circle cx="415" cy="386" r="12" fill="#7c3aed"/><circle cx="450" cy="404" r="12" fill="#ef4444"/><circle cx="472" cy="388" r="10" fill="#2563eb"/>
      <rect x="690" y="310" width="155" height="285" rx="42" fill="rgba(255,255,255,0.88)"/>
      <rect x="700" y="470" width="135" height="115" rx="22" fill="#f472b6" opacity="0.70"/>
      <rect x="700" y="430" width="135" height="55" rx="12" fill="#e5e7eb" opacity="0.85"/>
      <rect x="700" y="390" width="135" height="45" rx="12" fill="#f9fafb" opacity="0.95"/>
      <circle cx="750" cy="386" r="12" fill="#7c3aed"/><circle cx="785" cy="404" r="12" fill="#ef4444"/><circle cx="807" cy="388" r="10" fill="#2563eb"/>
    `);
  if (t.includes('coconut flour mug cake')) return make('#78350f','#f97316','Coconut Flour Mug Cake','Warm chocolate mug cake',`
      <rect x="395" y="300" width="155" height="280" rx="30" fill="rgba(255,255,255,0.92)"/>
      <rect x="405" y="355" width="135" height="205" rx="26" fill="#8b5e3c"/>
      <rect x="700" y="300" width="155" height="280" rx="30" fill="rgba(255,255,255,0.92)"/>
      <rect x="710" y="355" width="135" height="205" rx="26" fill="#8b5e3c"/>
      <circle cx="470" cy="380" r="24" fill="#f8fafc" opacity="0.5"/>
      <circle cx="775" cy="380" r="24" fill="#f8fafc" opacity="0.5"/>
    `);
  if (t.includes('ricotta lemon cups')) return make('#f59e0b','#fbbf24','Ricotta Lemon Cups','Lemon ricotta dessert cups',`
      <rect x="360" y="310" width="160" height="285" rx="34" fill="rgba(255,255,255,0.90)"/>
      <rect x="370" y="375" width="140" height="195" rx="24" fill="#fef08a"/>
      <circle cx="430" cy="360" r="34" fill="#facc15"/>
      <rect x="690" y="310" width="160" height="285" rx="34" fill="rgba(255,255,255,0.90)"/>
      <rect x="700" y="375" width="140" height="195" rx="24" fill="#fef08a"/>
      <circle cx="760" cy="360" r="34" fill="#facc15"/>
    `);
  if (t.includes('keto tiramisu cups')) return make('#4b5563','#111827','Keto Tiramisu Cups','Espresso mascarpone layers',`
      <rect x="355" y="305" width="165" height="290" rx="28" fill="rgba(255,255,255,0.92)"/>
      <rect x="365" y="470" width="145" height="110" rx="16" fill="#5b3a29"/>
      <rect x="365" y="405" width="145" height="70" rx="16" fill="#ede9fe"/>
      <rect x="690" y="305" width="165" height="290" rx="28" fill="rgba(255,255,255,0.92)"/>
      <rect x="700" y="470" width="145" height="110" rx="16" fill="#5b3a29"/>
      <rect x="700" y="405" width="145" height="70" rx="16" fill="#ede9fe"/>
    `);
  if (t.includes('banana nice cream')) return make('#f59e0b','#fde68a','Banana Nice Cream','Frozen banana soft serve',`
      <path d="M430 560 C430 470 520 390 590 390 C660 390 750 470 750 560" fill="#fef3c7"/>
      <path d="M465 540 C465 480 535 430 590 430 C645 430 715 480 715 540" fill="#facc15" opacity="0.95"/>
      <circle cx="590" cy="390" r="38" fill="#f59e0b" opacity="0.8"/>
    `);
  if (t.includes('raspberry almond clafoutis')) return make('#7c2d12','#fb7185','Raspberry Almond Clafoutis','Baked berry custard',`
      <circle cx="495" cy="510" r="150" fill="#f8e8c8"/>
      <circle cx="495" cy="505" r="128" fill="#fde68a"/>
      <circle cx="450" cy="480" r="22" fill="#e11d48"/><circle cx="535" cy="460" r="22" fill="#e11d48"/><circle cx="570" cy="515" r="22" fill="#e11d48"/><circle cx="430" cy="540" r="22" fill="#e11d48"/>
    `);
  if (t.includes('coconut energy bites')) return make('#0f766e','#14b8a6','Coconut Energy Bites','Chewy coconut balls',`
      <circle cx="450" cy="500" r="52" fill="#f8fafc"/>
      <circle cx="560" cy="470" r="52" fill="#f8fafc"/>
      <circle cx="670" cy="515" r="52" fill="#f8fafc"/>
      <circle cx="780" cy="485" r="52" fill="#f8fafc"/>
    `);
  return make('#2563eb','#0D9488','SweetSafe Recipes','Fresh dessert inspiration',`<rect x="390" y="330" width="420" height="230" rx="30" fill="rgba(255,255,255,0.22)"/>`);
}
function imgFor(r){ return r.img || recipeArt(r.name); }
function scaleIngredient(text, scale){
  const fracMap={'½':0.5,'¼':0.25,'¾':0.75,'⅓':1/3,'⅔':2/3,'⅛':0.125,'⅜':0.375,'⅝':0.625,'⅞':0.875};
  let s=String(text);
  const mixed=s.match(/^(\d+)\s*([¼½¾⅓⅔⅛⅜⅝⅞])\b/);
  if(mixed){ const v=(parseFloat(mixed[1])+fracMap[mixed[2]])*scale; return s.replace(mixed[0], prettyAmount(v)); }
  const frac=s.match(/^([¼½¾⅓⅔⅛⅜⅝⅞])\b/);
  if(frac){ const v=fracMap[frac[1]]*scale; return s.replace(frac[0], prettyAmount(v)); }
  const dec=s.match(/^(\d+(?:\.\d+)?)\b/);
  if(dec){ const v=parseFloat(dec[1])*scale; return s.replace(dec[1], prettyAmount(v)); }
  return s;
}
function prettyAmount(n){
  const rounded=Math.round(n*8)/8;
  if (Math.abs(rounded - Math.round(rounded)) < 1e-9) return String(Math.round(rounded));
  const map={0.125:'⅛',0.25:'¼',0.375:'⅜',0.5:'½',0.625:'⅝',0.75:'¾',0.875:'⅞'};
  if (map[rounded]) return map[rounded];
  return String(Number(rounded.toFixed(2)).toString());
}
function setTheme(mode){
  theme = mode || (document.body.classList.contains('dark-mode') ? 'dark' : 'light');
  document.body.classList.toggle('dark-mode', theme === 'dark');
  localStorage.setItem(STORAGE_KEYS.theme, theme);
  const btn = document.getElementById('theme-toggle');
  if (btn) btn.innerHTML = theme === 'dark' ? '☀️ Light' : '🌙 Dark';
  toast(theme === 'dark' ? 'Dark mode on' : 'Light mode on');
}
function applyTheme(){ setTheme(theme); }
function injectUI(){
  const nav=document.querySelector('nav');
  if (nav && !document.getElementById('theme-toggle')){
    const btn=document.createElement('button');
    btn.className='theme-toggle';
    btn.id='theme-toggle';
    btn.type='button';
    btn.onclick=()=>setTheme(theme==='dark'?'light':'dark');
    nav.insertBefore(btn, nav.querySelector('.nav-cta'));
  }
  const recipesHdr=document.querySelector('#page-recipes .page-hdr');
  if (recipesHdr && !document.getElementById('filters-toolbar')){
    const toolbar=document.createElement('div');
    toolbar.className='filters-toolbar';
    toolbar.id='filters-toolbar';
    toolbar.innerHTML=`
      <div class="filter-box"><label>Sort</label><select id="sort-select"><option>Featured</option><option>Rating</option><option>Time</option><option>Calories</option><option>A-Z</option></select></div>
      <div class="filter-box"><label>Prep time</label><select id="prep-select"><option>Any</option><option>Under 10</option><option>Under 15</option><option>Under 30</option></select></div>
      <div class="filter-box"><label>Calories</label><select id="cal-select"><option>Any</option><option>Under 120</option><option>120-160</option><option>160-200</option><option>200+</option></select></div>
      <div class="filter-box"><label>Difficulty</label><select id="diff-select"><option>All</option><option>Easy</option><option>Medium</option></select></div>`;
    recipesHdr.insertAdjacentElement('afterend', toolbar);
    document.getElementById('sort-select').addEventListener('change', e=>{ currentSort=e.target.value; renderRecipes(); });
    document.getElementById('prep-select').addEventListener('change', e=>{ currentPrep=e.target.value; renderRecipes(); });
    document.getElementById('cal-select').addEventListener('change', e=>{ currentCalories=e.target.value; renderRecipes(); });
    document.getElementById('diff-select').addEventListener('change', e=>{ currentDifficulty=e.target.value; renderRecipes(); });
    const tabs=document.querySelector('.cat-tabs');
    if (tabs && !tabs.querySelector('[data-cat="Saved"]')){
      const saved=document.createElement('button');
      saved.className='ct';
      saved.dataset.cat='Saved';
      saved.textContent='Saved';
      saved.onclick=()=>setCat('Saved');
      tabs.appendChild(saved);
    }
  }
}
function buildCard(r){
  const rt = recipeRating(r);
  const fav = favorites.has(r.id);
  return `<div class="rcard" onclick="showDetail(${r.id})">
    <div class="rcard-img">
      <img src="${imgFor(r)}" alt="${escapeHTML(r.name)}" loading="lazy" onerror="this.src='${recipeArt(r.name)}'">
      <div class="card-top-actions"><button class="fav-btn ${fav?'on':''}" onclick="event.stopPropagation();toggleFavorite(${r.id})">${fav?'♥':'♡'}</button><div class="rating-chip"><span>★</span> ${rt.avg.toFixed(1)}</div></div>
      <div class="card-overlay"></div>
      <div class="badges"><span class="badge b-red">${r.sugar} sugar</span><span class="badge b-amber">${r.carbs} carbs</span></div>
      <div class="cat-badge">${r.cat}</div>
    </div>
    <div class="rcard-body">
      <div class="rcard-title">${escapeHTML(r.name)}</div>
      <div class="rcard-desc">${escapeHTML(r.desc)}</div>
      <div class="card-rating-row"><span class="avg">${rt.avg.toFixed(1)}/5</span><span>${rt.votes} ratings</span></div>
      <div class="rcard-meta"><span class="meta-item">⏱ ${r.time} mins</span><span class="divider-dot"></span><span class="meta-item">🔥 ${r.cal} cal</span></div>
    </div>
  </div>`;
}
function renderFeatured(){
  const el=document.getElementById('featured-grid'); if(!el) return;
  el.innerHTML = RECIPES.filter(r=>r.featured).slice(0,6).map(buildCard).join('');
}
function passesFilters(r){
  const search = currentSearch.trim().toLowerCase();
  const matchesSearch = !search || [r.name,r.desc,r.cat,(r.ingredients||[]).join(' ')].join(' ').toLowerCase().includes(search);
  const matchesCat = currentCat==='All' || currentCat==='Saved' ? true : r.cat===currentCat;
  const matchesSaved = currentCat!=='Saved' || favorites.has(r.id);
  const matchesDiff = currentDifficulty==='All' || r.difficulty===currentDifficulty;
  const matchesPrep = currentPrep==='Any' || (currentPrep==='Under 10' ? r.time<=10 : currentPrep==='Under 15' ? r.time<=15 : r.time<=30);
  const c=r.cal;
  const matchesCal = currentCalories==='Any' || (currentCalories==='Under 120' ? c<120 : currentCalories==='120-160' ? c>=120 && c<=160 : currentCalories==='160-200' ? c>160 && c<=200 : c>200);
  return matchesSearch && matchesCat && matchesSaved && matchesDiff && matchesPrep && matchesCal;
}
function sortList(list){
  const arr=[...list];
  switch(currentSort){
    case 'Rating': return arr.sort((a,b)=>recipeRating(b).avg-recipeRating(a).avg);
    case 'Time': return arr.sort((a,b)=>a.time-b.time);
    case 'Calories': return arr.sort((a,b)=>a.cal-b.cal);
    case 'A-Z': return arr.sort((a,b)=>a.name.localeCompare(b.name));
    default: return arr.sort((a,b)=>(b.featured===a.featured?0:(b.featured?1:-1)) || recipeRating(b).avg-recipeRating(a).avg);
  }
}
function renderRecipes(){
  const g=document.getElementById('recipes-grid'); if(!g) return;
  const list = sortList(RECIPES.filter(passesFilters));
  g.innerHTML = list.length ? list.map(buildCard).join('') : `<div class="no-results"><div class="no-results-icon">🔍</div><h3>No recipes found</h3><p>Try a different filter or category.</p></div>`;
}
function setCat(cat){
  currentCat = cat;
  document.querySelectorAll('.ct').forEach(b=>b.classList.toggle('active', b.dataset.cat===cat));
  renderRecipes();
}
function filterRecipes(){ currentSearch = document.getElementById('search-input')?.value || ''; renderRecipes(); }
function goRecipes(cat){ currentCat=cat; goPage('recipes'); setTimeout(()=>setCat(cat), 0); }
function goPage(p){
  if (p!=='detail') prevPage = p;
  document.querySelectorAll('.page').forEach(el=>el.classList.remove('active'));
  const target=document.getElementById('page-'+p);
  if (target) target.classList.add('active');
  document.querySelectorAll('.nl').forEach(b=>b.classList.toggle('active', b.dataset.page===p));
  if (p==='recipes') renderRecipes();
  window.scrollTo({top:0, behavior:'smooth'});
}
function toggleTag(el){ el.classList.toggle('on'); }
function toggleFavorite(id){
  const nowFav = !favorites.has(id);
  if (nowFav) favorites.add(id); else favorites.delete(id);
  saveJSON(STORAGE_KEYS.favs, [...favorites]);
  renderFeatured(); renderRecipes();
  if (currentDetailId===id) showDetail(id);
  toast(nowFav ? 'Saved to favourites' : 'Removed from favourites');
}
function scaledIngredients(recipe){
  return (recipe.ingredients||[]).map(i=>scaleIngredient(i, currentScale));
}
function addToShopping(item){
  const clean = String(item).trim();
  if (!clean || shoppingList.includes(clean)) return;
  shoppingList.push(clean);
  saveJSON(STORAGE_KEYS.shopping, shoppingList);
  if (currentDetailId) showDetail(currentDetailId);
  toast('Added to shopping list');
}
function removeFromShopping(item){
  shoppingList = shoppingList.filter(x=>x!==item);
  saveJSON(STORAGE_KEYS.shopping, shoppingList);
  if (currentDetailId) showDetail(currentDetailId);
  toast('Removed from shopping list');
}
function copyShopping(){
  navigator.clipboard?.writeText(shoppingList.join('\n'));
  toast('Shopping list copied');
}
function copyRecipe(recipe){
  const txt = `${recipe.name}\n\nIngredients:\n- ${recipe.ingredients.join('\n- ')}\n\nSteps:\n- ${recipe.steps.join('\n- ')}`;
  navigator.clipboard?.writeText(txt);
  toast('Recipe copied');
}
function startTimer(minutes){
  const mins = Math.max(1, parseInt(minutes,10)||0);
  timerState.endAt = Date.now() + mins*60000;
  if (timerState.tick) clearInterval(timerState.tick);
  timerState.tick = setInterval(updateTimerDisplay, 1000);
  updateTimerDisplay();
  toast(`Timer started for ${mins} min`);
}
function stopTimer(){
  if (timerState.tick) clearInterval(timerState.tick);
  timerState.tick=null; timerState.endAt=0;
  updateTimerDisplay();
}
function updateTimerDisplay(){
  const el=document.getElementById('timer-display'); if (!el) return;
  if (!timerState.endAt){ el.textContent='00:00'; return; }
  const left = Math.max(0, timerState.endAt - Date.now());
  const mm = String(Math.floor(left/60000)).padStart(2,'0');
  const ss = String(Math.floor((left%60000)/1000)).padStart(2,'0');
  el.textContent = `${mm}:${ss}`;
  if (left<=0){ stopTimer(); alert('Timer finished!'); }
}
function rateRecipe(id, val){ ratings[id] = val; saveJSON(STORAGE_KEYS.ratings, ratings); renderFeatured(); renderRecipes(); if (currentDetailId===id) showDetail(id); }
function toggleStepDone(recipeId, idx){
  const key=String(recipeId); if(!stepState[key]) stepState[key]=[]; stepState[key][idx]=!stepState[key][idx]; saveJSON(STORAGE_KEYS.steps, stepState); showDetail(recipeId);
}
function printRecipe(){ window.print(); }
function showDetail(id){
  const r = recById(id); if(!r) return;
  currentDetailId=id; currentScale=1;
  const rating=recipeRating(r);
  const related = RECIPES.filter(x=>x.id!==r.id).filter(x=>x.cat===r.cat || x.difficulty===r.difficulty).slice(0,3);
  const stepsDone = stepState[String(id)] || [];
  const scaled = scaledIngredients(r);
  const nutri = r.nutrition || {sugar:0, carbs:0, protein:0, fat:0};
  const maxNutri = Math.max(nutri.sugar||1, nutri.carbs||1, nutri.protein||1, nutri.fat||1);
  document.getElementById('detail-content').innerHTML = `
    <button class="back-btn" onclick="goPage('${prevPage}')">← Back to ${prevPage==='home'?'Home':'Recipes'}</button>
    <div class="detail-grid">
      <div class="detail-img"><img src="${imgFor(r)}" alt="${escapeHTML(r.name)}" loading="lazy" onerror="this.src='${recipeArt(r.name)}'"></div>
      <div class="detail-info">
        <div class="detail-cats"><span class="d-tag">${r.cat}</span><span class="d-tag">Diabetes-Friendly</span><span class="d-tag">Low Sugar</span><span class="d-tag">${r.difficulty}</span></div>
        <div class="detail-title">${escapeHTML(r.name)}</div>
        <div class="detail-desc">${escapeHTML(r.desc)}</div>
        <div class="stats-grid">
          <div class="stat-box"><div class="stat-val">${r.sugar}</div><div class="stat-lbl">Sugar</div></div>
          <div class="stat-box"><div class="stat-val">${r.carbs}</div><div class="stat-lbl">Net Carbs</div></div>
          <div class="stat-box"><div class="stat-val">${r.time}m</div><div class="stat-lbl">Time</div></div>
          <div class="stat-box"><div class="stat-val">${r.cal}</div><div class="stat-lbl">Calories</div></div>
        </div>
        <div class="detail-actions">
          <button class="action-btn" onclick="toggleFavorite(${r.id})">${favorites.has(r.id)?'♥ Saved':'♡ Save'}</button>
          <button class="action-btn" onclick="copyRecipe(recById(${r.id}))">Copy Recipe</button>
          <button class="action-btn" onclick="printRecipe()">Print</button>
        </div>
      </div>
    </div>

    <div class="detail-subgrid">
      <div class="control-panel">
        <div class="panel-h">Serving Size</div>
        <div class="servings-row">
          <span>Scale ingredients</span>
          <select id="serving-select" onchange="currentScale=parseFloat(this.value); showDetail(${r.id})">
            <option value="1" ${currentScale===1?'selected':''}>1x</option>
            <option value="2" ${currentScale===2?'selected':''}>2x</option>
            <option value="4" ${currentScale===4?'selected':''}>4x</option>
            <option value="6" ${currentScale===6?'selected':''}>6x</option>
          </select>
        </div>
      </div>
      <div class="timer-panel">
        <div class="panel-h">Cooking Timer</div>
        <div class="timer-display" id="timer-display">00:00</div>
        <div class="timer-controls">
          <input id="timer-mins" type="number" min="1" value="10" style="width:100px" />
          <button class="small-btn" onclick="startTimer(document.getElementById('timer-mins').value)">Start</button>
          <button class="small-btn" onclick="stopTimer()">Stop</button>
        </div>
      </div>
    </div>

    <div class="content-grid">
      <div>
        <div class="sec-h">Ingredients</div>
        <ul class="ingr-list">${scaled.map(i=>`<li class="clickable-ingr ${shoppingList.includes(i)?'added':''}" onclick="addToShopping('${escapeHTML(i)}')"><span class="ingr-dot"></span>${escapeHTML(i)}</li>`).join('')}</ul>
      </div>
      <div>
        <div class="sec-h">Instructions</div>
        <ol class="steps-list">${r.steps.map((s,i)=>`<li><span class="step-n" onclick="toggleStepDone(${r.id},${i})" style="cursor:pointer;${stepsDone[i]?'filter:brightness(1.15)':''}">${stepsDone[i]?'✓':i+1}</span><span style="text-decoration:${stepsDone[i]?'line-through':'none'};opacity:${stepsDone[i]?'.7':'1'}">${escapeHTML(s)}</span></li>`).join('')}</ol>
        ${r.tip?`<div class="tip-box">💡 ${escapeHTML(r.tip)}</div>`:''}
      </div>
    </div>

    <div class="detail-subgrid">
      <div class="shopping-panel">
        <div class="panel-h">Shopping List</div>
        <ul class="shopping-list">${shoppingList.length ? shoppingList.map(x=>`<li><span>${escapeHTML(x)}</span><button class="small-btn" onclick="removeFromShopping('${escapeHTML(x)}')">Remove</button></li>`).join('') : '<li>No items yet — tap ingredients to add them.</li>'}</ul>
        <div class="list-actions"><button class="small-btn" onclick="copyShopping()">Copy list</button><button class="small-btn" onclick="shoppingList=[]; saveJSON(STORAGE_KEYS.shopping, shoppingList); showDetail(${r.id})">Clear</button></div>
      </div>
      <div class="rating-panel">
        <div class="panel-h">Rate this recipe</div>
        <div class="rating-stars">${[1,2,3,4,5].map(n=>`<button class="${(ratings[r.id]||r.rating||0)>=n?'on':''}" onclick="rateRecipe(${r.id},${n})">★</button>`).join('')} <span class="rating-note">${rating.avg.toFixed(1)}/5 from ${rating.votes} ratings</span></div>
      </div>
    </div>

    <div class="detail-subgrid">
      <div class="nutrition-panel">
        <div class="panel-h">Nutrition Breakdown</div>
        <div class="nutri-bars">${['sugar','carbs','protein','fat'].map(k=>`<div class="nutri-row"><div>${k.toUpperCase()}</div><div class="nutri-track"><div class="nutri-fill" style="width:${Math.min(100, ((nutri[k]||0)/maxNutri)*100)}%"></div></div><div class="nutri-val">${((nutri[k]||0)*currentScale).toFixed(1)}</div></div>`).join('')}</div>
      </div>
      <div class="control-panel">
        <div class="panel-h">Related Recipes</div>
        <div class="related-grid">${related.map(x=>buildCard(x)).join('')}</div>
      </div>
    </div>
  `;
  goPage('detail');
  updateTimerDisplay();
}
async function generateRecipe(){
  const ing=document.getElementById('ingredients-input').value.trim();
  if(!ing){ showErr('Please enter some ingredients first!'); return; }
  const prefs=[...document.querySelectorAll('.dtag.on')].map(t=>t.textContent).join(', ');
  const btn=document.getElementById('gen-btn');
  document.getElementById('gen-spinner').style.display='block';
  document.getElementById('gen-btn-txt').textContent='Creating your recipe…';
  btn.disabled=true;
  document.getElementById('err-msg').style.display='none';
  document.getElementById('gen-out').style.display='none';
  document.getElementById('loading-card').style.display='block';
  try{
    const base = ing.split(',').map(s=>s.trim()).filter(Boolean).slice(0,6);
    const r = {
      name: `${base[0] || 'Custom'} SweetSafe Dessert`,
      description:`A custom diabetes-friendly dessert built from the ingredients you have${prefs ? ' and tailored to: ' + prefs : ''}.`,
      prepTime: base.length > 3 ? '15 mins' : '10 mins',
      calories: 160,
      sugar:'4g',
      carbs:'12g',
      difficulty: base.length > 4 ? 'Medium' : 'Easy',
      ingredients: base.length ? base.map(x=>`• ${x}`) : ['• Your ingredients here'],
      steps:['Combine the ingredients until smooth.','Chill or bake as needed.','Serve and enjoy.'],
      tip:'You can tap the save button to keep this recipe in your favorites.'
    };
    renderGenerated(r);
    toast('Custom recipe created');
  }catch(e){ showErr('Something went wrong. Please try again.'); }
  finally{
    btn.disabled=false;
    document.getElementById('gen-spinner').style.display='none';
    document.getElementById('gen-btn-txt').textContent='✦ Generate My Recipe';
    document.getElementById('loading-card').style.display='none';
  }
}
function showErr(msg){ const b=document.getElementById('err-msg'); b.textContent=msg; b.style.display='block'; }
let toastTimer=null;
function toast(msg){ const el=document.getElementById('toast'); if(!el) return; el.textContent=msg; el.classList.add('show'); clearTimeout(toastTimer); toastTimer=setTimeout(()=>el.classList.remove('show'), 1900); }
function renderGenerated(r){
  const out=document.getElementById('gen-out');
  out.innerHTML=`
    <div style="display:flex;justify-content:space-between;align-items:flex-start;gap:1rem;margin-bottom:1rem">
      <div><div class="gen-name">${escapeHTML(r.name)}</div><div class="gen-desc">${escapeHTML(r.description)}</div></div>
      <span class="d-tag" style="white-space:nowrap;flex-shrink:0">${escapeHTML(r.difficulty)}</span>
    </div>
    <div class="gen-stats">
      <div class="gs"><div class="gs-v">${r.sugar}</div><div class="gs-l">Sugar</div></div>
      <div class="gs"><div class="gs-v">${r.carbs}</div><div class="gs-l">Net Carbs</div></div>
      <div class="gs"><div class="gs-v">${r.prepTime}</div><div class="gs-l">Prep Time</div></div>
      <div class="gs"><div class="gs-v">${r.calories}</div><div class="gs-l">Calories</div></div>
    </div>
    <div class="gen-grid">
      <div><div class="gen-sec-h">Ingredients</div><ul class="gen-ingr-list">${r.ingredients.map(i=>`<li>🔹 ${escapeHTML(i)}</li>`).join('')}</ul></div>
      <div><div class="gen-sec-h">Instructions</div><ol class="gen-steps-list">${r.steps.map((s,i)=>`<li><span class="step-n">${i+1}</span><span>${escapeHTML(s)}</span></li>`).join('')}</ol></div>
    </div>
    ${r.tip?`<div class="tip-box" style="margin-top:1.25rem">💡 ${escapeHTML(r.tip)}</div>`:''}
  `;
  out.style.display='block';
}
function init(){
  injectUI();
  applyTheme();
  renderFeatured();
  renderRecipes();
  updateTimerDisplay();
}
window.addEventListener('DOMContentLoaded', init);
window.addEventListener('beforeunload', ()=>{ if(timerState.tick) clearInterval(timerState.tick); });
</script>
