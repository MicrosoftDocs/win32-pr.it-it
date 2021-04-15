---
title: clip
description: Elimina il pixel corrente se il valore specificato è minore di zero.
ms.assetid: c9f84a27-5572-45aa-a12f-4446614b7be5
keywords:
- clip HLSL
topic_type:
- apiref
api_name:
- clip
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 92a75f2839dbbb605d976e07fffa5c2f9b27fd86
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976719"
---
# <a name="clip"></a><span data-ttu-id="8fe5e-104">clip</span><span class="sxs-lookup"><span data-stu-id="8fe5e-104">clip</span></span>

<span data-ttu-id="8fe5e-105">Elimina il pixel corrente se il valore specificato è minore di zero.</span><span class="sxs-lookup"><span data-stu-id="8fe5e-105">Discards the current pixel if the specified value is less than zero.</span></span>



| <span data-ttu-id="8fe5e-106">clip (*x*)</span><span class="sxs-lookup"><span data-stu-id="8fe5e-106">clip(*x*)</span></span> |
|-----------|



 

## <a name="parameters"></a><span data-ttu-id="8fe5e-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="8fe5e-107">Parameters</span></span>



| <span data-ttu-id="8fe5e-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="8fe5e-108">Item</span></span>                                                   | <span data-ttu-id="8fe5e-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8fe5e-109">Description</span></span>                            |
|--------------------------------------------------------|----------------------------------------|
| <span data-ttu-id="8fe5e-110"><span id="x"></span><span id="X"></span>*x*</span><span class="sxs-lookup"><span data-stu-id="8fe5e-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="8fe5e-111">\[nel \] valore specificato.</span><span class="sxs-lookup"><span data-stu-id="8fe5e-111">\[in\] The specified value.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="8fe5e-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8fe5e-112">Return Value</span></span>

<span data-ttu-id="8fe5e-113">No.</span><span class="sxs-lookup"><span data-stu-id="8fe5e-113">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="8fe5e-114">Osservazioni</span><span class="sxs-lookup"><span data-stu-id="8fe5e-114">Remarks</span></span>

<span data-ttu-id="8fe5e-115">Usare la funzione di **clip** HLSL intrinseca per simulare i piani di ritaglio se ogni componente del parametro *x* rappresenta la distanza da un piano.</span><span class="sxs-lookup"><span data-stu-id="8fe5e-115">Use the **clip** HLSL intrinsic function to simulate clipping planes if each component of the *x* parameter represents the distance from a plane.</span></span>

<span data-ttu-id="8fe5e-116">Usare anche la funzione di **ritaglio** per verificare il comportamento alfa, come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="8fe5e-116">Also, use the **clip** function to test for alpha behavior, as shown in the following example:</span></span>


```
clip( Input.Color.A < 0.1f ? -1:1 );
```



## <a name="type-description"></a><span data-ttu-id="8fe5e-117">Descrizione del tipo</span><span class="sxs-lookup"><span data-stu-id="8fe5e-117">Type Description</span></span>



| <span data-ttu-id="8fe5e-118">Nome</span><span class="sxs-lookup"><span data-stu-id="8fe5e-118">Name</span></span> | [<span data-ttu-id="8fe5e-119">**Tipo di modello**</span><span class="sxs-lookup"><span data-stu-id="8fe5e-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [<span data-ttu-id="8fe5e-120">**Tipo di componente**</span><span class="sxs-lookup"><span data-stu-id="8fe5e-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="8fe5e-121">Dimensione</span><span class="sxs-lookup"><span data-stu-id="8fe5e-121">Size</span></span> |
|------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="8fe5e-122">*x*</span><span class="sxs-lookup"><span data-stu-id="8fe5e-122">*x*</span></span>  | <span data-ttu-id="8fe5e-123">[**scalare**](dx-graphics-hlsl-intrinsic-functions.md), **vettore** o **matrice**</span><span class="sxs-lookup"><span data-stu-id="8fe5e-123">[**scalar**](dx-graphics-hlsl-intrinsic-functions.md), **vector**, or **matrix**</span></span> | [<span data-ttu-id="8fe5e-124">**float**</span><span class="sxs-lookup"><span data-stu-id="8fe5e-124">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="8fe5e-125">any</span><span class="sxs-lookup"><span data-stu-id="8fe5e-125">any</span></span>  |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="8fe5e-126">Modello Shader minimo</span><span class="sxs-lookup"><span data-stu-id="8fe5e-126">Minimum Shader Model</span></span>

<span data-ttu-id="8fe5e-127">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="8fe5e-127">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="8fe5e-128">Modello di shader</span><span class="sxs-lookup"><span data-stu-id="8fe5e-128">Shader Model</span></span>                                              | <span data-ttu-id="8fe5e-129">Supportato</span><span class="sxs-lookup"><span data-stu-id="8fe5e-129">Supported</span></span>               |
|-----------------------------------------------------------|-------------------------|
| [<span data-ttu-id="8fe5e-130">Modello Shader 4</span><span class="sxs-lookup"><span data-stu-id="8fe5e-130">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="8fe5e-131">Sì (solo pixel shader)</span><span class="sxs-lookup"><span data-stu-id="8fe5e-131">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="8fe5e-132">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8fe5e-132">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="8fe5e-133">Sì (solo pixel shader)</span><span class="sxs-lookup"><span data-stu-id="8fe5e-133">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="8fe5e-134">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8fe5e-134">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="8fe5e-135">Sì (solo pixel shader)</span><span class="sxs-lookup"><span data-stu-id="8fe5e-135">yes (pixel shader only)</span></span> |
| [<span data-ttu-id="8fe5e-136">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8fe5e-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="8fe5e-137">Sì (solo pixel shader)</span><span class="sxs-lookup"><span data-stu-id="8fe5e-137">yes (pixel shader only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="8fe5e-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8fe5e-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fe5e-139">**Funzioni intrinseche (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="8fe5e-139">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

