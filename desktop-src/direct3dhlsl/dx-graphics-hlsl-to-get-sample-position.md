---
title: GetSamplePosition (oggetto trama di DirectX HLSL)
description: Ottiene la posizione dell'esempio specificato.
ms.assetid: 4e622b85-82d6-4339-b03a-becbe5f9aa57
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 062bf08064faf112fdc1efe5b371fcad72efeeea
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/20/2019
ms.locfileid: "104398200"
---
# <a name="getsampleposition-directx-hlsl-texture-object"></a><span data-ttu-id="f6c73-103">GetSamplePosition (oggetto trama di DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f6c73-103">GetSamplePosition (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="f6c73-104">Ottiene la posizione dell'esempio specificato.</span><span class="sxs-lookup"><span data-stu-id="f6c73-104">Gets the position of the specified sample.</span></span>



|                                        |
|----------------------------------------|
| <span data-ttu-id="f6c73-105">RET Object. GetSamplePosition (int s);</span><span class="sxs-lookup"><span data-stu-id="f6c73-105">ret Object.GetSamplePosition( int s );</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="f6c73-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f6c73-106">Parameters</span></span>



| <span data-ttu-id="f6c73-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="f6c73-107">Item</span></span>                                                                                           | <span data-ttu-id="f6c73-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f6c73-108">Description</span></span>                                                                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6c73-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Oggetto*</span><span class="sxs-lookup"><span data-stu-id="f6c73-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Object*</span></span><br/> | <span data-ttu-id="f6c73-110">Un Texture2DMS o un tipo di [oggetto trama](dx-graphics-hlsl-to-type.md) Texture2DMSArray.</span><span class="sxs-lookup"><span data-stu-id="f6c73-110">A Texture2DMS or a Texture2DMSArray [texture-object](dx-graphics-hlsl-to-type.md) type.</span></span><br/> |
| <span data-ttu-id="f6c73-111"><span id="s"></span><span id="S"></span>*s*</span><span class="sxs-lookup"><span data-stu-id="f6c73-111"><span id="s"></span><span id="S"></span>*s*</span></span><br/>                                         | <span data-ttu-id="f6c73-112">\[nell' \] indice di esempio in base zero.</span><span class="sxs-lookup"><span data-stu-id="f6c73-112">\[in\] The zero-based sample index.</span></span><br/>                                                      |



 

## <a name="return-value"></a><span data-ttu-id="f6c73-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f6c73-113">Return Value</span></span>

<span data-ttu-id="f6c73-114">Restituisce la posizione di esempio (x, y), un vettore a virgola mobile a due componenti.</span><span class="sxs-lookup"><span data-stu-id="f6c73-114">Returns the (x,y) sample position, a two-component floating-point vector.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="f6c73-115">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="f6c73-115">Minimum Shader Model</span></span>

<span data-ttu-id="f6c73-116">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="f6c73-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="f6c73-117">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f6c73-117">vs\_4\_0</span></span> | <span data-ttu-id="f6c73-118">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="f6c73-118">vs\_4\_1</span></span>  | <span data-ttu-id="f6c73-119">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f6c73-119">ps\_4\_0</span></span> | <span data-ttu-id="f6c73-120">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="f6c73-120">ps\_4\_1</span></span>  | <span data-ttu-id="f6c73-121">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f6c73-121">gs\_4\_0</span></span> | <span data-ttu-id="f6c73-122">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="f6c73-122">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
|          | <span data-ttu-id="f6c73-123">x</span><span class="sxs-lookup"><span data-stu-id="f6c73-123">x</span></span>         |          | <span data-ttu-id="f6c73-124">x</span><span class="sxs-lookup"><span data-stu-id="f6c73-124">x</span></span>         |          | <span data-ttu-id="f6c73-125">x</span><span class="sxs-lookup"><span data-stu-id="f6c73-125">x</span></span>         |



 

-   <span data-ttu-id="f6c73-126">Il modello di Shader 4,1 è disponibile in Direct3D 10,1 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="f6c73-126">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6c73-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="f6c73-127">Remarks</span></span>

<span data-ttu-id="f6c73-128">Un pixel shader può essere valutato in base alla frequenza di campionamento (eseguire una pixel shader una sola volta per campione) o alla frequenza in pixel (eseguire una pixel shader una volta per pixel).</span><span class="sxs-lookup"><span data-stu-id="f6c73-128">A pixel shader can be evaluated at sample frequency (run a pixel shader once per sample) or at pixel frequency (run a pixel shader once per pixel).</span></span> <span data-ttu-id="f6c73-129">Per \_ richiamare una pixel shader a pixel shader una frequenza di campionamento, il valore di input viene quindi utilizzato come indice di esempio durante il campionamento della destinazione di rendering.</span><span class="sxs-lookup"><span data-stu-id="f6c73-129">Attach the SV\_SampleIndex semantic to a pixel shader input to invoke a pixel shader at sample frequency, the input value is then used as a sample index when sampling the render target.</span></span>

<span data-ttu-id="f6c73-130">È possibile interpolare un input di pixel shader in diversi modi.</span><span class="sxs-lookup"><span data-stu-id="f6c73-130">You can interpolate a pixel shader input in several ways.</span></span> <span data-ttu-id="f6c73-131">Per interpolare:</span><span class="sxs-lookup"><span data-stu-id="f6c73-131">To interpolate at:</span></span>

-   <span data-ttu-id="f6c73-132">Un pixel Center, non usare alcuna semantica.</span><span class="sxs-lookup"><span data-stu-id="f6c73-132">A pixel center, don't use any semantic.</span></span>
-   <span data-ttu-id="f6c73-133">Esempio, usare la \_ semantica SV SampleIndex.</span><span class="sxs-lookup"><span data-stu-id="f6c73-133">A sample, use the SV\_SampleIndex semantic.</span></span>
-   <span data-ttu-id="f6c73-134">Una posizione del centro, usare il modificatore di [ \_ baricentro](dx-graphics-hlsl-struct.md) .</span><span class="sxs-lookup"><span data-stu-id="f6c73-134">A centroid location, use the [\_centroid](dx-graphics-hlsl-struct.md) modifier.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f6c73-135">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f6c73-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6c73-136">Texture-oggetto</span><span class="sxs-lookup"><span data-stu-id="f6c73-136">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





