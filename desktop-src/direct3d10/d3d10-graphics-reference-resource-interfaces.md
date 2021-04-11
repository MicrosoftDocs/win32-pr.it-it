---
description: 'Direct3D 10 definisce una serie di interfacce per i due tipi di risorse di base: buffer e trame.'
ms.assetid: e53ca7ab-6ca5-4774-8a52-825b10c1a2ce
title: Interfacce di risorse (grafica Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f677130d99ede09cec86cf0d45bc0ec0bc5f9093
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126555"
---
# <a name="resource-interfaces-direct3d-10-graphics"></a><span data-ttu-id="d50a5-103">Interfacce di risorse (grafica Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="d50a5-103">Resource Interfaces (Direct3D 10 Graphics)</span></span>

<span data-ttu-id="d50a5-104">Direct3D 10 definisce una serie di interfacce per i due tipi di risorse di base: [buffer](d3d10-graphics-programming-guide-resources-types.md) e trame.</span><span class="sxs-lookup"><span data-stu-id="d50a5-104">Direct3D 10 defines a number of interfaces for the two basic types of resources: [buffers](d3d10-graphics-programming-guide-resources-types.md) and textures.</span></span>



| <span data-ttu-id="d50a5-105">Interfacce</span><span class="sxs-lookup"><span data-stu-id="d50a5-105">Interfaces</span></span>                                           | <span data-ttu-id="d50a5-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d50a5-106">Description</span></span>                                          |
|------------------------------------------------------|------------------------------------------------------|
| [<span data-ttu-id="d50a5-107">**Interfaccia ID3D10Buffer**</span><span class="sxs-lookup"><span data-stu-id="d50a5-107">**ID3D10Buffer Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)       | <span data-ttu-id="d50a5-108">Accede ai dati del buffer.</span><span class="sxs-lookup"><span data-stu-id="d50a5-108">Accesses buffer data.</span></span>                                |
| [<span data-ttu-id="d50a5-109">**Interfaccia ID3D10Resource**</span><span class="sxs-lookup"><span data-stu-id="d50a5-109">**ID3D10Resource Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)   | <span data-ttu-id="d50a5-110">Classe di base per una risorsa.</span><span class="sxs-lookup"><span data-stu-id="d50a5-110">Base class for a resource.</span></span>                           |
| [<span data-ttu-id="d50a5-111">**Interfaccia ID3D10Texture1D**</span><span class="sxs-lookup"><span data-stu-id="d50a5-111">**ID3D10Texture1D Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture1d) | <span data-ttu-id="d50a5-112">Accede ai dati in una trama 1D o in una matrice di trama 1D.</span><span class="sxs-lookup"><span data-stu-id="d50a5-112">Accesses data in a 1D texture or a 1D texture array.</span></span> |
| [<span data-ttu-id="d50a5-113">**Interfaccia ID3D10Texture2D**</span><span class="sxs-lookup"><span data-stu-id="d50a5-113">**ID3D10Texture2D Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture2d) | <span data-ttu-id="d50a5-114">Accede ai dati in una trama 2D o in una matrice di trame 2D</span><span class="sxs-lookup"><span data-stu-id="d50a5-114">Accesses data in a 2D texture or a 2D texture array</span></span>  |
| [<span data-ttu-id="d50a5-115">**Interfaccia ID3D10Texture3D**</span><span class="sxs-lookup"><span data-stu-id="d50a5-115">**ID3D10Texture3D Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture3d) | <span data-ttu-id="d50a5-116">Accede ai dati in una trama 3D o in una matrice di trama 3D.</span><span class="sxs-lookup"><span data-stu-id="d50a5-116">Accesses data in a 3D texture or a 3D texture array.</span></span> |



 

<span data-ttu-id="d50a5-117">Un'applicazione usa una visualizzazione per associare una risorsa a una [fase della pipeline](d3d10-graphics-programming-guide-pipeline-stages.md).</span><span class="sxs-lookup"><span data-stu-id="d50a5-117">An application uses a view to bind a resource to a [pipeline stage](d3d10-graphics-programming-guide-pipeline-stages.md).</span></span> <span data-ttu-id="d50a5-118">La [visualizzazione](d3d10-graphics-programming-guide-resources-access-views.md) definisce il modo in cui è possibile accedere alla risorsa durante il rendering.</span><span class="sxs-lookup"><span data-stu-id="d50a5-118">The [view](d3d10-graphics-programming-guide-resources-access-views.md) defines how the resource can be accessed during rendering.</span></span> <span data-ttu-id="d50a5-119">L'API contiene queste interfacce di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="d50a5-119">The API contains these view interfaces.</span></span>



| <span data-ttu-id="d50a5-120">Interfacce</span><span class="sxs-lookup"><span data-stu-id="d50a5-120">Interfaces</span></span>                                                               | <span data-ttu-id="d50a5-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d50a5-121">Description</span></span>                                                                                                  |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d50a5-122">**Interfaccia ID3D10DepthStencilView**</span><span class="sxs-lookup"><span data-stu-id="d50a5-122">**ID3D10DepthStencilView Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10depthstencilview)       | <span data-ttu-id="d50a5-123">Accede ai dati in una trama con [stencil di profondità](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md) .</span><span class="sxs-lookup"><span data-stu-id="d50a5-123">Accesses data in a [depth-stencil](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md) texture.</span></span> |
| [<span data-ttu-id="d50a5-124">**Interfaccia ID3D10RenderTargetView**</span><span class="sxs-lookup"><span data-stu-id="d50a5-124">**ID3D10RenderTargetView Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10rendertargetview)       | <span data-ttu-id="d50a5-125">Accede ai dati in una [destinazione di rendering](d3d10-graphics-programming-guide-resources-creating-textures.md).</span><span class="sxs-lookup"><span data-stu-id="d50a5-125">Accesses data in a [render target](d3d10-graphics-programming-guide-resources-creating-textures.md).</span></span>        |
| [<span data-ttu-id="d50a5-126">**Interfaccia ID3D10ShaderResourceView**</span><span class="sxs-lookup"><span data-stu-id="d50a5-126">**ID3D10ShaderResourceView Interface**</span></span>](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)   | <span data-ttu-id="d50a5-127">Accede ai dati in una risorsa shader in Direct3D 10,0.</span><span class="sxs-lookup"><span data-stu-id="d50a5-127">Accesses data in a shader-resource in Direct3D 10.0.</span></span>                                                         |
| [<span data-ttu-id="d50a5-128">**Interfaccia ID3D10ShaderResourceView1**</span><span class="sxs-lookup"><span data-stu-id="d50a5-128">**ID3D10ShaderResourceView1 Interface**</span></span>](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10shaderresourceview1) | <span data-ttu-id="d50a5-129">Accede ai dati in una risorsa shader in Direct3D 10,1.</span><span class="sxs-lookup"><span data-stu-id="d50a5-129">Accesses data in a shader-resource in Direct3D 10.1.</span></span>                                                         |
| [<span data-ttu-id="d50a5-130">**Interfaccia ID3D10View**</span><span class="sxs-lookup"><span data-stu-id="d50a5-130">**ID3D10View Interface**</span></span>](/windows/desktop/api/D3D10/nn-d3d10-id3d10view)                               | <span data-ttu-id="d50a5-131">Classe di base per una vista.</span><span class="sxs-lookup"><span data-stu-id="d50a5-131">Base class for a view.</span></span>                                                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="d50a5-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d50a5-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d50a5-133">Riferimento alla risorsa</span><span class="sxs-lookup"><span data-stu-id="d50a5-133">Resource Reference</span></span>](d3d10-graphics-reference-resource.md)
</dt> </dl>

 

 
