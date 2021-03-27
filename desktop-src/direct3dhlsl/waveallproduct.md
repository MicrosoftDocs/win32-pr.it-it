---
title: WaveActiveProduct (funzione)
description: Moltiplica i valori dell'espressione tra tutte le corsie attive nell'onda corrente e la replica in tutte le corsie attive.
ms.assetid: B259244D-C993-4F4A-AF09-F077D99AD025
keywords:
- Funzione WaveActiveProduct HLSL
topic_type:
- apiref
api_name:
- WaveActiveProduct
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b8e1d400541a2654657c1a462c38494d20af13e6
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "103873113"
---
# <a name="waveactiveproduct-function"></a><span data-ttu-id="c6311-104">WaveActiveProduct (funzione)</span><span class="sxs-lookup"><span data-stu-id="c6311-104">WaveActiveProduct function</span></span>

<span data-ttu-id="c6311-105">Moltiplica i valori dell'espressione tra tutte le corsie attive nell'onda corrente e la replica in tutte le corsie attive.</span><span class="sxs-lookup"><span data-stu-id="c6311-105">Multiplies the values of the expression together across all active lanes in the current wave and replicates it back to all active lanes.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6311-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c6311-106">Syntax</span></span>

``` syntax
<type> WaveActiveProduct(
   <type> expr
);
```

## <a name="parameters"></a><span data-ttu-id="c6311-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="c6311-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6311-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="c6311-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="c6311-109">Espressione da valutare.</span><span class="sxs-lookup"><span data-stu-id="c6311-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6311-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c6311-110">Return value</span></span>

<span data-ttu-id="c6311-111">Valore del prodotto.</span><span class="sxs-lookup"><span data-stu-id="c6311-111">The product value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6311-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="c6311-112">Remarks</span></span>

<span data-ttu-id="c6311-113">L'ordine delle operazioni non è definito.</span><span class="sxs-lookup"><span data-stu-id="c6311-113">The order of operations is undefined.</span></span>

<span data-ttu-id="c6311-114">Questa funzione è supportata dal modello di shader 6,0 in tutte le fasi dello shader.</span><span class="sxs-lookup"><span data-stu-id="c6311-114">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="c6311-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c6311-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6311-116">Panoramica del modello di shader 6</span><span class="sxs-lookup"><span data-stu-id="c6311-116">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="c6311-117">Modello shader 6</span><span class="sxs-lookup"><span data-stu-id="c6311-117">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




