---
description: Flag funzionalità stencil driver.
ms.assetid: 187c758c-5e7f-48ee-97cb-b1f30b709723
title: D3DSTENCILCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2e76c42acfcf8b6515e84679ea2fb540178608
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401384"
---
# <a name="d3dstencilcaps"></a><span data-ttu-id="fca7c-103">D3DSTENCILCAPS</span><span class="sxs-lookup"><span data-stu-id="fca7c-103">D3DSTENCILCAPS</span></span>

<span data-ttu-id="fca7c-104">Flag funzionalità stencil driver.</span><span class="sxs-lookup"><span data-stu-id="fca7c-104">Driver stencil capability flags.</span></span>



|                          |             |                                                                                                       |
|--------------------------|-------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fca7c-105">\#definire</span><span class="sxs-lookup"><span data-stu-id="fca7c-105">\#define</span></span>                 | <span data-ttu-id="fca7c-106">Valore</span><span class="sxs-lookup"><span data-stu-id="fca7c-106">Value</span></span>       | <span data-ttu-id="fca7c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fca7c-107">Description</span></span>                                                                                           |
| <span data-ttu-id="fca7c-108">D3DSTENCILCAPS \_ Keep</span><span class="sxs-lookup"><span data-stu-id="fca7c-108">D3DSTENCILCAPS\_KEEP</span></span>     | <span data-ttu-id="fca7c-109">0x00000001L</span><span class="sxs-lookup"><span data-stu-id="fca7c-109">0x00000001L</span></span> | <span data-ttu-id="fca7c-110">Non aggiornare la voce nel buffer dello stencil.</span><span class="sxs-lookup"><span data-stu-id="fca7c-110">Do not update the entry in the stencil buffer.</span></span> <span data-ttu-id="fca7c-111">Si tratta del valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="fca7c-111">This is the default value.</span></span>                             |
| <span data-ttu-id="fca7c-112">D3DSTENCILCAPS \_ zero</span><span class="sxs-lookup"><span data-stu-id="fca7c-112">D3DSTENCILCAPS\_ZERO</span></span>     | <span data-ttu-id="fca7c-113">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="fca7c-113">0x00000002L</span></span> | <span data-ttu-id="fca7c-114">Impostare la voce stencil-buffer su 0.</span><span class="sxs-lookup"><span data-stu-id="fca7c-114">Set the stencil-buffer entry to 0.</span></span>                                                                    |
| <span data-ttu-id="fca7c-115">D3DSTENCILCAPS \_ Sostituisci</span><span class="sxs-lookup"><span data-stu-id="fca7c-115">D3DSTENCILCAPS\_REPLACE</span></span>  | <span data-ttu-id="fca7c-116">0x00000004L</span><span class="sxs-lookup"><span data-stu-id="fca7c-116">0x00000004L</span></span> | <span data-ttu-id="fca7c-117">Sostituire la voce dello stencil buffer con il valore di riferimento.</span><span class="sxs-lookup"><span data-stu-id="fca7c-117">Replace the stencil-buffer entry with reference value.</span></span>                                                |
| <span data-ttu-id="fca7c-118">\_INCRSAT D3DSTENCILCAPS</span><span class="sxs-lookup"><span data-stu-id="fca7c-118">D3DSTENCILCAPS\_INCRSAT</span></span>  | <span data-ttu-id="fca7c-119">0x00000008L</span><span class="sxs-lookup"><span data-stu-id="fca7c-119">0x00000008L</span></span> | <span data-ttu-id="fca7c-120">Incrementa la voce dello stencil buffer, bloccando il valore massimo.</span><span class="sxs-lookup"><span data-stu-id="fca7c-120">Increment the stencil-buffer entry, clamping to the maximum value.</span></span>                                    |
| <span data-ttu-id="fca7c-121">\_DECRSAT D3DSTENCILCAPS</span><span class="sxs-lookup"><span data-stu-id="fca7c-121">D3DSTENCILCAPS\_DECRSAT</span></span>  | <span data-ttu-id="fca7c-122">0x00000010L</span><span class="sxs-lookup"><span data-stu-id="fca7c-122">0x00000010L</span></span> | <span data-ttu-id="fca7c-123">Decrementa la voce del buffer di stencil, che viene fissata a zero.</span><span class="sxs-lookup"><span data-stu-id="fca7c-123">Decrement the stencil-buffer entry, clamping to zero.</span></span>                                                 |
| <span data-ttu-id="fca7c-124">D3DSTENCILCAPS \_ invertito</span><span class="sxs-lookup"><span data-stu-id="fca7c-124">D3DSTENCILCAPS\_INVERT</span></span>   | <span data-ttu-id="fca7c-125">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="fca7c-125">0x00000020L</span></span> | <span data-ttu-id="fca7c-126">Inverti i bit nella voce dello stencil buffer.</span><span class="sxs-lookup"><span data-stu-id="fca7c-126">Invert the bits in the stencil-buffer entry.</span></span>                                                          |
| <span data-ttu-id="fca7c-127">\_Incr D3DSTENCILCAPS</span><span class="sxs-lookup"><span data-stu-id="fca7c-127">D3DSTENCILCAPS\_INCR</span></span>     | <span data-ttu-id="fca7c-128">0x00000040L</span><span class="sxs-lookup"><span data-stu-id="fca7c-128">0x00000040L</span></span> | <span data-ttu-id="fca7c-129">Incrementa la voce dello stencil buffer, eseguendo il wrapping su zero se il nuovo valore supera il valore massimo.</span><span class="sxs-lookup"><span data-stu-id="fca7c-129">Increment the stencil-buffer entry, wrapping to zero if the new value exceeds the maximum value.</span></span>      |
| <span data-ttu-id="fca7c-130">\_Decr D3DSTENCILCAPS</span><span class="sxs-lookup"><span data-stu-id="fca7c-130">D3DSTENCILCAPS\_DECR</span></span>     | <span data-ttu-id="fca7c-131">0x00000080L</span><span class="sxs-lookup"><span data-stu-id="fca7c-131">0x00000080L</span></span> | <span data-ttu-id="fca7c-132">Decrementa la voce dello stencil buffer, eseguendo il wrapping fino al valore massimo se il nuovo valore è minore di zero.</span><span class="sxs-lookup"><span data-stu-id="fca7c-132">Decrement the stencil-buffer entry, wrapping to the maximum value if the new value is less than zero.</span></span> |
| <span data-ttu-id="fca7c-133">\_TWOSIDED D3DSTENCILCAPS</span><span class="sxs-lookup"><span data-stu-id="fca7c-133">D3DSTENCILCAPS\_TWOSIDED</span></span> | <span data-ttu-id="fca7c-134">0x00000100L</span><span class="sxs-lookup"><span data-stu-id="fca7c-134">0x00000100L</span></span> | <span data-ttu-id="fca7c-135">Il dispositivo supporta lo stencil a due lati.</span><span class="sxs-lookup"><span data-stu-id="fca7c-135">The device supports two-sided stencil.</span></span>                                                                |



 

<span data-ttu-id="fca7c-136">Gli stencil: le voci del buffer sono valori integer compresi tra 0 e 2 Grigioni-1, dove n è la profondità di bit del buffer dello stencil.</span><span class="sxs-lookup"><span data-stu-id="fca7c-136">Stencil-buffer entries are integer values ranging from 0 through 2ⁿ - 1, where n is the bit depth of the stencil buffer.</span></span>

<span data-ttu-id="fca7c-137">Queste costanti vengono usate dal membro StencilCaps di [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="fca7c-137">These constants are used by the StencilCaps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="fca7c-138">Informazioni sulle costanti</span><span class="sxs-lookup"><span data-stu-id="fca7c-138">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="fca7c-139">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fca7c-139">Header</span></span>                   | <span data-ttu-id="fca7c-140">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="fca7c-140">d3d9caps.h</span></span> |
| <span data-ttu-id="fca7c-141">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="fca7c-141">Minimum operating system</span></span> | <span data-ttu-id="fca7c-142">Windows 98</span><span class="sxs-lookup"><span data-stu-id="fca7c-142">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="fca7c-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="fca7c-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fca7c-144">Costanti Direct3D</span><span class="sxs-lookup"><span data-stu-id="fca7c-144">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



