---
description: Data una scena che contiene molti oggetti che usano la stessa geometria, è possibile creare molte istanze di tale geometria con diversi orientamenti, dimensioni, colori e così via con prestazioni notevolmente migliori riducendo la quantità di dati che è necessario fornire al renderer.
ms.assetid: d8d9b0c8-b1c4-406d-bf2a-9716d725aec7
title: Creazione efficiente di più istanze di Geometry (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9981dff913b704fca5e6b211b57e3647fddd28c2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876201"
---
# <a name="efficiently-drawing-multiple-instances-of-geometry-direct3d-9"></a><span data-ttu-id="0d1a4-103">Creazione efficiente di più istanze di Geometry (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0d1a4-103">Efficiently Drawing Multiple Instances of Geometry (Direct3D 9)</span></span>

<span data-ttu-id="0d1a4-104">Data una scena che contiene molti oggetti che usano la stessa geometria, è possibile creare molte istanze di tale geometria con diversi orientamenti, dimensioni, colori e così via con prestazioni notevolmente migliori riducendo la quantità di dati che è necessario fornire al renderer.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-104">Given a scene that contains many objects that use the same geometry, you can draw many instances of that geometry at different orientations, sizes, colors, and so on with dramatically better performance by reducing the amount of data you need to supply to the renderer.</span></span>

<span data-ttu-id="0d1a4-105">Questa operazione può essere eseguita tramite l'utilizzo di due tecniche: la prima per il disegno della geometria indicizzata e la seconda per la geometria non indicizzata.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-105">This can be accomplished through the use of two techniques: the first for drawing indexed geometry and the second for non-indexed geometry.</span></span> <span data-ttu-id="0d1a4-106">Entrambe le tecniche usano due buffer vertex: uno per fornire i dati geometrici e uno per fornire i dati dell'istanza per oggetto.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-106">Both techniques use two vertex buffers: one to supply geometry data and one to supply per-object instance data.</span></span> <span data-ttu-id="0d1a4-107">I dati dell'istanza possono essere un'ampia gamma di informazioni, ad esempio una trasformazione, i dati dei colori o i dati di illuminazione, ovvero qualsiasi elemento che è possibile descrivere in una dichiarazione di vertice.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-107">The instance data can be a wide variety of information such as a transform, color data, or lighting data - basically anything that you can describe in a vertex declaration.</span></span> <span data-ttu-id="0d1a4-108">Il disegno di molte istanze di Geometry con queste tecniche può ridurre notevolmente la quantità di dati inviati al renderer.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-108">Drawing many instances of geometry with these techniques can dramatically reduce the amount of data sent to the renderer.</span></span>

-   [<span data-ttu-id="0d1a4-109">Disegno della geometria indicizzata</span><span class="sxs-lookup"><span data-stu-id="0d1a4-109">Drawing Indexed Geometry</span></span>](#drawing-indexed-geometry)
    -   [<span data-ttu-id="0d1a4-110">Confronto delle prestazioni della geometria indicizzata</span><span class="sxs-lookup"><span data-stu-id="0d1a4-110">Indexed Geometry Performance Comparison</span></span>](#indexed-geometry-performance-comparison)
-   [<span data-ttu-id="0d1a4-111">Disegno di una geometria non indicizzata</span><span class="sxs-lookup"><span data-stu-id="0d1a4-111">Drawing Non-Indexed Geometry</span></span>](#drawing-non-indexed-geometry)
    -   [<span data-ttu-id="0d1a4-112">Confronto tra le prestazioni della geometria non indicizzata</span><span class="sxs-lookup"><span data-stu-id="0d1a4-112">Non-Indexed Geometry Performance Comparison</span></span>](#non-indexed-geometry-performance-comparison)
-   [<span data-ttu-id="0d1a4-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0d1a4-113">Related topics</span></span>](#related-topics)

## <a name="drawing-indexed-geometry"></a><span data-ttu-id="0d1a4-114">Disegno della geometria indicizzata</span><span class="sxs-lookup"><span data-stu-id="0d1a4-114">Drawing Indexed Geometry</span></span>

<span data-ttu-id="0d1a4-115">Il buffer vertex contiene dati per vertice definiti da una dichiarazione di vertice.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-115">The vertex buffer contains per-vertex data that is defined by a vertex declaration.</span></span> <span data-ttu-id="0d1a4-116">Si supponga che una parte di ogni vertice includa dati di geometria e che parte di ogni vertice includa dati di istanza per oggetto, come illustrato nel diagramma seguente.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-116">Suppose that part of each vertex contains geometry data, and part of each vertex contains per-object instance data, as shown in the following diagram.</span></span>

![diagramma di un buffer vertex per la geometria indicizzata](images/drawingmultipleinstances.png)

<span data-ttu-id="0d1a4-118">Questa tecnica richiede un dispositivo che supporta il \_ modello di vertex shader da 3 0.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-118">This technique requires a device that supports the 3\_0 vertex shader model.</span></span> <span data-ttu-id="0d1a4-119">Questa tecnica funziona con qualsiasi shader programmabile ma non con la pipeline della funzione fissa.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-119">This technique works with any programmable shader but not with the fixed function pipeline.</span></span>

<span data-ttu-id="0d1a4-120">Per i buffer dei vertici sopra indicati, di seguito sono riportate le dichiarazioni di buffer dei vertici corrispondenti:</span><span class="sxs-lookup"><span data-stu-id="0d1a4-120">For the vertex buffers shown above, here are the corresponding vertex buffer declarations:</span></span>


```
const D3DVERTEXELEMENT9 g_VBDecl_Geometry[] =
{
{0,  0, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0},
{0, 12, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL,   0},
{0, 24, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TANGENT,  0},
{0, 36, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_BINORMAL, 0},
{0, 48, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 0},
D3DDECL_END()
};

const D3DVERTEXELEMENT9 g_VBDecl_InstanceData[] =
{
{1, 0,  D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 1},
{1, 16, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 2},
{1, 32, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 3},
{1, 48, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 4},
{1, 64, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_COLOR,    0},
D3DDECL_END()
};
```



<span data-ttu-id="0d1a4-121">Queste dichiarazioni definiscono due buffer vertici.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-121">These declarations define two vertex buffers.</span></span> <span data-ttu-id="0d1a4-122">La prima dichiarazione (per il flusso 0, indicata dagli zeri nella colonna 1) definisce i dati geometrici che sono costituiti dai dati di coordinate di posizione, normale, tangente, binormale e trama.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-122">The first declaration (for stream 0, indicated by the zeros in column 1) defines the geometry data which consists of: position, normal, tangent, binormal, and texture coordinate data.</span></span>

<span data-ttu-id="0d1a4-123">La seconda dichiarazione (per il flusso 1, indicata da quelli nella colonna 1) definisce i dati dell'istanza per oggetto.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-123">The second declaration (for stream 1, indicated by the ones in column 1) defines the per-object instance data.</span></span> <span data-ttu-id="0d1a4-124">Ogni istanza è definita da numeri a virgola mobile a 4 4 componenti e da un colore a quattro componenti.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-124">Each instance is defined by four four-component floating point numbers, and a four-component color.</span></span> <span data-ttu-id="0d1a4-125">I primi quattro valori possono essere usati per inizializzare una matrice 4x4, il che significa che questi dati saranno dimensionati in modo univoco, posizionati e ruotano ogni istanza della geometria.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-125">The first four values could be used to initialize a 4x4 matrix, which means that this data will uniquely size, position, and rotate each instance of the geometry.</span></span> <span data-ttu-id="0d1a4-126">I primi quattro componenti usano una semantica delle coordinate di trama che, in questo caso, significa "questo è un numero generale di quattro componenti".</span><span class="sxs-lookup"><span data-stu-id="0d1a4-126">The first four components use a texture coordinate semantic which, in this case, means "this is a general four-component number."</span></span> <span data-ttu-id="0d1a4-127">Quando si usano dati arbitrari in una dichiarazione di vertice, usare una semantica delle coordinate di trama per contrassegnarla.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-127">When you use arbitrary data in a vertex declaration, use a texture coordinate semantic to mark it.</span></span> <span data-ttu-id="0d1a4-128">L'ultimo elemento del flusso viene usato per i dati di colore.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-128">The last element in the stream is used for color data.</span></span> <span data-ttu-id="0d1a4-129">Questo può essere applicato nel vertex shader per assegnare a ogni istanza un colore univoco.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-129">This could be applied in the vertex shader to give each instance a unique color.</span></span>

<span data-ttu-id="0d1a4-130">Prima di eseguire il rendering, è necessario chiamare [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) per associare i flussi del buffer dei vertici al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-130">Before rendering, you need to call [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) to bind the vertex buffer streams to the device.</span></span> <span data-ttu-id="0d1a4-131">Di seguito è riportato un esempio che associa entrambi i buffer dei vertici:</span><span class="sxs-lookup"><span data-stu-id="0d1a4-131">Here is an example that binds both vertex buffers:</span></span>


```
// Set up the geometry data stream
pd3dDevice->SetStreamSourceFreq(0,
    (D3DSTREAMSOURCE_INDEXEDDATA | g_numInstancesToDraw));
pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
    D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

// Set up the instance data stream
pd3dDevice->SetStreamSourceFreq(1,
    (D3DSTREAMSOURCE_INSTANCEDATA | 1));
pd3dDevice->SetStreamSource(1, g_VB_InstanceData, 0, 
    D3DXGetDeclVertexSize( g_VBDecl_InstanceData, 1 ));
```



<span data-ttu-id="0d1a4-132">[**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) utilizza [D3DSTREAMSOURCE \_ INDEXEDDATA](other-direct3d-constants.md) per identificare i dati della geometria indicizzata.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-132">[**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) uses [D3DSTREAMSOURCE\_INDEXEDDATA](other-direct3d-constants.md) to identify the indexed geometry data.</span></span> <span data-ttu-id="0d1a4-133">In questo caso, il flusso 0 contiene i dati indicizzati che descrivono la geometria dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-133">In this case, stream 0 contains the indexed data that describes the object geometry.</span></span> <span data-ttu-id="0d1a4-134">Questo valore viene combinato logicamente con il numero di istanze della geometria da creare.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-134">This value is logically combined with the number of instances of the geometry to draw.</span></span>

<span data-ttu-id="0d1a4-135">Si noti che D3DSTREAMSOURCE \_ INDEXEDDATA e il numero di istanze da creare devono sempre essere impostati nel flusso zero.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-135">Note that D3DSTREAMSOURCE\_INDEXEDDATA and the number of instances to draw must always be set in stream zero.</span></span>

<span data-ttu-id="0d1a4-136">Nella seconda chiamata, [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) utilizza [D3DSTREAMSOURCE \_ INSTANCEDATA](other-direct3d-constants.md) per identificare il flusso contenente i dati dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-136">In the second call, [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) uses [D3DSTREAMSOURCE\_INSTANCEDATA](other-direct3d-constants.md) to identify the stream containing the instance data.</span></span> <span data-ttu-id="0d1a4-137">Questo valore viene combinato logicamente con 1 poiché ogni vertice contiene un set di dati dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-137">This value is logically combined with 1 since each vertex contains one set of instance data.</span></span>

<span data-ttu-id="0d1a4-138">Le ultime due chiamate a [**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) associano i puntatori del buffer del vertice al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-138">The last two calls to [**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) bind the vertex buffer pointers to the device.</span></span>

<span data-ttu-id="0d1a4-139">Al termine del rendering dei dati dell'istanza, assicurarsi di reimpostare la frequenza del flusso dei vertici sullo stato predefinito, che non utilizza le istanze.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-139">When you are finished rendering the instance data, be sure to reset the vertex stream frequency back to its default state (which does not use instancing).</span></span> <span data-ttu-id="0d1a4-140">Poiché in questo esempio sono stati usati due flussi, impostare entrambi i flussi, come illustrato di seguito:</span><span class="sxs-lookup"><span data-stu-id="0d1a4-140">Because this example used two streams, set both streams as shown below:</span></span>


```
pd3dDevice->SetStreamSourceFreq(0,1);
pd3dDevice->SetStreamSourceFreq(1,1);
```



### <a name="indexed-geometry-performance-comparison"></a><span data-ttu-id="0d1a4-141">Confronto delle prestazioni della geometria indicizzata</span><span class="sxs-lookup"><span data-stu-id="0d1a4-141">Indexed Geometry Performance Comparison</span></span>

<span data-ttu-id="0d1a4-142">Sebbene non sia possibile creare una singola conclusione su quanto questa tecnica può ridurre il tempo di rendering in ogni applicazione, considerare la differenza nella quantità di dati trasmessi nel runtime e il numero di modifiche di stato che verranno ridotte se si usa la tecnica di creazione di istanze.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-142">While it is not possible to make a single conclusion about how much this technique could reduce the render time in every application, consider the difference in the amount of data streamed into the runtime and the number of state changes that will be reduced if you use the instancing technique.</span></span> <span data-ttu-id="0d1a4-143">Questa sequenza di rendering sfrutta i vantaggi della creazione di più istanze della stessa geometria:</span><span class="sxs-lookup"><span data-stu-id="0d1a4-143">This render sequence takes advantage of drawing multiple instances of the same geometry:</span></span>


```
if( SUCCEEDED( pd3dDevice->BeginScene() ) )
{
    // Set up the geometry data stream
    pd3dDevice->SetStreamSourceFreq(0,
                (D3DSTREAMSOURCE_INDEXEDDATA | g_numInstancesToDraw));
    pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
                D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

    // Set up the instance data stream
    pd3dDevice->SetStreamSourceFreq(1,
                (D3DSTREAMSOURCE_INSTANCEDATA | 1));
    pd3dDevice->SetStreamSource(1, g_VB_InstanceData, 0, 
                D3DXGetDeclVertexSize( g_VBDecl_InstanceData, 1 ));

    pd3dDevice->SetVertexDeclaration( ... );
    pd3dDevice->SetVertexShader( ... );
    pd3dDevice->SetIndices( ... );

    pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, 0, 0, 
                g_dwNumVertices, 0, g_dwNumIndices/3 );
    
    pd3dDevice->EndScene();
}
```



<span data-ttu-id="0d1a4-144">Si noti che il ciclo di rendering viene chiamato una volta, che i dati di geometria vengono trasmessi una sola volta e n istanze viene trasmesso una volta.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-144">Notice that the render loop is called once, the geometry data is streamed once, and n instances are streamed once.</span></span> <span data-ttu-id="0d1a4-145">Questa successiva sequenza di rendering è identica alla funzionalità, ma non sfrutta le istanze:</span><span class="sxs-lookup"><span data-stu-id="0d1a4-145">This next render sequence is identical in functionality, but does not take advantage of instancing:</span></span>


```
if( SUCCEEDED( pd3dDevice->BeginScene() ) )
{
    for(int i=0; i < g_numObjects; i++)
    {
        pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
                D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));


        pd3dDevice->SetVertexDeclaration( ... );
        pd3dDevice->SetVertexShader( ... );
        pd3dDevice->SetIndices( ... );

        pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, 0, 0, 
                g_dwNumVertices, 0, g_dwNumIndices/3 );
    }                             
    
    pd3dDevice->EndScene();
}
```



<span data-ttu-id="0d1a4-146">Si noti che l'intero ciclo di rendering viene sottoposta a incapsulamento da un secondo ciclo per disegnare ogni oggetto.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-146">Notice that the entire render loop is wrapped by a second loop to draw each object.</span></span> <span data-ttu-id="0d1a4-147">I dati geometrici vengono ora trasmessi nel renderer n volte (anziché una volta) e gli Stati della pipeline possono anche essere impostati in ridondanza per ogni oggetto disegnato.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-147">Now the geometry data is streamed into the renderer n times (instead of once) and any pipeline states may also be set redundantly for each object drawn.</span></span> <span data-ttu-id="0d1a4-148">Questa sequenza di rendering è molto probabile che risulti notevolmente più lenta.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-148">This render sequence is very likely to be significantly slower.</span></span> <span data-ttu-id="0d1a4-149">Si noti inoltre che i parametri di [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) non sono stati modificati tra i due cicli di rendering.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-149">Notice also that the parameters to [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) have not changed between the two render loops.</span></span>

## <a name="drawing-non-indexed-geometry"></a><span data-ttu-id="0d1a4-150">Disegno di una geometria non indicizzata</span><span class="sxs-lookup"><span data-stu-id="0d1a4-150">Drawing Non-Indexed Geometry</span></span>

<span data-ttu-id="0d1a4-151">Nel [disegno della geometria indicizzata](#drawing-indexed-geometry), i buffer dei vertici sono stati configurati per disegnare più istanze della geometria indicizzata con maggiore efficienza.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-151">In [Drawing Indexed Geometry](#drawing-indexed-geometry), vertex buffers were configured to draw multiple instances of indexed geometry with greater efficiency.</span></span> <span data-ttu-id="0d1a4-152">È anche possibile usare [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) per creare una geometria non indicizzata.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-152">You can also use [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) to draw non-indexed geometry.</span></span> <span data-ttu-id="0d1a4-153">Questa operazione richiede un layout di vertex buffer diverso e presenta vincoli diversi.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-153">This requires a different vertex buffer layout and has different constraints.</span></span> <span data-ttu-id="0d1a4-154">Per creare una geometria non indicizzata, preparare i buffer del vertice come illustrato nel diagramma seguente.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-154">To draw non-indexed geometry, prepare your vertex buffers like the following diagram.</span></span>

![diagramma di un buffer vertex per la geometria non indicizzata](images/olderstyleinstancing.png)

<span data-ttu-id="0d1a4-156">Questa tecnica non è supportata dall'accelerazione hardware su qualsiasi dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-156">This technique is not supported by hardware acceleration on any device.</span></span> <span data-ttu-id="0d1a4-157">È supportato solo dall'elaborazione dei vertici software e funziona solo con gli shader [vs \_ 3 \_ 0](../direct3dhlsl/dx9-graphics-reference-asm-vs-3-0.md) .</span><span class="sxs-lookup"><span data-stu-id="0d1a4-157">It is only supported by software vertex processing and will work only with [vs\_3\_0](../direct3dhlsl/dx9-graphics-reference-asm-vs-3-0.md) shaders.</span></span>

<span data-ttu-id="0d1a4-158">Poiché questa tecnica funziona con la geometria non indicizzata, non esiste alcun buffer di indice.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-158">Because this technique works with non-indexed geometry, there is no index buffer.</span></span> <span data-ttu-id="0d1a4-159">Come illustrato nel diagramma, il buffer dei vertici che contiene la geometria contiene n copie dei dati geometrici.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-159">As the diagram shows, the vertex buffer that contains geometry contains n copies of the geometry data.</span></span> <span data-ttu-id="0d1a4-160">Per ogni istanza disegnata, i dati di geometria vengono letti dal primo buffer dei vertici e i dati dell'istanza vengono letti dal secondo buffer del vertice.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-160">For each instance drawn, the geometry data is read from the first vertex buffer and the instance data is read from the second vertex buffer.</span></span>

<span data-ttu-id="0d1a4-161">Di seguito sono riportate le dichiarazioni di buffer vertex corrispondenti:</span><span class="sxs-lookup"><span data-stu-id="0d1a4-161">Here are the corresponding vertex buffer declarations:</span></span>


```
const D3DVERTEXELEMENT9 g_VBDecl_Geometry[] =
{
{0,  0, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0},
{0, 12, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL,   0},
{0, 24, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TANGENT,  0},
{0, 36, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_BINORMAL, 0},
{0, 48, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 0},
D3DDECL_END()
};

const D3DVERTEXELEMENT9 g_VBDecl_InstanceData[] =
{
{1, 0,  D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 1},
{1, 16, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 2},
{1, 32, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 3},
{1, 48, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 4},
{1, 64, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_COLOR,    0},
D3DDECL_END()
};
```



<span data-ttu-id="0d1a4-162">Queste dichiarazioni sono identiche alle dichiarazioni effettuate nell'esempio di geometria indicizzata.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-162">These declarations are identical to the declarations made in the indexed geometry example.</span></span> <span data-ttu-id="0d1a4-163">Ancora una volta, la prima dichiarazione (per il flusso 0) definisce i dati geometrici e la seconda dichiarazione (per il flusso 1) definisce i dati dell'istanza per oggetto.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-163">Once again, the first declaration (for stream 0) defines the geometry data and the second declaration (for stream 1) defines the per-object instance data.</span></span> <span data-ttu-id="0d1a4-164">Quando si crea il primo buffer vertex, assicurarsi di caricarlo con il numero di istanze dei dati geometrici che verranno disegnati.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-164">When you create the first vertex buffer, be sure to load it with the number of instances of the geometry data that you will be drawing.</span></span>

<span data-ttu-id="0d1a4-165">Prima del rendering, è necessario configurare il divisore che indica al runtime come dividere il primo buffer del vertice in n istanze.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-165">Before rendering, you need to set up the divider which tells the runtime how to divide up the first vertex buffer into n instances.</span></span> <span data-ttu-id="0d1a4-166">Impostare quindi il divisore usando [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) come segue:</span><span class="sxs-lookup"><span data-stu-id="0d1a4-166">Then set the divider using [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) like this:</span></span>


```
// Set the divider
pd3dDevice->SetStreamSourceFreq(0, 1);
// Bind the stream to the vertex buffer
pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
        D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

// Set up the instance data stream
pd3dDevice->SetStreamSourceFreq(1, verticesPerInstance);
pd3dDevice->SetStreamSource(1, g_VB_InstanceData, 0, 
        D3DXGetDeclVertexSize( g_VBDecl_InstanceData, 1 ));
```



<span data-ttu-id="0d1a4-167">La prima chiamata a [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) indica che il flusso 0 contiene n istanze di vertici m.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-167">The first call to [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) says that stream 0 contains n instances of m vertices.</span></span> <span data-ttu-id="0d1a4-168">[**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) associa quindi il flusso 0 al buffer del vertice di geometria.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-168">[**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) then binds stream 0 to the geometry vertex buffer.</span></span>

<span data-ttu-id="0d1a4-169">Nella seconda chiamata, [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) identifica il flusso 1 come origine dei dati dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-169">In the second call, [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) identifies stream 1 as the source of the instance data.</span></span> <span data-ttu-id="0d1a4-170">Il secondo parametro è il numero di vertici in ogni oggetto (m).</span><span class="sxs-lookup"><span data-stu-id="0d1a4-170">The second parameter is the number of vertices in each object (m).</span></span> <span data-ttu-id="0d1a4-171">Tenere presente che il flusso di dati dell'istanza deve essere sempre dichiarato come secondo flusso.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-171">Remember that the instance data stream must always be declared as the second stream.</span></span> <span data-ttu-id="0d1a4-172">[**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) quindi associa il flusso 1 al buffer vertex che contiene i dati dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-172">[**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) then binds stream 1 to the vertex buffer that contains the instance data.</span></span>

<span data-ttu-id="0d1a4-173">Al termine del rendering dei dati dell'istanza, assicurarsi di reimpostare la frequenza del flusso dei vertici sullo stato predefinito.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-173">When you are finished rendering the instance data, be sure to reset the vertex stream frequency back to its default state.</span></span> <span data-ttu-id="0d1a4-174">Poiché in questo esempio sono stati usati due flussi, impostare entrambi i flussi, come illustrato di seguito:</span><span class="sxs-lookup"><span data-stu-id="0d1a4-174">Because this example used two streams, set both streams as shown below:</span></span>


```
pd3dDevice->SetStreamSourceFreq(0,1);
pd3dDevice->SetStreamSourceFreq(1,1);
```



### <a name="non-indexed-geometry-performance-comparison"></a><span data-ttu-id="0d1a4-175">Confronto tra le prestazioni della geometria non indicizzata</span><span class="sxs-lookup"><span data-stu-id="0d1a4-175">Non-Indexed Geometry Performance Comparison</span></span>

<span data-ttu-id="0d1a4-176">Il vantaggio principale di questo stile di istanza è che può essere utilizzato su una geometria non indicizzata.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-176">The major advantage of this instancing style is that it can be used on non-indexed geometry.</span></span> <span data-ttu-id="0d1a4-177">Sebbene non sia possibile creare una singola conclusione su quanto questa tecnica può ridurre il tempo di rendering in ogni applicazione, considerare la differenza nella quantità di dati trasmessi nel runtime e il numero di modifiche di stato che verranno ridotte per la sequenza di rendering seguente:</span><span class="sxs-lookup"><span data-stu-id="0d1a4-177">While it is not possible to make a single conclusion about how much this technique could reduce the render time in every application, consider the difference in the amount of data streamed into the runtime, and the number of state changes that will be reduced for the following render sequence:</span></span>


```
if( SUCCEEDED( pd3dDevice->BeginScene() ) )
{
    // Set the divider
    pd3dDevice->SetStreamSourceFreq(0, 1);
    pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
                D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

    // Set up the instance data stream
    pd3dDevice->SetStreamSourceFreq(1, verticesPerInstance));
    pd3dDevice->SetStreamSource(1, g_VB_InstanceData, 0, 
                D3DXGetDeclVertexSize( g_VBDecl_InstanceData, 1 ));

    pd3dDevice->SetVertexDeclaration( ... );
    pd3dDevice->SetVertexShader( ... );
    pd3dDevice->SetIndices( ... );

    pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, 0, 0, 
                g_dwNumVertices, 0, g_dwNumIndices/3 );
    
    pd3dDevice->EndScene();
}
```



<span data-ttu-id="0d1a4-178">Si noti che il ciclo di rendering viene chiamato una volta.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-178">Notice that the render loop is called once.</span></span> <span data-ttu-id="0d1a4-179">Il flusso dei dati di geometria viene eseguito una sola volta, anche se sono presenti n istanze della geometria da trasmettere.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-179">The geometry data is streamed once although there are n instances of the geometry being streamed.</span></span> <span data-ttu-id="0d1a4-180">Il flusso dei dati dal buffer del vertice dell'istanza viene eseguito una sola volta.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-180">The data from the instance vertex buffer is streamed once.</span></span> <span data-ttu-id="0d1a4-181">Questa successiva sequenza di rendering è identica alla funzionalità, ma non sfrutta le istanze:</span><span class="sxs-lookup"><span data-stu-id="0d1a4-181">This next render sequence is identical in functionality, but does not take advantage of instancing:</span></span>


```
if( SUCCEEDED( pd3dDevice->BeginScene() ) )
{
    for(int i=0; i < g_numObjects; i++)
    {
        pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
                D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

        pd3dDevice->SetVertexDeclaration( ... );
        pd3dDevice->SetVertexShader( ... );
        pd3dDevice->SetIndices( ... );

        pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, 0, 0, 
                g_dwNumVertices, 0, g_dwNumIndices/3 );
    }
    
    pd3dDevice->EndScene();
}
```



<span data-ttu-id="0d1a4-182">Senza istanze, il ciclo di rendering deve essere sottoposta a incapsulamento da un secondo ciclo per disegnare ogni oggetto.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-182">Without instancing, the render loop needs to be wrapped by a second loop to draw each object.</span></span> <span data-ttu-id="0d1a4-183">Eliminando il secondo ciclo di rendering, è necessario prevedere prestazioni migliori a causa di un minor numero di modifiche allo stato di rendering chiamate all'interno del ciclo.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-183">By eliminating the second render loop, you should expect better performance due to fewer render state changes that are called inside the loop.</span></span>

<span data-ttu-id="0d1a4-184">Nel complesso, è ragionevole aspettarsi che la tecnica indicizzata ([disegno della geometria indicizzata](#drawing-indexed-geometry)) risulti migliore rispetto alla tecnica non indicizzata ([disegno di una geometria non indicizzata](#drawing-non-indexed-geometry)) perché la tecnica indicizzata trasmette solo una copia dei dati geometrici.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-184">Overall, it is reasonable to expect the indexed technique ([Drawing Indexed Geometry](#drawing-indexed-geometry)) to perform better than the non-indexed technique ([Drawing Non-Indexed Geometry](#drawing-non-indexed-geometry)) because the indexed technique only streams one copy of the geometry data.</span></span> <span data-ttu-id="0d1a4-185">Si noti che i parametri di [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) non sono stati modificati per nessuna delle sequenze di rendering.</span><span class="sxs-lookup"><span data-stu-id="0d1a4-185">Notice that the parameters to [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) have not changed for any of the render sequences.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0d1a4-186">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0d1a4-186">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d1a4-187">Argomenti avanzati</span><span class="sxs-lookup"><span data-stu-id="0d1a4-187">Advanced Topics</span></span>](advanced-topics.md)
</dt> <dt>

<span data-ttu-id="0d1a4-188">[Esempio di istanze](https://msdn.microsoft.com/library/Ee418269(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="0d1a4-188">[Instancing Sample](https://msdn.microsoft.com/library/Ee418269(v=VS.85).aspx)</span></span>
</dt> </dl>

 

 
