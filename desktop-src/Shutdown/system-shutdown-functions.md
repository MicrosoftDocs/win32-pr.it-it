---
description: Le funzioni seguenti vengono utilizzate con l'arresto del sistema.
ms.assetid: 6a08a769-1acf-49eb-ba95-beaf56a374bf
title: Funzioni di arresto del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd457c86129b3e5f80d6359018c1474f837b9e33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967608"
---
# <a name="system-shutdown-functions"></a>Funzioni di arresto del sistema

Le funzioni seguenti vengono utilizzate con l'arresto del sistema.



| Funzione                                                         | Descrizione                                                                                                                         |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**AbortSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-abortsystemshutdowna)               | Arresta un arresto del sistema che è stato avviato.                                                                                    |
| [**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows)                               | Disconnette l'utente interattivo.                                                                                                      |
| [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex)                           | Disconnette l'utente interattivo, arresta il sistema o arresta e riavvia il sistema...                                        |
| [**InitiateShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiateshutdowna)                     | Avvia un arresto e un riavvio del computer specificato e riavvia tutte le applicazioni che sono state registrate per il riavvio.    |
| [**InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna)         | Avvia un arresto e un riavvio facoltativo del computer specificato.                                                                |
| [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa)     | Avvia un arresto e un riavvio facoltativo del computer specificato e, facoltativamente, registra il motivo dell'arresto.            |
| [**LockWorkStation**](/windows/desktop/api/Winuser/nf-winuser-lockworkstation)                       | Blocca la visualizzazione della workstation.                                                                                                    |
| [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate)   | Indica che il sistema non può essere arrestato e imposta una stringa del motivo da visualizzare all'utente se l'arresto del sistema è stato avviato. |
| [**ShutdownBlockReasonDestroy**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasondestroy) | Indica che è possibile arrestare il sistema e liberare la stringa del motivo.                                                             |
| [**ShutdownBlockReasonQuery**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasonquery)     | Recupera la stringa del motivo impostata dalla funzione [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) .                     |



 

 

 



