---
title: WaveReadLaneFirst (funzione)
description: Restituisce il valore dell'espressione per la corsia attiva dell'onda corrente con l'indice più piccolo.
ms.assetid: 89CA4FD5-4573-42ED-88D3-01C79C69FF6F
keywords:
- Funzione WaveReadLaneFirst HLSL
topic_type:
- apiref
api_name:
- WaveReadLaneFirst
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 04d10e5439b8cd653f7c0a37d3a951167561f964
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104976887"
---
# <a name="wavereadlanefirst-function"></a><span data-ttu-id="2b93e-104">WaveReadLaneFirst (funzione)</span><span class="sxs-lookup"><span data-stu-id="2b93e-104">WaveReadLaneFirst function</span></span>

<span data-ttu-id="2b93e-105">Restituisce il valore dell'espressione per la corsia attiva dell'onda corrente con l'indice più piccolo.</span><span class="sxs-lookup"><span data-stu-id="2b93e-105">Returns the value of the expression for the active lane of the current wave with the smallest index.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b93e-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2b93e-106">Syntax</span></span>

``` syntax
<type> WaveReadLaneFirst(
   <type> expr
);
```

## <a name="parameters"></a><span data-ttu-id="2b93e-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="2b93e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b93e-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="2b93e-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="2b93e-109">Espressione da valutare.</span><span class="sxs-lookup"><span data-stu-id="2b93e-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b93e-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2b93e-110">Return value</span></span>

<span data-ttu-id="2b93e-111">Il valore risultante è uniforme nell'onda.</span><span class="sxs-lookup"><span data-stu-id="2b93e-111">The resulting value is uniform across the wave.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b93e-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="2b93e-112">Remarks</span></span>

<span data-ttu-id="2b93e-113">Questa funzione è supportata dal modello di shader 6,0 in tutte le fasi dello shader.</span><span class="sxs-lookup"><span data-stu-id="2b93e-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="2b93e-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2b93e-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b93e-115">Panoramica del modello di shader 6</span><span class="sxs-lookup"><span data-stu-id="2b93e-115">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="2b93e-116">Modello shader 6</span><span class="sxs-lookup"><span data-stu-id="2b93e-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




