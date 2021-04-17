---
title: Thread a piedi
description: Uno snapshot che include l'elenco di thread contiene informazioni su ogni thread di ogni processo attualmente in esecuzione.
ms.assetid: 2440b781-652d-4d73-b173-87504e7b49b5
keywords:
- enumerazione
- Enumerazione, thread
- thread
- thread, enumerazione dei thread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32eff584aedaa3f6124cc358a4ee9d2a94962843
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300101"
---
# <a name="thread-walking"></a><span data-ttu-id="f3de4-107">Thread a piedi</span><span class="sxs-lookup"><span data-stu-id="f3de4-107">Thread Walking</span></span>

<span data-ttu-id="f3de4-108">Uno snapshot che include l'elenco di thread contiene informazioni su ogni thread di ogni processo attualmente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="f3de4-108">A snapshot that includes the thread list contains information about each thread of each currently executing process.</span></span> <span data-ttu-id="f3de4-109">È possibile recuperare le informazioni per il primo thread nell'elenco usando la funzione [**Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first) .</span><span class="sxs-lookup"><span data-stu-id="f3de4-109">You can retrieve information for the first thread in the list by using the [**Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first) function.</span></span> <span data-ttu-id="f3de4-110">Dopo aver recuperato il primo thread nell'elenco, è possibile recuperare le informazioni per i thread successivi usando la funzione [**Thread32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next) .</span><span class="sxs-lookup"><span data-stu-id="f3de4-110">After retrieving the first thread in the list, you can retrieve information for subsequent threads by using the [**Thread32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next) function.</span></span> <span data-ttu-id="f3de4-111">**Thread32First** e **Thread32Next** riempiono una struttura [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) con informazioni sui singoli thread dello snapshot.</span><span class="sxs-lookup"><span data-stu-id="f3de4-111">**Thread32First** and **Thread32Next** fill a [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) structure with information about individual threads in the snapshot.</span></span>

<span data-ttu-id="f3de4-112">È possibile enumerare i thread di un processo specifico eseguendo uno snapshot che include i thread e quindi attraversando l'elenco dei thread, mantenendo le informazioni sui thread con lo stesso identificatore di processo del processo specificato.</span><span class="sxs-lookup"><span data-stu-id="f3de4-112">You can enumerate the threads of a specific process by taking a snapshot that includes the threads and then by traversing the thread list, keeping information about the threads that have the same process identifier as the specified process.</span></span>

<span data-ttu-id="f3de4-113">È possibile recuperare un codice di stato di errore esteso per [**Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first) e [**Thread32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next) utilizzando la funzione [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) .</span><span class="sxs-lookup"><span data-stu-id="f3de4-113">You can retrieve an extended error status code for [**Thread32First**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first) and [**Thread32Next**](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next) by using the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span>

> [!Note]  
> <span data-ttu-id="f3de4-114">Il contenuto del membro **th32ThreadID** di [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) è un identificatore del thread e può essere usato da qualsiasi funzione che richiede un identificatore di thread.</span><span class="sxs-lookup"><span data-stu-id="f3de4-114">The contents of the **th32ThreadID** member of [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) is a thread identifier and can be used by any functions that require a thread identifier.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f3de4-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f3de4-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3de4-116">Attraversamento dell'elenco dei thread</span><span class="sxs-lookup"><span data-stu-id="f3de4-116">Traversing the Thread List</span></span>](traversing-the-thread-list.md)
</dt> </dl>

 

 