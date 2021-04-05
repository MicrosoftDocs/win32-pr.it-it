---
description: Il \_ mutex MSIExecute viene impostato solo durante l'elaborazione della tabella InstallExecuteSequence, della tabella AdminExecuteSequence o della tabella AdvtExecuteSequence.
ms.assetid: 2186422d-ccb2-4f7e-8c6d-326c00e0d9a9
title: Mutex _MSIExecute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c22a9ca79e83e8593c2ee99884965acfd414ff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881198"
---
# <a name="_msiexecute-mutex"></a>\_Mutex MSIExecute

Il \_ mutex MSIExecute viene impostato solo durante l'elaborazione della tabella [InstallExecuteSequence](installexecutesequence-table.md), della [tabella AdminExecuteSequence](adminexecutesequence-table.md)o della [tabella AdvtExecuteSequence](advtexecutesequence-table.md).

Poiché non è possibile eseguire due installazioni nello stesso processo, un tentativo di chiamare il Application Programming Interface (API) del programma di installazione restituisce l'errore di \_ installazione \_ già in \_ esecuzione (1618) in due casi:

-   Mentre \_ è impostato il mutex MSIExecute.
-   Mentre il processo corrente sta elaborando la tabella [InstallUISequence](installuisequence-table.md) o la [tabella AdminUISequence](adminuisequence-table.md).

Per informazioni sull'applicazione installata, vedere i messaggi di [registrazione eventi](event-logging.md) .

Nei casi in cui è impraticabile restituire un errore di \_ installazione \_ già \_ in esecuzione, è possibile recuperare lo stato corrente del servizio Windows Installer prima di tentare di avviare l'installazione tramite la funzione [**QueryServiceStatusEx**](/windows/desktop/api/winsvc/nf-winsvc-queryservicestatusex) . Il servizio Windows Installer è attualmente in esecuzione se il valore del membro **dwControlsAccepted** della struttura del [**\_ \_ processo di stato del servizio**](/windows/desktop/api/winsvc/ns-winsvc-service_status_process) restituito è **servizio \_ accettazione \_ arresto**.

**Windows Installer 2,0:** Non supportato. L'uso della funzione [**QueryServiceStatusEx**](/windows/desktop/api/winsvc/nf-winsvc-queryservicestatusex) per recuperare lo stato corrente del servizio Windows Installer richiede Windows Installer versione 3,0 o successiva.

 

 
