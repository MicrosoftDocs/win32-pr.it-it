---
title: Funzione WaveReadLaneAt
description: Restituisce il valore dell'espressione per l'indice di corsia specificato all'interno dell'onda specificata.
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
ms.openlocfilehash: 573730053a93a110381637ef8e62dc08a4aa1535
ms.sourcegitcommit: 1897c2a39b4ac4ca4b1e4aec394cef2ce2619c03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/06/2021
ms.locfileid: "113316483"
---
# <a name="wavereadlaneat-function"></a><span data-ttu-id="0548b-104">Funzione WaveReadLaneAt</span><span class="sxs-lookup"><span data-stu-id="0548b-104">WaveReadLaneAt function</span></span>

<span data-ttu-id="0548b-105">Restituisce il valore dell'espressione per l'indice di corsia specificato all'interno dell'onda specificata.</span><span class="sxs-lookup"><span data-stu-id="0548b-105">Returns the value of the expression for the given lane index within the specified wave.</span></span>

## <a name="syntax"></a><span data-ttu-id="0548b-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0548b-106">Syntax</span></span>

``` syntax
<type> WaveReadLaneAt(
   <type> expr,
   uint laneIndex
);
```

## <a name="parameters"></a><span data-ttu-id="0548b-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="0548b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0548b-108">*Expr*</span><span class="sxs-lookup"><span data-stu-id="0548b-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="0548b-109">Espressione da valutare.</span><span class="sxs-lookup"><span data-stu-id="0548b-109">The expression to evaluate.</span></span>

</dd> <dt>

<span data-ttu-id="0548b-110">*laneIndex*</span><span class="sxs-lookup"><span data-stu-id="0548b-110">*laneIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="0548b-111">Indice della corsia per cui verrà restituito il risultato *expr.*</span><span class="sxs-lookup"><span data-stu-id="0548b-111">The index of the lane for which the *expr* result will be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0548b-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0548b-112">Return value</span></span>

<span data-ttu-id="0548b-113">Il valore risultante è il risultato di *expr*.</span><span class="sxs-lookup"><span data-stu-id="0548b-113">The resulting value is the result of *expr*.</span></span> <span data-ttu-id="0548b-114">Sarà uniforme se *laneIndex* è uniforme.</span><span class="sxs-lookup"><span data-stu-id="0548b-114">It will be uniform if *laneIndex* is uniform.</span></span>

## <a name="remarks"></a><span data-ttu-id="0548b-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="0548b-115">Remarks</span></span>

<span data-ttu-id="0548b-116">Questa funzione è in effetti una trasmissione del valore nella *laneIndex*'th lane.</span><span class="sxs-lookup"><span data-stu-id="0548b-116">This function is effectively a broadcast of the value in the *laneIndex*'th lane.</span></span>

<span data-ttu-id="0548b-117">Questa funzione è supportata dal modello shader 6.0 in tutte le fasi dello shader.</span><span class="sxs-lookup"><span data-stu-id="0548b-117">This function is supported from shader model 6.0 in all shader stages.</span></span>

## <a name="see-also"></a><span data-ttu-id="0548b-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0548b-118">See also</span></span>

* [<span data-ttu-id="0548b-119">Panoramica del modello shader 6</span><span class="sxs-lookup"><span data-stu-id="0548b-119">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
* [<span data-ttu-id="0548b-120">Modello shader 6</span><span class="sxs-lookup"><span data-stu-id="0548b-120">Shader Model 6</span></span>](shader-model-6-0.md)
