# Guía de Instalación y Configuración

## 🚀 Instalación Rápida (30 segundos)

### Prerrequisitos
- Claude Desktop con MCP habilitado
- Git instalado
- Cuentas configuradas: Microsoft To Do, HubSpot, Gmail

### Pasos de Instalación
```bash
# 1. Clonar repositorio
git clone https://github.com/isaacgarciaacc/ProjectManagement-Framework.git
cd ProjectManagement-Framework

# 2. Verificar estructura
ls -la  # Debe mostrar 10 módulos

# 3. Activar Framework
# En Claude: "framework" o "estado framework"
```

## ⚙️ Configuración Completa (3-5 minutos)

### 1. Memory MCP Setup
```json
{
  "memory": {
    "command": "npx @isaacgarciaacc/memory-server",
    "args": ["--data-dir", "./memory-data"]
  }
}
```

### 2. Microsoft To Do IDs
```javascript
const TODO_LISTS = {
  "acciones_reuniones": "AQMkADAwATM3ZmYAZS1kNmZmAC1jYTg5LTAwAi0wMAoALgAAA9Ys6KRsteJLrqPSNeq0bAQBAFz-u791xRxDn1wFCPi4B7cAB1LQhhsAAAA=",
  "seguimiento_semanal": "AQMkADAwATM3ZmYAZS1kNmZmAC1jYTg5LTAwAi0wMAoALgAAA9Ys6KRsteJLrqPSNeq0bAQBAFz-u791xRxDn1wFCPi4B7cAB1LQhhwAAAA=",
  "decisiones": "AQMkADAwATM3ZmYAZS1kNmZmAC1jYTg5LTAwAi0wMAoALgAAA9Ys6KRsteJLrqPSNeq0bAQBAFz-u791xRxDn1wFCPi4B7cAB1LQhh0AAAA="
};
```

### 3. HubSpot Configuration
```javascript
const HUBSPOT_CONFIG = {
  company_demo: 35618742022,
  deal_implementacion: 39559529801,
  contact_pm: 133927698314,
  contact_sponsor: 133913538599
};
```

### 4. Zapier MCP Limits
```python
ZAPIER_LIMITS = {
    "free_plan": "300 calls/month",
    "rate_limit": "5 calls/minute",
    "spacing": "15-20 seconds between calls"
}
```

## 🎯 Comandos Principales

### Comandos Framework
```bash
# Estado general
"framework"
"estado framework"

# Procesamiento específico
"tengo una reunión"           # → Template-Acta-Reunion
"nuevo proyecto"              # → Template-Plan-Proyecto  
"email SAT crítico"           # → Sistema-Email-AirCraftCare
"reporte semanal"            # → Template-Seguimiento-Tareas
"retrospectiva"              # → Template-Retrospectiva-Lecciones

# Recovery system
"Recuperar contexto [proyecto] y continuar donde nos quedamos"
```

### Comandos Desarrollo
```bash
# Nueva funcionalidad
"Desarrollar nueva funcionalidad: [descripción]"

# Análisis técnico
"consultar pom 3535519"
"revisar dependencias maven"

# Monitoreo
"actualizar documentación framework"
"revisión semanal framework"
```

## 📋 Verificación de Instalación

### Checklist Básico
- [ ] ✅ Repositorio clonado correctamente
- [ ] ✅ 10 módulos visibles en estructura
- [ ] ✅ README.md principal disponible
- [ ] ✅ Claude Desktop reconoce comando "framework"

### Checklist Avanzado
- [ ] ✅ Memory MCP respondiendo consultas
- [ ] ✅ Microsoft To Do conectado (crear tarea test)
- [ ] ✅ HubSpot CRM accesible (verificar Company Demo)
- [ ] ✅ Gmail procesamiento automático configurado
- [ ] ✅ Templates funcionando (test con "tengo una reunión")

### Test de Integración
```bash
# Test Memory MCP
"consultar estado Framework actual"
# Esperado: Respuesta <2 segundos con métricas

# Test Microsoft To Do  
"crear tarea test framework"
# Esperado: Tarea creada en lista correspondiente

# Test HubSpot
"verificar configuración CRM"
# Esperado: Company Demo visible

# Test Templates
"tengo una reunión de prueba"
# Esperado: Template-Acta-Reunion activado
```

## 🔧 Solución de Problemas

### Error: Memory MCP no responde
```bash
# Verificar configuración
cat ~/.config/claude/claude_desktop_config.json

# Reiniciar Memory Server
pkill -f memory-server
npx @isaacgarciaacc/memory-server --restart
```

### Error: Microsoft To Do sin acceso
```bash
# Verificar autenticación
# En Claude: "verificar listas Microsoft To Do"
# Re-autorizar si necesario
```

### Error: HubSpot timeout
```bash
# Verificar API Key
# En Claude: "verificar conexión HubSpot"
# Rate limiting: esperar 15-20 segundos entre calls
```

### Error: Templates no se activan
```bash
# Verificar triggers
# Usar comandos exactos:
"tengo una reunión"     # ✅ Correcto
"reunion"               # ❌ Incorrecto
"nueva reunión"         # ❌ Incorrecto
```

## 📊 Configuración Empresarial

### Para Equipos (5-10 usuarios)
1. **Fork repositorio** para organización
2. **Configurar GitHub Teams** para colaboración
3. **Personalizar IDs** Microsoft To Do y HubSpot por usuario
4. **Establecer convenciones** naming específicas empresa
5. **Configurar CI/CD** para automatización deployment

### Para Organizaciones (10+ usuarios)
1. **GitHub Enterprise** para control avanzado
2. **HubSpot Professional** para CRM completo
3. **Microsoft 365 Business** para To Do empresarial
4. **Custom Memory MCP** deployment en infraestructura propia
5. **Training programa** para usuarios finales

## 🔐 Configuración Seguridad

### Variables de Entorno
```bash
# .env file
HUBSPOT_API_KEY=your_hubspot_api_key
MICROSOFT_TODO_CLIENT_ID=your_todo_client_id
GITHUB_TOKEN=your_github_token
MEMORY_MCP_KEY=your_memory_key
```

### Permisos GitHub
```yaml
# .github/permissions.yml
permissions:
  contents: write    # Para documentación
  issues: write      # Para tracking
  projects: write    # Para planning
  pull-requests: write  # Para colaboración
```

### Backup Strategy
```bash
# Backup automático diario
0 2 * * * cd /path/to/framework && git add . && git commit -m "Auto backup $(date)" && git push
```

## 📈 Métricas Post-Instalación

### Métricas Esperadas (Primeros 30 días)
- **Tiempo respuesta Memory MCP:** <2 segundos
- **Procesamiento reuniones:** <30 segundos  
- **Emails críticos:** <2 minutos
- **Proyectos nuevos:** <45 segundos
- **ROI inicial:** 300-500%

### KPIs de Adopción
- **Uso diario commands:** 10+ comandos framework
- **Templates activados:** 5+ por semana
- **Automatizaciones exitosas:** >95%
- **Tiempo ahorrado semanal:** 10+ horas
- **Satisfacción usuario:** >90%

## 🎓 Training y Onboarding

### Día 1: Instalación Básica
- Clonar repositorio
- Verificar prerequisites
- Test comandos básicos
- Primera reunión procesada

### Día 2-7: Integración Avanzada
- Configurar todas las integraciones MCP
- Personalizar templates
- Establecer workflows específicos
- Métricas baseline

### Día 8-30: Optimización
- Análisis uso patrones
- Customización triggers
- Integración empresa workflows
- Training equipo extenso

## 📞 Soporte Técnico

### Canales de Soporte
- **GitHub Issues:** Bugs y feature requests
- **Documentation:** Wiki completa
- **Community:** Discussions forum
- **Enterprise:** Email directo para implementaciones

### SLA Soporte
- **Issues críticos:** <4 horas
- **Bug reports:** <24 horas
- **Feature requests:** <72 horas
- **Documentation:** <1 semana

---

## ✅ Instalación Completada

Una vez completada la instalación, deberías poder ejecutar:

```bash
# Comando verificación final
"framework status completo"
```

**Respuesta esperada:**
```
✅ Framework 100% operacional
✅ Memory MCP: <2 segundos respuesta
✅ Microsoft To Do: 3 listas configuradas
✅ HubSpot CRM: Objetos sincronizados
✅ Templates: 10+ disponibles
✅ ROI estimado: 2,000%+

🚀 Framework Revolution activated!
```

---

*Guía de instalación generada automáticamente*  
*Framework versión: 1.0 - Julio 2025*  
*Soporte: GitHub Issues & Community*
