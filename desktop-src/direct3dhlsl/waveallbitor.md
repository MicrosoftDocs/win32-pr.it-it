---
title: WaveActiveBitOr (funzione)
description: Restituisce l'OR bit per bit di tutti i valori dell'espressione in tutte le corsie attive nell'onda corrente e la replica in tutte le corsie attive.
ms.assetid: FC8E5987-DAA7-41E6-A1AB-AA0E6A82CFC7
keywords:
- Funzione WaveActiveBitOr HLSL
topic_type:
- apiref
api_name:
- WaveActiveBitOr
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6870ac8406a581e358b00ef728562dc59118a933
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104047595"
---
# <a name="waveactivebitor-function"></a><span data-ttu-id="8fc52-104">WaveActiveBitOr (funzione)</span><span class="sxs-lookup"><span data-stu-id="8fc52-104">WaveActiveBitOr function</span></span>

<span data-ttu-id="8fc52-105">Restituisce l'OR bit per bit di tutti i valori dell'espressione in tutte le corsie attive nell'onda corrente e la replica in tutte le corsie attive.</span><span class="sxs-lookup"><span data-stu-id="8fc52-105">Returns the bitwise OR of all the values of the expression across all active lanes in the current wave and replicates it back to all active lanes.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fc52-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8fc52-106">Syntax</span></span>

``` syntax
<int_type> WaveActiveBitOr(
   <int_type> expr
);
```

## <a name="parameters"></a><span data-ttu-id="8fc52-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="8fc52-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fc52-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="8fc52-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="8fc52-109">Espressione da valutare.</span><span class="sxs-lookup"><span data-stu-id="8fc52-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fc52-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8fc52-110">Return value</span></span>

<span data-ttu-id="8fc52-111">Valore or bit per bit.</span><span class="sxs-lookup"><span data-stu-id="8fc52-111">The bitwise OR value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8fc52-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="8fc52-112">Remarks</span></span>

<span data-ttu-id="8fc52-113">Questa funzione è supportata dal modello di shader 6,0 in tutte le fasi dello shader.</span><span class="sxs-lookup"><span data-stu-id="8fc52-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="8fc52-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8fc52-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fc52-115">Panoramica del modello di shader 6</span><span class="sxs-lookup"><span data-stu-id="8fc52-115">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="8fc52-116">Modello shader 6</span><span class="sxs-lookup"><span data-stu-id="8fc52-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




