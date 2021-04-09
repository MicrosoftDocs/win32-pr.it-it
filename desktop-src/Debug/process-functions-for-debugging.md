---
description: La funzione CreateProcess consente a un debugger di avviare un processo ed eseguirne il debug.
ms.assetid: 7056e181-9bc5-4530-a7b8-d5ff1e345eef
title: Funzioni di elaborazione per il debug
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d31378a4115acfdd5a4a1836199b7387adeb6e3f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966052"
---
# <a name="process-functions-for-debugging"></a><span data-ttu-id="db848-103">Funzioni di elaborazione per il debug</span><span class="sxs-lookup"><span data-stu-id="db848-103">Process Functions for Debugging</span></span>

<span data-ttu-id="db848-104">La funzione [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) consente a un debugger di avviare un processo ed eseguirne il debug.</span><span class="sxs-lookup"><span data-stu-id="db848-104">The [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) function enables a debugger to start a process and debug it.</span></span> <span data-ttu-id="db848-105">Il parametro *fdwCreate* di **CreateProcess** viene usato per specificare il tipo di operazione di debug.</span><span class="sxs-lookup"><span data-stu-id="db848-105">The *fdwCreate* parameter of **CreateProcess** is used to specify the type of debugging operation.</span></span> <span data-ttu-id="db848-106">Se \_ viene specificato il flag del processo di debug per il parametro, un debugger esegue il debug del nuovo processo e di tutti i discendenti del processo, purché i discendenti vengano creati senza il flag del processo di debug \_ .</span><span class="sxs-lookup"><span data-stu-id="db848-106">If the DEBUG\_PROCESS flag is specified for the parameter, a debugger debugs the new process and all of the process's descendants, provided that the descendants are created without the DEBUG\_PROCESS flag.</span></span>

<span data-ttu-id="db848-107">Se il processo di DEBUG \_ e il debug \_ solo \_ \_ di questi flag di processo sono specificati per *fdwCreate*, un debugger esegue il debug del nuovo processo, ma nessuno dei relativi discendenti.</span><span class="sxs-lookup"><span data-stu-id="db848-107">If the DEBUG\_PROCESS and DEBUG\_ONLY\_THIS\_PROCESS flags are specified for *fdwCreate*, a debugger debugs the new process but none of its descendants.</span></span>

<span data-ttu-id="db848-108">Un debugger può eseguire il debug di un altro creando un processo con il flag del processo di DEBUG \_ .</span><span class="sxs-lookup"><span data-stu-id="db848-108">One debugger can debug another by creating a process with the DEBUG\_PROCESS flag.</span></span> <span data-ttu-id="db848-109">Il nuovo processo (il debugger sottoposto a debug) deve quindi creare un processo con il flag del processo di DEBUG \_ .</span><span class="sxs-lookup"><span data-stu-id="db848-109">The new process (the debugger being debugged) must then create a process with the DEBUG\_PROCESS flag.</span></span>

<span data-ttu-id="db848-110">La funzione [**OpenProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess) consente a un debugger di ottenere l'identificatore di un processo esistente.</span><span class="sxs-lookup"><span data-stu-id="db848-110">The [**OpenProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openprocess) function enables a debugger to obtain the identifier of an existing process.</span></span> <span data-ttu-id="db848-111">La funzione [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) utilizza questo identificatore per alleghi il debugger al processo. In genere, i debugger aprono un processo con i flag di scrittura della macchina virtuale di processo \_ \_ lettura ed elaborazione VM \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="db848-111">(The [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) function uses this identifier to attach the debugger to the process.) Typically, debuggers open a process with the PROCESS\_VM\_READ and PROCESS\_VM\_WRITE flags.</span></span> <span data-ttu-id="db848-112">L'uso di questi flag consente al debugger di leggere e scrivere nella memoria virtuale del processo usando le funzioni [**ReadProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-readprocessmemory) e [**WriteProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-writeprocessmemory) .</span><span class="sxs-lookup"><span data-stu-id="db848-112">Using these flags enables the debugger to read from and write to the virtual memory of the process by using the [**ReadProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-readprocessmemory) and [**WriteProcessMemory**](/windows/win32/api/memoryapi/nf-memoryapi-writeprocessmemory) functions.</span></span> <span data-ttu-id="db848-113">Per ulteriori informazioni, vedere [**processi e thread**](../procthread/processes-and-threads.md).</span><span class="sxs-lookup"><span data-stu-id="db848-113">For more information, see [**Processes and Threads**](../procthread/processes-and-threads.md).</span></span>

 

 
