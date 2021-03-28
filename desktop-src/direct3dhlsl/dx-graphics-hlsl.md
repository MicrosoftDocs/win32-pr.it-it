---
title: High-Level Shader Language (HLSL)
description: HLSL è il linguaggio shader di alto livello di tipo C usato con shader programmabili in DirectX.
ms.assetid: 09cdd8d6-0cf5-4f7e-b480-f748d2fa9ca9
ms.topic: article
ms.date: 01/11/2021
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.custom: contperf-fy21q3
ms.openlocfilehash: c0876cda302d4c6215b640c210e880795273cd6c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104981042"
---
# <a name="high-level-shader-language-hlsl"></a><span data-ttu-id="50908-103">High-Level Shader Language (HLSL)</span><span class="sxs-lookup"><span data-stu-id="50908-103">High-level shader language (HLSL)</span></span>

<span data-ttu-id="50908-104">HLSL è il linguaggio shader di alto livello di tipo C usato con shader programmabili in DirectX.</span><span class="sxs-lookup"><span data-stu-id="50908-104">HLSL is the C-like high-level shader language that you use with programmable shaders in DirectX.</span></span>

<span data-ttu-id="50908-105">Ad esempio, è possibile usare HLSL per scrivere un [vertex shader](../direct3d11/vertex-shader-stage.md)o un [pixel shader](../direct3d11/pixel-shader-stage.md)e usare gli shader nell'implementazione del renderer nell'applicazione [Direct3D](../direct3d12/directx-12-programming-guide.md) .</span><span class="sxs-lookup"><span data-stu-id="50908-105">For example, you can use HLSL to write a [vertex shader](../direct3d11/vertex-shader-stage.md), or a [pixel shader](../direct3d11/pixel-shader-stage.md), and use those shaders in the implementation of the renderer in your [Direct3D](../direct3d12/directx-12-programming-guide.md) application.</span></span>

<span data-ttu-id="50908-106">In alternativa, è possibile usare HLSL per scrivere un compute shader, ad esempio per implementare una simulazione fisica.</span><span class="sxs-lookup"><span data-stu-id="50908-106">Or you could use HLSL to write a compute shader, perhaps to implement a physics simulation.</span></span> <span data-ttu-id="50908-107">Tuttavia, se, ad esempio, si è inclini a scrivere un proprio operatore di convoluzione (per l'elaborazione di immagini) come HLSL in un compute shader, si otterranno prestazioni migliori in tale scenario se si usa [Direct Machine Learning (DirectML)](../direct3d12/dml.md) .</span><span class="sxs-lookup"><span data-stu-id="50908-107">However, if for example you're inclined to write your own convolution operator (for image processing) as HLSL in a compute shader, then you'll get better performance in that scenario if you use [Direct Machine Learning (DirectML)](../direct3d12/dml.md) instead.</span></span>

<span data-ttu-id="50908-108">HLSL è stato creato (a partire da DirectX 9) per configurare la [pipeline](../direct3d11/overviews-direct3d-11-graphics-pipeline.md)3D programmabile.</span><span class="sxs-lookup"><span data-stu-id="50908-108">HLSL was created (starting with DirectX 9) to set up the programmable 3D [pipeline](../direct3d11/overviews-direct3d-11-graphics-pipeline.md).</span></span> <span data-ttu-id="50908-109">È possibile programmare l'intera pipeline con le istruzioni HLSL.</span><span class="sxs-lookup"><span data-stu-id="50908-109">You can program the entire pipeline with HLSL instructions.</span></span>

## <a name="where-to-go-next"></a><span data-ttu-id="50908-110">Dove andare avanti</span><span class="sxs-lookup"><span data-stu-id="50908-110">Where to go next</span></span>

* [<span data-ttu-id="50908-111">Guida per programmatori per HLSL</span><span class="sxs-lookup"><span data-stu-id="50908-111">Programming guide for HLSL</span></span>](./dx-graphics-hlsl-pguide.md)
* [<span data-ttu-id="50908-112">Riferimento per HLSL</span><span class="sxs-lookup"><span data-stu-id="50908-112">Reference for HLSL</span></span>](./dx-graphics-hlsl-reference.md)

### <a name="programming-guide-for-hlsl"></a><span data-ttu-id="50908-113">Guida per programmatori per HLSL</span><span class="sxs-lookup"><span data-stu-id="50908-113">Programming guide for HLSL</span></span>

<span data-ttu-id="50908-114">Per un'introduzione concettuale a HLSL, vedere la [Guida alla programmazione di HLSL](./dx-graphics-hlsl-pguide.md).</span><span class="sxs-lookup"><span data-stu-id="50908-114">For a conceptual introduction to HLSL, see the [Programming guide for HLSL](./dx-graphics-hlsl-pguide.md).</span></span>

<span data-ttu-id="50908-115">Nella Guida alla programmazione vengono illustrati i diversi tipi di fasi dello shader e viene illustrato come creare, compilare, ottimizzare, associare e collegare shader.</span><span class="sxs-lookup"><span data-stu-id="50908-115">The programming guide discusses the different kinds of shader stages, and how to create, compile, optimize, bind, and link shaders.</span></span>

<span data-ttu-id="50908-116">Sono inoltre disponibili panoramiche e note sulla versione per le generazioni successive di versioni del modello shader rilasciate, tornando a HLSL Shader Model 5 (informazioni su).</span><span class="sxs-lookup"><span data-stu-id="50908-116">There you'll also find overviews of, and release notes about, the successive generations of shader model version that have been released, going back as far as HLSL shader model 5.</span></span>

### <a name="reference-for-hlsl"></a><span data-ttu-id="50908-117">Riferimento per HLSL</span><span class="sxs-lookup"><span data-stu-id="50908-117">Reference for HLSL</span></span>

<span data-ttu-id="50908-118">Per la documentazione di riferimento di HLSL, vedere il [riferimento per HLSL](./dx-graphics-hlsl-reference.md).</span><span class="sxs-lookup"><span data-stu-id="50908-118">For HLSL reference documentation, see the [Reference for HLSL](./dx-graphics-hlsl-reference.md).</span></span>

<span data-ttu-id="50908-119">La sezione di riferimento include un elenco completo della sintassi del linguaggio e delle funzioni intrinseche integrate in HLSL per semplificare i requisiti di codifica.</span><span class="sxs-lookup"><span data-stu-id="50908-119">The reference section has a complete listing of the language syntax and of the intrinsic functions that are built into HLSL in order to simplify your coding requirements.</span></span>

<span data-ttu-id="50908-120">È disponibile anche una discussione sui modelli di shader e i profili e il contenuto di riferimento del modello shader che torna a HLSL Shader Model 1.</span><span class="sxs-lookup"><span data-stu-id="50908-120">There also you'll find a discussion of shader models versus profiles, and shader model reference content going back as far as HLSL shader model 1.</span></span> <span data-ttu-id="50908-121">Sono disponibili anche le istruzioni per gli assembly, lo strumento D3DCompiler e informazioni sugli errori e gli avvisi che possono essere restituiti da uno shader.</span><span class="sxs-lookup"><span data-stu-id="50908-121">There's also content covering assembly instructions, the D3DCompiler tool, and info about the errors and warnings that a shader can return.</span></span>