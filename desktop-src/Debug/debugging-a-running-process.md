---
description: Per eseguire il debug di un processo già in esecuzione, il debugger deve usare DebugActiveProcess con l'identificatore di processo. Per recuperare un elenco di identificatori di processo, usare la funzione EnumProcesses o Process32First.
ms.assetid: 2662411f-a69a-442b-a177-a27ea025bb01
title: Debug di un processo in esecuzione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f93d184907bb66a651f04a5e144e40bf5955a672
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125736"
---
# <a name="debugging-a-running-process"></a>Debug di un processo in esecuzione

Per eseguire il debug di un processo già in esecuzione, il debugger deve usare [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) con l'identificatore di processo. Per recuperare un elenco di identificatori di processo, usare la funzione [**EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses) o [**Process32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first) .

[**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) connette il debugger al processo attivo. In questo caso, è possibile eseguire il debug solo del processo attivo; i processi figlio non possono. Il debugger deve disporre dell'accesso appropriato al processo in esecuzione per usare **DebugActiveProcess**. Per ulteriori informazioni sui diritti di accesso, vedere [Access Control](../secauthz/access-control.md).

Dopo aver creato o collegato il debugger al processo di cui si intende eseguire il debug, il sistema invia una notifica al debugger di tutti gli eventi di debug che si verificano nel processo e, se specificato, in tutti i processi figlio. Per ulteriori informazioni sugli eventi di debug, vedere [debug di eventi](debugging-events.md).

Per scollegare dal processo di cui è in corso il debug, il debugger deve usare la funzione [**DebugActiveProcessStop**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocessstop) .

 

 
