---
title: HLSL Shader Model 5
description: HLSL Shader Model 5
ms.assetid: 072c1ff2-ca1b-427c-9969-aa24ebb4ee38
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b33b0e2f009b796eb0b8828cc195fb9543ba2b9b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872657"
---
# <a name="hlsl-shader-model-5"></a><span data-ttu-id="788e7-103">HLSL Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="788e7-103">HLSL Shader Model 5</span></span>

<span data-ttu-id="788e7-104">Questa sezione contiene informazioni generali sulla High-Level Shader Language, in particolare le nuove funzionalità di Shader Model 5 introdotte in Microsoft Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="788e7-104">This section contains overview material for the High-Level Shader Language, specifically the new features in shader model 5 introduced in Microsoft Direct3D 11.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="788e7-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="788e7-105">In This Section</span></span>



| <span data-ttu-id="788e7-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="788e7-106">Item</span></span>                                                                                                                                                                                                               | <span data-ttu-id="788e7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="788e7-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="788e7-108"><span id="Dynamic_Linking"></span><span id="dynamic_linking"></span><span id="DYNAMIC_LINKING"></span>[Collegamento dinamico](overviews-direct3d-11-hlsl-dynamic-linking.md)</span><span class="sxs-lookup"><span data-stu-id="788e7-108"><span id="Dynamic_Linking"></span><span id="dynamic_linking"></span><span id="DYNAMIC_LINKING"></span>[Dynamic Linking](overviews-direct3d-11-hlsl-dynamic-linking.md)</span></span><br/>                                 | <span data-ttu-id="788e7-109">Il collegamento dinamico consente al runtime di prendere una decisione in fase di creazione, anziché in fase di compilazione, sul percorso del codice da eseguire.</span><span class="sxs-lookup"><span data-stu-id="788e7-109">Dynamic linking allows the runtime to make a decision at draw-time (rather than compile-time) about which code path to run.</span></span> <span data-ttu-id="788e7-110">In questo modo si riduce il problema di proliferazione dello shader causato da shader con firme di input quasi identiche.</span><span class="sxs-lookup"><span data-stu-id="788e7-110">This reduces the shader proliferation problem caused by shaders with nearly identical input signatures.</span></span><br/>                                                                                                                         |
| <span data-ttu-id="788e7-111"><span id="Geometry_Shader_Features"></span><span id="geometry_shader_features"></span><span id="GEOMETRY_SHADER_FEATURES"></span>[Funzionalità di Geometry shader](overviews-direct3d-11-hlsl-gs-features.md)</span><span class="sxs-lookup"><span data-stu-id="788e7-111"><span id="Geometry_Shader_Features"></span><span id="geometry_shader_features"></span><span id="GEOMETRY_SHADER_FEATURES"></span>[Geometry Shader Features](overviews-direct3d-11-hlsl-gs-features.md)</span></span><br/> | <span data-ttu-id="788e7-112">Nuove funzionalità di Geometry shader, tra cui: istanza, che fornisce un miglioramento delle prestazioni quando l'ordine delle primitive nel flusso non è rilevante e più flussi di output del punto in modo che uno shader possa restituire i vertici su più di un flusso.</span><span class="sxs-lookup"><span data-stu-id="788e7-112">New geometry shader features including: instancing, which provides a performance boost when the order of primitives in the stream doesn't matter, and multiple point output streams so a shader can output vertices on more than one stream.</span></span><br/>                                                                                                                |
| <span data-ttu-id="788e7-113"><span id="Tessellation"></span><span id="tessellation"></span><span id="TESSELLATION"></span>[Tassellatura](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)</span><span class="sxs-lookup"><span data-stu-id="788e7-113"><span id="Tessellation"></span><span id="tessellation"></span><span id="TESSELLATION"></span>[Tessellation](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)</span></span><br/>                                        | <span data-ttu-id="788e7-114">Il runtime di Direct3D 11 supporta tre nuove fasi che implementano lo schema a mosaico, che converte le aree di sottodivisione con dettagli più bassi in primitive di dettaglio nella GPU.</span><span class="sxs-lookup"><span data-stu-id="788e7-114">The Direct3D 11 runtime supports three new stages that implement tessellation, which converts low-detail subdivision surfaces into higher-detail primitives on the GPU.</span></span> <span data-ttu-id="788e7-115">Tessere a mosaico (o suddividere) superfici di ordine superiore in strutture appropriate per il rendering.</span><span class="sxs-lookup"><span data-stu-id="788e7-115">Tessellation tiles (or breaks up) high-order surfaces into suitable structures for rendering.</span></span> <span data-ttu-id="788e7-116">Le tre fasi a mosaico sono le fasi Hull-shader, mosaico e Domain-shader.</span><span class="sxs-lookup"><span data-stu-id="788e7-116">The three tessellation stages are hull-shader, tessellator, and domain-shader stages.</span></span><br/> |



 

<span data-ttu-id="788e7-117">Inoltre, la sezione di riferimento copre molti nuovi elementi API per il modello di shader 5, tra cui: [attributi](d3d11-graphics-reference-sm5-attributes.md), [funzioni intrinseche](d3d11-graphics-reference-sm5-intrinsics.md), [oggetti e metodi dello shader model 5](d3d11-graphics-reference-sm5-objects.md)e [valori di sistema](d3d11-graphics-reference-sm5-system-values.md).</span><span class="sxs-lookup"><span data-stu-id="788e7-117">In addition, the reference section covers many new API elements for shader model 5 including: [attributes](d3d11-graphics-reference-sm5-attributes.md), [intrinsic functions](d3d11-graphics-reference-sm5-intrinsics.md), [shader model 5 objects and methods](d3d11-graphics-reference-sm5-objects.md), and [system values](d3d11-graphics-reference-sm5-system-values.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="788e7-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="788e7-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="788e7-119">Guida alla programmazione per HLSL</span><span class="sxs-lookup"><span data-stu-id="788e7-119">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

