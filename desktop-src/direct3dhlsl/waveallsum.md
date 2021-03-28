---
title: WaveActiveSum (funzione)
description: Somma il valore dell'espressione in tutte le corsie attive nell'onda corrente e la replica in tutte le corsie nell'onda corrente.
ms.assetid: 94CEF4AA-D6DE-4B00-9743-F491F255FE3D
keywords:
- Funzione WaveActiveSum HLSL
topic_type:
- apiref
api_name:
- WaveActiveSum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b98ecf2521841b9da73e1b917d44f1d91b7876d2
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "103963562"
---
# <a name="waveactivesum-function"></a><span data-ttu-id="5d6da-104">WaveActiveSum (funzione)</span><span class="sxs-lookup"><span data-stu-id="5d6da-104">WaveActiveSum function</span></span>

<span data-ttu-id="5d6da-105">Somma il valore dell'espressione in tutte le corsie attive nell'onda corrente e la replica in tutte le corsie nell'onda corrente.</span><span class="sxs-lookup"><span data-stu-id="5d6da-105">Sums up the value of the expression across all active lanes in the current wave and replicates it to all lanes in the current wave.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d6da-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5d6da-106">Syntax</span></span>

``` syntax
<type> WaveActiveSum(
   <type> expr
);
```

## <a name="parameters"></a><span data-ttu-id="5d6da-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="5d6da-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d6da-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="5d6da-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="5d6da-109">Espressione da valutare.</span><span class="sxs-lookup"><span data-stu-id="5d6da-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d6da-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5d6da-110">Return value</span></span>

<span data-ttu-id="5d6da-111">Valore sum.</span><span class="sxs-lookup"><span data-stu-id="5d6da-111">The sum value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d6da-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="5d6da-112">Remarks</span></span>

<span data-ttu-id="5d6da-113">L'ordine delle operazioni non è definito.</span><span class="sxs-lookup"><span data-stu-id="5d6da-113">The order of operations is undefined.</span></span>

<span data-ttu-id="5d6da-114">Questa funzione è supportata dal modello di shader 6,0 in tutte le fasi dello shader.</span><span class="sxs-lookup"><span data-stu-id="5d6da-114">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="examples"></a><span data-ttu-id="5d6da-115">Esempi</span><span class="sxs-lookup"><span data-stu-id="5d6da-115">Examples</span></span>

``` syntax
float3 total = WaveActiveSum( position ); // sum positions in wave
float3 center = total/count;           // compute average of these positions
```

## <a name="see-also"></a><span data-ttu-id="5d6da-116">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="5d6da-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d6da-117">Panoramica del modello di shader 6</span><span class="sxs-lookup"><span data-stu-id="5d6da-117">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="5d6da-118">Modello shader 6</span><span class="sxs-lookup"><span data-stu-id="5d6da-118">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




