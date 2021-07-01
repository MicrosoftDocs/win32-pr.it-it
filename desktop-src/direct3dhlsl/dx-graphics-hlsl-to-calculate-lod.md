---
title: CalculateLevelOfDetail (oggetto trama DirectX HLSL)
description: Calcola il livello di dettaglio.
ms.assetid: 7c7c3754-45a9-49c6-8420-aac22f776b15
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9e307527f93c153f0f78ce58b4d70ead4f7c1bc4
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120556"
---
# <a name="calculatelevelofdetail-directx-hlsl-texture-object"></a><span data-ttu-id="e342e-103">CalculateLevelOfDetail (oggetto trama DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e342e-103">CalculateLevelOfDetail (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="e342e-104">Calcola il livello di dettaglio.</span><span class="sxs-lookup"><span data-stu-id="e342e-104">Calculates the level of detail.</span></span>

<span data-ttu-id="e342e-105">ret Object.CalculateLevelOfDetail( sampler \_ state S, float x );</span><span class="sxs-lookup"><span data-stu-id="e342e-105">ret Object.CalculateLevelOfDetail( sampler\_state S, float x );</span></span>



 

## <a name="parameters"></a><span data-ttu-id="e342e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e342e-106">Parameters</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e342e-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="e342e-107">Item</span></span></th>
<th><span data-ttu-id="e342e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e342e-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e342e-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Oggetto</em></span><span class="sxs-lookup"><span data-stu-id="e342e-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span><em>Object</em></span></span><br/></td>
<td><span data-ttu-id="e342e-110">Qualsiasi <a href="dx-graphics-hlsl-to-type.md">tipo di oggetto</a> trama (ad eccezione di Texture2DMS e Texture2DMSArray).</span><span class="sxs-lookup"><span data-stu-id="e342e-110">Any <a href="dx-graphics-hlsl-to-type.md">texture-object</a> type (except Texture2DMS and Texture2DMSArray).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e342e-111"><span id="S"></span><span id="s"></span><em>S</em></span><span class="sxs-lookup"><span data-stu-id="e342e-111"><span id="S"></span><span id="s"></span><em>S</em></span></span><br/></td>
<td><span data-ttu-id="e342e-112">[in] Stato <a href="/windows/desktop/direct3d10/d3d10-effect-sampler-syntax">del campionatore.</a></span><span class="sxs-lookup"><span data-stu-id="e342e-112">[in] A <a href="/windows/desktop/direct3d10/d3d10-effect-sampler-syntax">Sampler state</a>.</span></span> <span data-ttu-id="e342e-113">Si tratta di un oggetto dichiarato in un file di effetti che contiene assegnazioni di stato.</span><span class="sxs-lookup"><span data-stu-id="e342e-113">This is an object declared in an effect file that contains state assignments.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e342e-114"><span id="x"></span><span id="X"></span><em>X</em></span><span class="sxs-lookup"><span data-stu-id="e342e-114"><span id="x"></span><span id="X"></span><em>x</em></span></span><br/></td>
<td><span data-ttu-id="e342e-115">[in] Valore o valori di interpolazione lineare, ovvero un numero a virgola mobile compreso tra 0,0 e 1,0 inclusi.</span><span class="sxs-lookup"><span data-stu-id="e342e-115">[in] The linear interpolation value or values, which is a floating-point number between 0.0 and 1.0 inclusive.</span></span> <span data-ttu-id="e342e-116">Il numero di componenti dipende dal tipo di oggetto trama.</span><span class="sxs-lookup"><span data-stu-id="e342e-116">The number of components is dependent on the texture-object type.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e342e-117">Texture-Object tipo</span><span class="sxs-lookup"><span data-stu-id="e342e-117">Texture-Object Type</span></span></th>
<th><span data-ttu-id="e342e-118">Tipo di parametro</span><span class="sxs-lookup"><span data-stu-id="e342e-118">Parameter Type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e342e-119">Texture1D, Texture1DArray</span><span class="sxs-lookup"><span data-stu-id="e342e-119">Texture1D, Texture1DArray</span></span></td>
<td><span data-ttu-id="e342e-120">float1</span><span class="sxs-lookup"><span data-stu-id="e342e-120">float1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e342e-121">Texture2D, Texture2DArray</span><span class="sxs-lookup"><span data-stu-id="e342e-121">Texture2D, Texture2DArray</span></span></td>
<td><span data-ttu-id="e342e-122">float2</span><span class="sxs-lookup"><span data-stu-id="e342e-122">float2</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e342e-123">Texture3D, TextureCube, TextureCubeArray</span><span class="sxs-lookup"><span data-stu-id="e342e-123">Texture3D, TextureCube, TextureCubeArray</span></span> </td>
<td><span data-ttu-id="e342e-124">float3</span><span class="sxs-lookup"><span data-stu-id="e342e-124">float3</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="return-value"></a><span data-ttu-id="e342e-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e342e-125">Return Value</span></span>

<span data-ttu-id="e342e-126">Restituisce il lod calcolato, un singolo valore a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="e342e-126">Returns the calculated LOD, a single floating-point value.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="e342e-127">Modello shader minimo</span><span class="sxs-lookup"><span data-stu-id="e342e-127">Minimum Shader Model</span></span>

<span data-ttu-id="e342e-128">Questa funzione è supportata nei modelli shader seguenti.</span><span class="sxs-lookup"><span data-stu-id="e342e-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="e342e-129">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e342e-129">vs\_4\_0</span></span> | <span data-ttu-id="e342e-130">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="e342e-130">vs\_4\_1</span></span>  | <span data-ttu-id="e342e-131">ps \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e342e-131">ps\_4\_0</span></span> | <span data-ttu-id="e342e-132">ps \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="e342e-132">ps\_4\_1</span></span>  | <span data-ttu-id="e342e-133">gs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e342e-133">gs\_4\_0</span></span> | <span data-ttu-id="e342e-134">gs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="e342e-134">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
|          |           |          | <span data-ttu-id="e342e-135">x</span><span class="sxs-lookup"><span data-stu-id="e342e-135">x</span></span>         |          |           |



 

1.  <span data-ttu-id="e342e-136">TextureCubeArray è disponibile in Shader Model 4.1 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="e342e-136">TextureCubeArray is available in Shader Model 4.1 or higher.</span></span>
2.  <span data-ttu-id="e342e-137">Shader Model 4.1 è disponibile in Direct3D 10.1 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="e342e-137">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e342e-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e342e-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e342e-139">Oggetto texture</span><span class="sxs-lookup"><span data-stu-id="e342e-139">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

