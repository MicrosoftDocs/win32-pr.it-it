---
title: WaveActiveMin (funzione)
description: Restituisce il valore minimo dell'espressione in tutte le corsie attive nell'onda corrente che viene replicato nuovamente in tutte le corsie attive.
ms.assetid: BA762C02-894C-4AF9-A226-C1E3AAC286FF
keywords:
- Funzione WaveActiveMin HLSL
topic_type:
- apiref
api_name:
- WaveActiveMin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 91555df354ab2b7ffc447a9422c4811ae23e6e0c
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104047594"
---
# <a name="waveactivemin-function"></a><span data-ttu-id="d6aca-104">WaveActiveMin (funzione)</span><span class="sxs-lookup"><span data-stu-id="d6aca-104">WaveActiveMin function</span></span>

<span data-ttu-id="d6aca-105">Restituisce il valore minimo dell'espressione in tutte le corsie attive nell'onda corrente che viene replicato nuovamente in tutte le corsie attive.</span><span class="sxs-lookup"><span data-stu-id="d6aca-105">Returns the minimum value of the expression across all active lanes in the current wave replicates it back to all active lanes.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6aca-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d6aca-106">Syntax</span></span>

``` syntax
<type> WaveActiveMin(
   <type> expr
);
```

## <a name="parameters"></a><span data-ttu-id="d6aca-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="d6aca-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6aca-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="d6aca-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="d6aca-109">Espressione da valutare.</span><span class="sxs-lookup"><span data-stu-id="d6aca-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6aca-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d6aca-110">Return value</span></span>

<span data-ttu-id="d6aca-111">Valore minimo.</span><span class="sxs-lookup"><span data-stu-id="d6aca-111">The minimum value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6aca-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="d6aca-112">Remarks</span></span>

<span data-ttu-id="d6aca-113">L'ordine delle operazioni non è definito.</span><span class="sxs-lookup"><span data-stu-id="d6aca-113">The order of operations is undefined.</span></span>

<span data-ttu-id="d6aca-114">Questa funzione è supportata dal modello di shader 6,0 in tutte le fasi dello shader.</span><span class="sxs-lookup"><span data-stu-id="d6aca-114">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="examples"></a><span data-ttu-id="d6aca-115">Esempi</span><span class="sxs-lookup"><span data-stu-id="d6aca-115">Examples</span></span>

``` syntax
 float3 minPos = WaveActiveMin( myPoint.position );
    BoundingBox.min = min( minPos, BoundingBox.min );
```

## <a name="see-also"></a><span data-ttu-id="d6aca-116">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="d6aca-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6aca-117">Panoramica del modello di shader 6</span><span class="sxs-lookup"><span data-stu-id="d6aca-117">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="d6aca-118">Modello shader 6</span><span class="sxs-lookup"><span data-stu-id="d6aca-118">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




