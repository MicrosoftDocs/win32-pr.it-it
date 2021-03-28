---
title: WaveGetLaneIndex (funzione)
description: Restituisce l'indice della corsia corrente all'interno dell'onda corrente.
ms.assetid: C05BD814-23DF-432F-8669-C03842B77AC7
keywords:
- Funzione WaveGetLaneIndex HLSL
topic_type:
- apiref
api_name:
- WaveGetLaneIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8adea1091739981523ab19b69158ead9aafa600c
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104993616"
---
# <a name="wavegetlaneindex-function"></a><span data-ttu-id="ba650-104">WaveGetLaneIndex (funzione)</span><span class="sxs-lookup"><span data-stu-id="ba650-104">WaveGetLaneIndex function</span></span>

<span data-ttu-id="ba650-105">Restituisce l'indice della corsia corrente all'interno dell'onda corrente.</span><span class="sxs-lookup"><span data-stu-id="ba650-105">Returns the index of the current lane within the current wave.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba650-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ba650-106">Syntax</span></span>

``` syntax
uint WaveGetLaneIndex(void);
```

## <a name="parameters"></a><span data-ttu-id="ba650-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="ba650-107">Parameters</span></span>

<span data-ttu-id="ba650-108">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="ba650-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ba650-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ba650-109">Return value</span></span>

<span data-ttu-id="ba650-110">Indice della corsia corrente.</span><span class="sxs-lookup"><span data-stu-id="ba650-110">The current lane index.</span></span> <span data-ttu-id="ba650-111">Il risultato sarà compreso tra 0 e il risultato restituito da [**WaveGetLaneCount**](wavegetlanecount.md).</span><span class="sxs-lookup"><span data-stu-id="ba650-111">The result will be between 0 and the result returned from [**WaveGetLaneCount**](wavegetlanecount.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ba650-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="ba650-112">Remarks</span></span>

<span data-ttu-id="ba650-113">Questa funzione è supportata dal modello di shader 6,0 in tutte le fasi dello shader.</span><span class="sxs-lookup"><span data-stu-id="ba650-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="ba650-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ba650-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba650-115">Panoramica del modello di shader 6</span><span class="sxs-lookup"><span data-stu-id="ba650-115">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="ba650-116">Modello shader 6</span><span class="sxs-lookup"><span data-stu-id="ba650-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




