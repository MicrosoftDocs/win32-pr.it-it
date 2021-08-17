---
description: Elenca gli eventi di notifica di Winlogon.
ms.assetid: 48b0f389-5b3c-4b13-ad23-a8bc6bcd1850
title: Eventi di notifica di Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ea7359ef4d1d053e438d30564fcededbf3a0ccb10275cd6e4f669c2a20c54b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785717"
---
# <a name="winlogon-notification-events"></a>Eventi di notifica di Winlogon

[*Winlogon può*](../secgloss/w-gly.md) informare il pacchetto di notifica degli eventi seguenti.



| Event                               | Descrizione                                                                                                                                                                                                                                                                                                         |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Lock**<br/>                 | Questo evento si verifica quando l'utente blocca la workstation.<br/>                                                                                                                                                                                                                                                   |
| **Disconnessione**<br/>               | Questo evento si verifica quando un utente si disconnette dal sistema. **L'evento Disconnessione** viene eseguito in modo sincrono, anche se le impostazioni del Registro di sistema del pacchetto di notifica indicano che può gestire gli eventi in modo asincrono.<br/>                                                                                         |
| **Accesso**<br/>                | Questo evento si verifica quando un utente accede al sistema.<br/> Si noti che **l'evento Logon** si verifica prima del ripristino delle connessioni di rete dell'utente. Se il gestore eventi richiede l'accesso alle connessioni di rete dell'utente, deve gestire **l'evento StartShell** anziché l'evento **Logon.**<br/> |
| **Arresto**<br/>             | Questo evento si verifica subito prima dell'arresto del sistema.<br/>                                                                                                                                                                                                                                                     |
| **SmartCardLogonNotify**<br/> | Questo evento si verifica quando un utente accede al sistema con un smart card.<br/>                                                                                                                                                                                                                                   |
| **StartScreenSaver**<br/>     | Questo evento si verifica quando il screen saver è stato avviato. In genere, ciò si verifica dopo che un utente è stato inattivo per un periodo di tempo impostato.<br/> Le funzioni che gestisce questo evento non devono visualizzare un'interfaccia utente. **La notifica degli eventi StartScreenSaver** è destinata solo a scopo informativo.<br/> |
| **StartShell**<br/>           | Questo evento si verifica dopo che l'utente ha eseguito l'accesso al sistema, sono state stabilite connessioni di rete e il programma shell specificato dall'utente (in genere Windows Explorer) è stato avviato.<br/>                                                                                                                |
| **Avvio**<br/>              | Questo evento si verifica quando il sistema viene avviato o riavviato.<br/>                                                                                                                                                                                                                                               |
| **StopScreenSaver**<br/>      | Questo evento si verifica quando il screen saver è stato arrestato. In genere ciò si verifica quando è presente un'attività della tastiera o del mouse.<br/> Le funzioni che gestisce questo evento non devono visualizzare un'interfaccia utente. **La notifica dell'evento StopScreenSaver** è destinata solo a scopo informativo.<br/>                  |
| **Sblocca**<br/>               | Questo evento si verifica quando l'utente sblocca la workstation o quando un amministratore di sistema esegue l'override del blocco e disconnette l'utente.<br/>                                                                                                                                                                         |



 

 

 
