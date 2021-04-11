---
description: Metriche della velocità effettiva per informazioni sulla comprensione delle prestazioni di un'applicazione.
ms.assetid: c0bcf060-a0ed-4c85-9554-398ffe4b4235
title: Struttura D3DDEVINFO_D3D9BANDWIDTHTIMINGS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9BANDWIDTHTIMINGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3bfb98045e645f20fa77cf8523040b995f6c254a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104234977"
---
# <a name="d3ddevinfo_d3d9bandwidthtimings-structure"></a><span data-ttu-id="a7707-103">\_Struttura D3DDEVINFO D3D9BANDWIDTHTIMINGS</span><span class="sxs-lookup"><span data-stu-id="a7707-103">D3DDEVINFO\_D3D9BANDWIDTHTIMINGS structure</span></span>

<span data-ttu-id="a7707-104">Metriche della velocità effettiva per informazioni sulla comprensione delle prestazioni di un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a7707-104">Throughput metrics for help in understanding the performance of an application.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7707-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a7707-105">Syntax</span></span>


```C++
typedef struct D3DDEVINFO_D3D9BANDWIDTHTIMINGS {
  FLOAT MaxBandwidthUtilized;
  FLOAT FrontEndUploadMemoryUtilizedPercent;
  FLOAT VertexRateUtilizedPercent;
  FLOAT TriangleSetupRateUtilizedPercent;
  FLOAT FillRateUtilizedPercent;
} D3DDEVINFO_D3D9BANDWIDTHTIMINGS, *LPD3DDEVINFO_D3D9BANDWIDTHTIMINGS;
```



## <a name="members"></a><span data-ttu-id="a7707-106">Members</span><span class="sxs-lookup"><span data-stu-id="a7707-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a7707-107">**MaxBandwidthUtilized**</span><span class="sxs-lookup"><span data-stu-id="a7707-107">**MaxBandwidthUtilized**</span></span>
</dt> <dd>

<span data-ttu-id="a7707-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a7707-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a7707-109">La velocità massima di trasferimento dati o la larghezza di banda dalla CPU dell'host alla GPU.</span><span class="sxs-lookup"><span data-stu-id="a7707-109">The bandwidth or maximum data transfer rate from the host CPU to the GPU.</span></span> <span data-ttu-id="a7707-110">Si tratta in genere della larghezza di banda del bus PCI o AGP che connette la CPU e la GPU.</span><span class="sxs-lookup"><span data-stu-id="a7707-110">This is typically the bandwidth of the PCI or AGP bus which connects the CPU and the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="a7707-111">**FrontEndUploadMemoryUtilizedPercent**</span><span class="sxs-lookup"><span data-stu-id="a7707-111">**FrontEndUploadMemoryUtilizedPercent**</span></span>
</dt> <dd>

<span data-ttu-id="a7707-112">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a7707-112">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a7707-113">Percentuale di memoria utilizzata durante il caricamento dei dati dalla CPU dell'host alla GPU.</span><span class="sxs-lookup"><span data-stu-id="a7707-113">Memory utilized percentage when uploading data from the host CPU to the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="a7707-114">**VertexRateUtilizedPercent**</span><span class="sxs-lookup"><span data-stu-id="a7707-114">**VertexRateUtilizedPercent**</span></span>
</dt> <dd>

<span data-ttu-id="a7707-115">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a7707-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a7707-116">Percentuale di velocità effettiva vertice.</span><span class="sxs-lookup"><span data-stu-id="a7707-116">Vertex throughput percentage.</span></span> <span data-ttu-id="a7707-117">Questo è il numero di vertici elaborati rispetto alla velocità di elaborazione dei vertici massima teorica.</span><span class="sxs-lookup"><span data-stu-id="a7707-117">This is the number of vertices processed compared to the theoretical maximum vertex processing rate.</span></span>

</dd> <dt>

<span data-ttu-id="a7707-118">**TriangleSetupRateUtilizedPercent**</span><span class="sxs-lookup"><span data-stu-id="a7707-118">**TriangleSetupRateUtilizedPercent**</span></span>
</dt> <dd>

<span data-ttu-id="a7707-119">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a7707-119">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a7707-120">Percentuale di velocità effettiva di configurazione del triangolo.</span><span class="sxs-lookup"><span data-stu-id="a7707-120">Triangle set-up throughput percentage.</span></span> <span data-ttu-id="a7707-121">Questo è il numero di triangoli configurati per la rasterizzazione rispetto alla velocità di configurazione massima teorica del triangolo.</span><span class="sxs-lookup"><span data-stu-id="a7707-121">This is the number of triangles that are set up for rasterization compared to the theoretical maximum triangle set-up rate.</span></span>

</dd> <dt>

<span data-ttu-id="a7707-122">**FillRateUtilizedPercent**</span><span class="sxs-lookup"><span data-stu-id="a7707-122">**FillRateUtilizedPercent**</span></span>
</dt> <dd>

<span data-ttu-id="a7707-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a7707-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="a7707-124">Percentuale di velocità effettiva di riempimento pixel.</span><span class="sxs-lookup"><span data-stu-id="a7707-124">Pixel fill throughput percentage.</span></span> <span data-ttu-id="a7707-125">Il numero di pixel compilati rispetto al riempimento teorico dei pixel.</span><span class="sxs-lookup"><span data-stu-id="a7707-125">This is the number of pixels that are filled compared to the theoretical pixel fill.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a7707-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a7707-126">Requirements</span></span>



| <span data-ttu-id="a7707-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7707-127">Requirement</span></span> | <span data-ttu-id="a7707-128">Valore</span><span class="sxs-lookup"><span data-stu-id="a7707-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7707-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a7707-129">Header</span></span><br/> | <dl> <span data-ttu-id="a7707-130"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7707-130"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7707-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a7707-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7707-132">Strutture Direct3D</span><span class="sxs-lookup"><span data-stu-id="a7707-132">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="a7707-133">**GetData**</span><span class="sxs-lookup"><span data-stu-id="a7707-133">**GetData**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
