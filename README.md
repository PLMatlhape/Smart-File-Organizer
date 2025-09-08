# Smart-File-Organizer
smart-file-organizer/
│
├── package.json                    # Project dependencies and scripts
├── package-lock.json               # Lock file for dependencies
├── electron-builder.yml            # Build configuration for packaging
├── tsconfig.json                   # TypeScript configuration
├── .gitignore                      # Git ignore rules
├── README.md                       # Project documentation
│
├── src/                            # Source code directory
│   ├── main/                       # Main process (Backend/Electron main)
│   │   ├── main.ts                 # Main Electron process entry point
│   │   ├── app.ts                  # Application initialization and setup
│   │   ├── window-manager.ts       # Window creation and management
│   │   ├── tray.ts                 # System tray functionality
│   │   ├── startup.ts              # Windows startup integration
│   │   │
│   │   ├── services/               # Core business logic services
│   │   │   ├── file-watcher.ts     # File monitoring service
│   │   │   ├── file-organizer.ts   # File sorting and moving logic
│   │   │   ├── config-manager.ts   # Configuration management
│   │   │   ├── permission-manager.ts # File system permissions
│   │   │   └── priority-handler.ts  # Priority assignment logic
│   │   │
│   │   ├── models/                 # Data models and interfaces
│   │   │   ├── config.ts           # Configuration interfaces
│   │   │   ├── file-rule.ts        # File organization rules
│   │   │   └── priority.ts         # Priority level definitions
│   │   │
│   │   └── utils/                  # Utility functions
│   │       ├── file-helpers.ts     # File operation utilities
│   │       ├── path-helpers.ts     # Path manipulation utilities
│   │       └── logger.ts           # Logging utilities
│   │
│   ├── renderer/                   # Frontend (UI) code
│   │   ├── windows/                # Different UI windows
│   │   │   ├── main/               # Main settings window
│   │   │   │   ├── index.html      # Main window HTML
│   │   │   │   ├── main.ts         # Main window TypeScript
│   │   │   │   └── main.css        # Main window styling
│   │   │   │
│   │   │   ├── setup/              # First-time setup window
│   │   │   │   ├── index.html      # Setup window HTML
│   │   │   │   ├── setup.ts        # Setup window logic
│   │   │   │   └── setup.css       # Setup window styling
│   │   │   │
│   │   │   ├── priority-selector/  # Priority selection popup
│   │   │   │   ├── index.html      # Priority popup HTML
│   │   │   │   ├── priority.ts     # Priority selection logic
│   │   │   │   └── priority.css    # Priority popup styling
│   │   │   │
│   │   │   └── settings/           # Settings/configuration window
│   │   │       ├── index.html      # Settings window HTML
│   │   │       ├── settings.ts     # Settings window logic
│   │   │       └── settings.css    # Settings window styling
│   │   │
│   │   ├── shared/                 # Shared frontend utilities
│   │   │   ├── ipc-renderer.ts     # IPC communication helpers
│   │   │   ├── ui-helpers.ts       # Common UI functions
│   │   │   └── constants.ts        # Frontend constants
│   │   │
│   │   └── assets/                 # Frontend assets
│   │       ├── icons/              # Application icons
│   │       │   ├── app-icon.png    # Main app icon
│   │       │   ├── tray-icon.png   # System tray icon
│   │       │   └── tray-icon@2x.png # High DPI tray icon
│   │       │
│   │       ├── styles/             # Global stylesheets
│   │       │   ├── global.css      # Global styles
│   │       │   └── variables.css   # CSS variables
│   │       │
│   │       └── sounds/             # Notification sounds
│   │           └── notification.wav # File detected sound
│   │
│   └── preload/                    # Preload scripts (Security bridge)
│       ├── main-preload.ts         # Main window preload
│       ├── setup-preload.ts        # Setup window preload
│       ├── priority-preload.ts     # Priority popup preload
│       └── settings-preload.ts     # Settings window preload
│
├── config/                         # Configuration files
│   ├── default-config.json         # Default application settings
│   ├── file-extensions.json        # Supported file extensions mapping
│   └── priority-presets.json       # Default priority level presets
│
├── resources/                      # Build resources
│   ├── icons/                      # App icons for different platforms
│   │   ├── icon.ico                # Windows icon
│   │   ├── icon.png                # General purpose icon
│   │   └── installer-icon.ico      # Installer icon
│   │
│   └── installer/                  # Installer assets
│       ├── license.txt             # Application license
│       └── setup-banner.bmp        # Installer banner
│
├── dist/                           # Compiled/built files (auto-generated)
│   ├── main/                       # Compiled main process
│   ├── renderer/                   # Compiled renderer files
│   └── preload/                    # Compiled preload scripts
│
├── build/                          # Final built application (auto-generated)
│   ├── win-unpacked/               # Unpacked Windows build
│   └── Smart File Organizer Setup.exe # Windows installer
│
├── logs/                           # Application logs (auto-generated)
│   ├── main.log                    # Main process logs
│   └── error.log                   # Error logs
│
├── user-data/                      # User configuration (auto-generated)
│   ├── config.json                 # User's custom configuration
│   ├── rules.json                  # User's file organization rules
│   └── folders.json                # User's custom folder mappings
│
└── scripts/                        # Development and build scripts
    ├── build.js                    # Build script
    ├── dev.js                      # Development script
    └── package.js                  # Packaging script
