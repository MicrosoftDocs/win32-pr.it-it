---
title: QuadReadLaneAt (funzione)
description: Restituisce il valore di origine specificato dalla corsia identificata dall'ID della corsia all'interno del Quad corrente.
ms.assetid: 5CD7EE4C-E64E-46A3-ABDC-1BF65D0F96BE
keywords:
- Funzione QuadReadLaneAt HLSL
topic_type:
- apiref
api_name:
- QuadReadLaneAt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ddc772c2dca66873891483431eab14ad504da77e
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104474645"
---
# <a name="quadreadlaneat-function"></a><span data-ttu-id="28f4f-104">QuadReadLaneAt (funzione)</span><span class="sxs-lookup"><span data-stu-id="28f4f-104">QuadReadLaneAt function</span></span>

<span data-ttu-id="28f4f-105">Restituisce il valore di origine specificato dalla corsia identificata dall'ID della corsia all'interno del Quad corrente.</span><span class="sxs-lookup"><span data-stu-id="28f4f-105">Returns the specified source value from the lane identified by the lane ID within the current quad.</span></span>

## <a name="syntax"></a><span data-ttu-id="28f4f-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="28f4f-106">Syntax</span></span>


``` syntax
<type> QuadReadLaneAt(
   <type> sourceValue,
   uint   quadLaneID  
);
```



## <a name="parameters"></a><span data-ttu-id="28f4f-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="28f4f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28f4f-108">*Valore*</span><span class="sxs-lookup"><span data-stu-id="28f4f-108">*sourceValue*</span></span> 
</dt> <dd>

<span data-ttu-id="28f4f-109">Tipo richiesto.</span><span class="sxs-lookup"><span data-stu-id="28f4f-109">The requested type.</span></span>

</dd> <dt>

<span data-ttu-id="28f4f-110">*quadLaneID*</span><span class="sxs-lookup"><span data-stu-id="28f4f-110">*quadLaneID*</span></span> 
</dt> <dd>

<span data-ttu-id="28f4f-111">ID corsia; si tratta di un valore compreso tra 0 e 3.</span><span class="sxs-lookup"><span data-stu-id="28f4f-111">The lane ID; this will be a value from 0 to 3.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28f4f-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="28f4f-112">Return value</span></span>

<span data-ttu-id="28f4f-113">Valore di origine specificato.</span><span class="sxs-lookup"><span data-stu-id="28f4f-113">The specified source value.</span></span> <span data-ttu-id="28f4f-114">Il risultato di questa funzione è uniforme nel quad.</span><span class="sxs-lookup"><span data-stu-id="28f4f-114">The result of this function is uniform across the quad.</span></span> <span data-ttu-id="28f4f-115">Se la corsia di origine è inattiva, i risultati non sono definiti.</span><span class="sxs-lookup"><span data-stu-id="28f4f-115">If the source lane is inactive, the results are undefined.</span></span>

## <a name="remarks"></a><span data-ttu-id="28f4f-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="28f4f-116">Remarks</span></span>

<span data-ttu-id="28f4f-117">Per altre informazioni sui quad, vedere [Panoramica del modello di shader 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).</span><span class="sxs-lookup"><span data-stu-id="28f4f-117">For more information on quads, refer to [Overview of Shader Model 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).</span></span>

<span data-ttu-id="28f4f-118">Questa funzione è supportata dal modello di shader 6,0 solo in pixel e compute shader.</span><span class="sxs-lookup"><span data-stu-id="28f4f-118">This function is supported from shader model 6.0 only in pixel and compute shaders.</span></span>



 

## <a name="see-also"></a><span data-ttu-id="28f4f-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="28f4f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28f4f-120">Modello shader 6</span><span class="sxs-lookup"><span data-stu-id="28f4f-120">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




