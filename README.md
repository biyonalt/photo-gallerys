<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Responsive photo gallery with hover effects">
    <title>Modern Photo Gallery</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            padding: 40px 20px;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
        }

        h1 {
            text-align: center;
            color: white;
            margin-bottom: 40px;
            font-size: 2.5rem;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
        }

        .gallery {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 20px;
            perspective: 1000px;
        }

        .gallery-item {
            position: relative;
            overflow: hidden;
            border-radius: 12px;
            box-shadow: 0 8px 16px rgba(0,0,0,0.2);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            aspect-ratio: 1;
        }

        .gallery-item:hover {
            transform: translateY(-8px);
            box-shadow: 0 12px 24px rgba(0,0,0,0.3);
        }

        .gallery-item img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.4s ease;
        }

        .gallery-item:hover img {
            transform: scale(1.05);
        }

        .overlay {
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: rgba(0,0,0,0.5);
            display: flex;
            align-items: center;
            justify-content: center;
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        .gallery-item:hover .overlay {
            opacity: 1;
        }

        .overlay-text {
            color: white;
            font-size: 1.2rem;
            font-weight: 600;
            text-shadow: 1px 1px 2px rgba(0,0,0,0.5);
        }

        @media (max-width: 768px) {
            h1 {
                font-size: 2rem;
            }

            .gallery {
                grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
                gap: 15px;
            }
        }

        @media (max-width: 480px) {
            body {
                padding: 20px 10px;
            }

            h1 {
                font-size: 1.5rem;
                margin-bottom: 25px;
            }

            .gallery {
                grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
                gap: 10px;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>🎨 Modern Photo Gallery</h1>
        <div class="gallery">
            <div class="gallery-item">
                <img src="https://images.unsplash.com/photo-1506794778202-cad84cf45f1d?w=400&h=400&fit=crop" alt="Gallery image 1">
                <div class="overlay">
                    <span class="overlay-text">Photography</span>
                </div>
            </div>
            <div class="gallery-item">
                <img src="https://images.unsplash.com/photo-1517694712202-14dd9538aa97?w=400&h=400&fit=crop" alt="Gallery image 2">
                <div class="overlay">
                    <span class="overlay-text">Design</span>
                </div>
            </div>
            <div class="gallery-item">
                <img src="https://images.unsplash.com/photo-1506157786151-b8491531f063?w=400&h=400&fit=crop" alt="Gallery image 3">
                <div class="overlay">
                    <span class="overlay-text">Nature</span>
                </div>
            </div>
            <div class="gallery-item">
                <img src="https://images.unsplash.com/photo-1506794778202-cad84cf45f1d?w=400&h=400&fit=crop" alt="Gallery image 4">
                <div class="overlay">
                    <span class="overlay-text">Lifestyle</span>
                </div>
            </div>
            <div class="gallery-item">
                <img src="https://images.unsplash.com/photo-1517694712202-14dd9538aa97?w=400&h=400&fit=crop" alt="Gallery image 5">
                <div class="overlay">
                    <span class="overlay-text">Travel</span>
                </div>
            </div>
            <div class="gallery-item">
                <img src="https://images.unsplash.com/photo-1506157786151-b8491531f063?w=400&h=400&fit=crop" alt="Gallery image 6">
                <div class="overlay">
                    <span class="overlay-text">Adventure</span>
                </div>
            </div>
        </div>
    </div>
</body>
</html>
