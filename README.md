# Dashboard-Digitalisasi-Klaim-PT-JAMKRINDO
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dashboard Digitalisasi Klaim PT JAMKRINDO</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css" rel="stylesheet"/>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;500;700&display=swap" rel="stylesheet"/>
</head>
<body class="font-roboto bg-gray-900 text-white">
    <div class="p-4 grid grid-cols-1 lg:grid-cols-2 gap-4">
        <!-- Header Section -->
        <div class="col-span-1 lg:col-span-2 mb-4">
            <div class="flex items-center justify-between bg-blue-600 text-white p-4 rounded-lg shadow-md">
                <h1 class="text-xl font-bold">Dashboard Digitalisasi Klaim PT JAMKRINDO</h1>
                <div class="flex space-x-4">
                    <a class="hover:text-gray-300" href="#"><i class="fas fa-home"></i> Home</a>
                    <a class="hover:text-gray-300" href="#"><i class="fas fa-info-circle"></i> About</a>
                    <a class="hover:text-gray-300" href="#"><i class="fas fa-concierge-bell"></i> Services</a>
                    <a class="hover:text-gray-300" href="#"><i class="fas fa-envelope"></i> Contact</a>
                </div>
            </div>
        </div>
        
        <!-- Welcome Section -->
        <div class="col-span-1 lg:col-span-2 mb-4 text-center">
            <h2 class="text-2xl font-bold">Welcome to the Klaim Dashboard</h2>
            <p class="text-md text-gray-300">Monitor and analyze your claim data effectively.</p>
        </div>
        
        <!-- Filter Section -->
        <div class="bg-gray-800 shadow-md rounded-lg p-4 col-span-1 lg:col-span-2">
            <div class="mb-4 flex items-center">
                <i class="fas fa-filter text-blue-500 text-xl mr-2"></i>
                <h2 class="text-md font-semibold">Filter Data</h2>
            </div>
            <div class="grid grid-cols-1 md:grid-cols-3 gap-4">
                <div>
                    <label class="block text-sm font-medium text-gray-300" for="kanwil">Kanwil</label>
                    <select class="mt-1 block w-full py-2 px-3 border border-gray-600 bg-gray-700 text-white rounded-md shadow-sm focus:outline-none focus:ring-blue-500 focus:border-blue-500 sm:text-sm" id="kanwil">
                        <option>Semua Kanwil</option>
                        <option>Kanwil 1</option>
                        <option>Kanwil 2</option>
                        <option>Kanwil 3</option>
                        <option>Kanwil 4</option>
                        <option>Kanwil 5</option>
                    </select>
                </div>
                <div>
                    <label class="block text-sm font-medium text-gray-300" for="periode">Periode Waktu</label>
                    <input class="mt-1 block w-full py-2 px-3 border border-gray-600 bg-gray-700 text-white rounded-md shadow-sm focus:outline-none focus:ring-blue-500 focus:border-blue-500 sm:text-sm" id="periode" type="date"/>
                </div>
                <div>
                    <label class="block text-sm font-medium text-gray-300" for="status">Status Klaim</label>
                    <select class="mt-1 block w-full py-2 px-3 border border-gray-600 bg-gray-700 text-white rounded-md shadow-sm focus:outline-none focus:ring-blue-500 focus:border-blue-500 sm:text-sm" id="status">
                        <option>Semua Status</option>
                        <option>Diproses</option>
                        <option>Disetujui</option>
                        <option>Ditolak</option>
                    </select>
                </div>
                <div>
                    <label class="block text-sm font-medium text-gray-300" for="tipe-klaim">Tipe Klaim</label>
                    <select class="mt-1 block w-full py-2 px-3 border border-gray-600 bg-gray-700 text-white rounded-md shadow-sm focus:outline-none focus:ring-blue-500 focus:border-blue-500 sm:text-sm" id="tipe-klaim">
                        <option>Semua Tipe</option>
                        <option>Klaim Kredit Usaha Rakyat (KUR)</option>
                        <option>Klaim Asuransi</option>
                    </select>
                </div>
                <div>
                    <label class="block text-sm font-medium text-gray-300" for="nominal">Nominal Klaim</label>
                    <input class="mt-1 block w-full py-2 px-3 border border-gray-600 bg-gray-700 text-white rounded-md shadow-sm focus:outline-none focus:ring-blue-500 focus:border-blue-500 sm:text-sm" id="nominal" type="number" placeholder="Min"/>
                    <input class="mt-1 block w-full py-2 px-3 border border-gray-600 bg-gray-700 text-white rounded-md shadow-sm focus:outline-none focus:ring-blue-500 focus:border-blue-500 sm:text-sm" id="nominal" type="number" placeholder="Max"/>
                </div>
                <div>
                    <label class="block text-sm font-medium text-gray-300" for="kategori-risiko">Kategori Risiko</label>
                    <select class="mt-1 block w-full py-2 px-3 border border-gray-600 bg-gray-700 text-white rounded-md shadow-sm focus:outline-none focus:ring-blue-500 focus:border-blue-500 sm:text-sm" id="kategori-risiko">
                        <option>Semua Risiko</option>
                        <option>Rendah</option>
                        <option>Sedang</option>
                        <option>Tinggi</option>
                    </select>
                </div>
            </div>
        </div>
        
        <!-- KPI, Distribusi Klaim, Export Data Section -->
        <div class="col-span-1 lg:col-span-2 grid grid-cols-1 lg:grid-cols-3 gap-4">
            <!-- KPI Section -->
            <div class="bg-gray-800 shadow-md rounded-lg p-4">
                <div class="mb-4 flex items-center">
                    <i class="fas fa-chart-line text-blue-500 text-xl mr-2"></i>
                    <h2 class="text-md font-semibold">Ringkasan KPI</h2>
                </div>
                <div class="flex justify-between">
                    <div class="text-center">
                        <h3 class="text-sm text-gray-300">Klaim Diproses</h3>
                        <p class="text-xl font-bold text-blue-500">720</p>
                    </div>
                    <div class="text-center">
                        <h3 class="text-sm text-gray-300">Rata-rata Penyelesaian (Hari)</h3>
                        <p class="text-xl font-bold text-green-500">14</p>
                    </div>
                    <div class="text-center">
                        <h3 class="text-sm text-gray-300">SLA Terlampaui</h3>
                        <p class="text-xl font-bold text-red-500">12%</p>
                    </div>
                </div>
            </div>
            <!-- Bar Chart Section -->
            <div class="bg-gray-800 shadow-md rounded-lg p-4">
                <div class="mb-4 flex items-center">
                    <i class="fas fa-chart-bar text-green-500 text-xl mr-2"></i>
                    <h2 class="text-md font-semibold">Distribusi Klaim per Kanwil</h2>
                </div>
                <div class="h-48">
                    <canvas id="barChart"></canvas>
                </div>
            </div>
            <!-- Export Data Section -->
            <div class="bg-gray-800 shadow-md rounded-lg p-4">
                <div class="mb-4 flex items-center">
                    <i class="fas fa-file-export text-green-500 text-xl mr-2"></i>
                    <h2 class="text-md font-semibold">Export Data</h2>
                </div>
                <div class="flex space-x-4">
                    <button class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">Export to Excel</button>
                    <button class="bg-red-500 hover:bg-red-700 text-white font-bold py-2 px-4 rounded">Export to PDF</button>
                    <button class="bg-green-500 hover:bg-green-700 text-white font-bold py-2 px-4 rounded">Export to CSV</button>
                    <button class="bg-yellow-500 hover:bg-yellow-700 text-white font-bold py-2 px-4 rounded">Export to Google Sheets</button>
                </div>
            </div>
        </div>
        
        <!-- Trend, Breakdown, SLA Trend Chart Section -->
        <div class="col-span-1 lg:col-span-2 grid grid-cols-1 lg:grid-cols-3 gap-4">
            <!-- Trend Chart Section -->
            <div class="bg-gray-800 shadow-md rounded-lg p-4">
                <div class="mb-4 flex items-center">
                    <i class="fas fa-chart-line text-blue-500 text-xl mr-2"></i>
                    <h2 class="text-md font-semibold">Tren Penyelesaian Klaim per Bulan</h2>
                </div>
                <div class="h-48">
                    <canvas id="trendChart"></canvas>
                </div>
            </div>
            <!-- Breakdown Chart Section -->
            <div class="bg-gray-800 shadow-md rounded-lg p-4">
                <div class="mb-4 flex items-center">
                    <i class="fas fa-chart-pie text-purple-500 text-xl mr-2"></i>
                    <h2 class="text-md font-semibold">Breakdown Klaim Berdasarkan Jenis Penyebab Ditolak</h2>
                </div>
                <div class="h-48">
                    <canvas id="breakdownChart"></canvas>
                </div>
            </div>
            <!-- SLA Trend Chart Section -->
            <div class="bg-gray-800 shadow-md rounded-lg p-4">
                <div class="mb-4 flex items-center">
                    <i class="fas fa-chart-line text-red-500 text-xl mr-2"></i>
                    <h2 class="text-md font-semibold">Tren SLA Terlampaui per Bulan</h2>
                </div>
                <div class="h-48">
                    <canvas id="slaTrendChart"></canvas>
                </div>
            </div>
        </div>
        
        <!-- Real-Time Monitoring Table -->
        <div class="bg-gray-800 shadow-md rounded-lg p-4 col-span-1 lg:col-span-2">
            <div class="mb-4 flex items-center">
                <i class="fas fa-table text-yellow-500 text-xl mr-2"></i>
                <h2 class="text-md font-semibold">Tabel Monitoring Real-Time</h2>
            </div>
            <div class="overflow-x-auto">
                <table class="min-w-full bg-gray-800 text-white">
                    <thead class="bg-gray-700">
                        <tr>
                            <th class="py-2 px-4">Kanwil</th>
                            <th class="py-2 px-4">Status Klaim</th>
                            <th class="py-2 px-4">SLA</th>
                            <th class="py-2 px-4">Durasi Penyelesaian</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr class="border-b border-gray-700">
                            <td class="py-2 px-4">Kanwil 1</td>
                            <td class="py-2 px-4">Diproses</td>
                            <td class="py-2 px-4 text-green-500">On-Time</td>
                            <td class="py-2 px-4">12 Hari</td>
                        </tr>
                        <tr class="border-b border-gray-700">
                            <td class="py-2 px-4">Kanwil 2</td>
                            <td class="py-2 px-4">Disetujui</td>
                            <td class="py-2 px-4 text-yellow-500">Mendekati Deadline</td>
                            <td class="py-2 px-4">14 Hari</td>
                        </tr>
                        <tr class="border-b border-gray-700">
                            <td class="py-2 px-4">Kanwil 3</td>
                            <td class="py-2 px-4">Ditolak</td>
                            <td class="py-2 px-4 text-red-500">Terlampaui</td>
                            <td class="py-2 px-4">18 Hari</td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </div>
    </div>
    
    <!-- Notification Section -->
    <div class="fixed bottom-4 right-4 bg-red-500 text-white p-4 rounded-lg shadow-lg">
        <div class="flex items-center">
            <i class="fas fa-exclamation-triangle text-2xl mr-2"></i>
            <div>
                <h3 class="font-semibold">Peringatan SLA</h3>
                <p>Ada klaim yang mendekati atau sudah terlampaui batas SLA!</p>
            </div>
        </div>
    </div>
    
    <script>
        const barChartData = {
            labels: ["Kanwil 1", "Kanwil 2", "Kanwil 3", "Kanwil 4", "Kanwil 5"],
            datasets: [
                {
                    label: "Klaim Disetujui",
                    data: [120, 150, 100, 180, 90],
                    backgroundColor: "rgba(75, 192, 192, 0.6)",
                },
                {
                    label: "Klaim Ditolak",
                    data: [30, 50, 20, 40, 60],
                    backgroundColor: "rgba(255, 99, 132, 0.6)",
                },
            ],
        };

        const trendChartData = {
            labels: ["Jan", "Feb", "Mar", "Apr", "May", "Jun"],
            datasets: [
                {
                    label: "Rata-rata Penyelesaian Klaim (Hari)",
                    data: [15, 14, 13, 16, 14, 12],
                    borderColor: "rgba(75, 192, 192, 1)",
                    backgroundColor: "rgba(75, 192, 192, 0.2)",
                    fill: true,
                },
            ],
        };

        const breakdownChartData = {
            labels: ["Dokumen Tidak Lengkap", "Tidak Sesuai Kriteria", "Lainnya"],
            datasets: [
                {
                    data: [40, 30, 30],
                    backgroundColor: ["rgba(255, 99, 132, 0.6)", "rgba(54, 162, 235, 0.6)", "rgba(255, 206, 86, 0.6)"],
                },
            ],
        };

        const slaTrendChartData = {
            labels: ["Jan", "Feb", "Mar", "Apr", "May", "Jun"],
            datasets: [
                {
                    label: "SLA Terlampaui",
                    data: [5, 8, 6, 10, 7, 9],
                    borderColor: "rgba(255, 99, 132, 1)",
                    backgroundColor: "rgba(255, 99, 132, 0.2)",
                    fill: true,
                },
            ],
        };

        window.onload = function() {
            const barCtx = document.getElementById('barChart').getContext('2d');
            new Chart(barCtx, {
                type: 'bar',
                data: barChartData,
                options: {
                    responsive: true,
                    scales: {
                        y: {
                            beginAtZero: true
                        }
                    }
                }
            });

            const trendCtx = document.getElementById('trendChart').getContext('2d');
            new Chart(trendCtx, {
                type: 'line',
                data: trendChartData,
                options: {
                    responsive: true,
                    scales: {
                        y: {
                            beginAtZero: true
                        }
                    }
                }
            });

            const breakdownCtx = document.getElementById('breakdownChart').getContext('2d');
            new Chart(breakdownCtx, {
                type: 'pie',
                data: breakdownChartData,
                options: {
                    responsive: true,
                }
            });

            const slaTrendCtx = document.getElementById('slaTrendChart').getContext('2d');
            new Chart(slaTrendCtx, {
                type: 'line',
                data: slaTrendChartData,
                options: {
                    responsive: true,
                    scales: {
                        y: {
                            beginAtZero: true
                        }
                    }
                }
            });
        };
    </script>
</body>
</html>
