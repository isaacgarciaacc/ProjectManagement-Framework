# 📊 TEMPLATE ESTÁNDAR DASHBOARD PROYECTO

## 🎯 INFORMACIÓN TEMPLATE
**Template:** Dashboard Proyecto Framework v1.0  
**Basado en:** Protocolo Estándar Reportes Framework  
**Uso:** Dashboards proyectos específicos Framework  
**Ubicación Final:** `/docs/dashboards/YYYY-MM-DD-[proyecto]-dashboard.html`  

## 🎨 ESTRUCTURA HTML ESTÁNDAR

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>[PROYECTO] - Dashboard Ejecutivo</title>
    <style>
        /* ESTILOS ESTÁNDAR FRAMEWORK */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            color: #333;
        }

        .container {
            max-width: 1400px;
            margin: 0 auto;
            padding: 20px;
        }

        .header {
            text-align: center;
            margin-bottom: 40px;
            background: rgba(255, 255, 255, 0.95);
            padding: 30px;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
        }

        .header h1 {
            color: #2d3748;
            font-size: 2.5em;
            margin-bottom: 10px;
            background: linear-gradient(45deg, #667eea, #764ba2);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .project-info {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 15px;
            margin-bottom: 30px;
        }

        .info-card {
            background: rgba(255, 255, 255, 0.95);
            padding: 20px;
            border-radius: 15px;
            text-align: center;
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.1);
        }

        .metrics-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-bottom: 40px;
        }

        .metric-card {
            background: rgba(255, 255, 255, 0.95);
            padding: 25px;
            border-radius: 15px;
            text-align: center;
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.1);
            transition: transform 0.3s ease;
        }

        .metric-card:hover {
            transform: translateY(-5px);
        }

        .charts-section {
            background: rgba(255, 255, 255, 0.95);
            border-radius: 20px;
            padding: 40px;
            margin-bottom: 30px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
        }

        .timeline-section {
            background: rgba(255, 255, 255, 0.95);
            border-radius: 20px;
            padding: 40px;
            margin-bottom: 30px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
        }

        .status-indicator {
            display: inline-block;
            padding: 5px 15px;
            border-radius: 20px;
            font-size: 0.9em;
            font-weight: bold;
        }

        .status-completed { background: #48bb78; color: white; }
        .status-progress { background: #ed8936; color: white; }
        .status-pending { background: #a0aec0; color: white; }
        .status-risk { background: #e53e3e; color: white; }

        .progress-bar {
            width: 100%;
            height: 8px;
            background: #e2e8f0;
            border-radius: 4px;
            margin-top: 10px;
            overflow: hidden;
        }

        .progress-fill {
            height: 100%;
            background: linear-gradient(90deg, #667eea, #764ba2);
            border-radius: 4px;
            transition: width 0.3s ease;
        }

        .footer {
            text-align: center;
            background: rgba(255, 255, 255, 0.95);
            padding: 30px;
            border-radius: 20px;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
        }

        @media (max-width: 768px) {
            .header h1 { font-size: 2em; }
            .project-info { grid-template-columns: 1fr; }
            .metrics-grid { grid-template-columns: 1fr; }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header Proyecto -->
        <div class="header">
            <h1>🚀 [NOMBRE_PROYECTO]</h1>
            <p class="subtitle">[DESCRIPCIÓN_PROYECTO]</p>
            <div class="status-indicator status-[ESTADO]">[ESTADO_PROYECTO]</div>
        </div>

        <!-- Información Proyecto -->
        <div class="project-info">
            <div class="info-card">
                <h3>📅 Inicio</h3>
                <p>[FECHA_INICIO]</p>
            </div>
            <div class="info-card">
                <h3>🎯 Deadline</h3>
                <p>[FECHA_DEADLINE]</p>
            </div>
            <div class="info-card">
                <h3>👥 Equipo</h3>
                <p>[TAMAÑO_EQUIPO] personas</p>
            </div>
            <div class="info-card">
                <h3>💰 Presupuesto</h3>
                <p>[PRESUPUESTO]</p>
            </div>
        </div>

        <!-- Métricas Principales -->
        <div class="metrics-grid">
            <div class="metric-card">
                <div class="metric-value">[PROGRESO]%</div>
                <div class="metric-label">Progreso Total</div>
                <div class="progress-bar">
                    <div class="progress-fill" style="width: [PROGRESO]%;"></div>
                </div>
            </div>
            <div class="metric-card">
                <div class="metric-value">[ROI]%</div>
                <div class="metric-label">ROI Actual</div>
                <div class="progress-bar">
                    <div class="progress-fill" style="width: [ROI_PERCENT]%;"></div>
                </div>
            </div>
            <div class="metric-card">
                <div class="metric-value">[TAREAS_COMPLETADAS]</div>
                <div class="metric-label">Tareas Completadas</div>
            </div>
            <div class="metric-card">
                <div class="metric-value">[DÍAS_RESTANTES]</div>
                <div class="metric-label">Días Restantes</div>
            </div>
        </div>

        <!-- Visualizaciones Charts MCP -->
        <div class="charts-section">
            <h2 style="text-align: center; margin-bottom: 30px; color: #2d3748;">📊 Visualizaciones Proyecto</h2>
            
            <div class="charts-grid">
                <div class="chart-container">
                    <h3>📈 Progreso por Fases</h3>
                    <img src="[CHART_URL_1]" alt="Progreso Fases" />
                </div>
                
                <div class="chart-container">
                    <h3>💰 Gestión Presupuesto</h3>
                    <img src="[CHART_URL_2]" alt="Gestión Presupuesto" />
                </div>
            </div>

            <div class="chart-container" style="margin-top: 20px;">
                <h3>📊 Timeline Proyecto</h3>
                <img src="[CHART_URL_3]" alt="Timeline Proyecto" />
            </div>
        </div>

        <!-- Timeline/Cronograma -->
        <div class="timeline-section">
            <h2 style="text-align: center; margin-bottom: 30px; color: #2d3748;">🗓️ Cronograma Proyecto</h2>
            
            <div class="timeline-items">
                <!-- MILESTONE 1 -->
                <div class="timeline-item completed">
                    <div class="timeline-date">[FECHA_M1]</div>
                    <div class="timeline-content">
                        <h4>✅ [MILESTONE_1]</h4>
                        <p>[DESCRIPCIÓN_M1]</p>
                    </div>
                </div>
                
                <!-- MILESTONE 2 -->
                <div class="timeline-item progress">
                    <div class="timeline-date">[FECHA_M2]</div>
                    <div class="timeline-content">
                        <h4>🔄 [MILESTONE_2]</h4>
                        <p>[DESCRIPCIÓN_M2]</p>
                    </div>
                </div>
                
                <!-- MILESTONE 3 -->
                <div class="timeline-item pending">
                    <div class="timeline-date">[FECHA_M3]</div>
                    <div class="timeline-content">
                        <h4>⏳ [MILESTONE_3]</h4>
                        <p>[DESCRIPCIÓN_M3]</p>
                    </div>
                </div>
            </div>
        </div>

        <!-- Footer Framework -->
        <div class="footer">
            <p><strong>🏗️ Framework:</strong> Sistema de Gestión de Proyectos y Conocimiento</p>
            <p><strong>🎯 Metodología:</strong> Protocolo Estándar Reportes v1.0</p>
            <div class="tech-stack">
                Powered by: Charts MCP + GitHub Pages + Memory MCP + Framework Revolution
            </div>
        </div>
    </div>

    <script>
        // JavaScript Estándar Framework
        document.addEventListener('DOMContentLoaded', function() {
            // Animar progress bars
            const progressBars = document.querySelectorAll('.progress-fill');
            progressBars.forEach(bar => {
                const width = bar.style.width;
                bar.style.width = '0%';
                setTimeout(() => {
                    bar.style.width = width;
                }, 500);
            });

            // Auto-refresh en producción
            if (window.location.hostname !== 'localhost') {
                setTimeout(() => {
                    window.location.reload();
                }, 300000); // 5 minutos
            }
        });
    </script>
</body>
</html>
```

## 🔄 VARIABLES REEMPLAZO

### **INFORMACIÓN PROYECTO**
- `[NOMBRE_PROYECTO]` → Nombre completo proyecto
- `[DESCRIPCIÓN_PROYECTO]` → Descripción breve proyecto
- `[ESTADO_PROYECTO]` → Estado actual (En Progreso, Completado, etc.)
- `[ESTADO]` → Estado CSS (progress, completed, pending, risk)

### **FECHAS Y CRONOGRAMA**  
- `[FECHA_INICIO]` → Fecha inicio proyecto
- `[FECHA_DEADLINE]` → Fecha deadline proyecto
- `[FECHA_M1/M2/M3]` → Fechas milestones específicos
- `[DÍAS_RESTANTES]` → Días restantes para deadline

### **MÉTRICAS Y DATOS**
- `[PROGRESO]` → Porcentaje progreso total (número)
- `[ROI]` → ROI actual proyecto (número)
- `[ROI_PERCENT]` → ROI como porcentaje para progress bar
- `[TAREAS_COMPLETADAS]` → Número tareas completadas
- `[TAMAÑO_EQUIPO]` → Número personas equipo
- `[PRESUPUESTO]` → Presupuesto proyecto

### **CHARTS MCP URLS**
- `[CHART_URL_1]` → URL gráfico progreso fases
- `[CHART_URL_2]` → URL gráfico gestión presupuesto  
- `[CHART_URL_3]` → URL gráfico timeline proyecto

### **MILESTONES**
- `[MILESTONE_1/2/3]` → Nombres milestones
- `[DESCRIPCIÓN_M1/M2/M3]` → Descripciones milestones

## 🎯 COMANDOS GENERACIÓN

### **COMANDO CREAR DASHBOARD PROYECTO**
```
crear dashboard proyecto [nombre-proyecto]
```

**PROCESO AUTOMÁTICO:**
1. Consultar Memory MCP datos proyecto
2. Generar Charts MCP específicos proyecto  
3. Reemplazar variables template con datos reales
4. Crear archivo `/docs/dashboards/YYYY-MM-DD-[proyecto]-dashboard.html`
5. Commit automático GitHub MCP
6. URL compartible generada automáticamente

### **EJEMPLO COMANDO REAL**
```
crear dashboard proyecto Framework-Revolution
```

**RESULTADO:**
- **Archivo:** `/docs/dashboards/2025-01-06-Framework-Revolution-dashboard.html`
- **URL:** https://isaacgarciaacc.github.io/ProjectManagement-Framework/dashboards/2025-01-06-Framework-Revolution-dashboard.html

## 📊 CHARTS MCP ESTÁNDAR PROYECTO

### **CHART 1: PROGRESO POR FASES**
```javascript
// Column Chart - Progreso implementaciones/fases
data: [
  { category: 'Fase 1', value: 100, group: 'Completada' },
  { category: 'Fase 2', value: 75, group: 'En Progreso' },
  { category: 'Fase 3', value: 0, group: 'Pendiente' }
]
```

### **CHART 2: GESTIÓN PRESUPUESTO**  
```javascript
// Pie Chart - Distribución presupuesto
data: [
  { category: 'Recursos Humanos', value: 60 },
  { category: 'Tecnología', value: 25 },
  { category: 'Operaciones', value: 15 }
]
```

### **CHART 3: TIMELINE PROYECTO**
```javascript  
// Line Chart - Progreso temporal
data: [
  { time: 'Semana 1', value: 10 },
  { time: 'Semana 2', value: 25 },
  { time: 'Semana 3', value: 45 },
  { time: 'Semana 4', value: 70 }
]
```

## ✅ CHECKLIST VALIDACIÓN

### **ANTES DEPLOY**
- [ ] ✅ Variables reemplazadas correctamente
- [ ] ✅ Charts MCP URLs válidas y funcionando
- [ ] ✅ Responsive design tested
- [ ] ✅ JavaScript funcionando
- [ ] ✅ Naming convention seguida
- [ ] ✅ Colors Framework aplicados
- [ ] ✅ Footer Framework incluido

### **DESPUÉS DEPLOY**
- [ ] ✅ URL compartible accessible
- [ ] ✅ Load time <2 segundos
- [ ] ✅ Mobile/desktop compatible
- [ ] ✅ Memory MCP actualizada
- [ ] ✅ GitHub commit documentation

---

**🚀 Template Protocolo Estándar Reportes Framework v1.0**