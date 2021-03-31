---
title: Fase Stream-Output
description: Lo scopo della fase di output del flusso è quello di restituire o trasmettere continuamente i dati dei vertici dalla fase geometry-shader (o dalla fase vertex shader se la fase geometry-shader è inattiva) a uno o più buffer in memoria (vedere Introduzione con la fase di Stream-Output).
ms.assetid: f902dc93-9612-481b-a6bd-073e924a4c79
keywords:
- fase output flusso (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0879cde2ba2f1bb3ed9cc6121aaf378cd4af312
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104474684"
---
# <a name="stream-output-stage"></a><span data-ttu-id="a16cd-104">Fase Stream-Output</span><span class="sxs-lookup"><span data-stu-id="a16cd-104">Stream-Output Stage</span></span>

<span data-ttu-id="a16cd-105">Lo scopo della fase di output del flusso è quello di restituire o trasmettere continuamente i dati dei vertici dalla fase geometry-shader (o dalla fase vertex shader se la fase geometry-shader è inattiva) a uno o più buffer in memoria (vedere [Introduzione con la fase di Stream-Output](d3d10-graphics-programming-guide-output-stream-stage-getting-started.md)).</span><span class="sxs-lookup"><span data-stu-id="a16cd-105">The purpose of the stream-output stage is to continuously output (or stream) vertex data from the geometry-shader stage (or the vertex-shader stage if the geometry-shader stage is inactive) to one or more buffers in memory (see [Getting Started with the Stream-Output Stage](d3d10-graphics-programming-guide-output-stream-stage-getting-started.md)).</span></span>

<span data-ttu-id="a16cd-106">La fase di output del flusso (quindi) si trova nella pipeline immediatamente dopo la fase geometry-shader e immediatamente prima della fase di rasterizzazione, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="a16cd-106">The stream-output stage (SO) is located in the pipeline right after the geometry-shader stage and just before the rasterization stage, as shown in the following diagram.</span></span>

![diagramma della posizione della fase di output del flusso nella pipeline](images/d3d10-pipeline-stages-so.png)

<span data-ttu-id="a16cd-108">I dati trasmessi alla memoria possono essere letti nuovamente nella pipeline in un passaggio di rendering successivo oppure possono essere copiati in una risorsa di staging, in modo che possano essere letti dalla CPU.</span><span class="sxs-lookup"><span data-stu-id="a16cd-108">Data streamed out to memory can be read back into the pipeline in a subsequent rendering pass, or can be copied to a staging resource (so it can be read by the CPU).</span></span> <span data-ttu-id="a16cd-109">La quantità di dati trasmessi può variare. l'API [**sul ID3D11DeviceContext::D rawauto**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawauto) è progettata per gestire i dati senza la necessità di eseguire query (GPU) sulla quantità di dati scritti.</span><span class="sxs-lookup"><span data-stu-id="a16cd-109">The amount of data streamed out can vary; the [**ID3D11DeviceContext::DrawAuto**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawauto) API is designed to handle the data without the need to query (the GPU) about the amount of data written.</span></span>

<span data-ttu-id="a16cd-110">Quando una striscia o un triangolo è associato alla fase input-assembler, ogni striscia viene convertita in un elenco prima che vengano trasmessi. I vertici vengono sempre scritti come primitive complete (ad esempio, 3 vertici alla volta per i triangoli); le primitive incomplete non vengono mai trasmesse. I tipi primitivi con adiacenza scartano i dati adiacenza prima di trasmettere i dati in uscita.</span><span class="sxs-lookup"><span data-stu-id="a16cd-110">When a triangle or line strip is bound to the input-assembler stage, each strip is converted into a list before they are streamed out. Vertices are always written out as complete primitives (for example, 3 vertices at a time for triangles); incomplete primitives are never streamed out. Primitive types with adjacency discard the adjacency data before streaming data out.</span></span>

<span data-ttu-id="a16cd-111">Esistono due modi per inserire i dati di output del flusso nella pipeline:</span><span class="sxs-lookup"><span data-stu-id="a16cd-111">There are two ways to feed stream-output data into the pipeline:</span></span>

-   <span data-ttu-id="a16cd-112">Stream: i dati di output possono essere inseriti nella fase input-assembler.</span><span class="sxs-lookup"><span data-stu-id="a16cd-112">Stream-output data can be fed back into the input-assembler stage.</span></span>
-   <span data-ttu-id="a16cd-113">I dati di output di flusso possono essere letti da shader programmabili usando funzioni di caricamento (ad esempio, [Load](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-load)).</span><span class="sxs-lookup"><span data-stu-id="a16cd-113">Stream-output data can be read by programmable shaders using load functions (such as [Load](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-load)).</span></span>

<span data-ttu-id="a16cd-114">Per usare un buffer come risorsa di output del flusso, creare il buffer con il flag di [**\_ output del \_ flusso \_ di binding d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) .</span><span class="sxs-lookup"><span data-stu-id="a16cd-114">To use a buffer as a stream-output resource, create the buffer with the [**D3D11\_BIND\_STREAM\_OUTPUT**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_bind_flag) flag.</span></span> <span data-ttu-id="a16cd-115">La fase Stream-output supporta fino a 4 buffer contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="a16cd-115">The stream-output stage supports up to 4 buffers simultaneously.</span></span>

-   <span data-ttu-id="a16cd-116">Se si esegue il flusso di dati in più buffer, ogni buffer può acquisire solo un singolo elemento (fino a 4 componenti) di dati per vertice, con uno stride di dati implicito uguale alla larghezza dell'elemento in ogni buffer (compatibile con la modalità di associazione dei buffer a singolo elemento per l'input nelle fasi dello shader).</span><span class="sxs-lookup"><span data-stu-id="a16cd-116">If you are streaming data into multiple buffers, each buffer can only capture a single element (up to 4 components) of per-vertex data, with an implied data stride equal to the element width in each buffer (compatible with the way single element buffers can be bound for input into shader stages).</span></span> <span data-ttu-id="a16cd-117">Inoltre, se i buffer hanno dimensioni diverse, la scrittura viene arrestata non appena uno dei buffer è pieno.</span><span class="sxs-lookup"><span data-stu-id="a16cd-117">Furthermore, if the buffers have different sizes, writing stops as soon as any one of the buffers is full.</span></span>
-   <span data-ttu-id="a16cd-118">Se si esegue il flusso di dati in un singolo buffer, il buffer può acquisire fino a 64 componenti scalari di dati per vertice (256 byte o meno) o lo stride del vertice può essere fino a 2048 byte.</span><span class="sxs-lookup"><span data-stu-id="a16cd-118">If you are streaming data into a single buffer, the buffer can capture up to 64 scalar components of per-vertex data (256 bytes or less) or the vertex stride can be up to 2048 bytes.</span></span>


## <a name="in-this-section"></a><span data-ttu-id="a16cd-119">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="a16cd-119">In this section</span></span>



| <span data-ttu-id="a16cd-120">Argomento</span><span class="sxs-lookup"><span data-stu-id="a16cd-120">Topic</span></span>                                                                                                                               | <span data-ttu-id="a16cd-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a16cd-121">Description</span></span>                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a16cd-122">Introduzione con la fase di Stream-Output</span><span class="sxs-lookup"><span data-stu-id="a16cd-122">Getting Started with the Stream-Output Stage</span></span>](d3d10-graphics-programming-guide-output-stream-stage-getting-started.md)<br/> | <span data-ttu-id="a16cd-123">Questa sezione descrive come usare un geometry shader con la fase di output del flusso.</span><span class="sxs-lookup"><span data-stu-id="a16cd-123">This section describes how to use a geometry shader with the stream output stage.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="a16cd-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a16cd-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a16cd-125">Pipeline grafica</span><span class="sxs-lookup"><span data-stu-id="a16cd-125">Graphics Pipeline</span></span>](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[<span data-ttu-id="a16cd-126">Fasi della pipeline (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="a16cd-126">Pipeline Stages (Direct3D 10)</span></span>](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

