---
description: Ogni processo in Microsoft Windows a 32 bit dispone di uno spazio degli indirizzi virtuale che consente di indirizzare fino a 4 gigabyte di memoria.
ms.assetid: f259f3cb-81c0-4b5f-b6fa-9681a278019a
title: Informazioni sulla gestione della memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4110bf1d0768f1321fd89ddd1d5a985e3e54aa75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307268"
---
# <a name="about-memory-management"></a><span data-ttu-id="cc36b-103">Informazioni sulla gestione della memoria</span><span class="sxs-lookup"><span data-stu-id="cc36b-103">About Memory Management</span></span>

<span data-ttu-id="cc36b-104">Ogni processo in Microsoft Windows a 32 bit dispone di uno spazio degli indirizzi virtuale che consente di indirizzare fino a 4 gigabyte di memoria.</span><span class="sxs-lookup"><span data-stu-id="cc36b-104">Each process on 32-bit Microsoft Windows has its own virtual address space that enables addressing up to 4 gigabytes of memory.</span></span> <span data-ttu-id="cc36b-105">Ogni processo in Windows a 64 bit ha uno spazio di indirizzi virtuale di 8 terabyte.</span><span class="sxs-lookup"><span data-stu-id="cc36b-105">Each process on 64-bit Windows has a virtual address space of 8 terabytes.</span></span> <span data-ttu-id="cc36b-106">Tutti i thread di un processo possono accedere al proprio spazio degli indirizzi virtuali.</span><span class="sxs-lookup"><span data-stu-id="cc36b-106">All threads of a process can access its virtual address space.</span></span> <span data-ttu-id="cc36b-107">Tuttavia, i thread non possono accedere alla memoria che appartiene a un altro processo, evitando che un processo venga danneggiato da un altro processo.</span><span class="sxs-lookup"><span data-stu-id="cc36b-107">However, threads cannot access memory that belongs to another process, which protects a process from being corrupted by another process.</span></span>

<span data-ttu-id="cc36b-108">Per informazioni sullo spazio degli indirizzi virtuali e sulle funzioni di gestione della memoria, vedere gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="cc36b-108">For information on the virtual address space and the memory management functions, see the following topics.</span></span>

-   [<span data-ttu-id="cc36b-109">Spazio degli indirizzi virtuali</span><span class="sxs-lookup"><span data-stu-id="cc36b-109">Virtual Address Space</span></span>](virtual-address-space.md)
-   [<span data-ttu-id="cc36b-110">Pool di memoria</span><span class="sxs-lookup"><span data-stu-id="cc36b-110">Memory Pools</span></span>](memory-pools.md)
-   [<span data-ttu-id="cc36b-111">Informazioni sulle prestazioni della memoria</span><span class="sxs-lookup"><span data-stu-id="cc36b-111">Memory Performance Information</span></span>](memory-performance-information.md)
-   [<span data-ttu-id="cc36b-112">Funzioni di memoria virtuale</span><span class="sxs-lookup"><span data-stu-id="cc36b-112">Virtual Memory Functions</span></span>](virtual-memory-functions.md)
-   [<span data-ttu-id="cc36b-113">Funzioni heap</span><span class="sxs-lookup"><span data-stu-id="cc36b-113">Heap Functions</span></span>](heap-functions.md)
-   [<span data-ttu-id="cc36b-114">Mapping dei file</span><span class="sxs-lookup"><span data-stu-id="cc36b-114">File Mapping</span></span>](file-mapping.md)
-   [<span data-ttu-id="cc36b-115">Supporto per memoria di grandi dimensioni</span><span class="sxs-lookup"><span data-stu-id="cc36b-115">Large Memory Support</span></span>](large-memory-support.md)
-   [<span data-ttu-id="cc36b-116">Funzioni globali e locali</span><span class="sxs-lookup"><span data-stu-id="cc36b-116">Global and Local Functions</span></span>](global-and-local-functions.md)
-   [<span data-ttu-id="cc36b-117">Funzioni della libreria C standard</span><span class="sxs-lookup"><span data-stu-id="cc36b-117">Standard C Library Functions</span></span>](standard-c-library-functions.md)
-   [<span data-ttu-id="cc36b-118">Confronto tra i metodi di allocazione della memoria</span><span class="sxs-lookup"><span data-stu-id="cc36b-118">Comparing Memory Allocation Methods</span></span>](comparing-memory-allocation-methods.md)

 

 



