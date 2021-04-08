---
description: Le interfacce di rendering per Direct3D sono costituite da metodi che consentono di eseguire il rendering di primitive dai dati dei vertici archiviati in uno o più buffer di dati.
ms.assetid: e89eae14-f480-470c-b301-f7ff316ad339
title: Flussi di dati dei vertici (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efd45fc3f645de49060cd201a6a6e9e238712338
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746103"
---
# <a name="vertex-data-streams-direct3d-9"></a><span data-ttu-id="ec5ba-103">Flussi di dati dei vertici (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="ec5ba-103">Vertex Data Streams (Direct3D 9)</span></span>

<span data-ttu-id="ec5ba-104">Le interfacce di rendering per Direct3D sono costituite da metodi che consentono di eseguire il rendering di primitive dai dati dei vertici archiviati in uno o più buffer di dati.</span><span class="sxs-lookup"><span data-stu-id="ec5ba-104">The rendering interfaces for Direct3D consist of methods that render primitives from vertex data stored in one or more data buffers.</span></span> <span data-ttu-id="ec5ba-105">I dati dei vertici sono costituiti da elementi Vertex combinati per formare componenti del vertice.</span><span class="sxs-lookup"><span data-stu-id="ec5ba-105">Vertex data consists of vertex elements combined to form vertex components.</span></span> <span data-ttu-id="ec5ba-106">Gli elementi vertice, ovvero l'unità più piccola di un vertice, rappresentano entità quali la posizione, il normale o il colore.</span><span class="sxs-lookup"><span data-stu-id="ec5ba-106">Vertex elements, the smallest unit of a vertex, represent entities such as position, normal, or color.</span></span>

<span data-ttu-id="ec5ba-107">I componenti Vertex sono uno o più elementi Vertex archiviati in modo contiguo (interfoliazione per vertice) in un singolo buffer di memoria.</span><span class="sxs-lookup"><span data-stu-id="ec5ba-107">Vertex components are one or more vertex elements stored contiguously (interleaved per vertex) in a single memory buffer.</span></span> <span data-ttu-id="ec5ba-108">Un vertice completo è costituito da uno o più componenti, in cui ogni componente si trova in un buffer di memoria separato.</span><span class="sxs-lookup"><span data-stu-id="ec5ba-108">A complete vertex consists of one or more components, where each component is in a separate memory buffer.</span></span> <span data-ttu-id="ec5ba-109">Per eseguire il rendering di una primitiva, vengono letti e assemblati più componenti del vertice in modo che i vertici completi siano disponibili per l'elaborazione del vertice.</span><span class="sxs-lookup"><span data-stu-id="ec5ba-109">To render a primitive, multiple vertex components are read and assembled so that complete vertices are available for vertex processing.</span></span> <span data-ttu-id="ec5ba-110">Il diagramma seguente illustra il processo di rendering delle primitive usando i componenti dei vertici.</span><span class="sxs-lookup"><span data-stu-id="ec5ba-110">The following diagram shows the process of rendering primitives using vertex components.</span></span>

![diagramma del processo per il rendering delle primitive usando i componenti dei vertici](images/vertexdata.png)

<span data-ttu-id="ec5ba-112">Il rendering delle primitive è costituito da due passaggi.</span><span class="sxs-lookup"><span data-stu-id="ec5ba-112">Rendering primitives consists of two steps.</span></span> <span data-ttu-id="ec5ba-113">Per prima cosa, configurare uno o più flussi del componente vertex; in secondo luogo, richiamare un metodo [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) per eseguire il rendering da tali flussi.</span><span class="sxs-lookup"><span data-stu-id="ec5ba-113">First, set up one or more vertex component streams; second, invoke a [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) method to render from those streams.</span></span> <span data-ttu-id="ec5ba-114">L'identificazione di elementi Vertex all'interno di questi flussi di componenti è specificata dal vertex shader.</span><span class="sxs-lookup"><span data-stu-id="ec5ba-114">Identification of vertex elements within these component streams is specified by the vertex shader.</span></span>

<span data-ttu-id="ec5ba-115">I metodi [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) specificano un offset nei flussi di dati dei vertici, in modo che sia possibile eseguire il rendering di un subset arbitrario contiguo delle primitive all'interno di un set di dati dei vertici a ogni chiamata di disegna.</span><span class="sxs-lookup"><span data-stu-id="ec5ba-115">The [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) methods specify an offset in the vertex data streams so that an arbitrary contiguous subset of the primitives within one set of vertex data can be rendered with each draw invocation.</span></span> <span data-ttu-id="ec5ba-116">In questo modo è possibile modificare lo stato di rendering del dispositivo tra gruppi di primitivi di cui viene eseguito il rendering dagli stessi buffer dei vertici.</span><span class="sxs-lookup"><span data-stu-id="ec5ba-116">This enables you to change the device rendering state between groups of primitives that are rendered from the same vertex buffers.</span></span>

<span data-ttu-id="ec5ba-117">Sono supportati sia i metodi di disegno indicizzati che quelli non indicizzati.</span><span class="sxs-lookup"><span data-stu-id="ec5ba-117">Both indexed and nonindexed drawing methods are supported.</span></span> <span data-ttu-id="ec5ba-118">Per altre informazioni, vedere [rendering da vertex buffer e index buffers (Direct3D 9)](rendering-from-vertex-and-index-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="ec5ba-118">For more information, see [Rendering from Vertex and Index Buffers (Direct3D 9)](rendering-from-vertex-and-index-buffers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ec5ba-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ec5ba-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ec5ba-120">Primitive di rendering</span><span class="sxs-lookup"><span data-stu-id="ec5ba-120">Rendering Primitives</span></span>](rendering-primitives.md)
</dt> </dl>

 

 
