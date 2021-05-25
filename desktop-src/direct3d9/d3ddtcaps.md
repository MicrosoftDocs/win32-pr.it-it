---
description: Costanti che descrivono i tipi di dati dei vertici supportati da un dispositivo.
ms.assetid: 751d7b92-b187-40e5-882c-6fdb80e1ff5f
title: D3DDTCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97ded570b8f451ea7e99050467f70f945d202bd4
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343239"
---
# <a name="d3ddtcaps"></a><span data-ttu-id="5b5b0-103">D3DDTCAPS</span><span class="sxs-lookup"><span data-stu-id="5b5b0-103">D3DDTCAPS</span></span>

<span data-ttu-id="5b5b0-104">Costanti che descrivono i tipi di dati dei vertici supportati da un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5b5b0-104">Constants describing the vertex data types supported by a device.</span></span>



| <span data-ttu-id="5b5b0-105">\#Definire</span><span class="sxs-lookup"><span data-stu-id="5b5b0-105">\#define</span></span>              | <span data-ttu-id="5b5b0-106">Valore</span><span class="sxs-lookup"><span data-stu-id="5b5b0-106">Value</span></span>       | <span data-ttu-id="5b5b0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5b5b0-107">Description</span></span>                                                                                                                   |
|-----------------------|-------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b5b0-108">D3DDTCAPS \_ UBYTE4</span><span class="sxs-lookup"><span data-stu-id="5b5b0-108">D3DDTCAPS\_UBYTE4</span></span>     | <span data-ttu-id="5b5b0-109">0x00000001L</span><span class="sxs-lookup"><span data-stu-id="5b5b0-109">0x00000001L</span></span> | <span data-ttu-id="5b5b0-110">Byte senza segno 4D.</span><span class="sxs-lookup"><span data-stu-id="5b5b0-110">4D unsigned byte.</span></span>                                                                                                             |
| <span data-ttu-id="5b5b0-111">D3DDTCAPS \_ UBYTE4N</span><span class="sxs-lookup"><span data-stu-id="5b5b0-111">D3DDTCAPS\_UBYTE4N</span></span>    | <span data-ttu-id="5b5b0-112">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="5b5b0-112">0x00000002L</span></span> | <span data-ttu-id="5b5b0-113">Byte senza segno normalizzato e 4D.</span><span class="sxs-lookup"><span data-stu-id="5b5b0-113">Normalized, 4D unsigned byte.</span></span> <span data-ttu-id="5b5b0-114">Ognuno dei quattro byte viene normalizzato dividendo per 255,0.</span><span class="sxs-lookup"><span data-stu-id="5b5b0-114">Each of the four bytes is normalized by dividing to 255.0.</span></span>                                      |
| <span data-ttu-id="5b5b0-115">D3DDTCAPS \_ SHORT2N</span><span class="sxs-lookup"><span data-stu-id="5b5b0-115">D3DDTCAPS\_SHORT2N</span></span>    | <span data-ttu-id="5b5b0-116">0x00000004L</span><span class="sxs-lookup"><span data-stu-id="5b5b0-116">0x00000004L</span></span> | <span data-ttu-id="5b5b0-117">Normalized, 2D signed short, espanso in (first byte/32767.0, second byte/32767.0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="5b5b0-117">Normalized, 2D signed short, expanded to (first byte/32767.0, second byte/32767.0, 0, 1).</span></span>                                     |
| <span data-ttu-id="5b5b0-118">D3DDTCAPS \_ SHORT4N</span><span class="sxs-lookup"><span data-stu-id="5b5b0-118">D3DDTCAPS\_SHORT4N</span></span>    | <span data-ttu-id="5b5b0-119">0x00000008L</span><span class="sxs-lookup"><span data-stu-id="5b5b0-119">0x00000008L</span></span> | <span data-ttu-id="5b5b0-120">Normalizzato, 4D signed short, espanso in (primo byte/32767.0, secondo byte/32767.0, terzo byte/32767.0, quarto byte/32767.0).</span><span class="sxs-lookup"><span data-stu-id="5b5b0-120">Normalized, 4D signed short, expanded to (first byte/32767.0, second byte/32767.0, third byte/32767.0, fourth byte/32767.0).</span></span>  |
| <span data-ttu-id="5b5b0-121">D3DDTCAPS \_ USHORT2N</span><span class="sxs-lookup"><span data-stu-id="5b5b0-121">D3DDTCAPS\_USHORT2N</span></span>   | <span data-ttu-id="5b5b0-122">0x00000010L</span><span class="sxs-lookup"><span data-stu-id="5b5b0-122">0x00000010L</span></span> | <span data-ttu-id="5b5b0-123">Normalized, 2D unsigned short, espanso in (primo byte/65535.0, secondo byte/65535.0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="5b5b0-123">Normalized, 2D unsigned short, expanded to (first byte/65535.0, second byte/65535.0, 0, 1).</span></span>                                   |
| <span data-ttu-id="5b5b0-124">D3DDTCAPS \_ USHORT4N</span><span class="sxs-lookup"><span data-stu-id="5b5b0-124">D3DDTCAPS\_USHORT4N</span></span>   | <span data-ttu-id="5b5b0-125">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="5b5b0-125">0x00000020L</span></span> | <span data-ttu-id="5b5b0-126">Normalizzato 4D unsigned short, espanso a (primo byte/65535.0, secondo byte/65535.0, terzo byte/65535.0, quarto byte/65535.0).</span><span class="sxs-lookup"><span data-stu-id="5b5b0-126">Normalized 4D unsigned short, expanded to (first byte/65535.0, second byte/65535.0, third byte/65535.0, fourth byte/65535.0).</span></span> |
| <span data-ttu-id="5b5b0-127">D3DDTCAPS \_ UDEC3</span><span class="sxs-lookup"><span data-stu-id="5b5b0-127">D3DDTCAPS\_UDEC3</span></span>      | <span data-ttu-id="5b5b0-128">0x00000040L</span><span class="sxs-lookup"><span data-stu-id="5b5b0-128">0x00000040L</span></span> | <span data-ttu-id="5b5b0-129">Formato 3D senza segno 10 10 10 espanso in (valore, valore, valore, 1).</span><span class="sxs-lookup"><span data-stu-id="5b5b0-129">3D unsigned 10 10 10 format expanded to (value, value, value, 1).</span></span>                                                             |
| <span data-ttu-id="5b5b0-130">D3DDTCAPS \_ DEC3N</span><span class="sxs-lookup"><span data-stu-id="5b5b0-130">D3DDTCAPS\_DEC3N</span></span>      | <span data-ttu-id="5b5b0-131">0x00000080L</span><span class="sxs-lookup"><span data-stu-id="5b5b0-131">0x00000080L</span></span> | <span data-ttu-id="5b5b0-132">Formato 10 10 10 con segno 10 normalizzato ed espanso a (v \[ 0 \] /511.0, v \[ 1 \] /511.0, v \[ 2 \] /511.0, 1).</span><span class="sxs-lookup"><span data-stu-id="5b5b0-132">3D signed 10 10 10 format normalized and expanded to (v\[0\]/511.0, v\[1\]/511.0, v\[2\]/511.0, 1).</span></span>                           |
| <span data-ttu-id="5b5b0-133">D3DDTCAPS \_ FLOAT16 \_ 2</span><span class="sxs-lookup"><span data-stu-id="5b5b0-133">D3DDTCAPS\_FLOAT16\_2</span></span> | <span data-ttu-id="5b5b0-134">0x00000100L</span><span class="sxs-lookup"><span data-stu-id="5b5b0-134">0x00000100L</span></span> | <span data-ttu-id="5b5b0-135">Numeri a virgola mobile a 16 bit 2D.</span><span class="sxs-lookup"><span data-stu-id="5b5b0-135">2D 16-bit floating point numbers.</span></span>                                                                                             |
| <span data-ttu-id="5b5b0-136">D3DDTCAPS \_ FLOAT16 \_ 4</span><span class="sxs-lookup"><span data-stu-id="5b5b0-136">D3DDTCAPS\_FLOAT16\_4</span></span> | <span data-ttu-id="5b5b0-137">0x00000200L</span><span class="sxs-lookup"><span data-stu-id="5b5b0-137">0x00000200L</span></span> | <span data-ttu-id="5b5b0-138">Numeri a virgola mobile a 16 bit 4D.</span><span class="sxs-lookup"><span data-stu-id="5b5b0-138">4D 16-bit floating point numbers.</span></span>                                                                                             |



 

<span data-ttu-id="5b5b0-139">Queste costanti vengono usate dal membro DeclTypes di [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)</span><span class="sxs-lookup"><span data-stu-id="5b5b0-139">These constants are used by the DeclTypes member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="5b5b0-140">Informazioni costanti</span><span class="sxs-lookup"><span data-stu-id="5b5b0-140">Constant Information</span></span>



|  <span data-ttu-id="5b5b0-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b5b0-141">Requirement</span></span>                        | <span data-ttu-id="5b5b0-142">Valore</span><span class="sxs-lookup"><span data-stu-id="5b5b0-142">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="5b5b0-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5b5b0-143">Header</span></span>                   | <span data-ttu-id="5b5b0-144">d3d9caps.h</span><span class="sxs-lookup"><span data-stu-id="5b5b0-144">d3d9caps.h</span></span> |
| <span data-ttu-id="5b5b0-145">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="5b5b0-145">Minimum operating system</span></span> | <span data-ttu-id="5b5b0-146">Windows 98</span><span class="sxs-lookup"><span data-stu-id="5b5b0-146">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="5b5b0-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5b5b0-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b5b0-148">Costanti Direct3D</span><span class="sxs-lookup"><span data-stu-id="5b5b0-148">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



