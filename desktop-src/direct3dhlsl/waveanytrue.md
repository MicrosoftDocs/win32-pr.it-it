---
title: WaveActiveAnyTrue (funzione)
description: Restituisce true se l'espressione è true in una delle corsie attive nell'onda corrente.
ms.assetid: 203E2E1D-0AA2-4E4A-80F7-D1FE7579A742
keywords:
- Funzione WaveActiveAnyTrue HLSL
topic_type:
- apiref
api_name:
- WaveActiveAnyTrue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 16801c4329f5bc0bf325d8bb67e8c0bb94887678
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104993613"
---
# <a name="waveactiveanytrue-function"></a><span data-ttu-id="0d7bd-104">WaveActiveAnyTrue (funzione)</span><span class="sxs-lookup"><span data-stu-id="0d7bd-104">WaveActiveAnyTrue function</span></span>

<span data-ttu-id="0d7bd-105">Restituisce true se l'espressione è true in una delle corsie attive nell'onda corrente.</span><span class="sxs-lookup"><span data-stu-id="0d7bd-105">Returns true if the expression is true in any of the active lanes in the current wave.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d7bd-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0d7bd-106">Syntax</span></span>

``` syntax
bool WaveActiveAnyTrue(
   bool expr
);
```

## <a name="parameters"></a><span data-ttu-id="0d7bd-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="0d7bd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d7bd-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="0d7bd-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="0d7bd-109">Espressione booleana da valutare.</span><span class="sxs-lookup"><span data-stu-id="0d7bd-109">The boolean expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d7bd-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0d7bd-110">Return value</span></span>

<span data-ttu-id="0d7bd-111">True se l'espressione è true in una corsia.</span><span class="sxs-lookup"><span data-stu-id="0d7bd-111">True if the expression is true in any lane.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d7bd-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="0d7bd-112">Remarks</span></span>

<span data-ttu-id="0d7bd-113">Questa funzione è supportata dal modello di shader 6,0 in tutte le fasi dello shader.</span><span class="sxs-lookup"><span data-stu-id="0d7bd-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="0d7bd-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0d7bd-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d7bd-115">Panoramica del modello di shader 6</span><span class="sxs-lookup"><span data-stu-id="0d7bd-115">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="0d7bd-116">Modello shader 6</span><span class="sxs-lookup"><span data-stu-id="0d7bd-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




