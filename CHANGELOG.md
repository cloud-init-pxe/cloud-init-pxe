# Changelog

All notable changes to Cloud-Init-PXE will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [2.0.0] - 2024-06-04

### Major Update - Complete UI Overhaul

#### Added

- **Unified Modern Interface**: Completely replaced the dated Cloud-Init-PXE UI with a stunning modern design
- **Single Dashboard**: All features now accessible from one unified interface
- **Professional Dark Theme**: Beautiful dark theme by default with smooth animations
- **Light Theme Support**: Clean light theme option for different preferences
- **Collapsible Sidebar**: Smart navigation that remembers your preferences
- **Real-time System Stats**: Live CPU, memory, and version monitoring on dashboard
- **Toast Notifications**: Non-intrusive feedback system for all actions
- **Global Search**: Quick search functionality (ready for implementation)
- **Additional Templates**:
  - `ansible-ready.yaml` - Ansible-managed system setup
  - `monitoring-stack.yaml` - Prometheus + Grafana monitoring

#### Changed

- **Main Interface**: The modern UI is now the default at `/`
- **Legacy Access**: Original Cloud-Init-PXE UI moved to `/legacy`
- **Navigation Flow**: Improved user experience with logical grouping
- **Editor Experience**: Consistent CodeMirror implementation across all editors
- **Visual Hierarchy**: Better organization with cards and sections

#### Improved

- **Performance**: Optimized WebSocket communications
- **Responsiveness**: Better mobile and tablet experience
- **Code Quality**: Cleaner, more maintainable codebase
- **User Feedback**: Immediate visual feedback for all actions

## [1.0.0] - 2024-06-04

### Legacy

#### Added ✨

<!-- Overview of major feature categories -->
**Core Platform Features:**

- 🚀 Initial release of Cloud-Init Studio with complete configuration lifecycle management
- 📝 Cloud-init configuration management (create, edit, delete) with persistent storage
- 🔌 HTTP API endpoints for cloud-init integration:
  - User-data: `/cloud-init/user-data/<config>.yaml`
  - Meta-data: `/cloud-init/meta-data`
- 🌐 iPXE integration with custom boot menus
- 🔄 WebSocket-based real-time updates for collaborative editing

**User Interface:**

- 🎨 Dual interface options:
  - Classic Bootstrap interface for existing Cloud-Init-PXE users
  - Modern dark-themed "Studio" interface with advanced features
- 📱 Responsive design supporting desktop, tablet, and mobile devices
- 🌓 Dark/light theme toggle for user preference

**Editor Features:**

- ✅ YAML syntax validation with immediate feedback
- 📊 Live preview of documentation and YAML configurations
- 📋 One-click URL copying for easy sharing
- 📚 Markdown documentation support for configurations

**Templates & Pre-configurations:**

- 📦 Pre-built templates for common scenarios:
  - `basic-setup.yaml` - Essential server configuration
  - `kubernetes-node.yaml` - Ready-to-use Kubernetes node setup
  - `docker-host.yaml` - Container-optimized host configuration

**Deployment & Infrastructure:**

- 🐳 Docker and Docker Compose support for easy deployment
- 🔧 Non-invasive patching system for Cloud-Init-PXE integration
- 💾 Persistent storage for configurations (YAML files)

- Initial release of Cloud-Init Studio
- Cloud-init configuration management (create, edit, delete)
- Classic Bootstrap interface for existing Cloud-Init-PXE users
- Modern dark-themed "Studio" interface with advanced features
- Markdown documentation support for configurations
- Live preview of documentation and YAML
- Pre-built templates for common scenarios:
  - Basic server setup
  - Kubernetes node configuration
- HTTP API endpoints for cloud-init:
  - User-data: `/cloud-init/user-data/<config>.yaml`
  - Meta-data: `/cloud-init/meta-data`
- iPXE integration with custom boot menus
- WebSocket-based real-time updates
- YAML syntax validation
- One-click URL copying
- Dark/light theme toggle
- Responsive design for mobile and tablet
- Docker and Docker Compose support
- Non-invasive patching system for Cloud-Init-PXE
- Persistent storage for configurations

### Technical Details

- Based on Alpine Linux 3.21.3
- Node.js application with Express
- Socket.IO for real-time communication
- CodeMirror for code editing
- EasyMDE for markdown editing
- Supervisor for process management
- TFTP server included (tftp-hpa)

### Known Issues

- Documentation is stored in memory only (not persisted to disk)
- No authentication mechanism (designed for trusted networks)
- Limited to single-user scenarios

### Security

- Configurations are served without authentication
- Intended for use in trusted network environments only

## [Unreleased]

### Planned Features

- Persistent documentation storage
- Configuration versioning and history
- Import/Export functionality
- Authentication and multi-user support
- Configuration validation rules
- Kubernetes operator for cloud-init configs
- API rate limiting
- Audit logging
- Configuration templates marketplace
