# PROTOCOLO CARDINAL DE VERIFICACIÓN SEMÁNTICA
## NIVEL 1 - CRÍTICO - NUNCA VIOLABLE

**Fecha Establecimiento**: 07 Enero 2025  
**Autoridad**: Protocolo Cardinal Framework - Máxima Prioridad  
**Aplicación**: OBLIGATORIO para Claude como Cerebro Automatizado  

---

## 🚨 PROBLEMA IDENTIFICADO

**ERROR CRÍTICO DETECTADO**: Múltiples carpetas duplicadas para el mismo proyecto:
- `2025-07-04-Framework-Revolution-10-Implementaciones`
- `2025-07-04-Framework-Revolution` 
- `2025-07-05-Framework-Revolution`

**Impacto**: Rompe integridad organizacional, fragmenta documentación, crea confusión.

---

## 🛡️ PROTOCOLO CARDINAL - VERIFICACIÓN SEMÁNTICA OBLIGATORIA

### **REGLA 1: VERIFICACIÓN PREVIA MANDATORIA**

**ANTES** de crear cualquier documentación de proyecto, Claude DEBE:

1. **Búsqueda Memory MCP**: `memory:search_nodes('nombre_proyecto')`
2. **Verificación GitHub**: Revisar `03-Proyectos-Activos/` completo
3. **Análisis Semántico**: Identificar proyectos similares/relacionados
4. **Decisión Consolidación**: SI existe → consolidar, SI NO existe → crear nuevo

### **REGLA 2: PRINCIPIO UNA FUENTE DE VERDAD**

- **UN proyecto = UNA ubicación = UNA documentación = UN contexto**
- **PROHIBIDO**: Múltiples carpetas para el mismo concepto de proyecto
- **OBLIGATORIO**: Consolidación en carpeta más completa/reciente

### **REGLA 3: NOMENCLATURA CANÓNICA**

```
03-Proyectos-Activos/YYYY-MM-DD-Nombre-Proyecto-Principal/
```

- **Fecha**: Fecha de INICIO real del proyecto
- **Nombre**: Concepto principal sin variaciones
- **Ejemplo CORRECTO**: `2025-07-04-Framework-Revolution/`
- **Ejemplo INCORRECTO**: Múltiples variaciones del mismo concepto

### **REGLA 4: PROCESO DE CONSOLIDACIÓN AUTOMÁTICA**

Cuando se detecte duplicación:

1. **Identificar carpeta canónica** (más completa/reciente)
2. **Migrar contenido** de carpetas duplicadas
3. **Eliminar carpetas vacías/redundantes**
4. **Actualizar Memory MCP** con ubicación única
5. **Documentar consolidación** en historial proyecto

---

## 🔍 VERIFICACIÓN SEMÁNTICA DETALLADA

### **Búsquedas Obligatorias Antes de Crear**:

```bash
# Memory MCP
memory:search_nodes('Framework Revolution')
memory:search_nodes('implementaciones')
memory:search_nodes('revolution')

# GitHub MCP
github:get_file_contents() en 03-Proyectos-Activos/
Revisar nombres similares, conceptos relacionados

# Análisis Semántico
- ¿Mismo concepto con diferente fecha?
- ¿Evolución del mismo proyecto?
- ¿Subcomponente de proyecto existente?
```

### **Criterios de Consolidación**:

1. **Mismo concepto base** → Consolidar en una carpeta
2. **Evolución temporal** → Usar carpeta de fecha inicio original
3. **Subproyectos** → Subcarpetas dentro del proyecto principal
4. **Proyectos independientes** → Carpetas separadas únicamente

---

## 🛠️ IMPLEMENTACIÓN INMEDIATA

### **ACCIÓN CORRECTIVA FRAMEWORK REVOLUTION**:

1. **Carpeta Canónica**: `2025-07-04-Framework-Revolution/`
2. **Migrar contenido** de las otras 2 carpetas duplicadas
3. **Eliminar duplicados** después de migración
4. **Actualizar Memory MCP** con ubicación única

### **PROTOCOLO FUTURO**:

1. **ANTES** de cualquier `github:create_or_update_file`
2. **EJECUTAR** verificación semántica obligatoria
3. **CONFIRMAR** no duplicación
4. **PROCEDER** solo después de verificación exitosa

---

## 📋 CHECKLIST VERIFICACIÓN SEMÁNTICA

**ANTES de crear documentación de proyecto**:

- [ ] Búsqueda Memory MCP ejecutada
- [ ] Revisión GitHub 03-Proyectos-Activos/ completada
- [ ] Análisis semántico de nombres/conceptos realizado
- [ ] Confirmación no hay duplicaciones
- [ ] Ubicación canónica identificada
- [ ] Autorización para proceder otorgada

---

## 🎯 OBJETIVO PROTOCOLO

**GARANTIZAR**:
- Integridad organizacional Framework
- Documentación consolidada y coherente  
- Navegación clara y sin confusión
- Mantenimiento eficiente del conocimiento
- Escalabilidad sin fragmentación

---

## ⚡ IMPLEMENTACIÓN AUTOMÁTICA

Este protocolo se implementa **AUTOMÁTICAMENTE** en:
- Memory MCP (actualización entidades)
- Protocolo inicio automático Framework
- Trigger detection matrix
- Verificación contextual obligatoria

**RESULTADO**: Framework Organization Integrity = 100%

---

**AUTORIDAD**: Protocolo Cardinal Nivel 1  
**VIGENCIA**: Permanente desde 07 Enero 2025  
**REVISIÓN**: Anual o tras detección de violaciones  
**ENFORCEMENT**: Automático vía Claude Cerebro Automatizado