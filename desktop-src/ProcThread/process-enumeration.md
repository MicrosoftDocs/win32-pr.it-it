---
description: Tutti gli utenti hanno accesso in lettura all'elenco di processi nel sistema e sono disponibili diverse funzioni che enumerano i processi attivi. La funzione da usare dipende da fattori quali il supporto della piattaforma desiderata.
ms.assetid: 4c73fb10-7ee8-4d8a-9cdb-a2ae59aef5bd
title: Elaborazione enumerazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 911d11a50e898656b56fe89001811b939473c2e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311968"
---
# <a name="process-enumeration"></a><span data-ttu-id="92ab2-104">Elaborazione enumerazione</span><span class="sxs-lookup"><span data-stu-id="92ab2-104">Process Enumeration</span></span>

<span data-ttu-id="92ab2-105">Tutti gli utenti hanno accesso in lettura all'elenco di processi nel sistema e sono disponibili diverse funzioni che enumerano i processi attivi.</span><span class="sxs-lookup"><span data-stu-id="92ab2-105">All users have read access to the list of processes in the system and there are a number of different functions that enumerate the active processes.</span></span> <span data-ttu-id="92ab2-106">La funzione da usare dipende da fattori quali il supporto della piattaforma desiderata.</span><span class="sxs-lookup"><span data-stu-id="92ab2-106">The function you should use will depend on factors such as desired platform support.</span></span>

<span data-ttu-id="92ab2-107">Le funzioni seguenti vengono utilizzate per enumerare i processi.</span><span class="sxs-lookup"><span data-stu-id="92ab2-107">The following functions are used to enumerate processes.</span></span>



| <span data-ttu-id="92ab2-108">Funzione</span><span class="sxs-lookup"><span data-stu-id="92ab2-108">Function</span></span>                                                    | <span data-ttu-id="92ab2-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="92ab2-109">Description</span></span>                                                                        |
|-------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="92ab2-110">**EnumProcesses**</span><span class="sxs-lookup"><span data-stu-id="92ab2-110">**EnumProcesses**</span></span>](/windows/win32/api/psapi/nf-psapi-enumprocesses)                     | <span data-ttu-id="92ab2-111">Recupera l'identificatore di processo per ogni oggetto processo nel sistema.</span><span class="sxs-lookup"><span data-stu-id="92ab2-111">Retrieves the process identifier for each process object in the system.</span></span>            |
| [<span data-ttu-id="92ab2-112">**Process32First**</span><span class="sxs-lookup"><span data-stu-id="92ab2-112">**Process32First**</span></span>](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first)                   | <span data-ttu-id="92ab2-113">Recupera le informazioni sul primo processo rilevato in uno snapshot del sistema.</span><span class="sxs-lookup"><span data-stu-id="92ab2-113">Retrieves information about the first process encountered in a system snapshot.</span></span>    |
| [<span data-ttu-id="92ab2-114">**Process32Next**</span><span class="sxs-lookup"><span data-stu-id="92ab2-114">**Process32Next**</span></span>](/windows/win32/api/tlhelp32/nf-tlhelp32-process32next)                     | <span data-ttu-id="92ab2-115">Recupera le informazioni sul processo successivo registrato in uno snapshot del sistema.</span><span class="sxs-lookup"><span data-stu-id="92ab2-115">Retrieves information about the next process recorded in a system snapshot.</span></span>        |
| [<span data-ttu-id="92ab2-116">**WTSEnumerateProcesses**</span><span class="sxs-lookup"><span data-stu-id="92ab2-116">**WTSEnumerateProcesses**</span></span>](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumerateprocessesa) | <span data-ttu-id="92ab2-117">Recupera le informazioni sui processi attivi sul server terminal specificato.</span><span class="sxs-lookup"><span data-stu-id="92ab2-117">Retrieves information about the active processes on the specified terminal server.</span></span> |



 

<span data-ttu-id="92ab2-118">Le funzioni TOOLHELP e [**EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses) enumerano tutti i processi.</span><span class="sxs-lookup"><span data-stu-id="92ab2-118">The toolhelp functions and [**EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses) enumerate all process.</span></span> <span data-ttu-id="92ab2-119">Per elencare i processi in esecuzione in un account utente specifico, usare [**WTSEnumerateProcesses**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumerateprocessesa) e filtrare nel SID utente.</span><span class="sxs-lookup"><span data-stu-id="92ab2-119">To list the processes that are running in a specific user account, use [**WTSEnumerateProcesses**](/windows/win32/api/wtsapi32/nf-wtsapi32-wtsenumerateprocessesa) and filter on the user SID.</span></span> <span data-ttu-id="92ab2-120">È possibile filtrare l'ID sessione per nascondere i processi in esecuzione in altre sessioni di Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="92ab2-120">You can filter on the session ID to hide processes running in other terminal server sessions.</span></span>

<span data-ttu-id="92ab2-121">È anche possibile filtrare i processi in base all'account utente, indipendentemente dalla funzione di enumerazione, chiamando [**OpenProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess), [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken)e [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) con **TokenUser**.</span><span class="sxs-lookup"><span data-stu-id="92ab2-121">You can also filter processes by user account, regardless of the enumeration function, by calling [**OpenProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess), [**OpenProcessToken**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocesstoken), and [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) with **TokenUser**.</span></span> <span data-ttu-id="92ab2-122">Tuttavia, non è possibile aprire un processo protetto da un descrittore di sicurezza a meno che non sia stato concesso l'accesso.</span><span class="sxs-lookup"><span data-stu-id="92ab2-122">However, you cannot open a process that is protected by a security descriptor unless you have been granted access.</span></span>

 

 
