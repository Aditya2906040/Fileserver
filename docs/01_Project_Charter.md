# Fileserver — Project Charter

**Version:** 1.0
**Status:** Draft
**Last Updated:** July 1, 2026

---

# 1. Project Name

**Fileserver**

---

# 2. Mission

Fileserver is a self-hosted file storage platform that enables users to centrally store, organize, and access their data from multiple client devices while retaining ownership of the underlying storage infrastructure.

---

# 3. Problem Statement

Modern users often store files across multiple devices, resulting in fragmented data, inconsistent backups, and limited accessibility. Existing cloud storage solutions address these issues but require users to trust third-party providers with both their data and infrastructure.

Fileserver aims to provide a self-hosted alternative where users retain ownership of their storage while benefiting from centralized file management and network accessibility.

---

# 4. Project Objectives

The objectives of the project are:

- Build a modular client-server file storage platform.
- Design a well-defined communication protocol between clients and the server.
- Develop the project incrementally, beginning with a LAN-based implementation.
- Maintain a clean and extensible architecture that supports future enhancements.
- Use the project as a practical exercise in modern C++, networking, systems programming, and software architecture.

---

# 5. Target Users

## Initial Users

- Project developer
- Family members
- Friends

## Future Users

- Developers
- Colleagues
- Freelancers
- Content creators (e.g., photographers and video editors)
- Small teams and businesses requiring self-hosted storage

---

# 6. Phase 1 Scope

Phase 1 focuses on establishing a reliable LAN-based file storage system.

The implementation includes:

- Linux-based server
- Linux client
- TCP communication
- Custom application-layer protocol
- User authentication (hardcoded credentials)
- Per-user storage directories
- User data isolation, ensuring each authenticated user can access only their own files
- File upload
- File download
- File listing
- Persistent storage
- Multi-client support using a thread-per-client model
- Project documentation

Although Phase 1 does not include cryptographic protection or advanced authorization mechanisms, the system shall enforce logical isolation between users by restricting all file operations to the authenticated user's designated storage area.

---

# 7. Out of Scope (Phase 1)

The following features are intentionally excluded from Phase 1:

- Raspberry Pi deployment
- Remote Internet access
- Cloud infrastructure
- Web dashboard
- Graphical user interface
- Mobile applications
- File synchronization
- File sharing
- End-to-end encryption
- Compression
- Versioning
- Discovery protocols
- Database integration
- User registration
- Role-based access control

These items belong to future phases unless explicitly re-scoped.

---

# 8. Technical Constraints

Phase 1 will be developed under the following constraints:

- Target platform: Linux
- Programming language: C++20
- Communication: TCP
- Interface: Command Line Interface (CLI)
- Build system: CMake
- Development approach: Documentation-first, implementation-second

---

# 9. Phase 1 Success Criteria

Phase 1 is considered complete when:

- The server operates continuously without crashes during normal usage.
- Multiple authenticated clients can connect concurrently.
- Users can upload files successfully.
- Users can download files successfully.
- Users can list only their own files.
- Uploaded files remain available after server restart.
- Core operations are logged.
- Documentation accurately reflects the implementation.

---

# 10. Guiding Principles

1. Correctness before optimization.
2. Simplicity before unnecessary abstraction.
3. Design for extension without implementing speculative features.
4. Document important architectural decisions before implementation.
5. Maintain modular components with clearly defined responsibilities.
6. Use third-party libraries only when they provide a clear engineering benefit; understand their purpose before adopting them.
7. Treat documentation as part of the software, not as an afterthought.

---

# 11. Long-Term Vision

Fileserver is intended to evolve beyond its initial LAN implementation into a complete self-hosted storage platform.

Future milestones include:

- Raspberry Pi deployment
- External SSD/HDD support
- Secure remote access
- Web-based management interface
- Strong authentication and authorization
- Data encryption
- Synchronization across devices
- Commercial-grade deployment capabilities

These milestones are outside the scope of Phase 1 and will be addressed in future project roadmaps.
