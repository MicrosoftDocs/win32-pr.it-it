---
description: Informazioni su come usare la funzione CreateThread per creare un nuovo thread per un processo. I debugger in genere devono esaminare o modificare il contenuto dei registri di un thread.
ms.assetid: df59eedd-45ec-4564-96a5-8cecb345cfcc
title: Funzioni di thread per il debug
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff168d4840032a6199ef03e0cf2117c8ea87f4d6
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403984"
---
# <a name="thread-functions-for-debugging"></a><span data-ttu-id="a48d6-104">Funzioni di thread per il debug</span><span class="sxs-lookup"><span data-stu-id="a48d6-104">Thread Functions for Debugging</span></span>

<span data-ttu-id="a48d6-105">La [**funzione CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) crea un nuovo thread per un processo.</span><span class="sxs-lookup"><span data-stu-id="a48d6-105">The [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) function creates a new thread for a process.</span></span> <span data-ttu-id="a48d6-106">I debugger in genere devono esaminare o modificare il contenuto dei registri di un thread.</span><span class="sxs-lookup"><span data-stu-id="a48d6-106">Debuggers typically need to examine or change the contents of a thread's registers.</span></span> <span data-ttu-id="a48d6-107">A tale scopo, un debugger deve ottenere un handle per il thread usando la funzione [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) e specificando l'accesso appropriato al thread (THREAD \_ GET \_ CONTEXT, THREAD \_ SET CONTEXT \_ o entrambi).</span><span class="sxs-lookup"><span data-stu-id="a48d6-107">To accomplish this, a debugger must obtain a handle to the thread by using the [**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) function and specifying the appropriate access to the thread (THREAD\_GET\_CONTEXT, THREAD\_SET\_CONTEXT, or both).</span></span> <span data-ttu-id="a48d6-108">La [**funzione OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) consente a un debugger di ottenere l'identificatore di un thread esistente.</span><span class="sxs-lookup"><span data-stu-id="a48d6-108">The [**OpenThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-openthread) function enables a debugger to obtain the identifier of an existing thread.</span></span>

<span data-ttu-id="a48d6-109">Un processo con accesso appropriato a un thread può esaminare i registri del thread usando la [**funzione GetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadcontext) e impostare il contenuto dei registri del thread usando la [**funzione SetThreadContext.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadcontext)</span><span class="sxs-lookup"><span data-stu-id="a48d6-109">A process with appropriate access to a thread can examine the thread's registers by using the [**GetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadcontext) function and set the contents of the thread's registers by using the [**SetThreadContext**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadcontext) function.</span></span>

<span data-ttu-id="a48d6-110">Un processo può anche ottenere l'accesso THREAD \_ SUSPEND RESUME a un \_ thread.</span><span class="sxs-lookup"><span data-stu-id="a48d6-110">A process can also obtain THREAD\_SUSPEND\_RESUME access to a thread.</span></span> <span data-ttu-id="a48d6-111">Questo tipo di accesso consente a un debugger di controllare l'esecuzione di un thread con le [**funzioni SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) [**e ResumeThread.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread)</span><span class="sxs-lookup"><span data-stu-id="a48d6-111">This type of access enables a debugger to control a thread's execution with the [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) and [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) functions.</span></span> <span data-ttu-id="a48d6-112">Per altre informazioni sui thread, vedere [Processi e thread](../procthread/processes-and-threads.md).</span><span class="sxs-lookup"><span data-stu-id="a48d6-112">For more information about threads, see [Processes and Threads](../procthread/processes-and-threads.md).</span></span>

 

 
