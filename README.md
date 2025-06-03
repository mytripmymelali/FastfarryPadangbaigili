<!DOCTYPE html>
<html lang="id">
<head>
    <!-- ... (kode head sama seperti sebelumnya) ... -->
</head>
<body>
    <!-- ... (kode header sama seperti sebelumnya) ... -->

    <!-- Bagian yang sesuai dengan gambar -->
    <section class="repository-section">
        <div class="container">
            <div class="repo-header">
                <h2><i class="fab fa-github"></i> gethub.com/mytri</h2>
                <p>perjalananku... / FastfarryPad...</p>
            </div>
            
            <div class="repo-content">
                <div class="repo-title">
                    <h3>FastfarryPadangbaigili /</h3>
                    <p>README.md</p>
                    <span>di dalam utama</span>
                </div>
                
                <div class="repo-actions">
                    <button class="repo-btn" id="cancel-btn">Batalkan perubahan</button>
                    <button class="repo-btn primary" id="commit-btn">Komit perubahan...</button>
                </div>
                
                <div class="repo-editor">
                    <div class="editor-tabs">
                        <button class="tab-btn active">Sunting</button>
                        <button class="tab-btn">Pratinjau</button>
                    </div>
                    
                    <div class="editor-meta">
                        <span>Ruang <span id="space-count">2</span></span>
                    </div>
                    
                    <div class="editor-content">
                        <div class="editor-empty-state">
                            <p>Tidak ada b ⭐</p>
                            <p>1 Enter file contents here</p>
                        </div>
                        
                        <div class="editor-instructions">
                            <p>Gunakan Control + Shift + m untuk mengubah</p>
                            <p>tab fokus tombol yang sedang bergerak. Atau,</p>
                            <p>gunakan esc then tab untuk berpindah ke elemen</p>
                        </div>
                        
                        <div class="file-attachment">
                            <p>Lampirkan file dengan cara menyeret & melepas, memilih atau menempelkannya.</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- ... (bagian website lainnya tetap sama) ... -->

    <style>
        /* Gaya tambahan untuk bagian repository */
        .repository-section {
            padding: 60px 0;
            background-color: #f8f9fa;
            border-top: 1px solid #eaeaea;
            border-bottom: 1px solid #eaeaea;
        }
        
        .repo-header {
            background-color: #0d1117;
            color: white;
            padding: 15px 20px;
            border-radius: 6px 6px 0 0;
            margin-bottom: 1px;
        }
        
        .repo-header h2 {
            font-size: 1.2rem;
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .repo-header p {
            font-size: 0.9rem;
            color: #8b949e;
            margin-top: 5px;
        }
        
        .repo-content {
            background: white;
            border-radius: 0 0 6px 6px;
            box-shadow: 0 1px 3px rgba(0,0,0,0.1);
            overflow: hidden;
        }
        
        .repo-title {
            padding: 15px 20px;
            border-bottom: 1px solid #eaeaea;
            display: flex;
            align-items: center;
            gap: 8px;
            font-size: 0.95rem;
        }
        
        .repo-title h3 {
            font-weight: 600;
            color: #24292f;
        }
        
        .repo-title p {
            color: #24292f;
        }
        
        .repo-title span {
            color: #57606a;
        }
        
        .repo-actions {
            padding: 15px 20px;
            background: #f6f8fa;
            border-bottom: 1px solid #eaeaea;
            display: flex;
            gap: 10px;
        }
        
        .repo-btn {
            padding: 5px 15px;
            border: 1px solid #d0d7de;
            border-radius: 6px;
            background: white;
            font-size: 0.9rem;
            cursor: pointer;
            transition: all 0.2s;
        }
        
        .repo-btn.primary {
            background: #2da44e;
            color: white;
            border-color: #2da44e;
            font-weight: 500;
        }
        
        .repo-btn:hover {
            background: #f3f4f6;
        }
        
        .repo-btn.primary:hover {
            background: #2c974b;
        }
        
        .editor-tabs {
            display: flex;
            border-bottom: 1px solid #eaeaea;
            padding: 0 20px;
        }
        
        .tab-btn {
            padding: 8px 16px;
            background: transparent;
            border: none;
            cursor: pointer;
            font-size: 0.9rem;
            color: #57606a;
            position: relative;
        }
        
        .tab-btn.active {
            color: #24292f;
            font-weight: 600;
        }
        
        .tab-btn.active::after {
            content: '';
            position: absolute;
            bottom: -1px;
            left: 0;
            width: 100%;
            height: 2px;
            background: #fd8c73;
        }
        
        .editor-meta {
            padding: 5px 20px;
            background: #f6f8fa;
            border-bottom: 1px solid #eaeaea;
            text-align: right;
            font-size: 0.8rem;
            color: #57606a;
        }
        
        .editor-content {
            padding: 20px;
            min-height: 300px;
            font-family: 'SFMono-Regular', Consolas, 'Liberation Mono', Menlo, monospace;
            font-size: 0.9rem;
            color: #24292f;
            line-height: 1.6;
        }
        
        .editor-empty-state {
            background: #f6f8fa;
            border: 1px dashed #d0d7de;
            border-radius: 6px;
            padding: 20px;
            text-align: center;
            margin-bottom: 20px;
            color: #57606a;
        }
        
        .editor-instructions {
            background: #fff8c5;
            border: 1px solid #e0c000;
            border-radius: 6px;
            padding: 15px;
            margin-bottom: 20px;
            font-size: 0.85rem;
        }
        
        .file-attachment {
            background: #ddf4ff;
            border: 1px dashed #54aeff;
            border-radius: 6px;
            padding: 15px;
            text-align: center;
            color: #0550ae;
        }
    </style>

    <script>
        // ... (kode JavaScript sebelumnya tetap sama) ...
        
        // Tambahan fungsi untuk bagian repo
        document.querySelectorAll('.tab-btn').forEach(btn => {
            btn.addEventListener('click', function() {
                document.querySelectorAll('.tab-btn').forEach(b => b.classList.remove('active'));
                this.classList.add('active');
            });
        });
    </script>
</body>
</html>
