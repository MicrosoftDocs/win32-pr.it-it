---
title: Modello Shader 5
description: Questa sezione contiene le pagine di riferimento per HLSL Shader Model 5.
ms.assetid: ec646940-8901-45c5-a44c-434c8acae2aa
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f379301008190367a40959a319d01cfad127f6b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399221"
---
# <a name="shader-model-5"></a><span data-ttu-id="2880e-103">Modello Shader 5</span><span class="sxs-lookup"><span data-stu-id="2880e-103">Shader Model 5</span></span>

<span data-ttu-id="2880e-104">Questa sezione contiene le pagine di riferimento per HLSL Shader Model 5.</span><span class="sxs-lookup"><span data-stu-id="2880e-104">This section contains the reference pages for HLSL Shader Model 5.</span></span>

<span data-ttu-id="2880e-105">Shader Model 5 è un superset di funzionalità in [Shader Model 4](dx-graphics-hlsl-sm4.md).</span><span class="sxs-lookup"><span data-stu-id="2880e-105">Shader Model 5 is a superset of the capabilites in [Shader Model 4](dx-graphics-hlsl-sm4.md).</span></span> <span data-ttu-id="2880e-106">È stato progettato usando un core di shader comune che fornisce un set comune di funzionalità a tutti gli shader programmabili, che sono programmabili solo con HLSL.</span><span class="sxs-lookup"><span data-stu-id="2880e-106">It has been designed using a common-shader core which provides a common set of features to all programmable shaders, which are only programmable using HLSL.</span></span>



| <span data-ttu-id="2880e-107">Caratteristica</span><span class="sxs-lookup"><span data-stu-id="2880e-107">Feature</span></span>                   | <span data-ttu-id="2880e-108">Funzionalità</span><span class="sxs-lookup"><span data-stu-id="2880e-108">Capability</span></span>                                                                                                                                             |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2880e-109">Set di istruzioni</span><span class="sxs-lookup"><span data-stu-id="2880e-109">Instruction Set</span></span>           | [<span data-ttu-id="2880e-110">**Funzioni intrinseche HLSL**</span><span class="sxs-lookup"><span data-stu-id="2880e-110">**HLSL intrinsic functions**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                                                                               |
| <span data-ttu-id="2880e-111">Vertex shader max</span><span class="sxs-lookup"><span data-stu-id="2880e-111">Vertex Shader Max</span></span>         | <span data-ttu-id="2880e-112">Nessuna restrizione</span><span class="sxs-lookup"><span data-stu-id="2880e-112">No restriction</span></span>                                                                                                                                         |
| <span data-ttu-id="2880e-113">Pixel shader max</span><span class="sxs-lookup"><span data-stu-id="2880e-113">Pixel Shader Max</span></span>          | <span data-ttu-id="2880e-114">Nessuna restrizione</span><span class="sxs-lookup"><span data-stu-id="2880e-114">No restriction</span></span>                                                                                                                                         |
| <span data-ttu-id="2880e-115">Nuovi profili shader aggiunti</span><span class="sxs-lookup"><span data-stu-id="2880e-115">New Shader Profiles Added</span></span> | <span data-ttu-id="2880e-116">cs \_ 4 \_ 0, GS \_ 4 \_ 0 \* , PS \_ 4 \_ 0 \* , vs \_ 4 \_ 0, \* cs \_ 4 \_ 1, GS \_ 4 \_ 1 \* , PS \_ 4 \_ 1 \* , vs \_ 4 \_ 1 \* , cs \_ 5 \_ 0, DS \_ 5 \_ 0, GS \_ 5 \_ 0, HS \_ 5 \_ 0, PS \_ 5 \_ 0, vs \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="2880e-116">cs\_4\_0, gs\_4\_0\*, ps\_4\_0\*, vs\_4\_0\*, cs\_4\_1, gs\_4\_1\*, ps\_4\_1\*, vs\_4\_1\*, cs\_5\_0, ds\_5\_0, gs\_5\_0, hs\_5\_0, ps\_5\_0, vs\_5\_0</span></span> |



 

<span data-ttu-id="2880e-117">\* -GS \_ 4 \_ 0, GS \_ 4 \_ 1, PS \_ 4 \_ 0, PS \_ 4 \_ 1, vs \_ 4 \_ 0 e vs \_ 4 \_ 1 sono stati introdotti nel modello Shader 4,0, tuttavia, DirectX 11 aggiunge il supporto per [buffer strutturati](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) e buffer di indirizzi di byte al modello Shader 4 in esecuzione su hardware DirectX 10.</span><span class="sxs-lookup"><span data-stu-id="2880e-117">\* - gs\_4\_0, gs\_4\_1, ps\_4\_0, ps\_4\_1, vs\_4\_0 and vs\_4\_1 were introduced in Shader Model 4.0, however, DirectX 11 adds support for [structured buffers](/windows/desktop/direct3d11/direct3d-11-advanced-stages-cs-resources) and byte address buffers to Shader Model 4 running on DirectX 10 hardware.</span></span>

<span data-ttu-id="2880e-118">Shader Model 5 introduce il [compute shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader) che fornisce un calcolo ad alta velocità per utilizzo generico.</span><span class="sxs-lookup"><span data-stu-id="2880e-118">Shader Model 5 introduces the [compute shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader) which provides high-speed general purpose computing.</span></span>

<span data-ttu-id="2880e-119">Un elenco più completo delle funzionalità di Shader Model 5 è incluso in un elenco delle [funzionalità di Direct3D 11](/windows/desktop/direct3d11/direct3d-11-features).</span><span class="sxs-lookup"><span data-stu-id="2880e-119">A more complete listing of Shader Model 5 features is included in a listing of the [Direct3D 11 features](/windows/desktop/direct3d11/direct3d-11-features).</span></span>

<span data-ttu-id="2880e-120">La sezione di [assembly Shader Model 5](shader-model-5-assembly--directx-hlsl-.md) descrive le istruzioni di assembly supportate dal modello di shader 5.</span><span class="sxs-lookup"><span data-stu-id="2880e-120">The [Shader Model 5 Assembly](shader-model-5-assembly--directx-hlsl-.md) section describes the assembly instructions that the Shader Model 5 supports.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2880e-121">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="2880e-121">In This Section</span></span>



| <span data-ttu-id="2880e-122">Elemento</span><span class="sxs-lookup"><span data-stu-id="2880e-122">Item</span></span>                                                                                                                                                                                                                                                        | <span data-ttu-id="2880e-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2880e-123">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="2880e-124"><span id="Shader_Model_5_Attributes"></span><span id="shader_model_5_attributes"></span><span id="SHADER_MODEL_5_ATTRIBUTES"></span>[Attributi del modello di shader 5](d3d11-graphics-reference-sm5-attributes.md)</span><span class="sxs-lookup"><span data-stu-id="2880e-124"><span id="Shader_Model_5_Attributes"></span><span id="shader_model_5_attributes"></span><span id="SHADER_MODEL_5_ATTRIBUTES"></span>[Shader Model 5 Attributes](d3d11-graphics-reference-sm5-attributes.md)</span></span><br/>                                     | <span data-ttu-id="2880e-125">Pagine di riferimento per gli attributi dello shader model 5.</span><span class="sxs-lookup"><span data-stu-id="2880e-125">Reference pages for Shader Model 5 attributes.</span></span><br/>          |
| <span data-ttu-id="2880e-126"><span id="Shader_Model_5_Intrinsic_Functions"></span><span id="shader_model_5_intrinsic_functions"></span><span id="SHADER_MODEL_5_INTRINSIC_FUNCTIONS"></span>[Funzioni intrinseche del modello shader 5](d3d11-graphics-reference-sm5-intrinsics.md)</span><span class="sxs-lookup"><span data-stu-id="2880e-126"><span id="Shader_Model_5_Intrinsic_Functions"></span><span id="shader_model_5_intrinsic_functions"></span><span id="SHADER_MODEL_5_INTRINSIC_FUNCTIONS"></span>[Shader Model 5 Intrinsic Functions](d3d11-graphics-reference-sm5-intrinsics.md)</span></span><br/> | <span data-ttu-id="2880e-127">Pagine di riferimento per le funzioni intrinseche del modello shader 5.</span><span class="sxs-lookup"><span data-stu-id="2880e-127">Reference pages for Shader Model 5 intrinsic functions.</span></span><br/> |
| <span data-ttu-id="2880e-128"><span id="Shader_Model_5_Objects"></span><span id="shader_model_5_objects"></span><span id="SHADER_MODEL_5_OBJECTS"></span>[Oggetti Shader Model 5](d3d11-graphics-reference-sm5-objects.md)</span><span class="sxs-lookup"><span data-stu-id="2880e-128"><span id="Shader_Model_5_Objects"></span><span id="shader_model_5_objects"></span><span id="SHADER_MODEL_5_OBJECTS"></span>[Shader Model 5 Objects](d3d11-graphics-reference-sm5-objects.md)</span></span><br/>                                                    | <span data-ttu-id="2880e-129">Pagine di riferimento per oggetti e metodi dello shader model 5.</span><span class="sxs-lookup"><span data-stu-id="2880e-129">Reference pages for Shader Model 5 objects and methods.</span></span><br/> |
| <span data-ttu-id="2880e-130"><span id="Shader_Model_5_System_Values"></span><span id="shader_model_5_system_values"></span><span id="SHADER_MODEL_5_SYSTEM_VALUES"></span>[Valori di sistema di Shader Model 5](d3d11-graphics-reference-sm5-system-values.md)</span><span class="sxs-lookup"><span data-stu-id="2880e-130"><span id="Shader_Model_5_System_Values"></span><span id="shader_model_5_system_values"></span><span id="SHADER_MODEL_5_SYSTEM_VALUES"></span>[Shader Model 5 System Values](d3d11-graphics-reference-sm5-system-values.md)</span></span><br/>                      | <span data-ttu-id="2880e-131">Pagine di riferimento per i valori del sistema Shader Model 5.</span><span class="sxs-lookup"><span data-stu-id="2880e-131">Reference pages for Shader Model 5 system values.</span></span><br/>       |



 

## <a name="related-topics"></a><span data-ttu-id="2880e-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2880e-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2880e-133">Modelli shader rispetto ai profili shader</span><span class="sxs-lookup"><span data-stu-id="2880e-133">Shader Models vs Shader Profiles</span></span>](dx-graphics-hlsl-models.md)
</dt> </dl>

 

