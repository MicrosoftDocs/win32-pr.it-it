---
title: WaveGetLaneCount (funzione)
description: Restituisce il numero di corsie in un'onda in questa architettura.
ms.assetid: 04059B5E-0F62-4623-84AD-E41FF7166B34
keywords:
- Funzione WaveGetLaneCount HLSL
topic_type:
- apiref
api_name:
- WaveGetLaneCount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0bfdb3ce2dfde84b070fee57e7fc587a71d5f948
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104399935"
---
# <a name="wavegetlanecount-function"></a><span data-ttu-id="cabcb-104">WaveGetLaneCount (funzione)</span><span class="sxs-lookup"><span data-stu-id="cabcb-104">WaveGetLaneCount function</span></span>

<span data-ttu-id="cabcb-105">Restituisce il numero di corsie in un'onda in questa architettura.</span><span class="sxs-lookup"><span data-stu-id="cabcb-105">Returns the number of lanes in a wave on this architecture.</span></span>

## <a name="syntax"></a><span data-ttu-id="cabcb-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cabcb-106">Syntax</span></span>

``` syntax
uint WaveGetLaneCount(void);
```

## <a name="parameters"></a><span data-ttu-id="cabcb-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="cabcb-107">Parameters</span></span>

<span data-ttu-id="cabcb-108">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="cabcb-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cabcb-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cabcb-109">Return value</span></span>

<span data-ttu-id="cabcb-110">Il risultato sarà compreso tra 4 e 128 e includerà tutte le onde, ovvero attive, inattive e/o corsie helper.</span><span class="sxs-lookup"><span data-stu-id="cabcb-110">The result will be between 4 and 128, and includes all waves: active, inactive, and/or helper lanes.</span></span> <span data-ttu-id="cabcb-111">Il risultato restituito da questa funzione può variare in modo significativo a seconda dell'implementazione del driver.</span><span class="sxs-lookup"><span data-stu-id="cabcb-111">The result returned from this function may vary significantly depending on the driver implementation.</span></span>

## <a name="remarks"></a><span data-ttu-id="cabcb-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="cabcb-112">Remarks</span></span>

<span data-ttu-id="cabcb-113">Questa funzione è supportata dal modello di shader 6,0 in tutte le fasi dello shader.</span><span class="sxs-lookup"><span data-stu-id="cabcb-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="examples"></a><span data-ttu-id="cabcb-114">Esempi</span><span class="sxs-lookup"><span data-stu-id="cabcb-114">Examples</span></span>

``` syntax
 uint laneCount = WaveGetLaneCount();    // number of lanes in wave
```

## <a name="see-also"></a><span data-ttu-id="cabcb-115">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="cabcb-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cabcb-116">Panoramica del modello di shader 6</span><span class="sxs-lookup"><span data-stu-id="cabcb-116">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="cabcb-117">Modello shader 6</span><span class="sxs-lookup"><span data-stu-id="cabcb-117">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




