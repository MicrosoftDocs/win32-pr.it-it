---
title: GetRenderTargetSamplePosition
description: Ottiene la posizione di campionamento (x, y) per un indice di esempio specificato.
ms.assetid: 07f14d1c-4fe5-4838-acce-d664cdc641e6
keywords:
- HLSL GetRenderTargetSamplePosition
topic_type:
- apiref
api_name:
- GetRenderTargetSamplePosition
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3b0cd944b175522ab7d722ae791f3548c6633b71
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103717776"
---
# <a name="getrendertargetsampleposition"></a><span data-ttu-id="c7d11-104">GetRenderTargetSamplePosition</span><span class="sxs-lookup"><span data-stu-id="c7d11-104">GetRenderTargetSamplePosition</span></span>

<span data-ttu-id="c7d11-105">Ottiene la posizione di campionamento (x, y) per un indice di esempio specificato.</span><span class="sxs-lookup"><span data-stu-id="c7d11-105">Gets the sampling position (x,y) for a given sample index.</span></span>



|                                                                                  |
|----------------------------------------------------------------------------------|
| <span data-ttu-id="c7d11-106">float<2> GetRenderTargetSamplePosition (in int<1> index</span><span class="sxs-lookup"><span data-stu-id="c7d11-106">float<2> GetRenderTargetSamplePosition( in int<1> Index</span></span><br/><span data-ttu-id="c7d11-107">);</span><span class="sxs-lookup"><span data-stu-id="c7d11-107">);</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="c7d11-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c7d11-108">Parameters</span></span>



| <span data-ttu-id="c7d11-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="c7d11-109">Item</span></span>                                                                                       | <span data-ttu-id="c7d11-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c7d11-110">Description</span></span>                                  |
|--------------------------------------------------------------------------------------------|----------------------------------------------|
| <span data-ttu-id="c7d11-111"><span id="Index"></span><span id="index"></span><span id="INDEX"></span>*Indice*</span><span class="sxs-lookup"><span data-stu-id="c7d11-111"><span id="Index"></span><span id="index"></span><span id="INDEX"></span>*Index*</span></span><br/> | <span data-ttu-id="c7d11-112">\[in \] un indice di esempio in base zero.</span><span class="sxs-lookup"><span data-stu-id="c7d11-112">\[in\] A zero-based sample index.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="c7d11-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c7d11-113">Return Value</span></span>

<span data-ttu-id="c7d11-114">Posizione (x, y) dell'esempio specificato.</span><span class="sxs-lookup"><span data-stu-id="c7d11-114">The (x,y) position of the given sample.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7d11-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="c7d11-115">Remarks</span></span>

<span data-ttu-id="c7d11-116">Usare questa funzione e [**GetRenderTargetSampleCount**](dx-graphics-hlsl-getrendertargetsamplecount.md) per trovare il numero e la posizione dei percorsi di campionamento per una destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="c7d11-116">Use this function and [**GetRenderTargetSampleCount**](dx-graphics-hlsl-getrendertargetsamplecount.md) to find out the number and position of the sampling locations for a render target.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="c7d11-117">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="c7d11-117">Minimum Shader Model</span></span>

<span data-ttu-id="c7d11-118">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="c7d11-118">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="c7d11-119">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="c7d11-119">Shader Model</span></span>                                                        | <span data-ttu-id="c7d11-120">Supportato</span><span class="sxs-lookup"><span data-stu-id="c7d11-120">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="c7d11-121">[Shader Model 4](dx-graphics-hlsl-sm4.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="c7d11-121">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="c7d11-122">sì</span><span class="sxs-lookup"><span data-stu-id="c7d11-122">yes</span></span>       |
| [<span data-ttu-id="c7d11-123">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c7d11-123">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)           | <span data-ttu-id="c7d11-124">no</span><span class="sxs-lookup"><span data-stu-id="c7d11-124">no</span></span>        |
| [<span data-ttu-id="c7d11-125">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c7d11-125">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)           | <span data-ttu-id="c7d11-126">no</span><span class="sxs-lookup"><span data-stu-id="c7d11-126">no</span></span>        |
| [<span data-ttu-id="c7d11-127">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c7d11-127">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)           | <span data-ttu-id="c7d11-128">no</span><span class="sxs-lookup"><span data-stu-id="c7d11-128">no</span></span>        |



 

## <a name="see-also"></a><span data-ttu-id="c7d11-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c7d11-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7d11-130">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="c7d11-130">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





