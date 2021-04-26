---
description: Flag di funzionalità dello stencil del driver.
ms.assetid: 187c758c-5e7f-48ee-97cb-b1f30b709723
title: D3DSTENCILCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6716748d77fe4c3620413f43ae4a4ae48076c09f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997378"
---
# <a name="d3dstencilcaps"></a><span data-ttu-id="b8797-103">D3DSTENCILCAPS</span><span class="sxs-lookup"><span data-stu-id="b8797-103">D3DSTENCILCAPS</span></span>

<span data-ttu-id="b8797-104">Flag di funzionalità dello stencil del driver.</span><span class="sxs-lookup"><span data-stu-id="b8797-104">Driver stencil capability flags.</span></span>



| <span data-ttu-id="b8797-105">\#Definire</span><span class="sxs-lookup"><span data-stu-id="b8797-105">\#define</span></span>                 | <span data-ttu-id="b8797-106">Valore</span><span class="sxs-lookup"><span data-stu-id="b8797-106">Value</span></span>       | <span data-ttu-id="b8797-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b8797-107">Description</span></span>                                                                                           |
|--------------------------|-------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8797-108">D3DSTENCILCAPS \_ KEEP</span><span class="sxs-lookup"><span data-stu-id="b8797-108">D3DSTENCILCAPS\_KEEP</span></span>     | <span data-ttu-id="b8797-109">0x00000001L</span><span class="sxs-lookup"><span data-stu-id="b8797-109">0x00000001L</span></span> | <span data-ttu-id="b8797-110">Non aggiornare la voce nel buffer degli stencil.</span><span class="sxs-lookup"><span data-stu-id="b8797-110">Do not update the entry in the stencil buffer.</span></span> <span data-ttu-id="b8797-111">Si tratta del valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="b8797-111">This is the default value.</span></span>                             |
| <span data-ttu-id="b8797-112">D3DSTENCILCAPS \_ ZERO</span><span class="sxs-lookup"><span data-stu-id="b8797-112">D3DSTENCILCAPS\_ZERO</span></span>     | <span data-ttu-id="b8797-113">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="b8797-113">0x00000002L</span></span> | <span data-ttu-id="b8797-114">Impostare la voce stencil-buffer su 0.</span><span class="sxs-lookup"><span data-stu-id="b8797-114">Set the stencil-buffer entry to 0.</span></span>                                                                    |
| <span data-ttu-id="b8797-115">D3DSTENCILCAPS \_ REPLACE</span><span class="sxs-lookup"><span data-stu-id="b8797-115">D3DSTENCILCAPS\_REPLACE</span></span>  | <span data-ttu-id="b8797-116">0x00000004L</span><span class="sxs-lookup"><span data-stu-id="b8797-116">0x00000004L</span></span> | <span data-ttu-id="b8797-117">Sostituire la voce stencil-buffer con il valore di riferimento.</span><span class="sxs-lookup"><span data-stu-id="b8797-117">Replace the stencil-buffer entry with reference value.</span></span>                                                |
| <span data-ttu-id="b8797-118">D3DSTENCILCAPS \_ INCRSAT</span><span class="sxs-lookup"><span data-stu-id="b8797-118">D3DSTENCILCAPS\_INCRSAT</span></span>  | <span data-ttu-id="b8797-119">0x00000008L</span><span class="sxs-lookup"><span data-stu-id="b8797-119">0x00000008L</span></span> | <span data-ttu-id="b8797-120">Incrementare la voce dello stencil buffer, fissando il valore massimo.</span><span class="sxs-lookup"><span data-stu-id="b8797-120">Increment the stencil-buffer entry, clamping to the maximum value.</span></span>                                    |
| <span data-ttu-id="b8797-121">D3DSTENCILCAPS \_ DECRSAT</span><span class="sxs-lookup"><span data-stu-id="b8797-121">D3DSTENCILCAPS\_DECRSAT</span></span>  | <span data-ttu-id="b8797-122">0x00000010L</span><span class="sxs-lookup"><span data-stu-id="b8797-122">0x00000010L</span></span> | <span data-ttu-id="b8797-123">Decrementare la voce dello stencil buffer, fissando a zero.</span><span class="sxs-lookup"><span data-stu-id="b8797-123">Decrement the stencil-buffer entry, clamping to zero.</span></span>                                                 |
| <span data-ttu-id="b8797-124">D3DSTENCILCAPS \_ INVERT</span><span class="sxs-lookup"><span data-stu-id="b8797-124">D3DSTENCILCAPS\_INVERT</span></span>   | <span data-ttu-id="b8797-125">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="b8797-125">0x00000020L</span></span> | <span data-ttu-id="b8797-126">Invertire i bit nella voce stencil-buffer.</span><span class="sxs-lookup"><span data-stu-id="b8797-126">Invert the bits in the stencil-buffer entry.</span></span>                                                          |
| <span data-ttu-id="b8797-127">D3DSTENCILCAPS \_ INCR</span><span class="sxs-lookup"><span data-stu-id="b8797-127">D3DSTENCILCAPS\_INCR</span></span>     | <span data-ttu-id="b8797-128">0x00000040L</span><span class="sxs-lookup"><span data-stu-id="b8797-128">0x00000040L</span></span> | <span data-ttu-id="b8797-129">Incrementare la voce stencil-buffer, a capo su zero se il nuovo valore supera il valore massimo.</span><span class="sxs-lookup"><span data-stu-id="b8797-129">Increment the stencil-buffer entry, wrapping to zero if the new value exceeds the maximum value.</span></span>      |
| <span data-ttu-id="b8797-130">DECREMENTO D3DSTENCILCAPS \_</span><span class="sxs-lookup"><span data-stu-id="b8797-130">D3DSTENCILCAPS\_DECR</span></span>     | <span data-ttu-id="b8797-131">0x00000080L</span><span class="sxs-lookup"><span data-stu-id="b8797-131">0x00000080L</span></span> | <span data-ttu-id="b8797-132">Decrementare la voce stencil-buffer, a capo fino al valore massimo se il nuovo valore è minore di zero.</span><span class="sxs-lookup"><span data-stu-id="b8797-132">Decrement the stencil-buffer entry, wrapping to the maximum value if the new value is less than zero.</span></span> |
| <span data-ttu-id="b8797-133">D3DSTENCILCAPS \_ TWOSIDED</span><span class="sxs-lookup"><span data-stu-id="b8797-133">D3DSTENCILCAPS\_TWOSIDED</span></span> | <span data-ttu-id="b8797-134">0x00000100L</span><span class="sxs-lookup"><span data-stu-id="b8797-134">0x00000100L</span></span> | <span data-ttu-id="b8797-135">Il dispositivo supporta stencil a due lati.</span><span class="sxs-lookup"><span data-stu-id="b8797-135">The device supports two-sided stencil.</span></span>                                                                |



 

<span data-ttu-id="b8797-136">Le voci stencil-buffer sono valori interi compresi tra 0 e 2ⁿ - 1, dove n è la profondità in bit del buffer degli stencil.</span><span class="sxs-lookup"><span data-stu-id="b8797-136">Stencil-buffer entries are integer values ranging from 0 through 2ⁿ - 1, where n is the bit depth of the stencil buffer.</span></span>

<span data-ttu-id="b8797-137">Queste costanti vengono usate dal membro StencilCaps di [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)</span><span class="sxs-lookup"><span data-stu-id="b8797-137">These constants are used by the StencilCaps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="b8797-138">Informazioni sulle costanti</span><span class="sxs-lookup"><span data-stu-id="b8797-138">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="b8797-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b8797-139">Header</span></span>                   | <span data-ttu-id="b8797-140">d3d9caps.h</span><span class="sxs-lookup"><span data-stu-id="b8797-140">d3d9caps.h</span></span> |
| <span data-ttu-id="b8797-141">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="b8797-141">Minimum operating system</span></span> | <span data-ttu-id="b8797-142">Windows 98</span><span class="sxs-lookup"><span data-stu-id="b8797-142">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b8797-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="b8797-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8797-144">Costanti Direct3D</span><span class="sxs-lookup"><span data-stu-id="b8797-144">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



