---
description: Costanti che descrivono i tipi di dati dei vertici supportati da un dispositivo.
ms.assetid: 751d7b92-b187-40e5-882c-6fdb80e1ff5f
title: D3DDTCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49131fed9961782a6ade3d3ec5f541bb0fe63a50
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304794"
---
# <a name="d3ddtcaps"></a><span data-ttu-id="18a6f-103">D3DDTCAPS</span><span class="sxs-lookup"><span data-stu-id="18a6f-103">D3DDTCAPS</span></span>

<span data-ttu-id="18a6f-104">Costanti che descrivono i tipi di dati dei vertici supportati da un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="18a6f-104">Constants describing the vertex data types supported by a device.</span></span>



|                       |             |                                                                                                                               |
|-----------------------|-------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18a6f-105">\#definire</span><span class="sxs-lookup"><span data-stu-id="18a6f-105">\#define</span></span>              | <span data-ttu-id="18a6f-106">Valore</span><span class="sxs-lookup"><span data-stu-id="18a6f-106">Value</span></span>       | <span data-ttu-id="18a6f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="18a6f-107">Description</span></span>                                                                                                                   |
| <span data-ttu-id="18a6f-108">\_UBYTE4 D3DDTCAPS</span><span class="sxs-lookup"><span data-stu-id="18a6f-108">D3DDTCAPS\_UBYTE4</span></span>     | <span data-ttu-id="18a6f-109">0x00000001L</span><span class="sxs-lookup"><span data-stu-id="18a6f-109">0x00000001L</span></span> | <span data-ttu-id="18a6f-110">byte senza segno 4D.</span><span class="sxs-lookup"><span data-stu-id="18a6f-110">4D unsigned byte.</span></span>                                                                                                             |
| <span data-ttu-id="18a6f-111">\_Dati UBYTE4N D3DDTCAPS</span><span class="sxs-lookup"><span data-stu-id="18a6f-111">D3DDTCAPS\_UBYTE4N</span></span>    | <span data-ttu-id="18a6f-112">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="18a6f-112">0x00000002L</span></span> | <span data-ttu-id="18a6f-113">Normalizzato, byte senza segno 4D.</span><span class="sxs-lookup"><span data-stu-id="18a6f-113">Normalized, 4D unsigned byte.</span></span> <span data-ttu-id="18a6f-114">Ognuno dei quattro byte viene normalizzato dividendo in 255,0.</span><span class="sxs-lookup"><span data-stu-id="18a6f-114">Each of the four bytes is normalized by dividing to 255.0.</span></span>                                      |
| <span data-ttu-id="18a6f-115">\_SHORT2N D3DDTCAPS</span><span class="sxs-lookup"><span data-stu-id="18a6f-115">D3DDTCAPS\_SHORT2N</span></span>    | <span data-ttu-id="18a6f-116">0x00000004L</span><span class="sxs-lookup"><span data-stu-id="18a6f-116">0x00000004L</span></span> | <span data-ttu-id="18a6f-117">Normalizzato, short con segno 2D, espanso fino a (primo byte/32767.0, secondo byte/32767.0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="18a6f-117">Normalized, 2D signed short, expanded to (first byte/32767.0, second byte/32767.0, 0, 1).</span></span>                                     |
| <span data-ttu-id="18a6f-118">\_SHORT4N D3DDTCAPS</span><span class="sxs-lookup"><span data-stu-id="18a6f-118">D3DDTCAPS\_SHORT4N</span></span>    | <span data-ttu-id="18a6f-119">0x00000008L</span><span class="sxs-lookup"><span data-stu-id="18a6f-119">0x00000008L</span></span> | <span data-ttu-id="18a6f-120">Normalizzato, 4D con firma breve, espanso fino a (primo byte/32767.0, secondo byte/32767.0, terzo byte/32767.0, quarto byte/32767.0).</span><span class="sxs-lookup"><span data-stu-id="18a6f-120">Normalized, 4D signed short, expanded to (first byte/32767.0, second byte/32767.0, third byte/32767.0, fourth byte/32767.0).</span></span>  |
| <span data-ttu-id="18a6f-121">\_USHORT2N D3DDTCAPS</span><span class="sxs-lookup"><span data-stu-id="18a6f-121">D3DDTCAPS\_USHORT2N</span></span>   | <span data-ttu-id="18a6f-122">0x00000010L</span><span class="sxs-lookup"><span data-stu-id="18a6f-122">0x00000010L</span></span> | <span data-ttu-id="18a6f-123">Normalizzato, breve senza segno 2D, espanso in (primo byte/65535.0, secondo byte/65535.0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="18a6f-123">Normalized, 2D unsigned short, expanded to (first byte/65535.0, second byte/65535.0, 0, 1).</span></span>                                   |
| <span data-ttu-id="18a6f-124">\_USHORT4N D3DDTCAPS</span><span class="sxs-lookup"><span data-stu-id="18a6f-124">D3DDTCAPS\_USHORT4N</span></span>   | <span data-ttu-id="18a6f-125">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="18a6f-125">0x00000020L</span></span> | <span data-ttu-id="18a6f-126">Normalizzato di 4D senza segno, espanso fino a (primo byte/65535.0, secondo byte/65535.0, terzo byte/65535.0, quarto byte/65535.0).</span><span class="sxs-lookup"><span data-stu-id="18a6f-126">Normalized 4D unsigned short, expanded to (first byte/65535.0, second byte/65535.0, third byte/65535.0, fourth byte/65535.0).</span></span> |
| <span data-ttu-id="18a6f-127">\_UDEC3 D3DDTCAPS</span><span class="sxs-lookup"><span data-stu-id="18a6f-127">D3DDTCAPS\_UDEC3</span></span>      | <span data-ttu-id="18a6f-128">0x00000040L</span><span class="sxs-lookup"><span data-stu-id="18a6f-128">0x00000040L</span></span> | <span data-ttu-id="18a6f-129">formato 3D senza segno 10 10 10 espanso a (valore, valore, valore, 1).</span><span class="sxs-lookup"><span data-stu-id="18a6f-129">3D unsigned 10 10 10 format expanded to (value, value, value, 1).</span></span>                                                             |
| <span data-ttu-id="18a6f-130">\_DEC3N D3DDTCAPS</span><span class="sxs-lookup"><span data-stu-id="18a6f-130">D3DDTCAPS\_DEC3N</span></span>      | <span data-ttu-id="18a6f-131">0x00000080L</span><span class="sxs-lookup"><span data-stu-id="18a6f-131">0x00000080L</span></span> | <span data-ttu-id="18a6f-132">formato con firma 3D 10 10 10 normalizzato ed espanso a (v \[ 0 \] /511,0, v \[ 1 \] /511,0, v \[ 2 \] /511,0, 1).</span><span class="sxs-lookup"><span data-stu-id="18a6f-132">3D signed 10 10 10 format normalized and expanded to (v\[0\]/511.0, v\[1\]/511.0, v\[2\]/511.0, 1).</span></span>                           |
| <span data-ttu-id="18a6f-133">D3DDTCAPS \_ FLOAT16 \_ 2</span><span class="sxs-lookup"><span data-stu-id="18a6f-133">D3DDTCAPS\_FLOAT16\_2</span></span> | <span data-ttu-id="18a6f-134">0x00000100L</span><span class="sxs-lookup"><span data-stu-id="18a6f-134">0x00000100L</span></span> | <span data-ttu-id="18a6f-135">numeri a virgola mobile a 16 bit 2D.</span><span class="sxs-lookup"><span data-stu-id="18a6f-135">2D 16-bit floating point numbers.</span></span>                                                                                             |
| <span data-ttu-id="18a6f-136">D3DDTCAPS \_ FLOAT16 \_ 4</span><span class="sxs-lookup"><span data-stu-id="18a6f-136">D3DDTCAPS\_FLOAT16\_4</span></span> | <span data-ttu-id="18a6f-137">0x00000200L</span><span class="sxs-lookup"><span data-stu-id="18a6f-137">0x00000200L</span></span> | <span data-ttu-id="18a6f-138">numeri a virgola mobile a 16 bit 4D.</span><span class="sxs-lookup"><span data-stu-id="18a6f-138">4D 16-bit floating point numbers.</span></span>                                                                                             |



 

<span data-ttu-id="18a6f-139">Queste costanti vengono usate dal membro DeclTypes di [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="18a6f-139">These constants are used by the DeclTypes member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="18a6f-140">Informazioni sulle costanti</span><span class="sxs-lookup"><span data-stu-id="18a6f-140">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="18a6f-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="18a6f-141">Header</span></span>                   | <span data-ttu-id="18a6f-142">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="18a6f-142">d3d9caps.h</span></span> |
| <span data-ttu-id="18a6f-143">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="18a6f-143">Minimum operating system</span></span> | <span data-ttu-id="18a6f-144">Windows 98</span><span class="sxs-lookup"><span data-stu-id="18a6f-144">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="18a6f-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="18a6f-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18a6f-146">Costanti Direct3D</span><span class="sxs-lookup"><span data-stu-id="18a6f-146">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



