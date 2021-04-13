---
title: WaveReadLaneAt (funzione)
description: Restituisce il valore dell'espressione per l'indice della corsia specificato all'interno dell'onda specificata.
ms.assetid: CA9467D9-8885-4A5D-87F3-5BA40AE78993
keywords:
- Funzione WaveReadLaneAt HLSL
topic_type:
- apiref
api_name:
- WaveReadLaneAt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e40940f2df6685a3096da6886ad3bcb6d9ca99af
ms.sourcegitcommit: 4423a9d48f1c90d2ec2eca68e9cae30df1787f25
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/25/2020
ms.locfileid: "104398811"
---
# <a name="wavereadlaneat-function"></a><span data-ttu-id="e9232-104">WaveReadLaneAt (funzione)</span><span class="sxs-lookup"><span data-stu-id="e9232-104">WaveReadLaneAt function</span></span>

<span data-ttu-id="e9232-105">Restituisce il valore dell'espressione per l'indice della corsia specificato all'interno dell'onda specificata.</span><span class="sxs-lookup"><span data-stu-id="e9232-105">Returns the value of the expression for the given lane index within the specified wave.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9232-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e9232-106">Syntax</span></span>

``` syntax
<type> WaveReadLaneAt(
   <type> expr,
   uint laneIndex
);
```

## <a name="parameters"></a><span data-ttu-id="e9232-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="e9232-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9232-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="e9232-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="e9232-109">Espressione da valutare.</span><span class="sxs-lookup"><span data-stu-id="e9232-109">The expression to evaluate.</span></span>

</dd> <dt>

<span data-ttu-id="e9232-110">*laneIndex*</span><span class="sxs-lookup"><span data-stu-id="e9232-110">*laneIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="e9232-111">Indice della corsia per cui verrà restituito il risultato *expr* .</span><span class="sxs-lookup"><span data-stu-id="e9232-111">The index of the lane for which the *expr* result will be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9232-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e9232-112">Return value</span></span>

<span data-ttu-id="e9232-113">Il valore risultante è il risultato di *expr*.</span><span class="sxs-lookup"><span data-stu-id="e9232-113">The resulting value is the result of *expr*.</span></span> <span data-ttu-id="e9232-114">Sarà uniforme se *laneIndex* è uniforme.</span><span class="sxs-lookup"><span data-stu-id="e9232-114">It will be uniform if *laneIndex* is uniform.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9232-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="e9232-115">Remarks</span></span>

<span data-ttu-id="e9232-116">Questa funzione è effettivamente una trasmissione del valore nella corsia laneIndex'th.</span><span class="sxs-lookup"><span data-stu-id="e9232-116">This function is effectively a broadcast of the value in the laneIndex’th lane.</span></span>

<span data-ttu-id="e9232-117">Questa funzione è supportata dal modello shader 6,0, nei tipi di shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="e9232-117">This function is supported from shader model 6.0, in the following types of shaders:</span></span>



| <span data-ttu-id="e9232-118">Vertice</span><span class="sxs-lookup"><span data-stu-id="e9232-118">Vertex</span></span> | <span data-ttu-id="e9232-119">Hull</span><span class="sxs-lookup"><span data-stu-id="e9232-119">Hull</span></span> | <span data-ttu-id="e9232-120">Dominio</span><span class="sxs-lookup"><span data-stu-id="e9232-120">Domain</span></span> | <span data-ttu-id="e9232-121">Geometria</span><span class="sxs-lookup"><span data-stu-id="e9232-121">Geometry</span></span> | <span data-ttu-id="e9232-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="e9232-122">Pixel</span></span> | <span data-ttu-id="e9232-123">Calcolo</span><span class="sxs-lookup"><span data-stu-id="e9232-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="e9232-124">x</span><span class="sxs-lookup"><span data-stu-id="e9232-124">x</span></span>     | <span data-ttu-id="e9232-125">x</span><span class="sxs-lookup"><span data-stu-id="e9232-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="e9232-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e9232-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9232-127">Panoramica del modello di shader 6</span><span class="sxs-lookup"><span data-stu-id="e9232-127">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="e9232-128">Modello shader 6</span><span class="sxs-lookup"><span data-stu-id="e9232-128">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




