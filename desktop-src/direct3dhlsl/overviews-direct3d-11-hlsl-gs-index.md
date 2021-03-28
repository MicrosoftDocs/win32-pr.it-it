---
title: Come indicizzare più flussi di output
description: In Shader Model 5 un geometry shader può supportare fino a 4 flussi distinti. Ciò significa che un singolo shader può restituire un output compreso tra uno e quattro flussi di output, a seconda del numero di flussi dichiarati.
ms.assetid: 2ddde992-6746-4033-9190-bde7d7b14add
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f8564917be9565e862043e370840f8ac7280f174
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044187"
---
# <a name="how-to-index-multiple-output-streams"></a><span data-ttu-id="a9b72-104">Procedura: indicizzare più flussi di output</span><span class="sxs-lookup"><span data-stu-id="a9b72-104">How To: Index Multiple Output Streams</span></span>

<span data-ttu-id="a9b72-105">In Shader Model 5 un geometry shader può supportare fino a 4 flussi distinti.</span><span class="sxs-lookup"><span data-stu-id="a9b72-105">In shader model 5, a geometry shader can support up to 4 separate streams.</span></span> <span data-ttu-id="a9b72-106">Ciò significa che un singolo shader può restituire un output compreso tra uno e quattro flussi di output, a seconda del numero di flussi dichiarati.</span><span class="sxs-lookup"><span data-stu-id="a9b72-106">This means a single shader can output between one and four output streams, depending on the number of streams declared.</span></span>

<span data-ttu-id="a9b72-107">Per indicizzare più flussi di output</span><span class="sxs-lookup"><span data-stu-id="a9b72-107">To index multiple output streams</span></span>

1.  <span data-ttu-id="a9b72-108">Definire un flusso di dati utilizzando un tipo di modello di flusso.</span><span class="sxs-lookup"><span data-stu-id="a9b72-108">Define a data stream using a stream template type.</span></span>

    ```
        inout PointStream<OutVertex1> myStream1, 
    ```

    

2.  <span data-ttu-id="a9b72-109">Definire un secondo flusso di dati utilizzando un tipo di modello di flusso.</span><span class="sxs-lookup"><span data-stu-id="a9b72-109">Define a second data stream using a stream template type.</span></span>

    ```
        inout PointStream<OutVertex2> myStream2 )
    ```

    

3.  <span data-ttu-id="a9b72-110">Inviare i dati a (o entrambi) a flussi usando le funzioni intrinseche degli oggetti di output del flusso (ad esempio, Append o RestartStrip).</span><span class="sxs-lookup"><span data-stu-id="a9b72-110">Output data to either (or both) streams using the stream output object intrinsic functions (such as Append or RestartStrip).</span></span>

    ```
    void MyGS( 
        InVertex verts[2], 
        inout PointStream<OutVertex1> myStream1, 
        inout PointStream<OutVertex2> myStream2 )
    {
        OutVertex1 myVert1 = TransformVertex1( verts[0] );
        OutVertex2 myVert2 = TransformVertex2( verts[1] );
        myStream1.Append( myVert1 );
        myStream2.Append( myVert2 );
    }
    ```

    

<span data-ttu-id="a9b72-111">Quando si usa un singolo flusso di output, è possibile emettere strisce triangolari, strisce o elenchi di punti.</span><span class="sxs-lookup"><span data-stu-id="a9b72-111">When using a single output stream, you can emit triangle strips, line strips, or point lists.</span></span> <span data-ttu-id="a9b72-112">Quando si archiviano le strisce a triangolo e a linee nel buffer di flusso out, queste vengono espanse rispettivamente negli elenchi a triangolo e a linee.</span><span class="sxs-lookup"><span data-stu-id="a9b72-112">When you store triangle and line strips in the stream out buffer, they are expanded to triangle and line lists respectively.</span></span> <span data-ttu-id="a9b72-113">È anche possibile rasterizzare un flusso e non inviarlo a un buffer di memoria.</span><span class="sxs-lookup"><span data-stu-id="a9b72-113">You can also rasterize one stream and not send it to a memory buffer.</span></span>

<span data-ttu-id="a9b72-114">Quando si usano più flussi di output, tutti i flussi devono contenere punti e fino a un flusso di output può essere inviato al rasterizzatore.</span><span class="sxs-lookup"><span data-stu-id="a9b72-114">When using multiple output streams, all streams must contain points, and up to one output stream can be sent to the rasterizer.</span></span> <span data-ttu-id="a9b72-115">Più comunemente, un'applicazione non Rasterizza alcun flusso.</span><span class="sxs-lookup"><span data-stu-id="a9b72-115">More commonly, an application will not rasterize any stream.</span></span>

<span data-ttu-id="a9b72-116">Dopo avere trasmesso i dati a un buffer, è possibile usare tali dati per eseguire il rendering di qualsiasi tipo primitivo, non solo del tipo primitivo usato per riempire il buffer.</span><span class="sxs-lookup"><span data-stu-id="a9b72-116">After you stream data to a buffer, you can use that data to render any primitive type, not just the primitive type that you used to fill the buffer.</span></span>

<span data-ttu-id="a9b72-117">L'output totale dello shader Geometry è limitato a 1024 valori scalari.</span><span class="sxs-lookup"><span data-stu-id="a9b72-117">The total output of the geometry shader is limited to 1024 scalars.</span></span> <span data-ttu-id="a9b72-118">Quando sono presenti più flussi, il numero di scalari viene calcolato dal tipo di flusso più grande moltiplicato per il numero massimo di vertici.</span><span class="sxs-lookup"><span data-stu-id="a9b72-118">When multiple streams exist, the number of scalars is computed from the largest stream type multiplied by the maximum vertex count.</span></span>



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a9b72-119">Differenze tra il modello di Shader 4 e il modello di shader 5:</span><span class="sxs-lookup"><span data-stu-id="a9b72-119">Differences between shader model 4 and shader model 5:</span></span><br/> <span data-ttu-id="a9b72-120">Modello Shader 4:</span><span class="sxs-lookup"><span data-stu-id="a9b72-120">Shader model 4:</span></span><br/>
<ul>
<li><span data-ttu-id="a9b72-121">Il numero massimo di scalari per l'output del flusso è 64.</span><span class="sxs-lookup"><span data-stu-id="a9b72-121">Maximum number of scalars for stream output is 64.</span></span></li>
<li><span data-ttu-id="a9b72-122">La maschera di registro per componente deve corrispondere nell'intervallo di indici.</span><span class="sxs-lookup"><span data-stu-id="a9b72-122">The per-component register mask must match across the index range.</span></span></li>
</ul>
<span data-ttu-id="a9b72-123">Modello Shader 5:</span><span class="sxs-lookup"><span data-stu-id="a9b72-123">Shader model 5:</span></span><br/>
<ul>
<li><span data-ttu-id="a9b72-124">Il numero massimo di scalari per l'output del flusso è 128.</span><span class="sxs-lookup"><span data-stu-id="a9b72-124">Maximum number of scalars for stream output is 128.</span></span></li>
<li><span data-ttu-id="a9b72-125">Non è necessario che la maschera di registro per componente corrisponda nell'intervallo di indici.</span><span class="sxs-lookup"><span data-stu-id="a9b72-125">The per-component register mask does not need to match across the index range.</span></span></li>
<li><span data-ttu-id="a9b72-126">L'indicizzazione dinamica degli output deve essere valida in tutti i flussi.</span><span class="sxs-lookup"><span data-stu-id="a9b72-126">Dynamic indexing of outputs must be legal across all streams.</span></span></li>
<li><span data-ttu-id="a9b72-127">Non è necessario che le modalità di interpolazione corrispondano per i flussi.</span><span class="sxs-lookup"><span data-stu-id="a9b72-127">Interpolation modes do not need to match for the streams.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="a9b72-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a9b72-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9b72-129">Funzionalità di Geometry shader</span><span class="sxs-lookup"><span data-stu-id="a9b72-129">Geometry Shader Features</span></span>](overviews-direct3d-11-hlsl-gs-features.md)
</dt> </dl>

 

 





