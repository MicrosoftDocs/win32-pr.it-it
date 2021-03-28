---
title: QuadReadAcrossX (funzione)
description: Restituisce il valore locale specificato letto dall'altra corsia in questo quad nella direzione X.
ms.assetid: 7A7E0623-30EC-4167-90A5-D79E10A394CC
keywords:
- Funzione QuadReadAcrossX HLSL
topic_type:
- apiref
api_name:
- QuadReadAcrossX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cd41b0bd84861d23153f02ba6328d17b70287866
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104118662"
---
# <a name="quadreadacrossx-function"></a><span data-ttu-id="a05c3-104">QuadReadAcrossX (funzione)</span><span class="sxs-lookup"><span data-stu-id="a05c3-104">QuadReadAcrossX function</span></span>

<span data-ttu-id="a05c3-105">Restituisce il valore locale specificato letto dall'altra corsia in questo quad nella direzione X.</span><span class="sxs-lookup"><span data-stu-id="a05c3-105">Returns the specified local value read from the other lane in this quad in the X direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="a05c3-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a05c3-106">Syntax</span></span>

``` syntax
<type> QuadReadAcrossX(
   <type> localValue
);
```

## <a name="parameters"></a><span data-ttu-id="a05c3-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="a05c3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a05c3-108">*localValue*</span><span class="sxs-lookup"><span data-stu-id="a05c3-108">*localValue*</span></span> 
</dt> <dd>

<span data-ttu-id="a05c3-109">Tipo richiesto.</span><span class="sxs-lookup"><span data-stu-id="a05c3-109">The requested type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a05c3-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a05c3-110">Return value</span></span>

<span data-ttu-id="a05c3-111">Valore locale specificato.</span><span class="sxs-lookup"><span data-stu-id="a05c3-111">The specified local value.</span></span> <span data-ttu-id="a05c3-112">Se la corsia di origine è inattiva, i risultati non sono definiti.</span><span class="sxs-lookup"><span data-stu-id="a05c3-112">If the source lane is inactive, the results are undefined.</span></span>

## <a name="remarks"></a><span data-ttu-id="a05c3-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="a05c3-113">Remarks</span></span>

<span data-ttu-id="a05c3-114">Per altre informazioni sui quad, vedere [Panoramica del modello di shader 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).</span><span class="sxs-lookup"><span data-stu-id="a05c3-114">For more information on quads, refer to [Overview of Shader Model 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).</span></span>

<span data-ttu-id="a05c3-115">Questa funzione è supportata dal modello di shader 6,0 solo in pixel e compute shader.</span><span class="sxs-lookup"><span data-stu-id="a05c3-115">This function is supported from shader model 6.0 only in pixel and compute shaders.</span></span>



 

## <a name="see-also"></a><span data-ttu-id="a05c3-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a05c3-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a05c3-117">Modello shader 6</span><span class="sxs-lookup"><span data-stu-id="a05c3-117">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




