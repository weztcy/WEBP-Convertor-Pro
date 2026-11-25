# Portfolio Project Data — WEBP Convertor Pro

- **Category:** `desktop-mobile` (`Desktop App`)
- **Category Label:** `Desktop App`
- **Accent Color:** `amber`
- **Target Assets Folder:** `public/images/projects/webp_convertor_pro/`
- **Required Local Images:** `banner.webp`, `image01.webp` .. `image03.webp`

## TypeScript Data (`ProjectCaseStudy`)

```typescript
{
  "id": "webp-convertor-pro",
  "code": "PRO-54 // APP-08",
  "title": "WEBP Convertor Pro",
  "category": "desktop-mobile",
  "categoryLabel": "Desktop App",
  "year": "2025",
  "status": "Completed",
  "accentColor": "amber",
  "repoUrl": "https://github.com/weztcy/WEBP-Convertor-Pro",
  "license": "MIT License",
  "banner": "/images/projects/webp_convertor_pro/banner.webp",
  "summary": "High-speed local batch image-to-WEBP desktop converter with multiprocessing workers, PySide6 workspace, and real-time CPU/RAM telemetry.",
  "projectDescription": "WEBP Convertor Pro is a local-first Windows desktop application built with Python, PySide6, and Pillow for batch converting JPG, JPEG, and PNG images into WEBP. It scales across CPU logical threads via ProcessPoolExecutor and visualizes live CPU, RAM, and compression savings.",
  "architectureSummary": "PySide6 UI and QThread job orchestration dispatching Pillow WEBP encoding across hardware-scaled ProcessPoolExecutor workers with live psutil telemetry.",
  "techStack": [
    "Python",
    "PySide6",
    "Pillow",
    "PyQtGraph",
    "psutil",
    "qt-material",
    "PyInstaller"
  ],
  "telemetryMatrix": {
    "projectType": "Desktop Application",
    "targetPlatform": "Windows Desktop (x64)",
    "primaryDomain": "Batch Image Processing",
    "architecturePipeline": "PySide6 UI + ProcessPoolExecutor",
    "testingAndAudit": "Verified",
    "projectStatus": "Completed",
    "projectYear": "2025"
  },
  "desktopMobileProjectInfo": {
    "applicationType": "Native Desktop Utility",
    "targetPlatform": "Windows",
    "developmentStatus": "Completed",
    "developmentYear": "2025",
    "applicationCategory": "Batch Media & Image Optimization"
  },
  "desktopMobileBackground": "Web developers and designers frequently process hundreds of product or editorial images into WEBP, yet browser-based converters impose upload limits, privacy risks, and slow sequential throughput. WEBP Convertor Pro delivers a private offline desktop workspace that saturates multi-core CPUs locally.",
  "desktopMobileProblemStatements": [
    {
      "title": "Cloud Converter Latency and Privacy Exposure",
      "description": "Uploading large batches of unoptimized JPG and PNG assets to third-party web tools introduces network bottlenecks, file-count caps, and unnecessary exposure of client media.",
      "issueCode": "ISSUE_01"
    },
    {
      "title": "Single-Threaded Conversion Bottlenecks",
      "description": "Sequential Python or GUI-thread image encoding leaves modern multi-core processors underutilized and freezes desktop interfaces during bulk folder exports.",
      "issueCode": "ISSUE_02"
    },
    {
      "title": "Opaque Compression and Resource Feedback",
      "description": "Basic CLI scripts lack interactive thumbnail inspection, safe stale-preview guarding, and real-time visibility into worker utilization, encoding speed, and net storage savings.",
      "issueCode": "ISSUE_03"
    }
  ],
  "desktopMobileObjectives": [
    {
      "title": "Hardware-Adaptive Parallel Throughput",
      "description": "Automatically compute optimal worker counts from logical CPU threads and execute Pillow WEBP encoding across isolated worker processes without blocking the Qt event loop.",
      "targetTag": "TARGET_01"
    },
    {
      "title": "Responsive Large-Library Inspection",
      "description": "Scan directories asynchronously on a background QThread and cache MD5-keyed WebP thumbnails and previews locally to keep browsing smooth for thousand-image batches.",
      "targetTag": "TARGET_02"
    },
    {
      "title": "Transparent Execution Telemetry",
      "description": "Surface live CPU and RAM usage plots, active worker pool occupancy, per-file progress, and post-run space savings directly within the desktop workspace.",
      "targetTag": "TARGET_03"
    }
  ],
  "desktopMobileFeatures": [
    {
      "title": "Multi-Mode Asset Ingestion",
      "description": "Import single images, multiple files, drag-and-drop selections, or entire directory trees via asynchronous recursive scanning for JPG, JPEG, and PNG assets.",
      "badge": "INGESTION"
    },
    {
      "title": "Cached Image Library & Safe Preview",
      "description": "Browse thumbnails in a responsive grid with disk-cached 100px thumbnails and 400px previews protected against stale asynchronous loader overwrites.",
      "badge": "LIBRARY"
    },
    {
      "title": "Lossy, Lossless & Profile Tuning",
      "description": "Configure Lossy or Lossless compression, fine-tune quality from 1 to 100, normalize RGBA transparency, and select Fast, Standard Quality, or Maximum Compression profiles.",
      "badge": "ENCODING"
    },
    {
      "title": "Multiprocessing Worker Pool & Live Analytics",
      "description": "Execute selected or full-library batches across a ProcessPoolExecutor pool with cancellation support, PyQtGraph CPU/RAM charts, and output compression statistics.",
      "badge": "TELEMETRY"
    }
  ],
  "desktopMobileInterfaceShowcase": [
    {
      "imageUrl": "/images/projects/webp_convertor_pro/image01.webp"
    },
    {
      "imageUrl": "/images/projects/webp_convertor_pro/image02.webp"
    },
    {
      "imageUrl": "/images/projects/webp_convertor_pro/image03.webp"
    }
  ],
  "desktopMobileUserFlow": {
    "summary": "Users launch from the overview landing screen into a single-scroll Conversion Workspace where they import images, inspect cached previews, configure WEBP compression modes and output paths, execute batch jobs, and monitor live CPU, RAM, and compression analytics.",
    "steps": [
      {
        "step": "01",
        "title": "Enter Conversion Workspace",
        "description": "User clicks Start Converting on the HomePage, switching the QStackedWidget in MainWindow to the ConvertPage workspace.",
        "actorOrNode": "User / MainWindow"
      },
      {
        "step": "02",
        "title": "Import Images or Scan Folder",
        "description": "Files added via drag-and-drop or dialogs populate ImageLibrary; folder imports trigger an asynchronous ImageScanner QThread emitting ImageModel items.",
        "actorOrNode": "ImageLibrary / ImageScanner"
      },
      {
        "step": "03",
        "title": "Inspect Thumbnails & Configure Encoding",
        "description": "ThumbnailCache serves disk-cached WebP thumbnails and previews while the user selects Lossy or Lossless mode, quality slider, encoding profile, and output folder.",
        "actorOrNode": "ThumbnailCache / SettingsPanel"
      },
      {
        "step": "04",
        "title": "Run Parallel WEBP Batch & Review Metrics",
        "description": "ConversionService launches ConversionThread and ProcessPoolManager to encode images across worker processes while SystemMonitor and ConversionStats render live telemetry.",
        "actorOrNode": "ProcessPoolManager / SystemMonitor"
      }
    ]
  },
  "desktopMobileArchitecture": {
    "summary": "The application separates PySide6 UI widgets from Qt service coordinators and multiprocessing workers. ConversionService owns a ConversionThread that runs ProcessPoolManager across CPU-scaled processes while QTimer-driven SystemMonitor streams hardware telemetry to PyQtGraph charts.",
    "layers": [
      {
        "name": "Presentation Layer",
        "role": "Renders the dark-themed workspace, drag-and-drop import, thumbnail grid, settings controls, and live charts",
        "tech": "PySide6 & PyQtGraph",
        "components": ["MainWindow", "HomePage", "ConvertPage", "ImageSection", "PerformancePanel"]
      },
      {
        "name": "Service & Threading Layer",
        "role": "Coordinates image collection state, background folder scanning, and non-blocking conversion lifecycle signals",
        "tech": "PySide6 QObject & QThread",
        "components": ["ImageLibrary", "ImageScanner", "ConversionService", "ConversionThread", "SystemMonitor"]
      },
      {
        "name": "Multiprocessing & Encoding Core",
        "role": "Calculates hardware worker limits and runs isolated Pillow WEBP conversion tasks across CPU cores",
        "tech": "Python Multiprocessing & Pillow",
        "components": ["ProcessPoolManager", "PerformanceConfig", "process_single_image", "convert_image", "WEBP_PROFILES"]
      },
      {
        "name": "Local Cache & Output Storage",
        "role": "Maintains MD5-keyed thumbnail/preview WebP caches and writes converted WEBP assets to disk",
        "tech": "Local Filesystem & MD5 Hash",
        "components": ["ThumbnailCache", "create_output_path", "get_default_output"]
      }
    ]
  },
  "desktopMobileDataManagement": {
    "storageType": "Local Filesystem Directories & MD5 Disk Cache",
    "stateEngine": "PySide6 Qt Signals/Slots & ImageLibrary QObject Store",
    "offlineSyncStrategy": "100% Offline Local Execution Without Remote Sync",
    "cachingMechanism": "Two-Tier ThumbnailCache (In-Memory QPixmap Dictionary + Disk WebP Cache)"
  },
  "desktopMobilePlatformImplementation": [
    {
      "title": "Frozen Multiprocessing & PyInstaller Bundling",
      "description": "Calls multiprocessing.freeze_support() at entry in main.py and packages via WEBP-Converter.spec with explicit PIL WebP/JPEG/PNG hidden imports, QtWebEngine exclusions, UPX compression, and Windows VSVersionInfo metadata.",
      "badge": "PACKAGING"
    },
    {
      "title": "Hardware-Aware Process Pool Scaling",
      "description": "PerformanceConfig inspects os.cpu_count() and psutil physical/memory stats to allocate max(2, min(cpu_threads - 1, 32)) workers for ProcessPoolExecutor with cancel_futures teardown support.",
      "badge": "CONCURRENCY"
    },
    {
      "title": "Real-Time OS Resource Telemetry",
      "description": "SystemMonitor polls psutil.cpu_percent() and psutil.virtual_memory() on a 1000 ms QTimer and emits snapshots to rolling 60-point PyQtGraph ResourceChart widgets.",
      "badge": "TELEMETRY"
    }
  ],
  "desktopMobileTechSpecs": {
    "programmingLanguage": "Python",
    "framework": "PySide6",
    "localStorage": "Local Disk WebP Cache"
  },
  "desktopMobilePlatformSpecs": {
    "targetPlatform": "Windows Desktop",
    "packageFormat": "Standalone Windows Executable",
    "targetArchitecture": "64-bit x86 Architecture",
    "buildFootprint": "67.93 MB Executable"
  }
}
```
