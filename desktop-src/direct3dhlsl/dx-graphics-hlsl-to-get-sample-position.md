---
title: GetSamplePosition (oggetto trama DirectX HLSL)
description: Ottiene la posizione dell'esempio specificato.
ms.assetid: 4e622b85-82d6-4339-b03a-becbe5f9aa57
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9a1e5f4dc71d5af2e7973ef180c919a49e65ef81
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118586"
---
# <a name="getsampleposition-directx-hlsl-texture-object"></a><span data-ttu-id="788b6-103">GetSamplePosition (oggetto trama DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="788b6-103">GetSamplePosition (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="788b6-104">Ottiene la posizione dell'esempio specificato.</span><span class="sxs-lookup"><span data-stu-id="788b6-104">Gets the position of the specified sample.</span></span>

<span data-ttu-id="788b6-105">ret Object.GetSamplePosition( int s );</span><span class="sxs-lookup"><span data-stu-id="788b6-105">ret Object.GetSamplePosition( int s );</span></span>



 

## <a name="parameters"></a><span data-ttu-id="788b6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="788b6-106">Parameters</span></span>



| <span data-ttu-id="788b6-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="788b6-107">Item</span></span>                                                                                           | <span data-ttu-id="788b6-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="788b6-108">Description</span></span>                                                                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="788b6-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Oggetto*</span><span class="sxs-lookup"><span data-stu-id="788b6-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Object*</span></span><br/> | <span data-ttu-id="788b6-110">Tipo [texture-object](dx-graphics-hlsl-to-type.md) Texture2DMS o Texture2DMSArray.</span><span class="sxs-lookup"><span data-stu-id="788b6-110">A Texture2DMS or a Texture2DMSArray [texture-object](dx-graphics-hlsl-to-type.md) type.</span></span><br/> |
| <span data-ttu-id="788b6-111"><span id="s"></span><span id="S"></span>*s*</span><span class="sxs-lookup"><span data-stu-id="788b6-111"><span id="s"></span><span id="S"></span>*s*</span></span><br/>                                         | <span data-ttu-id="788b6-112">\[\]nell'indice di esempio in base zero.</span><span class="sxs-lookup"><span data-stu-id="788b6-112">\[in\] The zero-based sample index.</span></span><br/>                                                      |



 

## <a name="return-value"></a><span data-ttu-id="788b6-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="788b6-113">Return Value</span></span>

<span data-ttu-id="788b6-114">Restituisce la posizione di esempio (x,y), un vettore a virgola mobile a due componenti.</span><span class="sxs-lookup"><span data-stu-id="788b6-114">Returns the (x,y) sample position, a two-component floating-point vector.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="788b6-115">Modello shader minimo</span><span class="sxs-lookup"><span data-stu-id="788b6-115">Minimum Shader Model</span></span>

<span data-ttu-id="788b6-116">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="788b6-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="788b6-117">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="788b6-117">vs\_4\_0</span></span> | <span data-ttu-id="788b6-118">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="788b6-118">vs\_4\_1</span></span>  | <span data-ttu-id="788b6-119">ps \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="788b6-119">ps\_4\_0</span></span> | <span data-ttu-id="788b6-120">ps \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="788b6-120">ps\_4\_1</span></span>  | <span data-ttu-id="788b6-121">gs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="788b6-121">gs\_4\_0</span></span> | <span data-ttu-id="788b6-122">gs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="788b6-122">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
|          | <span data-ttu-id="788b6-123">x</span><span class="sxs-lookup"><span data-stu-id="788b6-123">x</span></span>         |          | <span data-ttu-id="788b6-124">x</span><span class="sxs-lookup"><span data-stu-id="788b6-124">x</span></span>         |          | <span data-ttu-id="788b6-125">x</span><span class="sxs-lookup"><span data-stu-id="788b6-125">x</span></span>         |



 

-   <span data-ttu-id="788b6-126">Shader Model 4.1 è disponibile in Direct3D 10.1 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="788b6-126">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="remarks"></a><span data-ttu-id="788b6-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="788b6-127">Remarks</span></span>

<span data-ttu-id="788b6-128">Un pixel shader può essere valutato alla frequenza di campionamento (eseguire un'pixel shader una volta per campione) o alla frequenza dei pixel (eseguire una pixel shader una volta per pixel).</span><span class="sxs-lookup"><span data-stu-id="788b6-128">A pixel shader can be evaluated at sample frequency (run a pixel shader once per sample) or at pixel frequency (run a pixel shader once per pixel).</span></span> <span data-ttu-id="788b6-129">Collegare la semantica SV SampleIndex a un input pixel shader per richiamare un pixel shader alla frequenza di campionamento, il valore di input viene quindi usato come indice di esempio durante il campionamento della \_ destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="788b6-129">Attach the SV\_SampleIndex semantic to a pixel shader input to invoke a pixel shader at sample frequency, the input value is then used as a sample index when sampling the render target.</span></span>

<span data-ttu-id="788b6-130">È possibile eseguire l'interpolazione pixel shader'input in diversi modi.</span><span class="sxs-lookup"><span data-stu-id="788b6-130">You can interpolate a pixel shader input in several ways.</span></span> <span data-ttu-id="788b6-131">Per eseguire l'interpolazione in:</span><span class="sxs-lookup"><span data-stu-id="788b6-131">To interpolate at:</span></span>

-   <span data-ttu-id="788b6-132">Un pixel al centro, non usare alcuna semantica.</span><span class="sxs-lookup"><span data-stu-id="788b6-132">A pixel center, don't use any semantic.</span></span>
-   <span data-ttu-id="788b6-133">Un esempio, usare la semantica SV \_ SampleIndex.</span><span class="sxs-lookup"><span data-stu-id="788b6-133">A sample, use the SV\_SampleIndex semantic.</span></span>
-   <span data-ttu-id="788b6-134">Posizione centrale, usare il [ \_ modificatore centroid.](dx-graphics-hlsl-struct.md)</span><span class="sxs-lookup"><span data-stu-id="788b6-134">A centroid location, use the [\_centroid](dx-graphics-hlsl-struct.md) modifier.</span></span>

## <a name="related-topics"></a><span data-ttu-id="788b6-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="788b6-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="788b6-136">Oggetto texture</span><span class="sxs-lookup"><span data-stu-id="788b6-136">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





