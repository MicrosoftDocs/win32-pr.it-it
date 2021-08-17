---
description: Il mutex MSIExecute viene impostato solo durante l'elaborazione della tabella \_ InstallExecuteSequence, adminExecuteSequence o AdvtExecuteSequence.
ms.assetid: 2186422d-ccb2-4f7e-8c6d-326c00e0d9a9
title: _MSIExecute Mutex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cbca288c2d75051c1d6247a1123c453509c635df2872c3724d27d9a2fa27cc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066551"
---
# <a name="_msiexecute-mutex"></a>\_MSIExecute Mutex

Il mutex MSIExecute viene impostato solo durante l'elaborazione della tabella \_ [InstallExecuteSequence](installexecutesequence-table.md), della tabella [AdminExecuteSequence](adminexecutesequence-table.md)o della tabella [AdvtExecuteSequence](advtexecutesequence-table.md).

Poiché due installazioni non possono essere eseguite nello stesso processo, un tentativo di chiamare l'API del programma di installazione restituisce ERROR \_ INSTALL \_ ALREADY RUNNING \_ (1618) in due casi:

-   Mentre è \_ impostato il mutex MSIExecute.
-   Durante l'elaborazione della tabella [InstallUISequence o](installuisequence-table.md) della tabella [AdminUISequence](adminuisequence-table.md)da parte del processo corrente.

Per informazioni [sull'applicazione](event-logging.md) da installare, vedere Messaggi di registrazione eventi.

Nei casi in cui non è pratico restituire un errore ERROR INSTALL ALREADY RUNNING, è possibile recuperare lo stato corrente del servizio Windows Installer prima di provare ad avviare l'installazione usando la funzione \_ \_ \_ [**QueryServiceStatusEx.**](/windows/desktop/api/winsvc/nf-winsvc-queryservicestatusex) Il Windows Installer è attualmente in esecuzione se il valore del membro **dwControlsAccepted** della struttura [**SERVICE STATUS \_ \_ PROCESS**](/windows/desktop/api/winsvc/ns-winsvc-service_status_process) restituita è **SERVICE ACCEPT \_ \_ SHUTDOWN.**

**Windows Installer 2.0:** Non supportato. L'uso della [**funzione QueryServiceStatusEx**](/windows/desktop/api/winsvc/nf-winsvc-queryservicestatusex) per recuperare lo stato corrente del servizio Windows Installer richiede Windows Installer versione 3.0 o successiva.

 

 
