---
title: WaveActiveMax (funzione)
description: Restituisce il valore massimo dell'espressione in tutte le corsie attive nell'onda corrente e la replica in tutte le corsie attive.
ms.assetid: 19101C56-2618-4F34-8725-DF92198ABDA4
keywords:
- Funzione WaveActiveMax HLSL
topic_type:
- apiref
api_name:
- WaveActiveMax
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7c0fd10f578d598c326cdfb4cf943d3a35fe78a9
ms.sourcegitcommit: a232805e6c618673f2df904111cc4f5a33e15504
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/07/2020
ms.locfileid: "104399987"
---
# <a name="waveactivemax-function"></a><span data-ttu-id="360e3-104">WaveActiveMax (funzione)</span><span class="sxs-lookup"><span data-stu-id="360e3-104">WaveActiveMax function</span></span>

<span data-ttu-id="360e3-105">Restituisce il valore massimo dell'espressione in tutte le corsie attive nell'onda corrente e la replica in tutte le corsie attive.</span><span class="sxs-lookup"><span data-stu-id="360e3-105">Returns the maximum value of the expression across all active lanes in the current wave and replicates it back to all active lanes.</span></span>

## <a name="syntax"></a><span data-ttu-id="360e3-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="360e3-106">Syntax</span></span>

``` syntax
<type> WaveActiveMax(
   <type> expr
);
```

## <a name="parameters"></a><span data-ttu-id="360e3-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="360e3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="360e3-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="360e3-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="360e3-109">Espressione da valutare.</span><span class="sxs-lookup"><span data-stu-id="360e3-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="360e3-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="360e3-110">Return value</span></span>

<span data-ttu-id="360e3-111">Valore massimo.</span><span class="sxs-lookup"><span data-stu-id="360e3-111">The maximum value.</span></span>

## <a name="remarks"></a><span data-ttu-id="360e3-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="360e3-112">Remarks</span></span>

<span data-ttu-id="360e3-113">L'ordine delle operazioni non è definito.</span><span class="sxs-lookup"><span data-stu-id="360e3-113">The order of operations is undefined.</span></span>

<span data-ttu-id="360e3-114">Questa funzione è supportata dal modello di shader 6,0 in tutte le fasi dello shader.</span><span class="sxs-lookup"><span data-stu-id="360e3-114">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="examples"></a><span data-ttu-id="360e3-115">Esempi</span><span class="sxs-lookup"><span data-stu-id="360e3-115">Examples</span></span>

``` syntax
 float3 maxPos = WaveActiveMax( myPoint.position );
    BoundingBox.max = max( maxPos, BoundingBox.max );
```

## <a name="see-also"></a><span data-ttu-id="360e3-116">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="360e3-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="360e3-117">Panoramica del modello di shader 6</span><span class="sxs-lookup"><span data-stu-id="360e3-117">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="360e3-118">Modello shader 6</span><span class="sxs-lookup"><span data-stu-id="360e3-118">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




