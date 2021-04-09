---
description: I metodi di disegno indicizzati e non indicizzati sono supportati da Direct3D.
ms.assetid: 9b94ab86-2a6a-4abd-ab56-95315f473226
title: Rendering dai buffer di Vertex e index (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbc42da3f25787d42b0bdccdd808013f51bfa3e4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876189"
---
# <a name="rendering-from-vertex-and-index-buffers-direct3d-9"></a><span data-ttu-id="2f021-103">Rendering dai buffer di Vertex e index (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2f021-103">Rendering from Vertex and Index Buffers (Direct3D 9)</span></span>

<span data-ttu-id="2f021-104">I metodi di disegno indicizzati e non indicizzati sono supportati da Direct3D.</span><span class="sxs-lookup"><span data-stu-id="2f021-104">Both indexed and nonindexed drawing methods are supported by Direct3D.</span></span> <span data-ttu-id="2f021-105">I metodi indicizzati utilizzano un singolo set di indici per tutti i componenti dei vertici.</span><span class="sxs-lookup"><span data-stu-id="2f021-105">The indexed methods use a single set of indices for all vertex components.</span></span> <span data-ttu-id="2f021-106">I dati dei vertici vengono archiviati nei buffer dei vertici e i dati dell'indice vengono archiviati nei buffer di indice.</span><span class="sxs-lookup"><span data-stu-id="2f021-106">Vertex data is stored in vertex buffers, and index data is stored in index buffers.</span></span> <span data-ttu-id="2f021-107">Di seguito sono elencati alcuni scenari comuni per la creazione di primitive mediante i buffer di Vertex e di indice.</span><span class="sxs-lookup"><span data-stu-id="2f021-107">Listed below are a few common scenarios for drawing primitives using vertex and index buffers.</span></span>

<span data-ttu-id="2f021-108">In questi esempi viene confrontato l'uso di [**IDirect3DDevice9::D rawprimitive**](/windows/desktop/api) e [**IDirect3DDevice9::D rawindexedprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive)</span><span class="sxs-lookup"><span data-stu-id="2f021-108">These examples compare the use of [**IDirect3DDevice9::DrawPrimitive**](/windows/desktop/api) and [**IDirect3DDevice9::DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive)</span></span>

## <a name="scenario-1-drawing-two-triangles-without-indexing"></a><span data-ttu-id="2f021-109">Scenario 1: disegno di due triangoli senza indicizzazione</span><span class="sxs-lookup"><span data-stu-id="2f021-109">Scenario 1: Drawing Two Triangles without Indexing</span></span>

<span data-ttu-id="2f021-110">Si immagini di voler creare il quad illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="2f021-110">Let's say you want to draw the quad that is shown in the following illustration.</span></span>

![illustrazione di un quadrato costituito da due triangoli](images/dip-fig1.png)

<span data-ttu-id="2f021-112">Se si usa il tipo primitivo elenco di triangolo per eseguire il rendering dei due triangoli, ogni triangolo verrà archiviato come 3 singoli vertici, ottenendo così un buffer di vertice simile a quello riportato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="2f021-112">If you use the Triangle List primitive type to render the two triangles, each triangle will be stored as 3 individual vertices, resulting in a similar vertex buffer to the following illustration.</span></span>

![diagramma di un buffer vertex che definisce tre vertici per due triangoli](images/dip-fig2.png)

<span data-ttu-id="2f021-114">La chiamata di disegno è molto semplice; a partire dalla posizione 0 all'interno del buffer dei vertici, creare due triangoli.</span><span class="sxs-lookup"><span data-stu-id="2f021-114">The drawing call is very straightforward; starting at location 0 within the vertex buffer, draw two triangles.</span></span> <span data-ttu-id="2f021-115">Se l'eliminazione è abilitata, l'ordine dei vertici sarà importante.</span><span class="sxs-lookup"><span data-stu-id="2f021-115">If culling is enabled, the order of the vertices will be important.</span></span> <span data-ttu-id="2f021-116">Questo esempio presuppone lo stato di eliminazione in senso antiorario predefinito, quindi i triangoli visibili devono essere disegnati in ordine orario.</span><span class="sxs-lookup"><span data-stu-id="2f021-116">This example assumes the default counter-clockwise culling state, so visible triangles must be drawn in clockwise order.</span></span> <span data-ttu-id="2f021-117">Il tipo primitivo dell'elenco di triangolo legge solo tre vertici in ordine lineare dal buffer per ogni triangolo, quindi questa chiamata trarrà triangoli (0, 1, 2) e (3, 4, 5):</span><span class="sxs-lookup"><span data-stu-id="2f021-117">The Triangle List primitive type simply reads three vertices in linear order from the buffer for each triangle, so this call will draw triangles (0, 1, 2) and (3, 4, 5):</span></span>


```
DrawPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
               0,                  // StartVertex
               2 );                // PrimitiveCount
```



## <a name="scenario-2-drawing-two-triangles-with-indexing"></a><span data-ttu-id="2f021-118">Scenario 2: disegno di due triangoli con indicizzazione</span><span class="sxs-lookup"><span data-stu-id="2f021-118">Scenario 2: Drawing Two Triangles with Indexing</span></span>

<span data-ttu-id="2f021-119">Come si noterà, il buffer dei vertici contiene dati duplicati in posizioni 0 e 4, 2 e 5.</span><span class="sxs-lookup"><span data-stu-id="2f021-119">As you'll notice, the vertex buffer contains duplicate data in locations 0 and 4, 2 and 5.</span></span> <span data-ttu-id="2f021-120">Questo ha senso perché i due triangoli condividono due vertici comuni.</span><span class="sxs-lookup"><span data-stu-id="2f021-120">That makes sense because the two triangles share two common vertices.</span></span> <span data-ttu-id="2f021-121">Questi dati duplicati sono inutili e il buffer dei vertici può essere compresso usando un buffer di indice.</span><span class="sxs-lookup"><span data-stu-id="2f021-121">This duplicate data is wasteful, and the vertex buffer can be compressed by using an index buffer.</span></span> <span data-ttu-id="2f021-122">Un buffer di vertice più piccolo riduce la quantità di dati dei vertici da inviare alla scheda grafica.</span><span class="sxs-lookup"><span data-stu-id="2f021-122">A smaller vertex buffer reduces the amount of vertex data that has to be sent to the graphics adapter.</span></span> <span data-ttu-id="2f021-123">Ancora più importante, l'uso di un buffer di indice consente all'adapter di archiviare i vertici in una cache dei vertici; Se la primitiva disegnata contiene un vertice usato di recente, è possibile recuperare tale vertice dalla cache anziché leggerlo dal buffer dei vertici, il che comporta un notevole aumento delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="2f021-123">Even more importantly, using an index buffer allows the adapter to store vertices in a vertex cache; if the primitive being drawn contains a recently-used vertex, that vertex can be fetched from the cache instead of reading it from the vertex buffer, which results in a big performance increase.</span></span>

<span data-ttu-id="2f021-124">Un buffer di indice ' Indexes ' nel buffer dei vertici, in modo che ogni vertice univoco debba essere archiviato una sola volta nel buffer dei vertici.</span><span class="sxs-lookup"><span data-stu-id="2f021-124">An index buffer 'indexes' into the vertex buffer so each unique vertex needs to be stored only once in the vertex buffer.</span></span> <span data-ttu-id="2f021-125">Il diagramma seguente illustra un approccio indicizzato allo scenario di disegno precedente.</span><span class="sxs-lookup"><span data-stu-id="2f021-125">The following diagram shows an indexed approach to the earlier drawing scenario.</span></span>

![diagramma di un buffer di indice per il buffer vertex precedente](images/dip-fig3.png)

<span data-ttu-id="2f021-127">Il buffer index archivia i valori di indice VB, che fanno riferimento a un vertice specifico all'interno del buffer del vertice.</span><span class="sxs-lookup"><span data-stu-id="2f021-127">The index buffer stores VB Index values, which reference a particular vertex within the vertex buffer.</span></span> <span data-ttu-id="2f021-128">Un buffer vertex può essere considerato come una matrice di vertici, quindi l'indice VB è semplicemente l'indice nel buffer dei vertici per il vertice di destinazione.</span><span class="sxs-lookup"><span data-stu-id="2f021-128">A vertex buffer can be thought of as an array of vertices, so the VB Index is simply the index into the vertex buffer for the target vertex.</span></span> <span data-ttu-id="2f021-129">Analogamente, un indice IB è un indice nel buffer di indice.</span><span class="sxs-lookup"><span data-stu-id="2f021-129">Similarly, an IB Index is an index into the index buffer.</span></span> <span data-ttu-id="2f021-130">Questa operazione può risultare molto confusa molto rapidamente se non si è attenti, quindi assicurarsi di essere in grado di usare il vocabolario: Indice dei valori di indice VB nel buffer dei vertici, indice dei valori di indice IB nel buffer di indice e il buffer di indice stesso archivia i valori di indice VB.</span><span class="sxs-lookup"><span data-stu-id="2f021-130">This can get very confusing very quickly if you're not careful, so make sure you're clear on the vocabulary being used: VB Index values index into the vertex buffer, IB Index values index into the index buffer, and the index buffer itself stores VB Index values.</span></span>

<span data-ttu-id="2f021-131">La chiamata di disegno è illustrata di seguito.</span><span class="sxs-lookup"><span data-stu-id="2f021-131">The drawing call is shown below.</span></span> <span data-ttu-id="2f021-132">Il significato di tutti gli argomenti viene discusso a lungo per lo scenario di disegno successivo. per il momento, è sufficiente tenere presente che questa chiamata indica a Direct3D di eseguire il rendering di un elenco di triangolo contenente due triangoli, a partire dalla posizione 0 all'interno del buffer dell'indice.</span><span class="sxs-lookup"><span data-stu-id="2f021-132">The meanings of all the arguments are discussed at length for the next drawing scenario; for now, just note that this call is again instructing Direct3D to render a triangle list containing two triangles, starting at location 0 within the index buffer.</span></span> <span data-ttu-id="2f021-133">Questa chiamata attirerà gli stessi due triangoli nello stesso ordine di prima, assicurando un corretto orientamento in senso orario:</span><span class="sxs-lookup"><span data-stu-id="2f021-133">This call will draw the same two triangles in the exact same order as before, ensuring a proper clockwise orientation:</span></span>


```
   
DrawIndexedPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
                    0,                  // BaseVertexIndex
                    0,                  // MinIndex
                    4,                  // NumVertices
                    0,                  // StartIndex
                    2 );                // PrimitiveCount
```



## <a name="scenario-3-drawing-one-triangle-with-indexing"></a><span data-ttu-id="2f021-134">Scenario 3: disegno di un triangolo con indicizzazione</span><span class="sxs-lookup"><span data-stu-id="2f021-134">Scenario 3: Drawing One Triangle with Indexing</span></span>

<span data-ttu-id="2f021-135">Si supponga ora di voler disegnare solo il secondo triangolo, ma si vuole usare lo stesso buffer di vertex buffer e indice usato durante il disegno dell'intero quad, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="2f021-135">Pretend now that you want to draw only the second triangle, but you want to use the same vertex buffer and index buffer that are used when drawing the entire quad, as shown in the following diagram.</span></span>

![diagramma del buffer di indice e del vertex buffer per il secondo triangolo](images/dip-fig4.png)

<span data-ttu-id="2f021-137">Per questa chiamata di disegno, il primo indice IB usato è 3; Questo valore è denominato StartIndex.</span><span class="sxs-lookup"><span data-stu-id="2f021-137">For this drawing call, the first IB Index used is 3; this value is called the StartIndex.</span></span> <span data-ttu-id="2f021-138">L'indice VB più basso utilizzato è 0. Questo valore è denominato MinIndex.</span><span class="sxs-lookup"><span data-stu-id="2f021-138">The lowest VB Index used is 0; this value is called the MinIndex.</span></span> <span data-ttu-id="2f021-139">Sebbene siano necessari solo tre vertici per creare il triangolo, questi tre vertici vengono distribuiti in quattro posizioni adiacenti nel buffer dei vertici; il numero di posizioni all'interno del blocco contiguo della memoria del buffer dei vertici richiesto per la chiamata di disegno è denominato NumVertices e verrà impostato su 4 in questa chiamata.</span><span class="sxs-lookup"><span data-stu-id="2f021-139">Even though only three vertices are required to draw the triangle, those three vertices are spread across four adjacent locations in the vertex buffer; the number of locations within the contiguous block of vertex buffer memory required for the drawing call is called NumVertices, and will be set to 4 in this call.</span></span> <span data-ttu-id="2f021-140">I valori MinIndex e NumVertices sono semplicemente suggerimenti per consentire a Direct3D di ottimizzare l'accesso alla memoria durante l'elaborazione dei vertici software e possono semplicemente essere impostati per includere l'intero buffer di vertex al prezzo delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="2f021-140">The MinIndex and NumVertices values are really just hints to help Direct3D optimize memory access during software vertex processing, and could simply be set to include the entire vertex buffer at the price of performance.</span></span>

<span data-ttu-id="2f021-141">Di seguito è illustrata la chiamata di disegno per il singolo caso di triangolo. il significato dell'argomento BaseVertexIndex verrà illustrato di seguito:</span><span class="sxs-lookup"><span data-stu-id="2f021-141">Here is the drawing call for the single triangle case; the meaning of the BaseVertexIndex argument will be explained next:</span></span>


```
   
DrawIndexedPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
                    0,                  // BaseVertexIndex
                    0,                  // MinIndex
                    4,                  // NumVertices
                    3,                  // StartIndex
                    1 );                // PrimitiveCount
```



## <a name="scenario-4-drawing-one-triangle-with-offset-indexing"></a><span data-ttu-id="2f021-142">Scenario 4: disegno di un triangolo con indicizzazione offset</span><span class="sxs-lookup"><span data-stu-id="2f021-142">Scenario 4: Drawing One Triangle with Offset Indexing</span></span>

<span data-ttu-id="2f021-143">BaseVertexIndex è un valore che viene effettivamente aggiunto a ogni indice VB archiviato nel buffer dell'indice.</span><span class="sxs-lookup"><span data-stu-id="2f021-143">BaseVertexIndex is a value that's effectively added to every VB Index stored in the index buffer.</span></span> <span data-ttu-id="2f021-144">Se, ad esempio, è stato passato un valore di 50 per BaseVertexIndex durante la chiamata precedente, che sarebbe funzionalmente uguale all'uso del buffer di indice nel diagramma seguente per la durata della chiamata DrawIndexedPrimitive:</span><span class="sxs-lookup"><span data-stu-id="2f021-144">For example, if we had passed in a value of 50 for BaseVertexIndex during the previous call, that would functionally be the same as using the index buffer in the following diagram for the duration of the DrawIndexedPrimitive call:</span></span>

![diagramma di un buffer di indice con un valore di 50 per basevertexindex](images/dip-fig5.png)

<span data-ttu-id="2f021-146">Questo valore viene raramente impostato su un valore diverso da 0, ma può essere utile se si desidera separare il buffer dell'indice dal buffer vertex: se quando si compila il buffer di indice per una mesh particolare, la posizione della mesh nel buffer dei vertici non è ancora nota, è possibile semplicemente fingere che i vertici della mesh si trovino all'inizio del buffer dei vertici; Quando si tratta di eseguire la chiamata di progetto, è sufficiente passare la posizione iniziale effettiva come BaseVertexIndex.</span><span class="sxs-lookup"><span data-stu-id="2f021-146">This value is rarely set to anything other than 0, but can be useful if you want to decouple the index buffer from the vertex buffer: If when filling in the index buffer for a particular mesh the location of the mesh within the vertex buffer isn't yet known, you can simply pretend the mesh vertices will be located at the start of the vertex buffer; when it comes time to make the draw call, simply pass the actual starting location as the BaseVertexIndex.</span></span>

<span data-ttu-id="2f021-147">Questa tecnica può essere usata anche quando si disegnano più istanze di una mesh usando un singolo buffer di indice; Se, ad esempio, il buffer dei vertici conteneva due mesh con un ordine di disegno identico ma vertici leggermente diversi (probabilmente diversi colori diffusi o coordinate di trama), entrambe le mesh potevano essere disegnate usando valori diversi per BaseVertexIndex.</span><span class="sxs-lookup"><span data-stu-id="2f021-147">This technique can also be used when drawing multiple instances of a mesh using a single index buffer; for example, if the vertex buffer contained two meshes with identical draw order but slightly different vertices (perhaps different diffuse colors or texture coordinates), both meshes could be drawn by using different values for BaseVertexIndex.</span></span> <span data-ttu-id="2f021-148">Considerando questo concetto, è possibile usare un buffer di indice per creare più istanze di una mesh, ciascuna contenuta in un buffer vertex diverso, semplicemente ciclando il buffer dei vertici attivo e modificando il BaseVertexIndex in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="2f021-148">Taking this concept one step further, you could use one index buffer to draw multiple instances of a mesh, each contained in a different vertex buffer, simply by cycling which vertex buffer is active and adjusting the BaseVertexIndex as needed.</span></span> <span data-ttu-id="2f021-149">Si noti che anche il valore BaseVertexIndex viene aggiunto automaticamente all'argomento MinIndex, che ha senso quando viene visualizzato il modo in cui viene usato:</span><span class="sxs-lookup"><span data-stu-id="2f021-149">Note that the BaseVertexIndex value is also automatically added to the MinIndex argument, which makes sense when you see how it's used:</span></span>

<span data-ttu-id="2f021-150">Si supponga ora di voler creare di nuovo il secondo triangolo del Quad usando lo stesso buffer di indice precedente; Tuttavia, viene usato un buffer vertex diverso in cui il quad si trova in corrispondenza dell'indice VB 50.</span><span class="sxs-lookup"><span data-stu-id="2f021-150">Pretend now that we again want to draw only the second triangle of the quad using the same index buffer as before; however, a different vertex buffer is being used in which the quad is located at VB Index 50.</span></span> <span data-ttu-id="2f021-151">L'ordine relativo dei vertici Quad rimane invariato, ma solo la posizione iniziale all'interno del buffer dei vertici è diversa.</span><span class="sxs-lookup"><span data-stu-id="2f021-151">The relative order of the quad vertices remains unchanged, only the starting location within the vertex buffer is different.</span></span> <span data-ttu-id="2f021-152">Il buffer di indice e il buffer dei vertici avranno un aspetto simile al diagramma seguente.</span><span class="sxs-lookup"><span data-stu-id="2f021-152">The index buffer and vertex buffer would look like the following diagram.</span></span>

![diagramma del buffer di indice e del buffer di vertex con indice VB 50](images/dip-fig6.png)

<span data-ttu-id="2f021-154">Di seguito è indicata la chiamata di progetto appropriata; Si noti che BaseVertexIndex è l'unico valore che è stato modificato rispetto allo scenario precedente:</span><span class="sxs-lookup"><span data-stu-id="2f021-154">Here is the appropriate draw call; note that BaseVertexIndex is the only value which has changed from the previous scenario:</span></span>


```
   
DrawIndexedPrimitive( D3DPT_TRIANGLELIST, // PrimitiveType
                    50,                 // BaseVertexIndex
                    0,                  // MinIndex
                    4,                  // NumVertices
                    3,                  // StartIndex
                    1 );                // PrimitiveCount
```



## <a name="related-topics"></a><span data-ttu-id="2f021-155">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2f021-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f021-156">Primitive di rendering</span><span class="sxs-lookup"><span data-stu-id="2f021-156">Rendering Primitives</span></span>](rendering-primitives.md)
</dt> </dl>

 

 
