# Context: Perfil de GitHub Actualizado

## Resumen de Acciones Completadas

Se actualizó el repositorio especial de perfil de GitHub `SebastianMoralesDuque/SebastianMoralesDuque` con las siguientes mejoras:

### 1. Actualización del README.md
- **Archivo:** `README.md` (rama `main`)
- **Acción:** Reemplazo completo del contenido existente
- **Nuevas características:**
  - Diseño moderno con header animado (capsule-render)
  - Badges de LinkedIn, Portfolio y Email
  - Contador de vistas de perfil
  - Typing animation SVG
  - Clase Python interactiva que describe habilidades
  - Sección detallada de especialización en IA
  - Tabla de stack tecnológico con iconos
  - Principios de ingeniería
  - GitHub stats, streak, trophies
  - Gráficos de actividad
  - Footer animado

### 2. Creación de Workflow de Snake Animation
- **Archivo:** `.github/workflows/snake.yml` (rama `main`)
- **Funcionalidad:** Genera automáticamente una animación de serpiente (contribuciones) en formato SVG
- **Características técnicas:**
  - Se ejecuta diariamente a las 12:00 UTC (cron `0 12 * * *`)
  - Se activa manualmente (workflow_dispatch)
  - Se ejecuta en cada push a la rama `main`
  - Genera dos versiones: light y dark (github-dark palette)
  - Almacena los SVGs en la rama `output`

### 3. Activación del Workflow
- **Workflow:** `Generate Snake Animation`
- **Acción:** Ejecución manual con `gh workflow run`
- **Resultado:** Dos runs en progreso (push y workflow_dispatch)

## Archivos Modificados

| Archivo | Estado | Descripción |
|---------|--------|-------------|
| `README.md` | Modificado | Nuevo diseño completo de perfil |
| `.github/workflows/snake.yml` | Creado | Workflow para snake animation |

## Configuración Técnica

### Permisos GitHub
- **Usuario autenticado:** SebastianMoralesDuque
- **Token scopes:** gist, read:org, repo, workflow
- **Acceso:** Commits, push, pull, issues, workflows, gists

### Referencias en README
- **Snake SVGs:** Referenciados desde la rama `output`
  - `https://raw.githubusercontent.com/sebastianmoralesduque/sebastianmoralesduque/output/github-snake.svg`
  - `https://raw.githubusercontent.com/sebastianmoralesduque/sebastianmoralesduque/output/github-snake-dark.svg`
- **Stats y trophies:** Usan APIs públicas de GitHub (readme-stats, streak-stats, profile-trophy)

## Verificación del Estado

### Para verificar el perfil:
1. Visitar: `https://github.com/SebastianMoralesDuque`
2. Verificar que el README se muestre correctamente
3. Comprobar que la snake animation aparezca en la sección de contribuciones

### Para verificar los workflows:
```bash
gh run list --limit 5
gh workflow list
```

### Para verificar la rama output:
```bash
git fetch origin output
git checkout output
ls -la
```

## Notas para Otros Agentes.

1. **Permisos:** El token tiene todos los permisos necesarios para modificar el repositorio
2. **Snake animation:** Los SVGs se generan en la rama `output`, no en `main`
3. **Auto-actualización:** El workflow se ejecuta diariamente a las 12:00 UTC
4. **Personalización:** Los parámetros del workflow pueden editarse en `.github/workflows/snake.yml`
5. **README:** El diseño usa múltiples APIs externas (capsule-render, skillicons.dev, etc.)

## Comandos Útiles

```bash
# Ver estado actual
git status
git log --oneline -5

# Ejecutar workflow manualmente
gh workflow run "Generate Snake Animation" --ref main

# Ver run recientes
gh run list --limit 3

# Ver detalles de un run específico
gh run view <run-id>
```
