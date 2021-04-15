---
description: 'Questa sezione contiene informazioni sulle interfacce shader seguenti:'
ms.assetid: d8770b45-a05c-4dd8-9fa7-08fb4330d734
title: Interfacce shader (grafica Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 838a65d263533d0b2225515664e21c2d93114495
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483397"
---
# <a name="shader-interfaces-direct3d-10-graphics"></a><span data-ttu-id="aad3f-103">Interfacce shader (grafica Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="aad3f-103">Shader Interfaces (Direct3D 10 Graphics)</span></span>

<span data-ttu-id="aad3f-104">Questa sezione contiene informazioni sulle interfacce shader seguenti:</span><span class="sxs-lookup"><span data-stu-id="aad3f-104">This section contains information about the following shader interfaces:</span></span>

<span data-ttu-id="aad3f-105">Ognuna di queste interfacce shader gestisce uno shader compilato.</span><span class="sxs-lookup"><span data-stu-id="aad3f-105">Each of these shader interfaces manages a compiled shader.</span></span> <span data-ttu-id="aad3f-106">L'interfaccia viene creata quando viene compilato uno shader e viene quindi passata a diverse API che necessitano dell'accesso a uno shader compilato. ad esempio quando si associa uno shader a una fase della pipeline o si recupera una firma dello shader.</span><span class="sxs-lookup"><span data-stu-id="aad3f-106">The interface is created when a shader is compiled, and is then passed to various APIs that need access to a compiled shader; such as when binding a shader to a pipeline stage or getting a shader signature.</span></span>



| <span data-ttu-id="aad3f-107">Interfacce di Pipeline-Stage</span><span class="sxs-lookup"><span data-stu-id="aad3f-107">Pipeline-Stage Interfaces</span></span>                                      | <span data-ttu-id="aad3f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aad3f-108">Description</span></span>                                                                                                                                 |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aad3f-109">**Interfaccia ID3D10GeometryShader**</span><span class="sxs-lookup"><span data-stu-id="aad3f-109">**ID3D10GeometryShader Interface**</span></span>](/windows/win32/api/d3d10/nn-d3d10-id3d10geometryshader) | <span data-ttu-id="aad3f-110">Un geometry shader implementa l'elaborazione per primitiva nella [fase geometry-shader](d3d10-graphics-programming-guide-pipeline-stages.md).</span><span class="sxs-lookup"><span data-stu-id="aad3f-110">A geometry-shader implements per-primitive processing in the [geometry-shader stage](d3d10-graphics-programming-guide-pipeline-stages.md).</span></span> |
| [<span data-ttu-id="aad3f-111">**Interfaccia ID3D10PixelShader**</span><span class="sxs-lookup"><span data-stu-id="aad3f-111">**ID3D10PixelShader Interface**</span></span>](/windows/win32/api/d3d10/nn-d3d10-id3d10pixelshader)       | <span data-ttu-id="aad3f-112">Un pixel shader implementa l'elaborazione per pixel nella [fase pixel shader](d3d10-graphics-programming-guide-pipeline-stages.md).</span><span class="sxs-lookup"><span data-stu-id="aad3f-112">A pixel-shader implements per-pixel processing in the [pixel-shader stage](d3d10-graphics-programming-guide-pipeline-stages.md).</span></span>           |
| [<span data-ttu-id="aad3f-113">**Interfaccia ID3D10VertexShader**</span><span class="sxs-lookup"><span data-stu-id="aad3f-113">**ID3D10VertexShader Interface**</span></span>](/windows/win32/api/d3d10/nn-d3d10-id3d10vertexshader)     | <span data-ttu-id="aad3f-114">Un vertex shader implementa l'elaborazione per vertice nella [fase vertex shader](d3d10-graphics-programming-guide-pipeline-stages.md).</span><span class="sxs-lookup"><span data-stu-id="aad3f-114">A vertex-shader implements per-vertex processing in the [vertex-shader stage](d3d10-graphics-programming-guide-pipeline-stages.md).</span></span>        |



 

<span data-ttu-id="aad3f-115">Shader: le interfacce di Reflection consentono a un'applicazione di ispezionare il contenuto di uno shader in fase di progettazione/creazione.</span><span class="sxs-lookup"><span data-stu-id="aad3f-115">Shader-reflection interfaces allow an application to inspect the contents of a shader at design/author time.</span></span> <span data-ttu-id="aad3f-116">La reflection dello shader non è utile per impostare le variabili in fase di esecuzione perché è un mirror dei dati dello shader e pertanto non supporta alcun metodo per l'impostazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="aad3f-116">Shader reflection is not useful for setting variables at runtime as it is a mirror of the shader data, and therefore supports no methods for setting data.</span></span>



| <span data-ttu-id="aad3f-117">Interfacce di Shader-Reflection</span><span class="sxs-lookup"><span data-stu-id="aad3f-117">Shader-Reflection Interfaces</span></span>                                                                   | <span data-ttu-id="aad3f-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aad3f-118">Description</span></span>                                                                        |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="aad3f-119">**Interfaccia ID3D10ShaderReflection**</span><span class="sxs-lookup"><span data-stu-id="aad3f-119">**ID3D10ShaderReflection Interface**</span></span>](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflection)                             | <span data-ttu-id="aad3f-120">Interfaccia COM per la lettura di informazioni da uno shader compilato in fase di creazione.</span><span class="sxs-lookup"><span data-stu-id="aad3f-120">A COM interface for reading information from a compiled shader at author time.</span></span>     |
| [<span data-ttu-id="aad3f-121">**Interfaccia ID3D10ShaderReflectionConstantBuffer**</span><span class="sxs-lookup"><span data-stu-id="aad3f-121">**ID3D10ShaderReflectionConstantBuffer Interface**</span></span>](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflectionconstantbuffer) | <span data-ttu-id="aad3f-122">Interfaccia di supporto per ottenere un'interfaccia del buffer costante di Reflection shader.</span><span class="sxs-lookup"><span data-stu-id="aad3f-122">A helper interface for getting a shader-reflection constant-buffer interface.</span></span>      |
| [<span data-ttu-id="aad3f-123">**Interfaccia ID3D10ShaderReflectionType**</span><span class="sxs-lookup"><span data-stu-id="aad3f-123">**ID3D10ShaderReflectionType Interface**</span></span>](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflectiontype)                     | <span data-ttu-id="aad3f-124">Interfaccia di supporto per ottenere un'interfaccia shader-reflection-Type.</span><span class="sxs-lookup"><span data-stu-id="aad3f-124">A helper interface for getting a shader-reflection-type interface.</span></span>                 |
| [<span data-ttu-id="aad3f-125">**Interfaccia ID3D10ShaderReflectionVariable**</span><span class="sxs-lookup"><span data-stu-id="aad3f-125">**ID3D10ShaderReflectionVariable Interface**</span></span>](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflectionvariable)             | <span data-ttu-id="aad3f-126">Interfaccia di supporto per ottenere un'interfaccia shader-Reflection-variable.</span><span class="sxs-lookup"><span data-stu-id="aad3f-126">A helper interface for getting a shader-reflection-variable interface.</span></span>             |
| [<span data-ttu-id="aad3f-127">**Interfaccia ID3D10ShaderResourceView**</span><span class="sxs-lookup"><span data-stu-id="aad3f-127">**ID3D10ShaderResourceView Interface**</span></span>](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)                         | <span data-ttu-id="aad3f-128">Interfaccia di Reflection shader per la lettura di informazioni da una visualizzazione risorse shader.</span><span class="sxs-lookup"><span data-stu-id="aad3f-128">A shader-reflection interface for reading information from a shader-resource view.</span></span> |



 

<span data-ttu-id="aad3f-129">Le API di Reflection dello shader implementano un'interfaccia di Reflection COM shader ([**interfaccia ID3D10ShaderReflection**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflection)) e diverse interfacce Helper non com (il resto delle interfacce).</span><span class="sxs-lookup"><span data-stu-id="aad3f-129">Shader reflection APIs implement one COM shader reflection interface ([**ID3D10ShaderReflection Interface**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflection)) and several non-COM helper interfaces (the rest of the interfaces).</span></span> <span data-ttu-id="aad3f-130">L' **interfaccia ID3D10ShaderReflection** viene creata quando viene creato un oggetto di Reflection dello shader.</span><span class="sxs-lookup"><span data-stu-id="aad3f-130">**ID3D10ShaderReflection Interface** is created when a shader reflection object is created.</span></span> <span data-ttu-id="aad3f-131">Segue le regole COM standard; la creazione dell'interfaccia aumenta un conteggio dei riferimenti e l'interfaccia deve essere rilasciata quando non è più necessaria.</span><span class="sxs-lookup"><span data-stu-id="aad3f-131">It follows standard COM rules; creating the interface increases a reference count and the interface must be released when it is no longer needed.</span></span> <span data-ttu-id="aad3f-132">Le interfacce di Reflection shader rimanenti sono interfacce helper che non ereditano da IUnknown.</span><span class="sxs-lookup"><span data-stu-id="aad3f-132">The remaining shader-reflection interfaces are helper interfaces that do not inherit from IUnknown.</span></span> <span data-ttu-id="aad3f-133">Ciò significa che non modificano il conteggio dei riferimenti quando vengono creati e non è necessario eliminarli definitivamente al termine dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="aad3f-133">This means that they do not change any reference count when they are created, and they do not need to be destroyed when you are finished with them.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aad3f-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="aad3f-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aad3f-135">Riferimento shader</span><span class="sxs-lookup"><span data-stu-id="aad3f-135">Shader Reference</span></span>](d3d10-graphics-reference-d3d10-shader.md)
</dt> </dl>

 

 
