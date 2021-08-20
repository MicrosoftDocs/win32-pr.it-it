---
title: Funzioni principali dell'API della shell client
description: La tabella seguente offre una panoramica delle funzioni di base per l Windows aPI della shell client di gestione remota (WinRM).
ms.assetid: cd0e6b55-03e8-4ebe-aea8-35d268cdb18c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f36a081723af60acf08aa9b4123cc124c2635371bfb50053da457289343ceec5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118113344"
---
# <a name="client-shell-api-core-functions"></a>Funzioni principali dell'API della shell client

La tabella seguente offre una panoramica delle funzioni di base per l Windows aPI della shell client di gestione remota (WinRM).



| Funzioni di base                                                   | Descrizione                                                                                                                                                                     |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WSManCloseCommand**](/windows/desktop/api/Wsman/nf-wsman-wsmanclosecommand)                   | Chiude un comando.                                                                                                                                                               |
| [**WSManCloseOperation**](/windows/desktop/api/Wsman/nf-wsman-wsmancloseoperation)               | Chiude un'operazione.                                                                                                                                                            |
| [**WSManCloseSession**](/windows/desktop/api/Wsman/nf-wsman-wsmanclosesession)                   | Chiude una sessione di Gestione remota Windows.                                                                                                                                                         |
| [**WSManCloseShell**](/windows/desktop/api/Wsman/nf-wsman-wsmancloseshell)                       | Chiude un oggetto shell.                                                                                                                                                          |
| [**WSManConnectShell**](/windows/desktop/api/Wsman/nf-wsman-wsmanconnectshell)                   | Si connette a una sessione del server esistente.                                                                                                                                         |
| [**WSManConnectShellCommand**](/windows/desktop/api/Wsman/nf-wsman-wsmanconnectshellcommand)     | Si connette a un comando esistente in esecuzione in una shell.                                                                                                                             |
| [**WSManCreateSession**](/windows/desktop/api/Wsman/nf-wsman-wsmancreatesession)                 | Crea una sessione winrm.                                                                                                                                                        |
| [**WSManCreateShell**](/windows/desktop/api/Wsman/nf-wsman-wsmancreateshell)                     | Crea un oggetto shell.                                                                                                                                                         |
| [**WSManCreateShellEx**](/windows/desktop/api/Wsman/nf-wsman-wsmancreateshellex)                 | Crea un oggetto shell usando la stessa funzionalità della [**funzione WSManCreateShell,**](/windows/desktop/api/Wsman/nf-wsman-wsmancreateshell) con l'aggiunta di un ID shell specificato dal client.          |
| [**WSManDeinitialize**](/windows/desktop/api/Wsman/nf-wsman-wsmandeinitialize)                   | Deinitializes the WinRM client stack.                                                                                                                                           |
| [**WSManDisconnectShell**](/windows/desktop/api/Wsman/nf-wsman-wsmandisconnectshell)             | Disconnette la connessione di rete di una shell attiva e dei comandi associati.                                                                                              |
| [**WSManInitialize**](/windows/desktop/api/Wsman/nf-wsman-wsmaninitialize)                       | Inizializza WinRM.                                                                                                                                                              |
| [**WSManReceiveShellOutput**](/windows/desktop/api/Wsman/nf-wsman-wsmanreceiveshelloutput)       | Riceve l'output della shell.                                                                                                                                                          |
| [**WSManReconnectShell**](/windows/desktop/api/Wsman/nf-wsman-wsmanreconnectshell)               | Riconnette una sessione della shell disconnessa in precedenza. Per riconnettere i comandi associati della sessione shell, usare [**WSManReconnectShellCommand**](/windows/desktop/api/Wsman/nf-wsman-wsmanreconnectshellcommand). |
| [**WSManReconnectShellCommand**](/windows/desktop/api/Wsman/nf-wsman-wsmanreconnectshellcommand) | Riconnette un comando precedentemente disconnesso.                                                                                                                                   |
| [**WSManRunShellCommand**](/windows/desktop/api/Wsman/nf-wsman-wsmanrunshellcommand)             | Esegue un comando della shell.                                                                                                                                                           |
| [**WSManRunShellCommandEx**](/windows/desktop/api/Wsman/nf-wsman-wsmanrunshellcommandex)         | Fornisce la stessa funzionalità della funzione [**WSManRunShellCommand,**](/windows/desktop/api/Wsman/nf-wsman-wsmanrunshellcommand) con l'aggiunta di un'opzione di ID di comando.                                 |
| [**WSManSendShellInput**](/windows/desktop/api/Wsman/nf-wsman-wsmansendshellinput)               | Invia l'input a una shell.                                                                                                                                                         |
| [**WSManSignalShell**](/windows/desktop/api/Wsman/nf-wsman-wsmansignalshell)                     | Segnala una shell.                                                                                                                                                                |



 

 

 




