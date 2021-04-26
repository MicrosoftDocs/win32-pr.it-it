---
description: Costanti che descrivono i tipi di dati dei vertici supportati da un dispositivo.
ms.assetid: 751d7b92-b187-40e5-882c-6fdb80e1ff5f
title: D3DDTCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 094ca568554722f4da2606233f4ad2c1e59e892f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999448"
---
# <a name="d3ddtcaps"></a><span data-ttu-id="637c1-103">D3DDTCAPS</span><span class="sxs-lookup"><span data-stu-id="637c1-103">D3DDTCAPS</span></span>

<span data-ttu-id="637c1-104">Costanti che descrivono i tipi di dati dei vertici supportati da un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="637c1-104">Constants describing the vertex data types supported by a device.</span></span>



| <span data-ttu-id="637c1-105">\#Definire</span><span class="sxs-lookup"><span data-stu-id="637c1-105">\#define</span></span>              | <span data-ttu-id="637c1-106">Valore</span><span class="sxs-lookup"><span data-stu-id="637c1-106">Value</span></span>       | <span data-ttu-id="637c1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="637c1-107">Description</span></span>                                                                                                                   |
|-----------------------|-------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="637c1-108">D3DDTCAPS \_ UBYTE4</span><span class="sxs-lookup"><span data-stu-id="637c1-108">D3DDTCAPS\_UBYTE4</span></span>     | <span data-ttu-id="637c1-109">0x00000001L</span><span class="sxs-lookup"><span data-stu-id="637c1-109">0x00000001L</span></span> | <span data-ttu-id="637c1-110">Byte senza segno 4D.</span><span class="sxs-lookup"><span data-stu-id="637c1-110">4D unsigned byte.</span></span>                                                                                                             |
| <span data-ttu-id="637c1-111">D3DDTCAPS \_ UBYTE4N</span><span class="sxs-lookup"><span data-stu-id="637c1-111">D3DDTCAPS\_UBYTE4N</span></span>    | <span data-ttu-id="637c1-112">0x00000002L</span><span class="sxs-lookup"><span data-stu-id="637c1-112">0x00000002L</span></span> | <span data-ttu-id="637c1-113">Byte senza segno normalizzato 4D.</span><span class="sxs-lookup"><span data-stu-id="637c1-113">Normalized, 4D unsigned byte.</span></span> <span data-ttu-id="637c1-114">Ognuno dei quattro byte viene normalizzato dividendo a 255,0.</span><span class="sxs-lookup"><span data-stu-id="637c1-114">Each of the four bytes is normalized by dividing to 255.0.</span></span>                                      |
| <span data-ttu-id="637c1-115">D3DDTCAPS \_ SHORT2N</span><span class="sxs-lookup"><span data-stu-id="637c1-115">D3DDTCAPS\_SHORT2N</span></span>    | <span data-ttu-id="637c1-116">0x00000004L</span><span class="sxs-lookup"><span data-stu-id="637c1-116">0x00000004L</span></span> | <span data-ttu-id="637c1-117">Normalized, 2D signed short, expanded to (first byte/32767.0, second byte/32767.0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="637c1-117">Normalized, 2D signed short, expanded to (first byte/32767.0, second byte/32767.0, 0, 1).</span></span>                                     |
| <span data-ttu-id="637c1-118">D3DDTCAPS \_ SHORT4N</span><span class="sxs-lookup"><span data-stu-id="637c1-118">D3DDTCAPS\_SHORT4N</span></span>    | <span data-ttu-id="637c1-119">0x00000008L</span><span class="sxs-lookup"><span data-stu-id="637c1-119">0x00000008L</span></span> | <span data-ttu-id="637c1-120">Normalized, 4D signed short, expanded to (first byte/32767.0, second byte/32767.0, third byte/32767.0, fourth byte/32767.0).</span><span class="sxs-lookup"><span data-stu-id="637c1-120">Normalized, 4D signed short, expanded to (first byte/32767.0, second byte/32767.0, third byte/32767.0, fourth byte/32767.0).</span></span>  |
| <span data-ttu-id="637c1-121">D3DDTCAPS \_ USHORT2N</span><span class="sxs-lookup"><span data-stu-id="637c1-121">D3DDTCAPS\_USHORT2N</span></span>   | <span data-ttu-id="637c1-122">0x00000010L</span><span class="sxs-lookup"><span data-stu-id="637c1-122">0x00000010L</span></span> | <span data-ttu-id="637c1-123">Normalizzato, 2D unsigned short, espanso in (primo byte/65535.0, secondo byte/65535.0, 0, 1).</span><span class="sxs-lookup"><span data-stu-id="637c1-123">Normalized, 2D unsigned short, expanded to (first byte/65535.0, second byte/65535.0, 0, 1).</span></span>                                   |
| <span data-ttu-id="637c1-124">D3DDTCAPS \_ USHORT4N</span><span class="sxs-lookup"><span data-stu-id="637c1-124">D3DDTCAPS\_USHORT4N</span></span>   | <span data-ttu-id="637c1-125">0x00000020L</span><span class="sxs-lookup"><span data-stu-id="637c1-125">0x00000020L</span></span> | <span data-ttu-id="637c1-126">Normalized 4D unsigned short, expanded to (first byte/65535.0, second byte/65535.0, third byte/65535.0, fourth byte/65535.0).</span><span class="sxs-lookup"><span data-stu-id="637c1-126">Normalized 4D unsigned short, expanded to (first byte/65535.0, second byte/65535.0, third byte/65535.0, fourth byte/65535.0).</span></span> |
| <span data-ttu-id="637c1-127">D3DDTCAPS \_ UDEC3</span><span class="sxs-lookup"><span data-stu-id="637c1-127">D3DDTCAPS\_UDEC3</span></span>      | <span data-ttu-id="637c1-128">0x00000040L</span><span class="sxs-lookup"><span data-stu-id="637c1-128">0x00000040L</span></span> | <span data-ttu-id="637c1-129">Formato 3D senza segno 10 10 10 espanso in (valore, valore, valore, 1).</span><span class="sxs-lookup"><span data-stu-id="637c1-129">3D unsigned 10 10 10 format expanded to (value, value, value, 1).</span></span>                                                             |
| <span data-ttu-id="637c1-130">D3DDTCAPS \_ DEC3N</span><span class="sxs-lookup"><span data-stu-id="637c1-130">D3DDTCAPS\_DEC3N</span></span>      | <span data-ttu-id="637c1-131">0x00000080L</span><span class="sxs-lookup"><span data-stu-id="637c1-131">0x00000080L</span></span> | <span data-ttu-id="637c1-132">Formato 10 10 10 con segno 3D normalizzato ed espanso a (v \[ 0 \] /511.0, v \[ 1 \] /511.0, v \[ 2 \] /511.0, 1).</span><span class="sxs-lookup"><span data-stu-id="637c1-132">3D signed 10 10 10 format normalized and expanded to (v\[0\]/511.0, v\[1\]/511.0, v\[2\]/511.0, 1).</span></span>                           |
| <span data-ttu-id="637c1-133">D3DDTCAPS \_ FLOAT16 \_ 2</span><span class="sxs-lookup"><span data-stu-id="637c1-133">D3DDTCAPS\_FLOAT16\_2</span></span> | <span data-ttu-id="637c1-134">0x00000100L</span><span class="sxs-lookup"><span data-stu-id="637c1-134">0x00000100L</span></span> | <span data-ttu-id="637c1-135">Numeri a virgola mobile a 16 bit 2D.</span><span class="sxs-lookup"><span data-stu-id="637c1-135">2D 16-bit floating point numbers.</span></span>                                                                                             |
| <span data-ttu-id="637c1-136">D3DDTCAPS \_ FLOAT16 \_ 4</span><span class="sxs-lookup"><span data-stu-id="637c1-136">D3DDTCAPS\_FLOAT16\_4</span></span> | <span data-ttu-id="637c1-137">0x00000200L</span><span class="sxs-lookup"><span data-stu-id="637c1-137">0x00000200L</span></span> | <span data-ttu-id="637c1-138">Numeri a virgola mobile a 16 bit 4D.</span><span class="sxs-lookup"><span data-stu-id="637c1-138">4D 16-bit floating point numbers.</span></span>                                                                                             |



 

<span data-ttu-id="637c1-139">Queste costanti vengono usate dal membro DeclTypes di [**D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)</span><span class="sxs-lookup"><span data-stu-id="637c1-139">These constants are used by the DeclTypes member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="637c1-140">Informazioni sulle costanti</span><span class="sxs-lookup"><span data-stu-id="637c1-140">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="637c1-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="637c1-141">Header</span></span>                   | <span data-ttu-id="637c1-142">d3d9caps.h</span><span class="sxs-lookup"><span data-stu-id="637c1-142">d3d9caps.h</span></span> |
| <span data-ttu-id="637c1-143">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="637c1-143">Minimum operating system</span></span> | <span data-ttu-id="637c1-144">Windows 98</span><span class="sxs-lookup"><span data-stu-id="637c1-144">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="637c1-145">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="637c1-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="637c1-146">Costanti Direct3D</span><span class="sxs-lookup"><span data-stu-id="637c1-146">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



