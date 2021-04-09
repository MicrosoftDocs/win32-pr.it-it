---
description: Elenca gli eventi di notifica di Winlogon.
ms.assetid: 48b0f389-5b3c-4b13-ad23-a8bc6bcd1850
title: Eventi di notifica Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58827dc2699c92dfc3a814d2366608e1bd3fb662
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879034"
---
# <a name="winlogon-notification-events"></a>Eventi di notifica Winlogon

[*Winlogon*](../secgloss/w-gly.md) può informare il pacchetto di notifiche degli eventi seguenti.



| Event                               | Descrizione                                                                                                                                                                                                                                                                                                         |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Lock**<br/>                 | Questo evento si verifica quando l'utente blocca la workstation.<br/>                                                                                                                                                                                                                                                   |
| **Disconnessione**<br/>               | Questo evento si verifica quando un utente si disconnette dal sistema. L'evento di **disconnessione** viene eseguito in modo sincrono, anche se le impostazioni del registro di sistema del pacchetto di notifica indicano che è in grado di gestire eventi in modo asincrono.<br/>                                                                                         |
| **Accesso**<br/>                | Questo evento si verifica quando un utente accede al sistema.<br/> Si noti che l'evento **Logon** si verifica prima del ripristino delle connessioni di rete dell'utente. Se il gestore eventi richiede l'accesso alle connessioni di rete dell'utente, deve gestire l'evento **StartShell** anziché l'evento **Logon** .<br/> |
| **Arresto**<br/>             | Questo evento si verifica subito prima dell'arresto del sistema.<br/>                                                                                                                                                                                                                                                     |
| **SmartCardLogonNotify**<br/> | Questo evento si verifica quando un utente accede al sistema con una smart card.<br/>                                                                                                                                                                                                                                   |
| **StartScreenSaver**<br/>     | Questo evento si verifica quando il screen saver è stato avviato. Questa situazione si verifica in genere quando un utente è rimasto inattivo per un determinato periodo di tempo.<br/> Le funzioni che gestiscono questo evento non devono visualizzare un'interfaccia utente. La notifica degli eventi di **StartScreenSaver** è esclusivamente a scopo informativo.<br/> |
| **StartShell**<br/>           | Questo evento si verifica dopo che l'utente ha eseguito l'accesso al sistema, sono state stabilite connessioni di rete e il programma della shell specificato dall'utente (in genere Esplora risorse) è stato avviato.<br/>                                                                                                                |
| **Avvio**<br/>              | Questo evento si verifica quando il sistema viene avviato o riavviato.<br/>                                                                                                                                                                                                                                               |
| **StopScreenSaver**<br/>      | Questo evento si verifica quando il screen saver è stato arrestato. Questa situazione si verifica in genere quando è attiva la tastiera o l'attività del mouse.<br/> Le funzioni che gestiscono questo evento non devono visualizzare un'interfaccia utente. La notifica degli eventi di **StopScreenSaver** è esclusivamente a scopo informativo.<br/>                  |
| **Sblocca**<br/>               | Questo evento si verifica quando l'utente sblocca la workstation o quando un amministratore di sistema esegue l'override del blocco e disconnette l'utente.<br/>                                                                                                                                                                         |



 

 

 
