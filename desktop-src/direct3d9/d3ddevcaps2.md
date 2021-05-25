---
description: Flag di funzionalità del driver D3DDEVCAPS2.
ms.assetid: 3f3b9f86-dee3-4506-bd2e-1dcc8ba617ed
title: D3DDEVCAPS2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6296db9b338d5f9a8c8ede702a784baf1fdfd462
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343206"
---
# <a name="d3ddevcaps2"></a><span data-ttu-id="cb380-103">D3DDEVCAPS2</span><span class="sxs-lookup"><span data-stu-id="cb380-103">D3DDEVCAPS2</span></span>

<span data-ttu-id="cb380-104">Flag di funzionalità del driver D3DDEVCAPS2.</span><span class="sxs-lookup"><span data-stu-id="cb380-104">D3DDEVCAPS2 driver capability flags.</span></span>



| <span data-ttu-id="cb380-105">\#Definire</span><span class="sxs-lookup"><span data-stu-id="cb380-105">\#define</span></span>                                        | <span data-ttu-id="cb380-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cb380-106">Description</span></span>                                                                                                                                                                                                               |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb380-107">D3DDEVCAPS2 \_ ADAPTIVETESSRTPATCH</span><span class="sxs-lookup"><span data-stu-id="cb380-107">D3DDEVCAPS2\_ADAPTIVETESSRTPATCH</span></span>                | <span data-ttu-id="cb380-108">Il dispositivo supporta la tessellazione adattiva delle patch RT</span><span class="sxs-lookup"><span data-stu-id="cb380-108">Device supports adaptive tessellation of RT-patches</span></span>                                                                                                                                                                       |
| <span data-ttu-id="cb380-109">D3DDEVCAPS2 \_ ADAPTIVETESSNPATCH</span><span class="sxs-lookup"><span data-stu-id="cb380-109">D3DDEVCAPS2\_ADAPTIVETESSNPATCH</span></span>                 | <span data-ttu-id="cb380-110">Il dispositivo supporta la tessellazione adattiva delle N-patch.</span><span class="sxs-lookup"><span data-stu-id="cb380-110">Device supports adaptive tessellation of N-patches.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="cb380-111">D3DDEVCAPS2 \_ PUÒ \_ ESTENDERSI DALLE \_ \_ TRAME</span><span class="sxs-lookup"><span data-stu-id="cb380-111">D3DDEVCAPS2\_CAN\_STRETCHRECT\_FROM\_TEXTURES</span></span>   | <span data-ttu-id="cb380-112">Il dispositivo supporta [**StretchRect usando**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect) una trama come origine.</span><span class="sxs-lookup"><span data-stu-id="cb380-112">Device supports [**StretchRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect) using a texture as the source.</span></span>                                                                                                                       |
| <span data-ttu-id="cb380-113">D3DDEVCAPS2 \_ DMAPNPATCH</span><span class="sxs-lookup"><span data-stu-id="cb380-113">D3DDEVCAPS2\_DMAPNPATCH</span></span>                         | <span data-ttu-id="cb380-114">Il dispositivo supporta le mappe di spostamento per le patch N.</span><span class="sxs-lookup"><span data-stu-id="cb380-114">Device supports displacement maps for N-patches.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="cb380-115">D3DDEVCAPS2 \_ PRESAMPLEDDMAPNPATCH</span><span class="sxs-lookup"><span data-stu-id="cb380-115">D3DDEVCAPS2\_PRESAMPLEDDMAPNPATCH</span></span>               | <span data-ttu-id="cb380-116">Il dispositivo supporta mappe di spostamento precampionato per N-patch.</span><span class="sxs-lookup"><span data-stu-id="cb380-116">Device supports presampled displacement maps for N-patches.</span></span> <span data-ttu-id="cb380-117">Per altre informazioni sul mapping dello spostamento, vedere [Mapping di spostamento (Direct3D 9).](displacement-mapping.md)</span><span class="sxs-lookup"><span data-stu-id="cb380-117">For more information about displacement mapping, see [Displacement Mapping (Direct3D 9)](displacement-mapping.md).</span></span>                                           |
| <span data-ttu-id="cb380-118">D3DDEVCAPS2 \_ STREAMOFFSET</span><span class="sxs-lookup"><span data-stu-id="cb380-118">D3DDEVCAPS2\_STREAMOFFSET</span></span>                       | <span data-ttu-id="cb380-119">Il dispositivo supporta gli offset di flusso.</span><span class="sxs-lookup"><span data-stu-id="cb380-119">Device supports stream offsets.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="cb380-120">D3DDEVCAPS2 \_ VERTEXELEMENTSCANSHARESTREAMOFFSET</span><span class="sxs-lookup"><span data-stu-id="cb380-120">D3DDEVCAPS2\_VERTEXELEMENTSCANSHARESTREAMOFFSET</span></span> | <span data-ttu-id="cb380-121">Più elementi vertice possono condividere lo stesso offset in un flusso se D3DDEVCAPS2 VERTEXELEMENTSCANSHARESTREAMOFFSET è impostato dal dispositivo e la dichiarazione del vertice non ha un elemento \_ con D3DDECLUSAGE \_ POSITIONT0.</span><span class="sxs-lookup"><span data-stu-id="cb380-121">Multiple vertex elements can share the same offset in a stream if D3DDEVCAPS2\_VERTEXELEMENTSCANSHARESTREAMOFFSET is set by the device and the vertex declaration does not have an element with D3DDECLUSAGE\_POSITIONT0.</span></span> |



 

## <a name="constant-information"></a><span data-ttu-id="cb380-122">Informazioni sulle costanti</span><span class="sxs-lookup"><span data-stu-id="cb380-122">Constant Information</span></span>



| <span data-ttu-id="cb380-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb380-123">Requirement</span></span>                         | <span data-ttu-id="cb380-124">Valore</span><span class="sxs-lookup"><span data-stu-id="cb380-124">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="cb380-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cb380-125">Header</span></span>                   | <span data-ttu-id="cb380-126">d3d9caps.h</span><span class="sxs-lookup"><span data-stu-id="cb380-126">d3d9caps.h</span></span> |
| <span data-ttu-id="cb380-127">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="cb380-127">Minimum operating system</span></span> | <span data-ttu-id="cb380-128">Windows 98</span><span class="sxs-lookup"><span data-stu-id="cb380-128">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="cb380-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="cb380-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb380-130">Costanti Direct3D</span><span class="sxs-lookup"><span data-stu-id="cb380-130">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
