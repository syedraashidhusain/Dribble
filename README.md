# Project Responsive Web Design using Bootstrap
## Date:

## AIM:
To create a simplified clone of Dribbble (https://dribbble.com/) landing page.


## DESIGN STEPS:

### Step 1:
Clone the repository from GitHub.

### Step 2:
Create Django Admin project.

### Step 3:
Create a New App under the Django Admin project.

### Step 4:
Insert the necessary CSS and JavaScript files as external in order to use Bootstrap.

### Step 5:
Create a HTML file and include the needed Bootstrap components.

### Step 6:
Publish the website in the LocalHost.

## PROGRAM :
```
<!doctype html>
<html lang="en">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <title>Shotboard Dribbble </title>

    <!-- Bootstrap 5 CDN -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/css/bootstrap.min.css" rel="stylesheet">

    <style>
      :root{--accent:#ea4c89;--muted:#6c757d}
      body{font-family:Inter, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;}
      .brand{font-weight:700;color:var(--accent)}
      .hero{background:linear-gradient(180deg, rgba(234,76,137,0.06), rgba(255,255,255,0));padding:4.5rem 0}
      .shot-card{border-radius:0.75rem;overflow:hidden;box-shadow:0 8px 24px rgba(33,37,41,0.08)}
      .shot-card img{width:100%;height:200px;object-fit:cover}
      .avatar{width:36px;height:36px;border-radius:50%;object-fit:cover}
      .tag{background:#f8f9fa;border-radius:999px;padding:0.2rem 0.6rem;font-size:0.8rem;color:var(--muted)}
      footer{background:#0f1724;color:#e6eef8}
      @media(min-width:992px){.shot-card img{height:180px}}
    </style>
  </head>
  <body>

    <!-- NAVBAR -->
    <nav class="navbar navbar-expand-lg navbar-light bg-white border-bottom sticky-top">
      <div class="container">
        <a class="navbar-brand d-flex align-items-center gap-2" href="#">
          <svg width="34" height="34" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg"><circle cx="12" cy="12" r="10" fill="#ea4c89"/><path d="M8 12l2.5-3 3.5 4.5L16 9l3 4" stroke="#fff" stroke-width="0.8" stroke-linecap="round" stroke-linejoin="round"/></svg>
          <span class="brand">Shotboard</span>9kaqa,b
        </a>

        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navMenu">
          <span class="navbar-toggler-icon"></span>
        </button>

        <div class="collapse navbar-collapse" id="navMenu">
          <ul class="navbar-nav ms-auto align-items-lg-center">
            <li class="nav-item"><a class="nav-link" href="#">Explore</a></li>
            <li class="nav-item"><a class="nav-link" href="#">Jobs</a></li>
            <li class="nav-item"><a class="nav-link" href="#">Hire</a></li>
            <li class="nav-item d-none d-lg-block"><a class="nav-link" href="#">Community</a></li>
            <li class="nav-item ms-3">
              <a class="btn btn-outline-primary btn-sm me-2" href="#">Sign in</a>
              <a class="btn btn-primary btn-sm" href="#">Sign up</a>
            </li>
          </ul>
        </div>
      </div>
    </nav>

    <!-- HERO -->
    <header class="hero">
      <div class="container">
        <div class="row align-items-center">
          <div class="col-lg-7">
            <h1 class="display-6 fw-bold mb-3">Discover &amp; showcase creative work</h1>
            <p class="lead text-muted mb-4">A small Dribbble‑style landing showcasing shots, creators, and curated collections. Built with Bootstrap for responsiveness.</p>

            <form class="row g-2 g-sm-3 align-items-center">
              <div class="col-sm-7 col-12">
                <div class="form-floating">
                  <input class="form-control" id="search" placeholder="Search shots, designers...">
                  <label for="search">Search shots, designers...</label>
                </div>
              </div>
              <div class="col-sm-3 col-6">
                <select class="form-select" aria-label="Sort">
                  <option selected>Popular</option>
                  <option>Recent</option>
                  <option>Following</option>
                </select>
              </div>
              <div class="col-sm-2 col-6 d-grid">
                <button class="btn btn-dark">Search</button>
              </div>
            </form>

            <div class="mt-4 d-flex flex-wrap gap-2">
              <span class="tag">Design</span>
              <span class="tag">Branding</span>
              <span class="tag">UI/UX</span>
              <span class="tag">Illustration</span>
            </div>

          </div>

          <div class="col-lg-5 d-none d-lg-block">
            <div class="row g-3">
              <div class="col-6">
                <div class="shot-card">
                  <img src="https://picsum.photos/seed/p1/600/400" alt="shot">
                </div>
              </div>
              <div class="col-6">
                <div class="shot-card mb-3">
                  <img src="https://picsum.photos/seed/p2/600/400" alt="shot">
                </div>
                <div class="shot-card">
                  <img src="https://picsum.photos/seed/p3/600/400" alt="shot">
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </header>

    <!-- FEATURED SHOTS -->
    <section class="py-5">
      <div class="container">
        <div class="d-flex justify-content-between align-items-center mb-4">
          <h3 class="h5 mb-0">Featured shots</h3>
          <a href="#" class="text-decoration-none">View all →</a>
        </div>

        <div class="row g-4">
          <!-- repeatable card -->
          <div class="col-sm-6 col-md-4 col-lg-3">
            <div class="card shot-card">
              <img src="https://picsum.photos/seed/s1/800/600" class="card-img-top" alt="...">
              <div class="card-body">
                <h6 class="card-title mb-1">Coffee &amp; UI exploration</h6>
                <p class="text-muted small mb-2">By <img src="https://picsum.photos/seed/a1/64/64" class="avatar me-2"> Alex</p>
                <div class="d-flex justify-content-between align-items-center">
                  <small class="text-muted">240 likes</small>
                  <div>
                    <a class="btn btn-sm btn-outline-secondary" href="#">Save</a>
                  </div>
                </div>
              </div>
            </div>
          </div>

          <div class="col-sm-6 col-md-4 col-lg-3">
            <div class="card shot-card">
              <img src="https://picsum.photos/seed/s2/800/600" class="card-img-top" alt="...">
              <div class="card-body">
                <h6 class="card-title mb-1">Onboarding screens</h6>
                <p class="text-muted small mb-2">By <img src="https://picsum.photos/seed/a2/64/64" class="avatar me-2"> Mika</p>
                <div class="d-flex justify-content-between align-items-center">
                  <small class="text-muted">128 likes</small>
                  <a class="btn btn-sm btn-outline-secondary" href="#">Save</a>
                </div>
              </div>
            </div>
          </div>

          <div class="col-sm-6 col-md-4 col-lg-3">
            <div class="card shot-card">
              <img src="https://picsum.photos/seed/s3/800/600" class="card-img-top" alt="...">
              <div class="card-body">
                <h6 class="card-title mb-1">Illustration pack</h6>
                <p class="text-muted small mb-2">By <img src="https://picsum.photos/seed/a3/64/64" class="avatar me-2"> Leila</p>
                <div class="d-flex justify-content-between align-items-center">
                  <small class="text-muted">96 likes</small>
                  <a class="btn btn-sm btn-outline-secondary" href="#">Save</a>
                </div>
              </div>
            </div>
          </div>

          <div class="col-sm-6 col-md-4 col-lg-3">
            <div class="card shot-card">
              <img src="https://picsum.photos/seed/s4/800/600" class="card-img-top" alt="...">
              <div class="card-body">
                <h6 class="card-title mb-1">Landing hero concept</h6>
                <p class="text-muted small mb-2">By <img src="https://picsum.photos/seed/a4/64/64" class="avatar me-2"> Rohit</p>
                <div class="d-flex justify-content-between align-items-center">
                  <small class="text-muted">410 likes</small>
                  <a class="btn btn-sm btn-outline-secondary" href="#">Save</a>
                </div>
              </div>
            </div>
          </div>

        </div>

      </div>
    </section>

    <!-- CURATED COLLECTIONS -->
    <section class="py-4 bg-light">
      <div class="container">
        <div class="d-flex justify-content-between align-items-center mb-3">
          <h3 class="h6 mb-0">Curated collections</h3>
          <a href="#" class="text-decoration-none">Explore →</a>
        </div>

        <div class="row g-3">
          <div class="col-md-4">
            <div class="p-3 bg-white rounded-3 d-flex gap-3 align-items-center">
              <img src="https://picsum.photos/seed/c1/120/80" style="width:120px;height:80px;object-fit:cover;border-radius:8px;">
              <div>
                <h6 class="mb-1">Mobile UI Kits</h6>
                <small class="text-muted">120 items</small>
              </div>
            </div>
          </div>

          <div class="col-md-4">
            <div class="p-3 bg-white rounded-3 d-flex gap-3 align-items-center">
              <img src="https://picsum.photos/seed/c2/120/80" style="width:120px;height:80px;object-fit:cover;border-radius:8px;">
              <div>
                <h6 class="mb-1">Illustrations</h6>
                <small class="text-muted">84 items</small>
              </div>
            </div>
          </div>

          <div class="col-md-4">
            <div class="p-3 bg-white rounded-3 d-flex gap-3 align-items-center">
              <img src="https://picsum.photos/seed/c3/120/80" style="width:120px;height:80px;object-fit:cover;border-radius:8px;">
              <div>
                <h6 class="mb-1">Branding</h6>
                <small class="text-muted">62 items</small>
              </div>
            </div>
          </div>
        </div>

      </div>
    </section>

    <!-- FOOTER -->
    <footer class="pt-5 pb-4 mt-5">
      <div class="container">
        <div class="row">
          <div class="col-md-4 mb-3">
            <h5 class="mb-3">Shotboard</h5>
            <p class="small text-muted">Showcase your work, discover new design ideas, and connect with other creators.</p>
          </div>

          <div class="col-6 col-md-2 mb-3">
            <h6>Product</h6>
            <ul class="list-unstyled small">
              <li><a class="text-decoration-none text-muted" href="#">Explore</a></li>
              <li><a class="text-decoration-none text-muted" href="#">Team</a></li>
              <li><a class="text-decoration-none text-muted" href="#">API</a></li>
            </ul>
          </div>

          <div class="col-6 col-md-2 mb-3">
            <h6>Company</h6>
            <ul class="list-unstyled small">
              <li><a class="text-decoration-none text-muted" href="#">About</a></li>
              <li><a class="text-decoration-none text-muted" href="#">Careers</a></li>
              <li><a class="text-decoration-none text-muted" href="#">Press</a></li>
            </ul>
          </div>

          <div class="col-md-4">
            <h6>Subscribe</h6>
            <form class="row g-2">
              <div class="col-8">
                <input class="form-control form-control-sm" placeholder="Email address">
              </div>
              <div class="col-4 d-grid">
                <button class="btn btn-sm btn-outline-light">Subscribe</button>
              </div>
            </form>
            <p class="small text-muted mt-3">© <span id="year"></span> Shotboard — Built with Bootstrap</p>
          </div>
        </div>
      </div>
    </footer>

    <script>
      // small helpers
      document.getElementById('year').textContent = new Date().getFullYear();
    </script>

    <!-- Bootstrap JS -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.2/dist/js/bootstrap.bundle.min.js"></script>
  </body>
</html>
```
## OUTPUT:
<img width="1002" height="589" alt="image" src="https://github.com/user-attachments/assets/d68f3ffd-b2cb-4ceb-8ac5-a7356175405a" />


## RESULT:
The Project for responsive web design using Bootstrap is completed successfully.
