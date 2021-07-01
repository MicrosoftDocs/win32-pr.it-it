---
title: GetRenderTargetSamplePosition
description: Ottiene la posizione di campionamento (x,y) per un determinato indice di campionamento.
ms.assetid: 07f14d1c-4fe5-4838-acce-d664cdc641e6
keywords:
- GetRenderTargetSamplePosition HLSL
topic_type:
- apiref
api_name:
- GetRenderTargetSamplePosition
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c31bc829f8990517ddbea8be7c25eead413ab666
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120576"
---
# <a name="getrendertargetsampleposition"></a><span data-ttu-id="4421b-104">GetRenderTargetSamplePosition</span><span class="sxs-lookup"><span data-stu-id="4421b-104">GetRenderTargetSamplePosition</span></span>

<span data-ttu-id="4421b-105">Ottiene la posizione di campionamento (x,y) per un determinato indice di campionamento.</span><span class="sxs-lookup"><span data-stu-id="4421b-105">Gets the sampling position (x,y) for a given sample index.</span></span>

<span data-ttu-id="4421b-106">float<2> GetRenderTargetSamplePosition( in int<1> Index</span><span class="sxs-lookup"><span data-stu-id="4421b-106">float<2> GetRenderTargetSamplePosition( in int<1> Index</span></span><br/><span data-ttu-id="4421b-107">);</span><span class="sxs-lookup"><span data-stu-id="4421b-107">);</span></span>



 

## <a name="parameters"></a><span data-ttu-id="4421b-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4421b-108">Parameters</span></span>



| <span data-ttu-id="4421b-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="4421b-109">Item</span></span>                                                                                       | <span data-ttu-id="4421b-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4421b-110">Description</span></span>                                  |
|--------------------------------------------------------------------------------------------|----------------------------------------------|
| <span data-ttu-id="4421b-111"><span id="Index"></span><span id="index"></span><span id="INDEX"></span>*Indice*</span><span class="sxs-lookup"><span data-stu-id="4421b-111"><span id="Index"></span><span id="index"></span><span id="INDEX"></span>*Index*</span></span><br/> | <span data-ttu-id="4421b-112">\[in \] un indice di esempio in base zero.</span><span class="sxs-lookup"><span data-stu-id="4421b-112">\[in\] A zero-based sample index.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="4421b-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4421b-113">Return Value</span></span>

<span data-ttu-id="4421b-114">Posizione (x,y) dell'esempio specificato.</span><span class="sxs-lookup"><span data-stu-id="4421b-114">The (x,y) position of the given sample.</span></span>

## <a name="remarks"></a><span data-ttu-id="4421b-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="4421b-115">Remarks</span></span>

<span data-ttu-id="4421b-116">Usare questa funzione e [**GetRenderTargetSampleCount**](dx-graphics-hlsl-getrendertargetsamplecount.md) per individuare il numero e la posizione delle posizioni di campionamento per una destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="4421b-116">Use this function and [**GetRenderTargetSampleCount**](dx-graphics-hlsl-getrendertargetsamplecount.md) to find out the number and position of the sampling locations for a render target.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="4421b-117">Modello di shader minimo</span><span class="sxs-lookup"><span data-stu-id="4421b-117">Minimum Shader Model</span></span>

<span data-ttu-id="4421b-118">Questa funzione è supportata nei modelli di shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="4421b-118">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="4421b-119">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="4421b-119">Shader Model</span></span>                                                        | <span data-ttu-id="4421b-120">Supportato</span><span class="sxs-lookup"><span data-stu-id="4421b-120">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="4421b-121">[Modello shader 4 e](dx-graphics-hlsl-sm4.md) modelli di shader superiori</span><span class="sxs-lookup"><span data-stu-id="4421b-121">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="4421b-122">yes</span><span class="sxs-lookup"><span data-stu-id="4421b-122">yes</span></span>       |
| [<span data-ttu-id="4421b-123">Modello shader 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4421b-123">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)           | <span data-ttu-id="4421b-124">No</span><span class="sxs-lookup"><span data-stu-id="4421b-124">no</span></span>        |
| [<span data-ttu-id="4421b-125">Modello shader 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4421b-125">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)           | <span data-ttu-id="4421b-126">No</span><span class="sxs-lookup"><span data-stu-id="4421b-126">no</span></span>        |
| [<span data-ttu-id="4421b-127">Modello shader 1 (HLSL DirectX)</span><span class="sxs-lookup"><span data-stu-id="4421b-127">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)           | <span data-ttu-id="4421b-128">No</span><span class="sxs-lookup"><span data-stu-id="4421b-128">no</span></span>        |



 

## <a name="see-also"></a><span data-ttu-id="4421b-129">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="4421b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4421b-130">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="4421b-130">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





