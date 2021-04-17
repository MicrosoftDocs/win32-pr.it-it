---
description: La funzione CreateThread crea un nuovo thread per un processo.
ms.assetid: df59eedd-45ec-4564-96a5-8cecb345cfcc
title: Funzioni thread per il debug
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb5ab0865d5585656a5c22c24e2604032de8b888
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523673"
---
# <a name="thread-functions-for-debugging"></a><span data-ttu-id="e99de-103">Funzioni thread per il debug</span><span class="sxs-lookup"><span data-stu-id="e99de-103">Thread Functions for Debugging</span></span>

<span data-ttu-id="e99de-104">La funzione [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) crea un nuovo thread per un processo.</span><span class="sxs-lookup"><span data-stu-id="e99de-104">The [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) function creates a new thread for a process.</span></span> <span data-ttu-id="e99de-105">Per i debugger è in genere necessario esaminare o modificare il contenuto dei registri di un thread.</span><span class="sxs-lookup"><span data-stu-id="e99de-105">Debuggers typically need to examine or change the contents of a thread's registers.</span></span> <span data-ttu-id="e99de-106">A tale scopo, è necessario che un debugger ottenga un handle per il thread utilizzando la funzione [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) e specificando l'accesso appropriato al thread (contesto Get del thread, \_ contesto del set di \_ thread \_ \_ o entrambi).</span><span class="sxs-lookup"><span data-stu-id="e99de-106">To accomplish this, a debugger must obtain a handle to the thread by using the [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) function and specifying the appropriate access to the thread (THREAD\_GET\_CONTEXT, THREAD\_SET\_CONTEXT, or both).</span></span> <span data-ttu-id="e99de-107">La funzione [**OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) consente a un debugger di ottenere l'identificatore di un thread esistente.</span><span class="sxs-lookup"><span data-stu-id="e99de-107">The [**OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) function enables a debugger to obtain the identifier of an existing thread.</span></span>

<span data-ttu-id="e99de-108">Un processo con accesso appropriato a un thread può esaminare i registri del thread utilizzando la funzione [**GetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadcontext) e impostare il contenuto dei registri del thread utilizzando la funzione [**SetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadcontext) .</span><span class="sxs-lookup"><span data-stu-id="e99de-108">A process with appropriate access to a thread can examine the thread's registers by using the [**GetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadcontext) function and set the contents of the thread's registers by using the [**SetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadcontext) function.</span></span>

<span data-ttu-id="e99de-109">Un processo può inoltre ottenere \_ \_ l'accesso a un thread per sospendere la sospensione del thread.</span><span class="sxs-lookup"><span data-stu-id="e99de-109">A process can also obtain THREAD\_SUSPEND\_RESUME access to a thread.</span></span> <span data-ttu-id="e99de-110">Questo tipo di accesso consente a un debugger di controllare l'esecuzione di un thread con le funzioni [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) e [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) .</span><span class="sxs-lookup"><span data-stu-id="e99de-110">This type of access enables a debugger to control a thread's execution with the [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) and [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) functions.</span></span> <span data-ttu-id="e99de-111">Per ulteriori informazioni sui thread, vedere [processi e thread](../procthread/processes-and-threads.md).</span><span class="sxs-lookup"><span data-stu-id="e99de-111">For more information about threads, see [Processes and Threads](../procthread/processes-and-threads.md).</span></span>

 

 
