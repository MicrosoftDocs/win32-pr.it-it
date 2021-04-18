---
description: Percentuale del tempo di elaborazione dei dati nella pipeline.
ms.assetid: eb9dec27-2e45-4897-92af-8415c8fa08d4
title: Struttura D3DDEVINFO_D3D9PIPELINETIMINGS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9PIPELINETIMINGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 627eec0ea93181b14c308ab229ed603412511a91
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322405"
---
# <a name="d3ddevinfo_d3d9pipelinetimings-structure"></a><span data-ttu-id="e6ca5-103">\_Struttura D3DDEVINFO D3D9PIPELINETIMINGS</span><span class="sxs-lookup"><span data-stu-id="e6ca5-103">D3DDEVINFO\_D3D9PIPELINETIMINGS structure</span></span>

<span data-ttu-id="e6ca5-104">Percentuale del tempo di elaborazione dei dati nella pipeline.</span><span class="sxs-lookup"><span data-stu-id="e6ca5-104">Percent of time processing data in the pipeline.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6ca5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e6ca5-105">Syntax</span></span>


```C++
typedef struct D3DDEVINFO_D3D9PIPELINETIMINGS {
  FLOAT VertexProcessingTimePercent;
  FLOAT PixelProcessingTimePercent;
  FLOAT OtherGPUProcessingTimePercent;
  FLOAT GPUIdleTimePercent;
} D3DDEVINFO_D3D9PIPELINETIMINGS, *LPD3DDEVINFO_D3D9PIPELINETIMINGS;
```



## <a name="members"></a><span data-ttu-id="e6ca5-106">Members</span><span class="sxs-lookup"><span data-stu-id="e6ca5-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e6ca5-107">**VertexProcessingTimePercent**</span><span class="sxs-lookup"><span data-stu-id="e6ca5-107">**VertexProcessingTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="e6ca5-108">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e6ca5-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e6ca5-109">Percentuale di tempo impiegato per l'esecuzione di vertex shader.</span><span class="sxs-lookup"><span data-stu-id="e6ca5-109">Percent of time spent running vertex shaders.</span></span>

</dd> <dt>

<span data-ttu-id="e6ca5-110">**PixelProcessingTimePercent**</span><span class="sxs-lookup"><span data-stu-id="e6ca5-110">**PixelProcessingTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="e6ca5-111">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e6ca5-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e6ca5-112">Percentuale di tempo impiegato per l'esecuzione di pixel shader.</span><span class="sxs-lookup"><span data-stu-id="e6ca5-112">Percent of time spent running pixel shaders.</span></span>

</dd> <dt>

<span data-ttu-id="e6ca5-113">**OtherGPUProcessingTimePercent**</span><span class="sxs-lookup"><span data-stu-id="e6ca5-113">**OtherGPUProcessingTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="e6ca5-114">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e6ca5-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e6ca5-115">Percentuale di tempo impiegato per eseguire altre operazioni di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="e6ca5-115">Percent of time spent doing other processing.</span></span>

</dd> <dt>

<span data-ttu-id="e6ca5-116">**GPUIdleTimePercent**</span><span class="sxs-lookup"><span data-stu-id="e6ca5-116">**GPUIdleTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="e6ca5-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e6ca5-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e6ca5-118">Percentuale del tempo che non elabora alcun elemento.</span><span class="sxs-lookup"><span data-stu-id="e6ca5-118">Percent of time not processing anything.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e6ca5-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="e6ca5-119">Remarks</span></span>

<span data-ttu-id="e6ca5-120">Per ottenere prestazioni ottimali, è consigliabile un carico bilanciato.</span><span class="sxs-lookup"><span data-stu-id="e6ca5-120">For best performance, a balanced load is recommended.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6ca5-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e6ca5-121">Requirements</span></span>



| <span data-ttu-id="e6ca5-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6ca5-122">Requirement</span></span> | <span data-ttu-id="e6ca5-123">Valore</span><span class="sxs-lookup"><span data-stu-id="e6ca5-123">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6ca5-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e6ca5-124">Header</span></span><br/> | <dl> <span data-ttu-id="e6ca5-125"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6ca5-125"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6ca5-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e6ca5-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6ca5-127">Strutture Direct3D</span><span class="sxs-lookup"><span data-stu-id="e6ca5-127">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="e6ca5-128">**GetData**</span><span class="sxs-lookup"><span data-stu-id="e6ca5-128">**GetData**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
