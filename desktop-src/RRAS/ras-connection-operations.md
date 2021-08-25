---
title: Operazioni di connessione RAS
description: Windows NT e versioni successive forniscono le funzioni RasPhonebookDlg e RasDialDlg che visualizzano l'interfaccia utente predefinita per l'avvio di un'operazione di connessione RAS.
ms.assetid: 1e0f82e1-5995-4b47-970b-e6a7ff6d52e0
keywords:
- Operazioni di connessione, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27e86ddf1586ce11f43e6b34ef15b89cb2d382b28911968f0b0f08dabd086a86
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868461"
---
# <a name="ras-connection-operations"></a>Operazioni di connessione RAS

Windows NT e versioni successive forniscono le funzioni [**RasPhonebookDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasphonebookdlga) e [**RasDialDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga) che visualizzano l'interfaccia utente predefinita per l'avvio di un'operazione di connessione RAS. Per la maggior parte delle applicazioni, questo è il modo migliore per avviare un'operazione di connessione RAS. Windows 95 non supporta attualmente queste funzioni.

Nella parte restante di questa sezione vengono descritte le funzioni di basso livello per l'avvio di una connessione RAS. Queste funzioni sono disponibili sia in Windows NT 4.0 (e versioni successive) che Windows 95.

Un'applicazione client RAS usa [**la funzione RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) per stabilire una connessione a un server RAS. La **funzione RasDial** avvia l'operazione di connessione, che viene quindi eseguita dal servizio di accesso Gestione connessioni.

L'Gestione connessioni accesso remoto è un servizio che gestisce i dettagli di stabilire la connessione al server remoto. Questo servizio fornisce inoltre al client informazioni sullo stato durante l'operazione di connessione. L'accesso Gestione connessioni viene avviato automaticamente quando un'applicazione carica il RASAPI32.DLL.

La [**chiamata RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) specifica le informazioni seguenti quando avvia un'operazione di connessione:

-   Informazioni [di connessione](phone-book-files-and-connection-information.md) necessarie al Gestione connessioni accesso remoto per stabilire la connessione.
-   Gestore di [notifica facoltativo che](notification-handlers.md) riceve le notifiche di stato durante l'operazione di connessione. Se la [**chiamata RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) specifica un gestore di notifica, la chiamata è [asincrona.](asynchronous-operations.md) In caso contrario, [è sincrono.](synchronous-operations.md)
-   Struttura [**RASDIALEXTENSIONS facoltativa**](/previous-versions/windows/desktop/legacy/aa377029(v=vs.85)) per abilitare o disabilitare le estensioni per [**l'operazione RasDial.**](/windows/desktop/api/Ras/nf-ras-rasdiala) Le estensioni consentono a un client RAS di abilitare direttamente alcune impostazioni del modem, di controllare se [](paused-states.md) RAS usa i prefissi e i suffissi in una voce della rubrica e di supportare gli stati sospesi durante l'operazione di connessione.

 

 