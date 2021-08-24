---
description: Le funzioni seguenti vengono usate con l'arresto del sistema.
ms.assetid: 6a08a769-1acf-49eb-ba95-beaf56a374bf
title: Funzioni di arresto del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36b1304a2333d817be7cbb51ee599f37cda8b3e185f56cfc5959f1646e9ab639
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664341"
---
# <a name="system-shutdown-functions"></a>Funzioni di arresto del sistema

Le funzioni seguenti vengono usate con l'arresto del sistema.



| Funzione                                                         | Descrizione                                                                                                                         |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**AbortSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-abortsystemshutdowna)               | Arresta un arresto del sistema avviato.                                                                                    |
| [**ExitWindows**](/windows/desktop/api/Winuser/nf-winuser-exitwindows)                               | Disconnette l'utente interattivo.                                                                                                      |
| [**Exitwindowsex**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex)                           | Disconnette l'utente interattivo, arresta il sistema o arresta e riavvia il sistema.                                        |
| [**InitiateShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiateshutdowna)                     | Avvia un arresto e un riavvio del computer specificato e riavvia tutte le applicazioni registrate per il riavvio.    |
| [**InitiateSystemShutdown**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna)         | Avvia un arresto e un riavvio facoltativo del computer specificato.                                                                |
| [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa)     | Avvia un arresto e un riavvio facoltativo del computer specificato e, facoltativamente, registra il motivo dell'arresto.            |
| [**LockWorkStation**](/windows/desktop/api/Winuser/nf-winuser-lockworkstation)                       | Blocca la visualizzazione della workstation.                                                                                                    |
| [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate)   | Indica che non è possibile arrestare il sistema e imposta una stringa di motivo da visualizzare all'utente se viene avviato l'arresto del sistema. |
| [**ShutdownBlockReasonDestroy**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasondestroy) | Indica che il sistema può essere arrestato e libera la stringa del motivo.                                                             |
| [**ShutdownBlockReasonQuery**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasonquery)     | Recupera la stringa del motivo impostata dalla [**funzione ShutdownBlockReasonCreate.**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate)                     |



 

 

 



