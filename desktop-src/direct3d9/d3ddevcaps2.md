---
description: Flag della funzionalità del driver D3DDEVCAPS2.
ms.assetid: 3f3b9f86-dee3-4506-bd2e-1dcc8ba617ed
title: D3DDEVCAPS2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e774076f5ad93abf5ab1ffc343f573497592728f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225626"
---
# <a name="d3ddevcaps2"></a><span data-ttu-id="9b756-103">D3DDEVCAPS2</span><span class="sxs-lookup"><span data-stu-id="9b756-103">D3DDEVCAPS2</span></span>

<span data-ttu-id="9b756-104">Flag della funzionalità del driver D3DDEVCAPS2.</span><span class="sxs-lookup"><span data-stu-id="9b756-104">D3DDEVCAPS2 driver capability flags.</span></span>



|                                                 |                                                                                                                                                                                                                           |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b756-105">\#definire</span><span class="sxs-lookup"><span data-stu-id="9b756-105">\#define</span></span>                                        | <span data-ttu-id="9b756-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9b756-106">Description</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="9b756-107">\_ADAPTIVETESSRTPATCH D3DDEVCAPS2</span><span class="sxs-lookup"><span data-stu-id="9b756-107">D3DDEVCAPS2\_ADAPTIVETESSRTPATCH</span></span>                | <span data-ttu-id="9b756-108">Il dispositivo supporta lo schema a mosaico adattivo delle patch RT</span><span class="sxs-lookup"><span data-stu-id="9b756-108">Device supports adaptive tessellation of RT-patches</span></span>                                                                                                                                                                       |
| <span data-ttu-id="9b756-109">\_ADAPTIVETESSNPATCH D3DDEVCAPS2</span><span class="sxs-lookup"><span data-stu-id="9b756-109">D3DDEVCAPS2\_ADAPTIVETESSNPATCH</span></span>                 | <span data-ttu-id="9b756-110">Il dispositivo supporta lo schema a mosaico adattivo di N-patch.</span><span class="sxs-lookup"><span data-stu-id="9b756-110">Device supports adaptive tessellation of N-patches.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="9b756-111">D3DDEVCAPS2 \_ può \_ STRETCHRECT \_ da \_ trame</span><span class="sxs-lookup"><span data-stu-id="9b756-111">D3DDEVCAPS2\_CAN\_STRETCHRECT\_FROM\_TEXTURES</span></span>   | <span data-ttu-id="9b756-112">Il dispositivo supporta [**StretchRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect) usando una trama come origine.</span><span class="sxs-lookup"><span data-stu-id="9b756-112">Device supports [**StretchRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect) using a texture as the source.</span></span>                                                                                                                       |
| <span data-ttu-id="9b756-113">\_DMAPNPATCH D3DDEVCAPS2</span><span class="sxs-lookup"><span data-stu-id="9b756-113">D3DDEVCAPS2\_DMAPNPATCH</span></span>                         | <span data-ttu-id="9b756-114">Il dispositivo supporta le mappe di spostamento per N-patch.</span><span class="sxs-lookup"><span data-stu-id="9b756-114">Device supports displacement maps for N-patches.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="9b756-115">\_PRESAMPLEDDMAPNPATCH D3DDEVCAPS2</span><span class="sxs-lookup"><span data-stu-id="9b756-115">D3DDEVCAPS2\_PRESAMPLEDDMAPNPATCH</span></span>               | <span data-ttu-id="9b756-116">Il dispositivo supporta le mappe di spostamento precampionate per N-patch.</span><span class="sxs-lookup"><span data-stu-id="9b756-116">Device supports presampled displacement maps for N-patches.</span></span> <span data-ttu-id="9b756-117">Per ulteriori informazioni sul mapping di spostamento, vedere [mapping di spostamento (Direct3D 9)](displacement-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="9b756-117">For more information about displacement mapping, see [Displacement Mapping (Direct3D 9)](displacement-mapping.md).</span></span>                                           |
| <span data-ttu-id="9b756-118">\_STREAMOFFSET D3DDEVCAPS2</span><span class="sxs-lookup"><span data-stu-id="9b756-118">D3DDEVCAPS2\_STREAMOFFSET</span></span>                       | <span data-ttu-id="9b756-119">Il dispositivo supporta gli offset del flusso.</span><span class="sxs-lookup"><span data-stu-id="9b756-119">Device supports stream offsets.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="9b756-120">\_VERTEXELEMENTSCANSHARESTREAMOFFSET D3DDEVCAPS2</span><span class="sxs-lookup"><span data-stu-id="9b756-120">D3DDEVCAPS2\_VERTEXELEMENTSCANSHARESTREAMOFFSET</span></span> | <span data-ttu-id="9b756-121">Più elementi Vertex possono condividere lo stesso offset in un flusso se D3DDEVCAPS2 \_ VERTEXELEMENTSCANSHARESTREAMOFFSET è impostato dal dispositivo e la dichiarazione del vertice non contiene un elemento con D3DDECLUSAGE \_ POSITIONT0.</span><span class="sxs-lookup"><span data-stu-id="9b756-121">Multiple vertex elements can share the same offset in a stream if D3DDEVCAPS2\_VERTEXELEMENTSCANSHARESTREAMOFFSET is set by the device and the vertex declaration does not have an element with D3DDECLUSAGE\_POSITIONT0.</span></span> |



 

## <a name="constant-information"></a><span data-ttu-id="9b756-122">Informazioni sulle costanti</span><span class="sxs-lookup"><span data-stu-id="9b756-122">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="9b756-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9b756-123">Header</span></span>                   | <span data-ttu-id="9b756-124">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="9b756-124">d3d9caps.h</span></span> |
| <span data-ttu-id="9b756-125">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="9b756-125">Minimum operating system</span></span> | <span data-ttu-id="9b756-126">Windows 98</span><span class="sxs-lookup"><span data-stu-id="9b756-126">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="9b756-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="9b756-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b756-128">Costanti Direct3D</span><span class="sxs-lookup"><span data-stu-id="9b756-128">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
