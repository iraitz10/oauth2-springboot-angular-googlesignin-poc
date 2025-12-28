# Evidencias de Implementación - OKR 4

## Objetivo: Reducir brecha de seguridad

### 4.1: Controlar SBOM 
- **Implementado**: Generación automática de SBOM en formato CycloneDX
- **Evidencia**: Archivo `sbom-cyclonedx.json` generado en cada ejecución
- **Comparación**: Sistema configurado para comparar con versión anterior
- **Alerta**: Detecta cambios y genera notificación

### 4.2: Escaneo post-despliegue 
- **Implementado**: Escaneo automático después de cada despliegue
- **Frecuencia**: Programado semanalmente + trigger por cambios
- **Herramientas**: Análisis de dependencias y configuración
- **Evidencia**: `security-scan-report.md` generado automáticamente

### 4.3: Binarios versionados 
- **Implementado**: Sistema de versionado semántico automático
- **Formato**: vMAJOR.MINOR.PATCH-COMMIT (ej: v1.0.123-abc123def)
- **Almacenamiento**: GitHub Artifacts + checksum SHA256
- **Verificación**: Firmas digitales implementadas

### 4.4: Detección de secrets 
- **Implementado**: Escaneo automático de secrets en código
- **Prevención**: Template .env.example + GitHub Secrets
- **Detección**: Herramientas configuradas para identificar credenciales
- **Principio CIA**: Confidencialidad, Integridad, Disponibilidad garantizadas

### 4.5: Políticas de compliance 
- **Cumplimiento**: 83% de requisitos ISO 27001 y RGPD (i=83)
- **Documentación**: Políticas generadas automáticamente
- **Controles**: 10/12 controles implementados
- **Evidencia**: Checklist y acuerdos en `/documentation/compliance/`

---

## **Cómo verificar la implementación:**

1. **Ejecutar el workflow manualmente** desde GitHub Actions
2. **Revisar los artifacts generados** en cada ejecución
3. **Consultar la documentación** en `/documentation/compliance/`
4. **Verificar los reports** generados automáticamente

---

## **Métricas cumplidas:**

| Sub-OKR | Estado | Valor | Evidencia |
|---------|--------|-------|-----------|
| 4.1 | ✅ | SBOM generado y comparado | sbom-cyclonedx.json |
| 4.2 | ✅ | Escaneo post-despliegue | security-scan-report.md |
| 4.3 | ✅ | Versionado semántico | dist/*.jar + checksum |
| 4.4 | ✅ | 0 secrets detectados | gitleaks-report.json |
| 4.5 | ✅ | i=83% cumplimiento | SECURITY_POLICY.md |

---

**Fecha de implementación**: 28/12/2025  
**Responsable**: Iraitz Aiesa
**Repositorio**: https://github.com/iraitz10/oauth2-springboot-angular-googlesignin-poc
