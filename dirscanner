<?php

function scan_dirs_clean($base = '.', $output_file = 'wp_dirs_clean.txt') {
    $result = [];

    // Normalisasi base path
    $base = rtrim(realpath($base), DIRECTORY_SEPARATOR);
    $baseLen = strlen($base) + 1;

    $rii = new RecursiveIteratorIterator(
        new RecursiveDirectoryIterator($base, FilesystemIterator::SKIP_DOTS),
        RecursiveIteratorIterator::SELF_FIRST
    );

    foreach ($rii as $file) {
        if ($file->isDir()) {
            // Ambil path relatif
            $relativePath = substr($file->getPathname(), $baseLen);
            $relativePath = str_replace('\\', '/', $relativePath);
            $result[] = $relativePath . '/';
        }
    }

    // Tambahkan folder utama (langsung di bawah base dir)
    $topLevel = glob($base . '/*', GLOB_ONLYDIR);
    foreach ($topLevel as $folder) {
        $relativeTop = str_replace($base . '/', '', $folder) . '/';
        if (!in_array($relativeTop, $result)) {
            $result[] = $relativeTop;
        }
    }

    // Urutkan hasil
    sort($result);

    // Simpan ke file
    file_put_contents($output_file, implode(PHP_EOL, $result));

    echo "✅ Direktori berhasil dipindai dan disimpan ke: $output_file\n";
}

// Jalankan scanner
scan_dirs_clean('.', 'wp_dirs_clean.txt');
