'use strict';

// ─── HEADER SCROLL ────────────────────────────────────────────────
const header = document.querySelector('.site-header');
if (header) {
  window.addEventListener('scroll', () => {
    header.classList.toggle('scrolled', window.scrollY > 24);
  }, { passive: true });
}

// ─── HAMBURGER / MOBILE NAV ───────────────────────────────────────
const hamburger = document.getElementById('hamburger');
const mainNav   = document.getElementById('mainNav');

if (hamburger && mainNav) {
  const overlay = document.getElementById('nav-overlay');

  function openNav() {
    mainNav.classList.add('open');
    if (overlay) overlay.classList.add('open');
    hamburger.classList.add('open');
    hamburger.setAttribute('aria-expanded', 'true');
    document.body.style.overflow = 'hidden';
  }

  function closeNav() {
    mainNav.classList.remove('open');
    if (overlay) overlay.classList.remove('open');
    hamburger.classList.remove('open');
    hamburger.setAttribute('aria-expanded', 'false');
    document.body.style.overflow = '';
  }

  hamburger.addEventListener('click', () => {
    mainNav.classList.contains('open') ? closeNav() : openNav();
  });

  // Close when any nav link is tapped
  mainNav.querySelectorAll('a').forEach(a =>
    a.addEventListener('click', closeNav)
  );

  // Close when overlay is tapped
  if (overlay) overlay.addEventListener('click', closeNav);

  // Close on Escape key
  document.addEventListener('keydown', e => {
    if (e.key === 'Escape') closeNav();
  });
}


// ─── FAQ ACCORDION ────────────────────────────────────────────────
document.querySelectorAll('.faq-trigger').forEach(trigger => {
  trigger.addEventListener('click', () => {
    const item = trigger.closest('.faq-item');
    const isOpen = item.classList.contains('open');
    document.querySelectorAll('.faq-item.open').forEach(i => {
      i.classList.remove('open');
      i.querySelector('.faq-trigger').setAttribute('aria-expanded', 'false');
    });
    if (!isOpen) {
      item.classList.add('open');
      trigger.setAttribute('aria-expanded', 'true');
    }
  });
});

// ─── REVEAL ON SCROLL ─────────────────────────────────────────────
const revealObserver = new IntersectionObserver((entries) => {
  entries.forEach(e => {
    if (e.isIntersecting) {
      e.target.classList.add('visible');
      revealObserver.unobserve(e.target);
    }
  });
}, { threshold: 0.06, rootMargin: '0px 0px -16px 0px' });

document.querySelectorAll(
  '.reveal, .reveal-left, .reveal-scale, .svc-card, .testi-card, ' +
  '.industry-card, .value-card, .faq-item, .process-item, .metric, ' +
  '.ci-item, .ind-card, .platform-pill, .blog-card, .related-svc-card'
).forEach(el => {
  if (!el.classList.contains('reveal-left') && !el.classList.contains('reveal-scale')) {
    el.classList.add('reveal');
  }
  revealObserver.observe(el);
});

// ─── COUNTER ANIMATION ────────────────────────────────────────────
function countUp(el) {
  const text   = el.dataset.count || el.textContent.trim();
  const prefix = text.match(/^[^\d]*/)?.[0] || '';
  const suffix = text.match(/[^\d]*$/)?.[0] || '';
  const target = parseInt(text.replace(/\D/g, ''), 10);
  if (isNaN(target)) return;

  const dur  = 1400;
  const ease = t => t < 0.5 ? 4*t*t*t : 1 - Math.pow(-2*t+2, 3)/2;
  let start  = null;

  function frame(ts) {
    if (!start) start = ts;
    const p = Math.min((ts - start) / dur, 1);
    el.textContent = prefix + Math.round(ease(p) * target) + suffix;
    if (p < 1) requestAnimationFrame(frame);
    else el.textContent = prefix + target + suffix;
  }
  requestAnimationFrame(frame);
}

const counterObs = new IntersectionObserver((entries) => {
  entries.forEach(e => {
    if (e.isIntersecting) {
      countUp(e.target);
      counterObs.unobserve(e.target);
    }
  });
}, { threshold: 0.5 });

document.querySelectorAll('.metric-num, .hero-stat-num, .rstat .big, .about-img-badge .big')
  .forEach(el => { if (/\d/.test(el.textContent)) counterObs.observe(el); });

// ─── LAZY IMAGES ──────────────────────────────────────────────────
if ('IntersectionObserver' in window) {
  const lazyObs = new IntersectionObserver((entries) => {
    entries.forEach(e => {
      if (e.isIntersecting) {
        const img = e.target;
        if (img.dataset.src) { img.src = img.dataset.src; img.removeAttribute('data-src'); }
        lazyObs.unobserve(img);
      }
    });
  }, { rootMargin: '200px 0px' });
  document.querySelectorAll('img[data-src]').forEach(img => lazyObs.observe(img));
}

// ─── SMOOTH ANCHOR SCROLL ─────────────────────────────────────────
document.querySelectorAll('a[href^="#"]').forEach(a => {
  a.addEventListener('click', function (e) {
    const t = document.querySelector(this.getAttribute('href'));
    if (t) {
      e.preventDefault();
      const top = t.getBoundingClientRect().top + scrollY - 82;
      window.scrollTo({ top, behavior: 'smooth' });
    }
  });
});

// ─── ANALYTICS: Phone & Email clicks ──────────────────────────────
document.querySelectorAll('a[href^="tel:"]').forEach(a => {
  a.addEventListener('click', () => {
    if (typeof gtag === 'function') gtag('event', 'phone_click', {
      event_category: 'engagement',
      event_label: a.href,
      value: 1
    });
  });
});

document.querySelectorAll('a[href^="mailto:"]').forEach(a => {
  a.addEventListener('click', () => {
    if (typeof gtag === 'function') gtag('event', 'email_click', {
      event_category: 'engagement',
      event_label: a.href
    });
  });
});

// ─── ANALYTICS: Sticky Call button ────────────────────────────────
document.querySelectorAll('.sticky-call').forEach(a => {
  a.addEventListener('click', () => {
    if (typeof gtag === 'function') gtag('event', 'sticky_call_click', {
      event_category: 'engagement',
      event_label: 'Sticky Call Float Button',
      value: 1
    });
  });
});

// ─── ANALYTICS: CTA button clicks ─────────────────────────────────
document.querySelectorAll('.btn-gold, .btn-nav, [class*="cta"]').forEach(btn => {
  btn.addEventListener('click', () => {
    const label = btn.textContent.trim().substring(0, 50);
    if (typeof gtag === 'function') gtag('event', 'cta_click', {
      event_category: 'engagement',
      event_label: label
    });
  });
});

// ─── ANALYTICS: Form submissions ──────────────────────────────────
document.querySelectorAll('form').forEach(form => {
  form.addEventListener('submit', () => {
    const btn = form.querySelector('button[type="submit"]');
    if (btn) { btn.textContent = 'Sending…'; btn.disabled = true; btn.style.opacity = '0.65'; }
    if (typeof gtag === 'function') gtag('event', 'form_submit', {
      event_category: 'lead',
      event_label: document.title,
      value: 1
    });
  });
});

// ─── ANALYTICS: Scroll depth tracking ────────────────────────────
(function () {
  const depths = [25, 50, 75, 90];
  const fired  = new Set();
  window.addEventListener('scroll', () => {
    const pct = Math.round(
      (window.scrollY / (document.body.scrollHeight - window.innerHeight)) * 100
    );
    depths.forEach(d => {
      if (pct >= d && !fired.has(d)) {
        fired.add(d);
        if (typeof gtag === 'function') gtag('event', 'scroll_depth', {
          event_category: 'engagement',
          event_label: d + '%',
          non_interaction: true
        });
      }
    });
  }, { passive: true });
})();

// ─── ANALYTICS: Time on page (30s, 60s, 120s milestones) ─────────
(function () {
  const milestones = [30, 60, 120];
  milestones.forEach(sec => {
    setTimeout(() => {
      if (typeof gtag === 'function') gtag('event', 'time_on_page', {
        event_category: 'engagement',
        event_label: sec + 's',
        non_interaction: true
      });
    }, sec * 1000);
  });
})();

// ─── ANALYTICS: Outbound link clicks ──────────────────────────────
document.querySelectorAll('a[href^="http"]').forEach(a => {
  try {
    if (new URL(a.href).hostname !== location.hostname) {
      a.addEventListener('click', () => {
        if (typeof gtag === 'function') gtag('event', 'outbound_click', {
          event_category: 'engagement',
          event_label: a.href
        });
      });
    }
  } catch(e) {}
});

// ─── ANALYTICS: Map / directions click ────────────────────────────
document.querySelectorAll('a[href*="maps.google"]').forEach(a => {
  a.addEventListener('click', () => {
    if (typeof gtag === 'function') gtag('event', 'directions_click', {
      event_category: 'engagement',
      event_label: 'Google Maps directions'
    });
  });
});

// ─── STICKY CALL: hide near footer ───────────────────────────────
(function () {
  const stickyCall = document.querySelector('.sticky-call');
  const footer     = document.querySelector('.site-footer');
  if (!stickyCall || !footer) return;
  const obs = new IntersectionObserver((entries) => {
    entries.forEach(e => {
      stickyCall.style.opacity    = e.isIntersecting ? '0' : '';
      stickyCall.style.pointerEvents = e.isIntersecting ? 'none' : '';
    });
  }, { threshold: 0.1 });
  obs.observe(footer);
})();

// ─── BACK TO TOP ──────────────────────────────────────────────────
(function () {
  const btn = document.querySelector('.back-to-top');
  if (!btn) return;
  window.addEventListener('scroll', () => {
    btn.classList.toggle('visible', window.scrollY > 400);
  }, { passive: true });
  btn.addEventListener('click', () => {
    window.scrollTo({ top: 0, behavior: 'smooth' });
    if (typeof gtag === 'function') gtag('event', 'back_to_top', { event_category: 'engagement' });
  });
})();

// ─── HERO ENTRY ANIMATION ──────────────────────────────────────────
(function () {
  const heroLeft = document.querySelector('.hero-left');
  if (!heroLeft) return;
  const EASE = 'cubic-bezier(0.22,1,0.36,1)';
  const els = heroLeft.querySelectorAll(
    '.hero-badge,.hero-company-name,h1,.hero-desc,.hero-actions,.hero-stats'
  );
  // Set initial state synchronously before paint
  els.forEach(el => {
    el.style.cssText += ';opacity:0;transform:translateY(14px);';
  });
  // Animate on next frame — single rAF avoids the double-frame flash
  requestAnimationFrame(() => {
    els.forEach((el, i) => {
      el.style.transition = `opacity 0.65s ${EASE}, transform 0.65s ${EASE}`;
      el.style.transitionDelay = (80 + i * 90) + 'ms';
      el.style.opacity = '1';
      el.style.transform = 'none';
    });
  });
})();

// ─── FORM VALIDATION (per-field on blur) ──────────────────────────
(function () {
  const form = document.getElementById('contact-form');
  if (!form) return;

  function validateField(input) {
    const group = input.closest('.form-group');
    if (!group) return true;
    if (input.hasAttribute('required') && !input.value.trim()) {
      group.classList.add('field-error');
      group.classList.remove('field-success');
      let msg = group.querySelector('.field-error-msg');
      if (!msg) {
        msg = document.createElement('p');
        msg.className = 'field-error-msg';
        group.appendChild(msg);
      }
      msg.textContent = 'This field is required';
      return false;
    }
    if (input.type === 'email' && input.value.trim() && !/^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(input.value)) {
      group.classList.add('field-error');
      let msg = group.querySelector('.field-error-msg');
      if (!msg) { msg = document.createElement('p'); msg.className = 'field-error-msg'; group.appendChild(msg); }
      msg.textContent = 'Please enter a valid email address';
      return false;
    }
    group.classList.remove('field-error');
    group.classList.add('field-success');
    const msg = group.querySelector('.field-error-msg');
    if (msg) msg.remove();
    return true;
  }

  form.querySelectorAll('input, select, textarea').forEach(field => {
    field.addEventListener('blur', () => validateField(field));
    field.addEventListener('input', () => {
      if (field.closest('.form-group').classList.contains('field-error')) validateField(field);
    });
  });

  // Intercept submit to show spinner and validate all fields
  const origSubmit = form.onsubmit;
  form.addEventListener('submit', function(e) {
    const fields = form.querySelectorAll('input[required], select[required], textarea[required]');
    let valid = true;
    fields.forEach(f => { if (!validateField(f)) valid = false; });
    if (!valid) { e.preventDefault(); e.stopImmediatePropagation(); return; }
    const btn = document.getElementById('form-submit');
    if (btn) btn.classList.add('btn-loading');
  }, true);
})();


// ─── PERF MARK ────────────────────────────────────────────────────
if (window.performance?.mark) window.performance.mark('app_ready');
