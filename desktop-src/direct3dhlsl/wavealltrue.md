---
title: WaveActiveAllTrue (funzione)
description: Restituisce true se l'espressione è true in tutte le corsie attive nell'onda corrente.
ms.assetid: C4EC5A02-6070-4FF4-B855-F597FFFE66F0
keywords:
- Funzione WaveActiveAllTrue HLSL
topic_type:
- apiref
api_name:
- WaveActiveAllTrue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a26e0ce757257d6fdd8296239dcf086bff5f1666
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104474639"
---
# <a name="waveactivealltrue-function"></a><span data-ttu-id="49027-104">WaveActiveAllTrue (funzione)</span><span class="sxs-lookup"><span data-stu-id="49027-104">WaveActiveAllTrue function</span></span>

<span data-ttu-id="49027-105">Restituisce true se l'espressione è true in tutte le corsie attive nell'onda corrente.</span><span class="sxs-lookup"><span data-stu-id="49027-105">Returns true if the expression is true in all active lanes in the current wave.</span></span>

## <a name="syntax"></a><span data-ttu-id="49027-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="49027-106">Syntax</span></span>

``` syntax
bool WaveActiveAllTrue(
   bool expr
);
```

## <a name="parameters"></a><span data-ttu-id="49027-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="49027-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49027-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="49027-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="49027-109">Espressione booleana da valutare.</span><span class="sxs-lookup"><span data-stu-id="49027-109">The boolean expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49027-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="49027-110">Return value</span></span>

<span data-ttu-id="49027-111">True se l'espressione è true in tutte le corsie.</span><span class="sxs-lookup"><span data-stu-id="49027-111">True if the expression is true in all lanes.</span></span>

## <a name="remarks"></a><span data-ttu-id="49027-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="49027-112">Remarks</span></span>

<span data-ttu-id="49027-113">Questa funzione è supportata dal modello di shader 6,0 in tutte le fasi dello shader.</span><span class="sxs-lookup"><span data-stu-id="49027-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="49027-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="49027-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49027-115">Panoramica del modello di shader 6</span><span class="sxs-lookup"><span data-stu-id="49027-115">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="49027-116">Modello shader 6</span><span class="sxs-lookup"><span data-stu-id="49027-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




