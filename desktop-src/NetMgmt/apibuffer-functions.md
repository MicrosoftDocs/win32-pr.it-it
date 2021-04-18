---
title: Funzioni ApiBuffer
description: Le funzioni ApiBuffer di gestione della rete vengono usate per gestire l'allocazione di memoria usata da un'applicazione con le funzioni di gestione della rete.
ms.assetid: bf2fe8aa-dda6-4f6b-9c52-d7a96b96da18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b316c6b2ee2d4095c15d5e859dd0069978c7ff91
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300083"
---
# <a name="apibuffer-functions"></a><span data-ttu-id="3fa00-103">Funzioni ApiBuffer</span><span class="sxs-lookup"><span data-stu-id="3fa00-103">ApiBuffer Functions</span></span>

<span data-ttu-id="3fa00-104">Le funzioni ApiBuffer di gestione della rete vengono usate per gestire l'allocazione di memoria usata da un'applicazione con le funzioni di gestione della rete.</span><span class="sxs-lookup"><span data-stu-id="3fa00-104">The network management ApiBuffer functions are used to manage memory allocation used by an application with network management functions.</span></span> <span data-ttu-id="3fa00-105">Tuttavia, in generale, per la memoria usata da un'applicazione, è consigliabile usare le [funzioni di gestione della memoria](/windows/desktop/Memory/memory-management-functions) invece di queste funzioni ApiBuffer.</span><span class="sxs-lookup"><span data-stu-id="3fa00-105">However, in general, for other memory used by an application you should use the [memory management functions](/windows/desktop/Memory/memory-management-functions) instead of these ApiBuffer functions.</span></span>

<span data-ttu-id="3fa00-106">Le funzioni ApiBuffer sono elencate di seguito.</span><span class="sxs-lookup"><span data-stu-id="3fa00-106">The ApiBuffer functions are listed following.</span></span>



| <span data-ttu-id="3fa00-107">Funzione</span><span class="sxs-lookup"><span data-stu-id="3fa00-107">Function</span></span>                                                 | <span data-ttu-id="3fa00-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3fa00-108">Description</span></span>                                                                                                               |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3fa00-109">**NetApiBufferAllocate**</span><span class="sxs-lookup"><span data-stu-id="3fa00-109">**NetApiBufferAllocate**</span></span>](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferallocate)     | <span data-ttu-id="3fa00-110">Alloca memoria dall'heap.</span><span class="sxs-lookup"><span data-stu-id="3fa00-110">Allocates memory from the heap.</span></span> <span data-ttu-id="3fa00-111">Chiamare questa funzione quando è necessaria la compatibilità con la funzione **NetApiBufferFree** .</span><span class="sxs-lookup"><span data-stu-id="3fa00-111">Call this function when you require compatibility with the **NetApiBufferFree** function.</span></span> |
| [<span data-ttu-id="3fa00-112">**NetApiBufferFree**</span><span class="sxs-lookup"><span data-stu-id="3fa00-112">**NetApiBufferFree**</span></span>](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree)             | <span data-ttu-id="3fa00-113">Libera la memoria allocata dalla funzione **NetApiBufferAllocate** e da altre funzioni di gestione della rete.</span><span class="sxs-lookup"><span data-stu-id="3fa00-113">Frees memory allocated by the **NetApiBufferAllocate** function and other network management functions.</span></span>                   |
| [<span data-ttu-id="3fa00-114">**NetApiBufferReallocate**</span><span class="sxs-lookup"><span data-stu-id="3fa00-114">**NetApiBufferReallocate**</span></span>](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferreallocate) | <span data-ttu-id="3fa00-115">Modifica la dimensione di un buffer allocato da una chiamata alla funzione **NetApiBufferAllocate** .</span><span class="sxs-lookup"><span data-stu-id="3fa00-115">Changes the size of a buffer allocated by a call to the **NetApiBufferAllocate** function.</span></span>                                |
| [<span data-ttu-id="3fa00-116">**NetApiBufferSize**</span><span class="sxs-lookup"><span data-stu-id="3fa00-116">**NetApiBufferSize**</span></span>](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibuffersize)             | <span data-ttu-id="3fa00-117">Restituisce la dimensione, in byte, di un buffer allocato da una chiamata alla funzione **NetApiBufferAllocate** .</span><span class="sxs-lookup"><span data-stu-id="3fa00-117">Returns the size, in bytes, of a buffer allocated by a call to the **NetApiBufferAllocate** function.</span></span>                     |



 

<span data-ttu-id="3fa00-118">Per le funzioni utilizzabili in remoto che restituiscono informazioni al chiamante, la libreria di runtime RPC alloca il buffer contenente le informazioni restituite.</span><span class="sxs-lookup"><span data-stu-id="3fa00-118">For remotable functions that return information to the caller, the RPC run-time library allocates the buffer containing the return information.</span></span> <span data-ttu-id="3fa00-119">Al termine dell'elaborazione delle informazioni, il chiamante deve chiamare la funzione [**NetApiBufferFree**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree) per liberare il buffer allocato.</span><span class="sxs-lookup"><span data-stu-id="3fa00-119">When the caller has finished processing the information, it must call the [**NetApiBufferFree**](/windows/desktop/api/Lmapibuf/nf-lmapibuf-netapibufferfree) function to free the allocated buffer.</span></span>

 

 