---
title: WaveActiveBitAnd (funzione)
description: Restituisce l'operatore AND bit per bit di tutti i valori dell'espressione in tutte le corsie attive nell'onda corrente e lo replica in tutte le corsie attive.
ms.assetid: 602884CD-E656-4DEB-A30A-8A7D127A2217
keywords:
- Funzione WaveActiveBitAnd HLSL
topic_type:
- apiref
api_name:
- WaveActiveBitAnd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2b6a3b0b097ea8737e07a91fcfc6553f22b828f1
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104047601"
---
# <a name="waveactivebitand-function"></a><span data-ttu-id="30bbf-104">WaveActiveBitAnd (funzione)</span><span class="sxs-lookup"><span data-stu-id="30bbf-104">WaveActiveBitAnd function</span></span>

<span data-ttu-id="30bbf-105">Restituisce l'operatore AND bit per bit di tutti i valori dell'espressione in tutte le corsie attive nell'onda corrente e lo replica in tutte le corsie attive.</span><span class="sxs-lookup"><span data-stu-id="30bbf-105">Returns the bitwise AND of all the values of the expression across all active lanes in the current wave and replicates it back to all active lanes.</span></span>

## <a name="syntax"></a><span data-ttu-id="30bbf-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="30bbf-106">Syntax</span></span>


``` syntax
<int_type> WaveActiveBitAnd(
   <int_type> expr
);
```



## <a name="parameters"></a><span data-ttu-id="30bbf-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="30bbf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30bbf-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="30bbf-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="30bbf-109">Espressione da valutare.</span><span class="sxs-lookup"><span data-stu-id="30bbf-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30bbf-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="30bbf-110">Return value</span></span>

<span data-ttu-id="30bbf-111">Il valore AND bit per bit.</span><span class="sxs-lookup"><span data-stu-id="30bbf-111">The bitwise AND value.</span></span>

## <a name="remarks"></a><span data-ttu-id="30bbf-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="30bbf-112">Remarks</span></span>

<span data-ttu-id="30bbf-113">Questa funzione è supportata dal modello di shader 6,0 in tutte le fasi dello shader.</span><span class="sxs-lookup"><span data-stu-id="30bbf-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="30bbf-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="30bbf-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30bbf-115">Panoramica del modello di shader 6</span><span class="sxs-lookup"><span data-stu-id="30bbf-115">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="30bbf-116">Modello shader 6</span><span class="sxs-lookup"><span data-stu-id="30bbf-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




