---
title: WaveActiveBitXor (funzione)
description: Restituisce l'oggetto XOR bit per bit di tutti i valori dell'espressione in tutte le corsie attive nell'onda corrente e lo replica in tutte le corsie attive.
ms.assetid: A6807D17-1E6E-4997-AB52-32FAB5857219
keywords:
- Funzione WaveActiveBitXor HLSL
topic_type:
- apiref
api_name:
- WaveActiveBitXor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7e55ce8a43311f4f4c428e97bff1e107ab5c7038
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104047593"
---
# <a name="waveactivebitxor-function"></a><span data-ttu-id="028c0-104">WaveActiveBitXor (funzione)</span><span class="sxs-lookup"><span data-stu-id="028c0-104">WaveActiveBitXor function</span></span>

<span data-ttu-id="028c0-105">Restituisce l'oggetto XOR bit per bit di tutti i valori dell'espressione in tutte le corsie attive nell'onda corrente e lo replica in tutte le corsie attive.</span><span class="sxs-lookup"><span data-stu-id="028c0-105">Returns the bitwise XOR of all the values of the expression across all active lanes in the current wave and replicates it back to all active lanes.</span></span>

## <a name="syntax"></a><span data-ttu-id="028c0-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="028c0-106">Syntax</span></span>

``` syntax
<int_type> WaveActiveBitXor(
   <int_type> expr
);
```

## <a name="parameters"></a><span data-ttu-id="028c0-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="028c0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="028c0-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="028c0-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="028c0-109">Espressione da valutare.</span><span class="sxs-lookup"><span data-stu-id="028c0-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="028c0-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="028c0-110">Return value</span></span>

<span data-ttu-id="028c0-111">Valore XOR bit per bit.</span><span class="sxs-lookup"><span data-stu-id="028c0-111">The bitwise XOR value.</span></span>

## <a name="remarks"></a><span data-ttu-id="028c0-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="028c0-112">Remarks</span></span>

<span data-ttu-id="028c0-113">Questa funzione è supportata dal modello di shader 6,0 in tutte le fasi dello shader.</span><span class="sxs-lookup"><span data-stu-id="028c0-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="028c0-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="028c0-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="028c0-115">Panoramica del modello di shader 6</span><span class="sxs-lookup"><span data-stu-id="028c0-115">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="028c0-116">Modello shader 6</span><span class="sxs-lookup"><span data-stu-id="028c0-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




