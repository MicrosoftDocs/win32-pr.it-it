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
# <a name="debugging-a-running-process"></a><span data-ttu-id="2a95f-104">Debug di un processo in esecuzione</span><span class="sxs-lookup"><span data-stu-id="2a95f-104">Debugging a Running Process</span></span>

<span data-ttu-id="2a95f-105">Per eseguire il debug di un processo già in esecuzione, il debugger deve usare [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) con l'identificatore di processo.</span><span class="sxs-lookup"><span data-stu-id="2a95f-105">To debug a process that is already running, the debugger should use [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) with the process identifier.</span></span> <span data-ttu-id="2a95f-106">Per recuperare un elenco di identificatori di processo, usare la funzione [**EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses) o [**Process32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first) .</span><span class="sxs-lookup"><span data-stu-id="2a95f-106">To retrieve a list of process identifiers, use either the [**EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses) or [**Process32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first) function.</span></span>

<span data-ttu-id="2a95f-107">[**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) connette il debugger al processo attivo.</span><span class="sxs-lookup"><span data-stu-id="2a95f-107">[**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) attaches the debugger to the active process.</span></span> <span data-ttu-id="2a95f-108">In questo caso, è possibile eseguire il debug solo del processo attivo; i processi figlio non possono.</span><span class="sxs-lookup"><span data-stu-id="2a95f-108">In this case, only the active process can be debugged; its child processes cannot.</span></span> <span data-ttu-id="2a95f-109">Il debugger deve disporre dell'accesso appropriato al processo in esecuzione per usare **DebugActiveProcess**.</span><span class="sxs-lookup"><span data-stu-id="2a95f-109">The debugger must have appropriate access to the executing process to use **DebugActiveProcess**.</span></span> <span data-ttu-id="2a95f-110">Per ulteriori informazioni sui diritti di accesso, vedere [Access Control](../secauthz/access-control.md).</span><span class="sxs-lookup"><span data-stu-id="2a95f-110">For more information about access rights, see [Access Control](../secauthz/access-control.md).</span></span>

<span data-ttu-id="2a95f-111">Dopo aver creato o collegato il debugger al processo di cui si intende eseguire il debug, il sistema invia una notifica al debugger di tutti gli eventi di debug che si verificano nel processo e, se specificato, in tutti i processi figlio.</span><span class="sxs-lookup"><span data-stu-id="2a95f-111">After the debugger has either created or attached itself to the process it intends to debug, the system notifies the debugger of all debugging events that occur in the process, and, if specified, in any child processes.</span></span> <span data-ttu-id="2a95f-112">Per ulteriori informazioni sugli eventi di debug, vedere [debug di eventi](debugging-events.md).</span><span class="sxs-lookup"><span data-stu-id="2a95f-112">For more information about debugging events, see [Debugging Events](debugging-events.md).</span></span>

<span data-ttu-id="2a95f-113">Per scollegare dal processo di cui è in corso il debug, il debugger deve usare la funzione [**DebugActiveProcessStop**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocessstop) .</span><span class="sxs-lookup"><span data-stu-id="2a95f-113">To detach from the process being debugged, the debugger should use the [**DebugActiveProcessStop**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocessstop) function.</span></span>

 

 
