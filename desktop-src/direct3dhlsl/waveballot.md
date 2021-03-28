---
title: WaveActiveBallot (funzione)
description: Restituisce un uint4 contenente una maschera di maschera della valutazione dell'espressione booleana per tutte le corsie attive nell'onda corrente.
ms.assetid: 67FE28E0-F397-431A-8CF8-64E4AD88CDBC
keywords:
- Funzione WaveActiveBallot HLSL
topic_type:
- apiref
api_name:
- WaveActiveBallot
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e3cdd89fad7da1e4ba7f3d5e032370834166a114
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104517211"
---
# <a name="waveactiveballot-function"></a><span data-ttu-id="e7ae7-104">WaveActiveBallot (funzione)</span><span class="sxs-lookup"><span data-stu-id="e7ae7-104">WaveActiveBallot function</span></span>

<span data-ttu-id="e7ae7-105">Restituisce un uint4 contenente una maschera di maschera della valutazione dell'espressione booleana per tutte le corsie attive nell'onda corrente.</span><span class="sxs-lookup"><span data-stu-id="e7ae7-105">Returns a uint4 containing a bitmask of the evaluation of the Boolean expression for all active lanes in the current wave.</span></span> 

## <a name="syntax"></a><span data-ttu-id="e7ae7-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e7ae7-106">Syntax</span></span>

``` syntax
uint4 WaveBallot(
   bool expr
);
```

## <a name="parameters"></a><span data-ttu-id="e7ae7-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="e7ae7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7ae7-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="e7ae7-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="e7ae7-109">Espressione booleana da valutare.</span><span class="sxs-lookup"><span data-stu-id="e7ae7-109">The boolean expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7ae7-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e7ae7-110">Return value</span></span>

<span data-ttu-id="e7ae7-111">Uint4 contenente una maschera di maschera della valutazione dell'espressione booleana per tutte le corsie attive nell'onda corrente.</span><span class="sxs-lookup"><span data-stu-id="e7ae7-111">A uint4 containing a bitmask of the evaluation of the Boolean expression for all active lanes in the current wave.</span></span> <span data-ttu-id="e7ae7-112">Il bit meno significativo corrisponde alla corsia con indice zero.</span><span class="sxs-lookup"><span data-stu-id="e7ae7-112">The least-significant bit corresponds to the lane with index zero.</span></span> <span data-ttu-id="e7ae7-113">I bit corrispondenti alle linee inattive saranno pari a zero.</span><span class="sxs-lookup"><span data-stu-id="e7ae7-113">The bits corresponding to inactive lanes will be zero.</span></span> <span data-ttu-id="e7ae7-114">I bit maggiori o uguali a [**WaveGetLaneCount**](wavegetlanecount.md) saranno pari a zero.</span><span class="sxs-lookup"><span data-stu-id="e7ae7-114">The bits that are greater than or equal to [**WaveGetLaneCount**](wavegetlanecount.md) will be zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7ae7-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="e7ae7-115">Remarks</span></span>

<span data-ttu-id="e7ae7-116">Diverse GPU hanno larghezze del processore SIMD diverse (conteggi della corsia).</span><span class="sxs-lookup"><span data-stu-id="e7ae7-116">Different GPUs have different SIMD processor widths (lane counts).</span></span> <span data-ttu-id="e7ae7-117">La maggior parte di queste funzioni **WaveXXX** è in grado di funzionare al livello dell'astrazione in cui la larghezza del computer SIMD è nascosta.</span><span class="sxs-lookup"><span data-stu-id="e7ae7-117">Most of these **WaveXXX** functions are able to operate at level of abstraction where SIMD machine width is concealed.</span></span> <span data-ttu-id="e7ae7-118">Per ottimizzare la portabilità del codice tra le GPU, usare le funzioni intrinseche che non si basano sulla larghezza del computer.</span><span class="sxs-lookup"><span data-stu-id="e7ae7-118">To maximize portability of code across GPUs, use the intrinsics that don’t rely on machine width.</span></span> <span data-ttu-id="e7ae7-119">Ad esempio, usare:</span><span class="sxs-lookup"><span data-stu-id="e7ae7-119">For example, use:</span></span>

``` syntax
uint result = WaveActiveCountBits( bBit );
```

<span data-ttu-id="e7ae7-120">Anziché:</span><span class="sxs-lookup"><span data-stu-id="e7ae7-120">Instead of:</span></span>

``` syntax
uint result = countbits( WaveActiveBallot( bBit ) );
```

<span data-ttu-id="e7ae7-121">Questa funzione è supportata dal modello di shader 6,0 in tutte le fasi dello shader.</span><span class="sxs-lookup"><span data-stu-id="e7ae7-121">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="examples"></a><span data-ttu-id="e7ae7-122">Esempi</span><span class="sxs-lookup"><span data-stu-id="e7ae7-122">Examples</span></span>

``` syntax
// get a bitwise representation of the number of currently active lanes:
uint4 waveBits = WaveActiveBallot( true ); // convert to bits 
```

## <a name="see-also"></a><span data-ttu-id="e7ae7-123">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="e7ae7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7ae7-124">Panoramica del modello di shader 6</span><span class="sxs-lookup"><span data-stu-id="e7ae7-124">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="e7ae7-125">Modello shader 6</span><span class="sxs-lookup"><span data-stu-id="e7ae7-125">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




