---
title: GetRenderTargetSampleCount
description: Ottiene il numero di campioni per una destinazione di rendering.
ms.assetid: e813134e-c58c-4845-b519-c1074993801e
keywords:
- HLSL GetRenderTargetSampleCount
topic_type:
- apiref
api_name:
- GetRenderTargetSampleCount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 96c159a2ed63684b4bad2cbc6fa789c2dbd76edf
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104471998"
---
# <a name="getrendertargetsamplecount"></a><span data-ttu-id="184af-104">GetRenderTargetSampleCount</span><span class="sxs-lookup"><span data-stu-id="184af-104">GetRenderTargetSampleCount</span></span>

<span data-ttu-id="184af-105">Ottiene il numero di campioni per una destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="184af-105">Gets the number of samples for a render target.</span></span>



| <span data-ttu-id="184af-106">*Uint* GetRenderTargetSampleCount()</span><span class="sxs-lookup"><span data-stu-id="184af-106">*UINT* GetRenderTargetSampleCount()</span></span> |
|-------------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="184af-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="184af-107">Parameters</span></span>



| <span data-ttu-id="184af-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="184af-108">Item</span></span>                                                                                 | <span data-ttu-id="184af-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="184af-109">Description</span></span> |
|--------------------------------------------------------------------------------------|-------------|
| <span data-ttu-id="184af-110"><span id="None"></span><span id="none"></span><span id="NONE"></span>Nessuno</span><span class="sxs-lookup"><span data-stu-id="184af-110"><span id="None"></span><span id="none"></span><span id="NONE"></span>None</span></span><br/> |             |



 

## <a name="return-value"></a><span data-ttu-id="184af-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="184af-111">Return Value</span></span>

<span data-ttu-id="184af-112">Numero di campioni.</span><span class="sxs-lookup"><span data-stu-id="184af-112">The number of samples.</span></span>

## <a name="remarks"></a><span data-ttu-id="184af-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="184af-113">Remarks</span></span>

<span data-ttu-id="184af-114">Usare questa funzione e [**GetRenderTargetSamplePosition**](dx-graphics-hlsl-getrendertargetsampleposition.md) per trovare il numero e la posizione dei percorsi di campionamento per una destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="184af-114">Use this function and [**GetRenderTargetSamplePosition**](dx-graphics-hlsl-getrendertargetsampleposition.md) to find out the number and position of the sampling locations for a render target.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="184af-115">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="184af-115">Minimum Shader Model</span></span>

<span data-ttu-id="184af-116">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="184af-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="184af-117">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="184af-117">Shader Model</span></span>                                                        | <span data-ttu-id="184af-118">Supportato</span><span class="sxs-lookup"><span data-stu-id="184af-118">Supported</span></span> |
|---------------------------------------------------------------------|-----------|
| <span data-ttu-id="184af-119">[Shader Model 4](dx-graphics-hlsl-sm4.md) e versioni successive shader Models</span><span class="sxs-lookup"><span data-stu-id="184af-119">[Shader Model 4](dx-graphics-hlsl-sm4.md) and higher shader models</span></span> | <span data-ttu-id="184af-120">sì</span><span class="sxs-lookup"><span data-stu-id="184af-120">yes</span></span>       |
| [<span data-ttu-id="184af-121">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="184af-121">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)           | <span data-ttu-id="184af-122">no</span><span class="sxs-lookup"><span data-stu-id="184af-122">no</span></span>        |
| [<span data-ttu-id="184af-123">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="184af-123">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md)           | <span data-ttu-id="184af-124">no</span><span class="sxs-lookup"><span data-stu-id="184af-124">no</span></span>        |
| [<span data-ttu-id="184af-125">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="184af-125">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)           | <span data-ttu-id="184af-126">no</span><span class="sxs-lookup"><span data-stu-id="184af-126">no</span></span>        |



 

## <a name="see-also"></a><span data-ttu-id="184af-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="184af-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="184af-128">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="184af-128">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 





