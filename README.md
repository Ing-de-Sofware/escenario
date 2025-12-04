# Calidad - Escenario

¡Excelente estrategia! Para responder con seguridad, necesitas tener muy claro el **"dolor"** de la empresa antes de tu intervención. Si el profesor pregunta "¿Contra qué estás comparando?", tú necesitas describir un escenario de **"Caos Controlado"** (típico de una empresa Nivel 2 que quiere pasar a Nivel 3).

Aquí tienes el **Guion del Escenario Base (AS-IS)** completo. Apréndete estos "hechos" como si realmente hubieras trabajado allí.

---

### 1. La Narrativa General (El "Dolor" del Negocio)

Situación Inicial:

"InnovaTech Solutions creció muy rápido en los últimos 3 años. Pasaron de ser una startup pequeña a tener 18 bancos como clientes1. Esto rompió su forma de trabajo artesanal."

El Problema Central:

"La empresa operaba como 'Islas Independientes'. El Squad de 'CreditPro' trabajaba de una forma muy distinta al Squad de 'InvestHub'2. Usaban herramientas (Jira, GitLab), pero sin estándares. Esto causaba que, cuando un desarrollador cambiaba de equipo, su productividad caía a cero porque no entendía el flujo del nuevo equipo."

---

### 2. Escenarios Específicos por Proceso (Tu "Evidencia")

Aquí tienes los problemas específicos que "encontraron" en el diagnóstico, listos para ser comparados con tus mejoras.

### A. En Gestión de Requisitos (El "Teléfono Malogrado")

- **Lo que había (AS-IS):** Los requisitos llegaban por correos, reuniones informales o tickets de Jira mal redactados. No existía una **Matriz de Trazabilidad**.
- **El problema real:** Se aprobaban cambios funcionales sin consultar a Seguridad o Arquitectura.
- 
    
    **Dato para el profe:** "En el diagnóstico, simulamos una revisión de un proyecto pasado donde el 30% de los defectos en producción se debían a requisitos ambiguos que el desarrollador interpretó a su manera"3.
    
- **Tu Mejora:** Implementamos la **Trazabilidad Bidireccional** y el comité de cambios (CCB).

### B. En Desarrollo y Configuración (El "Infierno de Versiones")

- **Lo que había (AS-IS):** Tenían GitLab, pero el control de versiones era manual. A veces, un desarrollador sobrescribía el código de otro. El despliegue a producción dependía de un "héroe" (el DevOps senior) que sabía los pasos de memoria.
- **El problema real:** Si el DevOps se enfermaba, no había pase a producción. No había auditoría de qué versión exacta estaba en el servidor.
- 
    
    **Dato para el profe:** "Detectamos que no existía una **Línea Base (Baseline)** formal antes de los pases a producción. La integridad dependía de la memoria de las personas, no del proceso"4.
    
- **Tu Mejora:** Automatización con CI/CD y **Auditorías de Configuración (PCA)** antes del despliegue.

### C. En Seguridad (El "Bombero")

- **Lo que había (AS-IS):** La seguridad era **reactiva**. Hacían un escaneo de vulnerabilidades (Pentesting) justo *un día antes* de salir a producción.
- **El problema real:** Si encontraban una falla crítica un día antes, tenían que retrasar el lanzamiento o salir con riesgo (asumiendo multas).
- 
    
    **Dato para el profe:** "La empresa no tenía un **Plan de Tratamiento de Riesgos** formal. Los incidentes se resolvían, pero no se registraban lecciones aprendidas, por lo que el mismo ataque ocurría meses después"5.
    
- **Tu Mejora:** **Security by Design** (seguridad desde el diseño) y análisis estático (SAST) durante el desarrollo, no al final.

### D. En Gestión de Proyectos (La "Bola de Cristal")

- **Lo que había (AS-IS):** Se gestionaba por "sensación". El Project Manager preguntaba "¿Cómo vas?" y el desarrollador decía "Bien, al 90%".
- **El problema real:** Ese "90%" era subjetivo. Los proyectos siempre se atrasaban en el último 10%. No usaban métricas objetivas.
- 
    
    **Dato para el profe:** "No existía cálculo de **SPI (Índice de desempeño del cronograma)** ni **CPI (Índice de costo)**. Las estimaciones se basaban puramente en juicio experto sin datos históricos"6.
    
- **Tu Mejora:** Gestión Cuantitativa (Nivel 4) usando métricas de Valor Ganado (EVM) y simulación de riesgos.

### 3. Tabla Resumen para tu "Chulla" (Cheat Sheet)

Si te preguntan "¿Qué mejoraron?", usa esta tabla mental:

Área	Escenario "AS-IS" (Lo que supusimos)	Escenario "TO-BE" (Tu mejora)
Estándar	Cada Líder Técnico definía su forma de trabajar.	Repositorio Organizacional (OPD) único para todos.
Calidad	Revisión por pares informal ("mírame el código").	Quality Gates automáticos en SonarQube.
Riesgos	Cualitativo ("Me parece que es riesgo alto").	Cuantitativo (Simulación Monte Carlo: "80% de prob.").
Cambios	Se aceptaban cambios por chat/correo.	Comité de Control de Cambios (CCB) formal.
Seguridad	Al final del ciclo (Testing).	Integrada en todo el ciclo (DevSecOps).

### 4. Cómo decirlo en la exposición (Frase Ganadora)

Cuando te pregunten sobre la comparación, di esto:

> "Profesor, nuestro escenario base (AS-IS) fue diseñado representando una típica empresa Nivel 2: funcional pero dependiente de las personas.
> 
> 
> Por ejemplo, en el **Proceso de Desarrollo**, nuestra simulación estableció que el código funcionaba, pero las revisiones de seguridad eran manuales y tardías, generando un alto costo de retrabajo.
> 
> Nuestra mejora (**TO-BE**) no fue solo 'poner herramientas', sino cambiar el flujo: movimos la seguridad al inicio (Shift Left) e institucionalizamos las métricas. Pasamos de 'creer que vamos bien' a 'saber estadísticamente cómo vamos' mediante las prácticas de CMMI."
> 

Con este contexto, ya no tienes una "empresa fantasma", tienes un **Caso de Estudio Controlado**. ¡Dale con todo!

¡Excelente idea! Para que tu escenario base sea irrefutable ante las preguntas del profesor, es fundamental que la documentación **exista**, pero que sea **obsoleta o inconsistente**. Esto justifica por qué, a pesar de tener papeles, la empresa se mantiene en el Nivel 2.

Aquí tienes el complemento de la **Línea Base (AS-IS)** de InnovaTech Solutions, detallando el estado de sus documentos internos y la brecha CMMI que esta deficiencia genera:

## 📄 Complemento Documental del Escenario Base (AS-IS)

La Dirección de TI de InnovaTech Solutions posee un conjunto de documentos heredados de sus inicios, pero estos son incompletos, inconsistentes y no se usan de manera sistemática u obligatoria1.

Documento Existente (Simulado)	Proceso Clave	Estatus / Problema Crítico (AS-IS)	CMMI Brecha Justificada
Manual de Procesos de TI (MPT-2022)	General	Obsoleto2. Describe el ciclo de vida en cascada, mientras que los equipos operan bajo un modelo Scrum-Híbrido3. Solo cubre los procesos de Desarrollo y Mantenimiento, no la seguridad.	OPD (Organizational Process Definition) - El proceso definido no refleja la realidad operativa.
Directiva de Requisitos (DR-001)	Gestión de Requisitos	No existe una plantilla estandarizada4. Los requisitos se documentan, pero la Trazabilidad Bidireccional (Requisito $\rightarrow$ Prueba) es parcial o se hace manualmente5555.	RDM (Requirements Management) / VAL (Validation) - Falta de formalidad y automatización en la vinculación.
Política de Control de Cambios (PCC-TI)	Gestión de Configuración	No estipula un CCB formal666. Las aprobaciones de cambios mayores a la línea base se gestionan por correo o chat y son propensas a errores y retrasos7.	CM (Configuration Management) / GOV (Governance) - El control es manual, no estructurado y reactivo.
Guía de Codificación Segura (GCS)	Desarrollo y Seguridad	Existe, pero su uso es opcional8888. No está integrada de forma obligatoria al pipeline de Integración Continua (CI/CD)9999.	PQA (Process Quality Assurance) / VER (Verification) - La calidad no es asegurada ni consistente.
Registro de Riesgos (RR-Excel)	Gestión de Riesgos	Formato informal en Excel10. Solo registra riesgos de proyecto (plazo/costo), excluyendo riesgos de seguridad de la información11. No tiene escala de cuantificación (Nivel 4) ni KRIs12.	RSK (Risk Management) - No es integral ni sistemático.
Directiva de Soporte y Operación (DSO)	Operación y Mantenimiento	Se enfoca en la disponibilidad (Uptime), pero no exige métricas de calidad de servicio13. Faltan indicadores predictivos como MTTR o MTBF para el análisis de tendencias141414141414141414.	MA (Measurement and Analysis) - La gestión es reactiva, no predictiva.

## 💡 Estrategia de Defensa para el Profesor

Cuando el profesor pregunte por la evidencia de los vacíos, utiliza la técnica de **"Existía, pero no estaba institucionalizado o automatizado"**.

### Pregunta del Profesor sobre Evidencia

Pregunta Trampa del Profesor	Tu Respuesta (Usando la Línea Base)
"¿Qué documentos tomó usted para concluir que no había estándares de calidad?" 15	"Profesor, analizamos dos documentos clave: el Manual de Procesos de TI (MPT-2022), que estaba obsoleto, y la Guía de Codificación Segura. Concluimos que, aunque la guía existía, su aplicación era solo en un equipo (CreditPro), lo que es una brecha de PQA; la calidad no estaba institucionalizada a nivel de la organización, sino que dependía de la disciplina individual16."
	"¿Qué criterios sistemáticos de tratamiento quería ver en Gestión de Riesgos?" 17
	"¿Cómo mide que estamos bien?" 18


  
