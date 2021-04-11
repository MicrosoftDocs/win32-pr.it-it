---
title: Operazioni di connessione RAS
description: Windows NT e versioni successive forniscono le funzioni RasPhonebookDlg e RasDialDlg che visualizzano l'interfaccia utente predefinita per l'avvio di un'operazione di connessione RAS.
ms.assetid: 1e0f82e1-5995-4b47-970b-e6a7ff6d52e0
keywords:
- Operazioni di connessione, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0e2a78d34afd5aea3670730656e97886b6a5916
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872737"
---
# <a name="ras-connection-operations"></a>Operazioni di connessione RAS

Windows NT e versioni successive forniscono le funzioni [**RasPhonebookDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasphonebookdlga) e [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga) che visualizzano l'interfaccia utente predefinita per l'avvio di un'operazione di connessione RAS. Per la maggior parte delle applicazioni, questo è il modo migliore per avviare un'operazione di connessione RAS. Windows 95 attualmente non supporta queste funzioni.

Nella parte restante di questa sezione vengono descritte le funzioni di basso livello per l'avvio di una connessione RAS. Queste funzioni sono disponibili in bothWindows NT 4,0 (e versioni successive) e Windows 95.

Un'applicazione client RAS utilizza la funzione [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) per stabilire una connessione a un server RAS. La funzione **RasDial** avvia l'operazione di connessione, che viene quindi eseguita dalla gestione connessione di accesso remoto.

Gestione connessione di accesso remoto è un servizio che gestisce i dettagli per stabilire la connessione al server remoto. Questo servizio fornisce inoltre al client informazioni sullo stato durante l'operazione di connessione. La gestione connessione di accesso remoto viene avviata automaticamente quando un'applicazione carica il RASAPI32.DLL.

La chiamata [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) specifica le informazioni seguenti quando avvia un'operazione di connessione:

-   [Informazioni di connessione](phone-book-files-and-connection-information.md) necessarie alla gestione connessione di accesso remoto per stabilire la connessione.
-   Gestore di [notifiche](notification-handlers.md) facoltativo che riceve le notifiche di stato durante l'operazione di connessione. Se la chiamata [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) specifica un gestore di notifiche, la chiamata è [asincrona](asynchronous-operations.md); in caso contrario, è [sincrono](synchronous-operations.md).
-   Struttura [**RASDIALEXTENSIONS**](/previous-versions/windows/desktop/legacy/aa377029(v=vs.85)) facoltativa per abilitare o disabilitare le estensioni per l'operazione [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) . Le estensioni consentono a un client RAS di abilitare direttamente alcune impostazioni del modem, controllare se RAS utilizza i prefissi e i suffissi in una voce della rubrica telefonica e per supportare [gli stati sospesi](paused-states.md) durante l'operazione di connessione.

 

 