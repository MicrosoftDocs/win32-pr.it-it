---
title: WaveActiveAllEqual (funzione)
description: Restituisce true se l'espressione è la stessa per ogni corsia attiva nell'onda corrente (e di conseguenza uniforme).
ms.assetid: E0A051A8-0ADD-4EC7-8D9A-8820CED9DA9D
keywords:
- Funzione WaveActiveAllEqual HLSL
topic_type:
- apiref
api_name:
- WaveActiveAllEqual
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 34745e428fcd4453ce7274fc2a5accc6185f5b10
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "103734799"
---
# <a name="waveactiveallequal-function"></a><span data-ttu-id="596eb-104">WaveActiveAllEqual (funzione)</span><span class="sxs-lookup"><span data-stu-id="596eb-104">WaveActiveAllEqual function</span></span>

<span data-ttu-id="596eb-105">Restituisce true se l'espressione è la stessa per ogni corsia attiva nell'onda corrente (e di conseguenza uniforme).</span><span class="sxs-lookup"><span data-stu-id="596eb-105">Returns true if the expression is the same for every active lane in the current wave (and thus uniform across it).</span></span>

## <a name="syntax"></a><span data-ttu-id="596eb-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="596eb-106">Syntax</span></span>


``` syntax
bool WaveActiveAllEqual(
   <type> expr
);
```



## <a name="parameters"></a><span data-ttu-id="596eb-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="596eb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="596eb-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="596eb-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="596eb-109">Espressione da valutare.</span><span class="sxs-lookup"><span data-stu-id="596eb-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="596eb-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="596eb-110">Return value</span></span>

<span data-ttu-id="596eb-111">True se l'espressione è la stessa per ogni corsia attiva nell'onda corrente.</span><span class="sxs-lookup"><span data-stu-id="596eb-111">True if the expression is the same for every active lane in the current wave.</span></span>

## <a name="remarks"></a><span data-ttu-id="596eb-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="596eb-112">Remarks</span></span>

<span data-ttu-id="596eb-113">Questa funzione è supportata dal modello di shader 6,0 in tutte le fasi dello shader.</span><span class="sxs-lookup"><span data-stu-id="596eb-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="596eb-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="596eb-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="596eb-115">Panoramica del modello di shader 6</span><span class="sxs-lookup"><span data-stu-id="596eb-115">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="596eb-116">Modello shader 6</span><span class="sxs-lookup"><span data-stu-id="596eb-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




