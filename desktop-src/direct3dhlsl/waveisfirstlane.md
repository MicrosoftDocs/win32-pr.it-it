---
title: WaveIsFirstLane (funzione)
description: Restituisce true solo per la corsia attiva nell'onda corrente con l'indice più piccolo.
ms.assetid: 5D90F713-08C7-4BD4-867B-2E7CA3A85E87
keywords:
- Funzione WaveIsFirstLane HLSL
topic_type:
- apiref
api_name:
- WaveIsFirstLane
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 49e875463d8281ff7e7699694c02d087df1a372f
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104339659"
---
# <a name="waveisfirstlane-function"></a><span data-ttu-id="ecba6-104">WaveIsFirstLane (funzione)</span><span class="sxs-lookup"><span data-stu-id="ecba6-104">WaveIsFirstLane function</span></span>

<span data-ttu-id="ecba6-105">Restituisce true solo per la corsia attiva nell'onda corrente con l'indice più piccolo.</span><span class="sxs-lookup"><span data-stu-id="ecba6-105">Returns true only for the active lane in the current wave with the smallest index.</span></span>

## <a name="syntax"></a><span data-ttu-id="ecba6-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ecba6-106">Syntax</span></span>


``` syntax
bool WaveIsFirstLane(void);
```



## <a name="parameters"></a><span data-ttu-id="ecba6-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="ecba6-107">Parameters</span></span>

<span data-ttu-id="ecba6-108">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="ecba6-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ecba6-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ecba6-109">Return value</span></span>

<span data-ttu-id="ecba6-110">True solo per la corsia attiva nell'onda corrente con l'indice più piccolo.</span><span class="sxs-lookup"><span data-stu-id="ecba6-110">True only for the active lane in the current wave with the smallest index.</span></span>

## <a name="remarks"></a><span data-ttu-id="ecba6-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="ecba6-111">Remarks</span></span>

<span data-ttu-id="ecba6-112">Questa funzione può essere usata per identificare le operazioni che devono essere eseguite una sola volta per ogni Wave.</span><span class="sxs-lookup"><span data-stu-id="ecba6-112">This function can be used to identify operations that are to be executed only once per wave.</span></span>

<span data-ttu-id="ecba6-113">Questa funzione è supportata dal modello di shader 6,0 in tutte le fasi dello shader.</span><span class="sxs-lookup"><span data-stu-id="ecba6-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="examples"></a><span data-ttu-id="ecba6-114">Esempi</span><span class="sxs-lookup"><span data-stu-id="ecba6-114">Examples</span></span>

``` syntax
 if ( WaveIsFirstLane() )
{
    . . . // once per-wave code
}
```

## <a name="see-also"></a><span data-ttu-id="ecba6-115">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="ecba6-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecba6-116">Panoramica del modello di shader 6</span><span class="sxs-lookup"><span data-stu-id="ecba6-116">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="ecba6-117">Modello shader 6</span><span class="sxs-lookup"><span data-stu-id="ecba6-117">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




