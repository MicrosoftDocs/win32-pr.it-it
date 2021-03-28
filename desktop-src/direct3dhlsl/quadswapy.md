---
title: QuadReadAcrossY (funzione)
description: Restituisce il valore di origine specificato letto dall'altra corsia in questo quad nella direzione Y.
ms.assetid: 6C03D1E6-433F-4CCA-A5EA-C3F34BB2B93B
keywords:
- Funzione QuadReadAcrossY HLSL
topic_type:
- apiref
api_name:
- QuadReadAcrossY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 72b5ede0df733e60ba4b1bcc01a04f1daaedc708
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104976879"
---
# <a name="quadreadacrossy-function"></a><span data-ttu-id="7904f-104">QuadReadAcrossY (funzione)</span><span class="sxs-lookup"><span data-stu-id="7904f-104">QuadReadAcrossY function</span></span>

<span data-ttu-id="7904f-105">Restituisce il valore di origine specificato letto dall'altra corsia in questo quad nella direzione Y.</span><span class="sxs-lookup"><span data-stu-id="7904f-105">Returns the specified source value read from the other lane in this quad in the Y direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="7904f-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7904f-106">Syntax</span></span>

``` syntax
<type> QuadReadAcrossY(
   <type> localValue
);
```

## <a name="parameters"></a><span data-ttu-id="7904f-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="7904f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7904f-108">*localValue*</span><span class="sxs-lookup"><span data-stu-id="7904f-108">*localValue*</span></span> 
</dt> <dd>

<span data-ttu-id="7904f-109">Tipo richiesto.</span><span class="sxs-lookup"><span data-stu-id="7904f-109">The requested type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7904f-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7904f-110">Return value</span></span>

<span data-ttu-id="7904f-111">Valore di origine specificato.</span><span class="sxs-lookup"><span data-stu-id="7904f-111">The specified source value.</span></span> <span data-ttu-id="7904f-112">Se la corsia di origine è inattiva, i risultati non sono definiti.</span><span class="sxs-lookup"><span data-stu-id="7904f-112">If the source lane is inactive, the results are undefined.</span></span>

## <a name="remarks"></a><span data-ttu-id="7904f-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="7904f-113">Remarks</span></span>

<span data-ttu-id="7904f-114">Per altre informazioni sui quad, vedere [Panoramica del modello di shader 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).</span><span class="sxs-lookup"><span data-stu-id="7904f-114">For more information on quads, refer to [Overview of Shader Model 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).</span></span>

<span data-ttu-id="7904f-115">Questa funzione è supportata dal modello di shader 6,0 solo in pixel e compute shader.</span><span class="sxs-lookup"><span data-stu-id="7904f-115">This function is supported from shader model 6.0 only in pixel and compute shaders.</span></span>



 

## <a name="see-also"></a><span data-ttu-id="7904f-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7904f-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7904f-117">Modello shader 6</span><span class="sxs-lookup"><span data-stu-id="7904f-117">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




