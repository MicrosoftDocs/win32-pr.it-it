---
title: Funzioni della guida dello strumento
description: Elenca le funzioni della libreria della guida dello strumento.
ms.assetid: 83732bd6-f4cf-409d-ad17-86503d408dc3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54f9d95598f9b48343ea9731e1a826fb147a73a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045219"
---
# <a name="tool-help-functions"></a><span data-ttu-id="2b13c-103">Funzioni della guida dello strumento</span><span class="sxs-lookup"><span data-stu-id="2b13c-103">Tool Help Functions</span></span>

<span data-ttu-id="2b13c-104">Le funzioni seguenti fanno parte della libreria della Guida di strumenti.</span><span class="sxs-lookup"><span data-stu-id="2b13c-104">The following functions are part of the tool help library.</span></span>



| <span data-ttu-id="2b13c-105">Funzione</span><span class="sxs-lookup"><span data-stu-id="2b13c-105">Function</span></span>                                                           | <span data-ttu-id="2b13c-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2b13c-106">Description</span></span>                                                                                                      |
|--------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2b13c-107">**CreateToolhelp32Snapshot**</span><span class="sxs-lookup"><span data-stu-id="2b13c-107">**CreateToolhelp32Snapshot**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-createtoolhelp32snapshot)       | <span data-ttu-id="2b13c-108">Esegue uno snapshot dei processi specificati, nonché gli heap, i moduli e i thread utilizzati da questi processi.</span><span class="sxs-lookup"><span data-stu-id="2b13c-108">Takes a snapshot of the specified processes, as well as the heaps, modules, and threads used by these processes.</span></span> |
| [<span data-ttu-id="2b13c-109">**Heap32First**</span><span class="sxs-lookup"><span data-stu-id="2b13c-109">**Heap32First**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32first)                                 | <span data-ttu-id="2b13c-110">Recupera le informazioni sul primo blocco di un heap allocato da un processo.</span><span class="sxs-lookup"><span data-stu-id="2b13c-110">Retrieves information about the first block of a heap that has been allocated by a process.</span></span>                      |
| [<span data-ttu-id="2b13c-111">**Heap32ListFirst**</span><span class="sxs-lookup"><span data-stu-id="2b13c-111">**Heap32ListFirst**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listfirst)                         | <span data-ttu-id="2b13c-112">Recupera le informazioni sul primo heap allocato da un processo specificato.</span><span class="sxs-lookup"><span data-stu-id="2b13c-112">Retrieves information about the first heap that has been allocated by a specified process.</span></span>                       |
| [<span data-ttu-id="2b13c-113">**Heap32ListNext**</span><span class="sxs-lookup"><span data-stu-id="2b13c-113">**Heap32ListNext**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32listnext)                           | <span data-ttu-id="2b13c-114">Recupera le informazioni sull'heap successivo allocato da un processo.</span><span class="sxs-lookup"><span data-stu-id="2b13c-114">Retrieves information about the next heap that has been allocated by a process.</span></span>                                  |
| [<span data-ttu-id="2b13c-115">**Heap32Next**</span><span class="sxs-lookup"><span data-stu-id="2b13c-115">**Heap32Next**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-heap32next)                                   | <span data-ttu-id="2b13c-116">Recupera informazioni sul blocco successivo di un heap allocato da un processo.</span><span class="sxs-lookup"><span data-stu-id="2b13c-116">Retrieves information about the next block of a heap that has been allocated by a process.</span></span>                       |
| [<span data-ttu-id="2b13c-117">**Module32First**</span><span class="sxs-lookup"><span data-stu-id="2b13c-117">**Module32First**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32first)                             | <span data-ttu-id="2b13c-118">Recupera le informazioni sul primo modulo associato a un processo.</span><span class="sxs-lookup"><span data-stu-id="2b13c-118">Retrieves information about the first module associated with a process.</span></span>                                          |
| [<span data-ttu-id="2b13c-119">**Module32Next**</span><span class="sxs-lookup"><span data-stu-id="2b13c-119">**Module32Next**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-module32next)                               | <span data-ttu-id="2b13c-120">Recupera le informazioni sul modulo successivo associato a un processo o a un thread.</span><span class="sxs-lookup"><span data-stu-id="2b13c-120">Retrieves information about the next module associated with a process or thread.</span></span>                                 |
| [<span data-ttu-id="2b13c-121">**Process32First**</span><span class="sxs-lookup"><span data-stu-id="2b13c-121">**Process32First**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32first)                           | <span data-ttu-id="2b13c-122">Recupera le informazioni sul primo processo rilevato in uno snapshot del sistema.</span><span class="sxs-lookup"><span data-stu-id="2b13c-122">Retrieves information about the first process encountered in a system snapshot.</span></span>                                  |
| [<span data-ttu-id="2b13c-123">**Process32Next**</span><span class="sxs-lookup"><span data-stu-id="2b13c-123">**Process32Next**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-process32next)                             | <span data-ttu-id="2b13c-124">Recupera le informazioni sul processo successivo registrato in uno snapshot del sistema.</span><span class="sxs-lookup"><span data-stu-id="2b13c-124">Retrieves information about the next process recorded in a system snapshot.</span></span>                                      |
| [<span data-ttu-id="2b13c-125">**Thread32First**</span><span class="sxs-lookup"><span data-stu-id="2b13c-125">**Thread32First**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32first)                             | <span data-ttu-id="2b13c-126">Recupera le informazioni sul primo thread di qualsiasi processo rilevato in uno snapshot del sistema.</span><span class="sxs-lookup"><span data-stu-id="2b13c-126">Retrieves information about the first thread of any process encountered in a system snapshot.</span></span>                    |
| [<span data-ttu-id="2b13c-127">**Thread32Next**</span><span class="sxs-lookup"><span data-stu-id="2b13c-127">**Thread32Next**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-thread32next)                               | <span data-ttu-id="2b13c-128">Recupera le informazioni sul thread successivo di qualsiasi processo rilevato nello snapshot della memoria di sistema.</span><span class="sxs-lookup"><span data-stu-id="2b13c-128">Retrieves information about the next thread of any process encountered in the system memory snapshot.</span></span>            |
| [<span data-ttu-id="2b13c-129">**Toolhelp32ReadProcessMemory**</span><span class="sxs-lookup"><span data-stu-id="2b13c-129">**Toolhelp32ReadProcessMemory**</span></span>](/windows/desktop/api/TlHelp32/nf-tlhelp32-toolhelp32readprocessmemory) | <span data-ttu-id="2b13c-130">Copia la memoria allocata a un altro processo in un buffer fornito dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2b13c-130">Copies memory allocated to another process into an application-supplied buffer.</span></span>                                  |



 

 

 




