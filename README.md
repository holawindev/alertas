# 🚨 Proyecto ALERTAS – Ejemplo WinDev

Este proyecto demuestra cómo implementar una alerta visual (parpadeo del ícono en la taskbar) cuando la ventana de una app WinDev pierde el foco.

## 📋 Descripción

Funcionalidad basada en:
- Detección de ventana activa (via API `GetForegroundWindow`)
- Alternancia del ícono de la ventana usando `SendMessageW`
- Workaround específico para Windows 11, donde `FlashWindowEx` está bloqueado
- Control del parpadeo mediante `TimerSys`

> Incluye una documentación técnica detallada en `/DOCS/Documentación_ALERTAS.pdf`

## 🧠 Autor

👨‍💻 [@JuanBarbat](https://github.com/barbatdev)
📺 [HolaWindev – YouTube](https://www.youtube.com/@HolaWindev)
🎓 Formación, consultoría y comunidad sobre tecnologías PCSoft

## 🛠️ Requisitos

- WinDev 2025 o superior
- Proyecto Desktop (no compatible con WebDev)
- Sistema operativo Windows

## 🧪 ¿Cómo funciona?

Cuando el procedimiento `AlertBar()` se ejecuta, realiza lo siguiente:

1. Verifica si la ventana actual no está en primer plano.
2. Guarda el ícono original.
3. Alterna cada 500 ms el ícono con uno de alerta (`IDI_EXCLAMATION`) durante 10 ciclos o hasta que el usuario haga foco en la ventana.

## 💡 Extras

- El código está comentado y estructurado para aprendizaje.
- Útil como base para alertas no intrusivas en apps de escritorio.

---

📂 Proyecto parte del ecosistema [HolaWindev](https://holawindev.com)
