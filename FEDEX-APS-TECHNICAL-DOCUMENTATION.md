# 🏢 FEDEX APS TECHNICAL DOCUMENTATION
## SYSTEM UNDERSTANDING DOCUMENT (SUD) INTEGRATION

![Status](https://img.shields.io/badge/Status-100%25_Operacional-brightgreen)
![Team](https://img.shields.io/badge/Team-APS_India-blue)
![Applications](https://img.shields.io/badge/Applications-8_Critical-red)
![Support](https://img.shields.io/badge/Support-24/7-gold)

## 🎯 DESCRIPCIÓN GENERAL

**Rol**: Líder Técnico Accenture/FedEx APS Team  
**Responsabilidad**: 8 aplicaciones críticas Java/Spring Gen Converted Apps  
**Equipo**: APS India (Pandiyan Kallaperumall, Aravalu Cuellar, Virgilio Tade)  
**Contacto**: jgarcia.osv@fedex.com  
**Documentación**: System Understanding Document v1.0 (3/31/2025)

---

## 🏗️ ARQUITECTURA SISTEMA

### Stack Técnico Principal
```
Legacy → Spring Transformation
├── Java/Spring Environment
├── Apache Tomcat 9.0.99
├── Oracle Database / JMS, PCF
├── Maven (Dependencies Management)
├── RedHat RHEL8 Servers
└── DB2/Purescript Integration
```

### Módulos Arquitectura
```
Gen Converted Apps Architecture
├── Main - Logical Central
├── REST - Services Interfaces  
├── Web - Presentation Layers
└── Direct Dependencies (No standard REST calls)
```

---

## 📱 CATÁLOGO APLICACIONES (8 Críticas)

### 1. **3535519-FXF-OP-CUST-CTR-OPERS**
- **Tipo**: Gen Converted Apps
- **Función**: Información doors, bays, trailers Service Centers
- **Usuarios**: Personal operativo FedEx Freight
- **Criticidad**: Alta - Operaciones diarias

### 2. **3535347-Report Distribution**
- **Tipo**: Backend Web Services
- **Función**: Print, fax, email calls ACCOPS/Gen applications
- **Integración**: Legacy conversion to Spring
- **Criticidad**: Alta - Reportes críticos

### 3. **3535518-FXF-OP-ACCOPS-SHIPMENT-MENU**
- **Tipo**: Gen Converted Apps
- **Función**: Empleados search/display shipment details y history FedEx Freight
- **Interface**: Search y tracking shipments
- **Criticidad**: Alta - Búsquedas operativas

### 4. **3535535-FXF-OP-THIN-CLIENT-DOCK-COMP**
- **Tipo**: Java App Legacy GEN
- **Función**: Thin client dock computers model
- **Hardware**: Dock computer integration
- **Criticidad**: Media - Hardware específico

### 5. **3535517-FXF-OP-ACCOPS-LOGIN**
- **Tipo**: Gen Converted Apps
- **Función**: Printer/network drive utilities Freight Operations applications
- **Sistema**: Login y utilidades día/sesión
- **Criticidad**: Alta - Acceso sistema

### 6. **3535520-FXF-OP-DELIVERY-PLANNING**
- **Tipo**: Core Module
- **Función**: Shipment planification, delivery routes shipments
- **Proceso**: Planning y optimización rutas
- **Criticidad**: Alta - Planificación crítica

### 7. **6157-FXFOperationsIntegration (Dock Rest)**
- **Tipo**: REST Application
- **Función**: Middle layer REST application Dock Computer uses communicate DB services
- **Arquitectura**: Integration layer
- **Criticidad**: Alta - Integración sistemas

### 8. **6001-Exeology**
- **Tipo**: Third-party Dependency
- **Función**: Hazmat material classification FedEx transports
- **Proveedor**: External integration
- **Criticidad**: Media - Dependency externa

---

## 🔧 FUNCIONES NEGOCIO

### Conceptos Core FedEx Freight
```
Business Logic Hierarchy
├── Pro (Handling Unit/Pallet) - ID único
├── Shipment (1 o más Pros) - Agrupación
├── Handling Unit (Nombre Pro) - Unidad física
├── Suffix (Clasificaciones) - H0, 01, C0, Y0, C0/Y0
└── Service Centers - Puntos carga/descarga
```

### Operaciones Principales
- **Door Management**: Ver información doors service centers
- **Trailer Operations**: Mover PROs trailers asignados
- **Load/Unload**: PROs desde trailers, spot trailers service centers
- **Route Administration**: Administrar state información shipments/planning
- **State Management**: Información detallada shipments

### Business Partners
- **IT Personal**: Contacto principal Service Centers
- **Communications**: Notify about maintenance y updates distributions
- **Operations**: Performing activities como door assignments

---

## 🛠️ ENTORNO TÉCNICO

### Infraestructura Hardware
```
Production Environment
├── Linux Servers (RedHat RHEL8)
├── Windows Servers (Reporting)
├── Dock Computers (Thin Client)
└── Service Centers Infrastructure
```

### Software Components
```
Technology Stack
├── Application Server: Tomcat 9.1
├── Framework: Spring (Legacy conversion)
├── Database: Oracle DB, DB2, Purescript
├── Build Tool: Maven
├── OS: Linux/Windows separation
└── Virtualization: Citrix (supervisión servicios)
```

### Monitoring y Maintenance
- **AppDynamics**: Monitoring through sistema
- **Home - AppDynamics**: Dashboard principal
- **DB Monitoring**: Connection pools y performance
- **Error Tracking**: Common points of failure
- **Resolution Procedures**: DB connections close protocol

---

## 📋 PROCESOS DESARROLLO

### Metodología Agile Kanban
```
Development Workflow
├── Story Assignment → Team Member
├── Development Branch → Current application repositories
├── Local Testing → Business partners validation
├── Merge Approval → Development branch
├── Release Planning → Weekends deployment
└── UDeploy Platform → Target schedule
```

### Change Management
- **PDSM Change Request**: Template proceso
- **APS Team**: Normal activities development y support
- **Incident Management**: Containment state, support applications
- **UDeploy Team**: Deployment automation

### Knowledge Transfer
- **Documentation**: System Understanding Documents
- **Recipients**: Pandiyan Kallaperumall, Aravalu Cuellar, Virgilio Tade
- **Framework**: AO StartUp 3.1 - Transfer Knowledge process
- **Track**: People development

---

## 🚨 SOPORTE Y MANTENIMIENTO

### Backup & Recovery
```
Backup Strategy
├── Manual Process: Redeploy artifacts UDeploy platform
├── Backup Plan: Change request basis
├── Schedule: Planned outages/changes Saturdays 5-6 PM EST
├── Constraints: Normal time frame 1 PM EST
└── Purescript Jobs: DB sync various sources
```

### Jobs y Processes
```
Purescript Jobs
├── PIPEBC19, PIPEBC20 (Pipe Jobs)
├── OS1500OP (Operating System)
├── PIPEHVIR, PIPEFM01 (Pipeline)
├── IPEFM06, PIPEFM12 (Interface)
└── DB Sources: Keep sync between different databases
```

### Release Management
- **Current Focus**: Functionality overview
- **Release Planning**: No planes nuevos releases
- **Technology Updates**: Core improvements newer Java Core versions
- **Automation Opportunities**: Artifacts versioning Maven management

---

## 📊 MÉTRICAS Y KPIs

### Operational Metrics
- **Uptime**: 24/7 operations critical
- **Response Time**: Service center dependencies
- **Error Rate**: Tracked via AppDynamics
- **User Load**: Business partners y operational staff

### Support Metrics
- **Incident Response**: APS team coverage
- **Knowledge Transfer**: KT documentation completion
- **Team Coordination**: India APS team collaboration
- **Process Improvement**: Kanban methodology efficiency

---

## 🔄 PRÓXIMOS PASOS

### Immediate Actions
1. **Team Coordination**: Establecer comunicación directa equipo India APS
2. **Application Deep Dive**: Documentar específicamente cada una de las 8 aplicaciones
3. **Process Optimization**: Implementar mejoras metodología Kanban
4. **Monitoring Enhancement**: AppDynamics optimization

### Strategic Objectives
1. **Knowledge Consolidation**: Complete SUD documentation
2. **Team Leadership**: Effective India team coordination
3. **System Modernization**: Continue Legacy → Spring transformation
4. **Operational Excellence**: 24/7 support optimization

---

## 📞 CONTACTOS CRÍTICOS

### Team APS India
- **Pandiyan Kallaperumall**: Knowledge recipient
- **Aravalu Cuellar**: Knowledge recipient  
- **Virgilio Tade**: Knowledge recipient

### Technical Leadership
- **Jose Isaac Garcia Martinez**: Technical Leader
- **Email**: jgarcia.osv@fedex.com
- **Organization**: Accenture / FedEx OSV

### Business Partners
- **Brandon Thayn, Andy Jensen, Joshua Ezqueda, Jason Ponder**: Technical users
- **Okta Authentication**: Access control FedEx applications

---

**Framework Revolution v5.0** - FedEx APS Technical Documentation  
*System Understanding Document Integration Completed*  
*Technical Leadership: Jose Isaac Garcia - Accenture/FedEx OSV*  
*Documentation Date: July 17, 2025 - Based on SUD v1.0 (3/31/2025)*