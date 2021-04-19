---
title: Memoria. CPP
description: Nel componente provider di esempio, un esempio di codice che mostra l'allocazione e la liberazione della memoria è in memory. cpp. Le routine supportate sono elencate nella tabella seguente.
ms.assetid: dc5b3559-02fc-45e8-bbd0-482e4e3a7f8a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9add77dcdbbfc0ddab547cd537b352c9a68bdaf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297665"
---
# <a name="memorycpp"></a><span data-ttu-id="a3fbb-104">Memoria. CPP</span><span class="sxs-lookup"><span data-stu-id="a3fbb-104">MEMORY.CPP</span></span>

<span data-ttu-id="a3fbb-105">Nel componente provider di esempio, un esempio di codice che mostra l'allocazione e la liberazione della memoria è in memory. cpp.</span><span class="sxs-lookup"><span data-stu-id="a3fbb-105">In the example provider component, a code example showing memory allocation and freeing is in memory.cpp.</span></span> <span data-ttu-id="a3fbb-106">Le routine supportate sono elencate nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="a3fbb-106">Supported routines are listed in the following table.</span></span>



| <span data-ttu-id="a3fbb-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="a3fbb-107">Item</span></span>                | <span data-ttu-id="a3fbb-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a3fbb-108">Description</span></span>                                                           |
|---------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="a3fbb-109">**AllocProvMem**</span><span class="sxs-lookup"><span data-stu-id="a3fbb-109">**AllocProvMem**</span></span>    | <span data-ttu-id="a3fbb-110">Allocare memoria specificata.</span><span class="sxs-lookup"><span data-stu-id="a3fbb-110">Allocate specified memory.</span></span>                                            |
| <span data-ttu-id="a3fbb-111">**FreeProvMem**</span><span class="sxs-lookup"><span data-stu-id="a3fbb-111">**FreeProvMem**</span></span>     | <span data-ttu-id="a3fbb-112">Memoria libera indicata.</span><span class="sxs-lookup"><span data-stu-id="a3fbb-112">Free memory indicated.</span></span>                                                |
| <span data-ttu-id="a3fbb-113">**ReallocProvMem**</span><span class="sxs-lookup"><span data-stu-id="a3fbb-113">**ReallocProvMem**</span></span>  | <span data-ttu-id="a3fbb-114">Allocare memoria contigua.</span><span class="sxs-lookup"><span data-stu-id="a3fbb-114">Allocate contiguous memory.</span></span>                                           |
| <span data-ttu-id="a3fbb-115">**AllocProvStr**</span><span class="sxs-lookup"><span data-stu-id="a3fbb-115">**AllocProvStr**</span></span>    | <span data-ttu-id="a3fbb-116">Alloca una stringa LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="a3fbb-116">Allocate an LPWSTR string.</span></span>                                            |
| <span data-ttu-id="a3fbb-117">**FreeProvStr**</span><span class="sxs-lookup"><span data-stu-id="a3fbb-117">**FreeProvStr**</span></span>     | <span data-ttu-id="a3fbb-118">Stringa libera se non è già stata liberata.</span><span class="sxs-lookup"><span data-stu-id="a3fbb-118">Free string if not already freed.</span></span>                                     |
| <span data-ttu-id="a3fbb-119">**ReallocProvStr**</span><span class="sxs-lookup"><span data-stu-id="a3fbb-119">**ReallocProvStr**</span></span>  | <span data-ttu-id="a3fbb-120">Allocare memoria contigua.</span><span class="sxs-lookup"><span data-stu-id="a3fbb-120">Allocate contiguous memory.</span></span>                                           |
| <span data-ttu-id="a3fbb-121">**ProvAllocString**</span><span class="sxs-lookup"><span data-stu-id="a3fbb-121">**ProvAllocString**</span></span> | <span data-ttu-id="a3fbb-122">Verifica la stringa e il primo parametro.</span><span class="sxs-lookup"><span data-stu-id="a3fbb-122">Verifies string and first parameter.</span></span> <span data-ttu-id="a3fbb-123">Se OK, esegue l'allocazione.</span><span class="sxs-lookup"><span data-stu-id="a3fbb-123">If OK, then performs allocation.</span></span> |



 

 

 




