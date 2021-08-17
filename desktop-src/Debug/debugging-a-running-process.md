---
description: Per eseguire il debug di un processo già in esecuzione, il debugger deve usare DebugActiveProcess con l'identificatore del processo. Per recuperare un elenco di identificatori di processo, usare la funzione EnumProcesses o Process32First.
ms.assetid: 2662411f-a69a-442b-a177-a27ea025bb01
title: Debug di un processo in esecuzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f3cf141da9905c76659c2ae11e9b82e2e2f5fee9bd934dce835b129678995ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119279351"
---
# <a name="debugging-a-running-process"></a>Debug di un processo in esecuzione

Per eseguire il debug di un processo già in esecuzione, il debugger deve [**usare DebugActiveProcess con**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) l'identificatore del processo. Per recuperare un elenco di identificatori di processo, usare la [**funzione EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses) o [**Process32First.**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first)

[**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) collega il debugger al processo attivo. In questo caso, è possibile eseguire il debug solo del processo attivo. i processi figlio non possono. Il debugger deve avere accesso appropriato al processo in esecuzione per usare **DebugActiveProcess**. Per altre informazioni sui diritti di accesso, vedere [Controllo di accesso](../secauthz/access-control.md).

Dopo che il debugger ha creato o collegato se stesso al processo di cui intende eseguire il debug, il sistema notifica al debugger tutti gli eventi di debug che si verificano nel processo e, se specificati, in tutti i processi figlio. Per altre informazioni sul debug degli eventi, vedere [Debug di eventi](debugging-events.md).

Per disconnettersi dal processo in fase di debug, il debugger deve usare la [**funzione DebugActiveProcessStop.**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocessstop)

 

 
