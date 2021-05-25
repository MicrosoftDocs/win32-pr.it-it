---
description: Flag di funzionalità degli stencil del driver.
ms.assetid: 187c758c-5e7f-48ee-97cb-b1f30b709723
title: D3DSTENCILCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8999d73044a061cb8eea8f5829351c1d04079462
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343056"
---
# <a name="d3dstencilcaps"></a><span data-ttu-id="e3b74-103">D3DSTENCILCAPS</span><span class="sxs-lookup"><span data-stu-id="e3b74-103">D3DSTENCILCAPS</span></span>

<span data-ttu-id="e3b74-104">Flag di funzionalità stencil del driver.</span><span class="sxs-lookup"><span data-stu-id="e3b74-104">Driver stencil capability flags.</span></span>



| <span data-ttu-id="e3b74-105">\#Definire</span><span class="sxs-lookup"><span data-stu-id="e3b74-105">\#define</span></span>                 | <span data-ttu-id="e3b74-106">Valore</span><span class="sxs-lookup"><span data-stu-id="e3b74-106">Value</span></span>       | <span data-ttu-id="e3b74-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e3b74-107">Description</span></span>                                                                                           |
|--------------------------|-------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3b74-108">D3DSTENCILCAPS \_ KEEP</span><span class="sxs-lookup"><span data-stu-id="e3b74-108">D3DSTENCILCAPS\_KEEP</span></span>     | <span data-ttu-id="e3b74-109">0x00000001L</span><span class="sxs-lookup"><span data-stu-id="e3b74-109">0x00000001L</span></span> | <span data-ttu-id="e3b74-110">Non aggiornare la voce nel buffer degli stencil.</span><span class="sxs-lookup"><span data-stu-id="e3b74-110">Do not update the entry in the stencil buffer.</span></span> <span data-ttu-id="e3b74-111">Si tratta del valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="e3b74-111">This is the default value.</span></span>                             |
| <span data-ttu-id="e3b74-112">D3DSTENCILCAPS \_ ZERO</span><span class="sxs-lookup"><span data-stu-id="e3b74-112">D3DSTENCILCAPS\_ZERO</span></span>     | <span data-ttu-id="e3b74-113">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="e3b74-113">0x00000002L</span></span> | <span data-ttu-id="e3b74-114">Impostare la voce stencil-buffer su 0.</span><span class="sxs-lookup"><span data-stu-id="e3b74-114">Set the stencil-buffer entry to 0.</span></span>                                                                    |
| <span data-ttu-id="e3b74-115">D3DSTENCILCAPS \_ REPLACE</span><span class="sxs-lookup"><span data-stu-id="e3b74-115">D3DSTENCILCAPS\_REPLACE</span></span>  | <span data-ttu-id="e3b74-116">0x00000004L</span><span class="sxs-lookup"><span data-stu-id="e3b74-116">0x00000004L</span></span> | <span data-ttu-id="e3b74-117">Sostituire la voce stencil-buffer con il valore di riferimento.</span><span class="sxs-lookup"><span data-stu-id="e3b74-117">Replace the stencil-buffer entry with reference value.</span></span>                                                |
| <span data-ttu-id="e3b74-118">D3DSTENCILCAPS \_ INCRSAT</span><span class="sxs-lookup"><span data-stu-id="e3b74-118">D3DSTENCILCAPS\_INCRSAT</span></span>  | <span data-ttu-id="e3b74-119">0x00000008L</span><span class="sxs-lookup"><span data-stu-id="e3b74-119">0x00000008L</span></span> | <span data-ttu-id="e3b74-120">Incrementare la voce stencil-buffer, fissando al valore massimo.</span><span class="sxs-lookup"><span data-stu-id="e3b74-120">Increment the stencil-buffer entry, clamping to the maximum value.</span></span>                                    |
| <span data-ttu-id="e3b74-121">D3DSTENCILCAPS \_ DECRSAT</span><span class="sxs-lookup"><span data-stu-id="e3b74-121">D3DSTENCILCAPS\_DECRSAT</span></span>  | <span data-ttu-id="e3b74-122">0x00000010L</span><span class="sxs-lookup"><span data-stu-id="e3b74-122">0x00000010L</span></span> | <span data-ttu-id="e3b74-123">Decrementare la voce stencil-buffer, fissando a zero.</span><span class="sxs-lookup"><span data-stu-id="e3b74-123">Decrement the stencil-buffer entry, clamping to zero.</span></span>                                                 |
| <span data-ttu-id="e3b74-124">D3DSTENCILCAPS \_ INVERT</span><span class="sxs-lookup"><span data-stu-id="e3b74-124">D3DSTENCILCAPS\_INVERT</span></span>   | <span data-ttu-id="e3b74-125">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="e3b74-125">0x00000020L</span></span> | <span data-ttu-id="e3b74-126">Invertire i bit nella voce stencil-buffer.</span><span class="sxs-lookup"><span data-stu-id="e3b74-126">Invert the bits in the stencil-buffer entry.</span></span>                                                          |
| <span data-ttu-id="e3b74-127">D3DSTENCILCAPS \_ INCR</span><span class="sxs-lookup"><span data-stu-id="e3b74-127">D3DSTENCILCAPS\_INCR</span></span>     | <span data-ttu-id="e3b74-128">0x00000040L</span><span class="sxs-lookup"><span data-stu-id="e3b74-128">0x00000040L</span></span> | <span data-ttu-id="e3b74-129">Incrementare la voce dello stencil buffer, a capo su zero se il nuovo valore supera il valore massimo.</span><span class="sxs-lookup"><span data-stu-id="e3b74-129">Increment the stencil-buffer entry, wrapping to zero if the new value exceeds the maximum value.</span></span>      |
| <span data-ttu-id="e3b74-130">D3DSTENCILCAPS \_ DECR</span><span class="sxs-lookup"><span data-stu-id="e3b74-130">D3DSTENCILCAPS\_DECR</span></span>     | <span data-ttu-id="e3b74-131">0x00000080L</span><span class="sxs-lookup"><span data-stu-id="e3b74-131">0x00000080L</span></span> | <span data-ttu-id="e3b74-132">Decrementare la voce dello stencil buffer, a capo del valore massimo se il nuovo valore è minore di zero.</span><span class="sxs-lookup"><span data-stu-id="e3b74-132">Decrement the stencil-buffer entry, wrapping to the maximum value if the new value is less than zero.</span></span> |
| <span data-ttu-id="e3b74-133">D3DSTENCILCAPS \_ A DUE LATI</span><span class="sxs-lookup"><span data-stu-id="e3b74-133">D3DSTENCILCAPS\_TWOSIDED</span></span> | <span data-ttu-id="e3b74-134">0x00000100L</span><span class="sxs-lookup"><span data-stu-id="e3b74-134">0x00000100L</span></span> | <span data-ttu-id="e3b74-135">Il dispositivo supporta lo stencil a due lati.</span><span class="sxs-lookup"><span data-stu-id="e3b74-135">The device supports two-sided stencil.</span></span>                                                                |



 

<span data-ttu-id="e3b74-136">Le voci dello stencil buffer sono valori interi compresi tra 0 e 2ⁿ - 1, dove n è la profondità in bit del buffer di stencil.</span><span class="sxs-lookup"><span data-stu-id="e3b74-136">Stencil-buffer entries are integer values ranging from 0 through 2ⁿ - 1, where n is the bit depth of the stencil buffer.</span></span>

<span data-ttu-id="e3b74-137">Queste costanti vengono usate dal membro StencilCaps di [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)</span><span class="sxs-lookup"><span data-stu-id="e3b74-137">These constants are used by the StencilCaps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="e3b74-138">Informazioni costanti</span><span class="sxs-lookup"><span data-stu-id="e3b74-138">Constant Information</span></span>



| <span data-ttu-id="e3b74-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3b74-139">Requirement</span></span>                         | <span data-ttu-id="e3b74-140">Valore</span><span class="sxs-lookup"><span data-stu-id="e3b74-140">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="e3b74-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e3b74-141">Header</span></span>                   | <span data-ttu-id="e3b74-142">d3d9caps.h</span><span class="sxs-lookup"><span data-stu-id="e3b74-142">d3d9caps.h</span></span> |
| <span data-ttu-id="e3b74-143">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="e3b74-143">Minimum operating system</span></span> | <span data-ttu-id="e3b74-144">Windows 98</span><span class="sxs-lookup"><span data-stu-id="e3b74-144">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e3b74-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e3b74-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3b74-146">Costanti Direct3D</span><span class="sxs-lookup"><span data-stu-id="e3b74-146">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



