---
title: Introduzione con la fase di Input-Assembler
description: Sono necessari alcuni passaggi per inizializzare la fase di input-assembler (IA).
ms.assetid: 84c0ca29-2356-4b7f-98ee-ff1758edc540
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 901b3facfef781e3f44acf75bee737f280dece55
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399267"
---
# <a name="getting-started-with-the-input-assembler-stage"></a><span data-ttu-id="5f453-103">Introduzione con la fase di Input-Assembler</span><span class="sxs-lookup"><span data-stu-id="5f453-103">Getting Started with the Input-Assembler Stage</span></span>

<span data-ttu-id="5f453-104">Sono necessari alcuni passaggi per inizializzare la fase di input-assembler (IA).</span><span class="sxs-lookup"><span data-stu-id="5f453-104">There are a few steps necessary to initialize the input-assembler (IA) stage.</span></span> <span data-ttu-id="5f453-105">Ad esempio, è necessario creare risorse del buffer con i dati dei vertici necessari per la pipeline, indicare la fase IA in cui si trovano i buffer e il tipo di dati che contengono e specificare il tipo di primitive da assemblare dai dati.</span><span class="sxs-lookup"><span data-stu-id="5f453-105">For example, you need to create buffer resources with the vertex data that the pipeline needs, tell the IA stage where the buffers are and what type of data they contain, and specify the type of primitives to assemble from the data.</span></span>

<span data-ttu-id="5f453-106">In questo argomento vengono descritte le procedure di base necessarie per la configurazione della fase IA, illustrata nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="5f453-106">The basic steps involved in setting up the IA stage, shown in the following table, are covered in this topic.</span></span>



| <span data-ttu-id="5f453-107">Passaggio</span><span class="sxs-lookup"><span data-stu-id="5f453-107">Step</span></span>                                                                                    | <span data-ttu-id="5f453-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5f453-108">Description</span></span>                                                                                           |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5f453-109">Creare buffer di input</span><span class="sxs-lookup"><span data-stu-id="5f453-109">Create Input Buffers</span></span>](#create-input-buffers)                                           | <span data-ttu-id="5f453-110">Creare e inizializzare buffer di input con dati dei vertici di input.</span><span class="sxs-lookup"><span data-stu-id="5f453-110">Create and initialize input buffers with input vertex data.</span></span>                                           |
| [<span data-ttu-id="5f453-111">Creare l'oggetto Input-Layout</span><span class="sxs-lookup"><span data-stu-id="5f453-111">Create the Input-Layout Object</span></span>](#create-the-input-layout-object)                       | <span data-ttu-id="5f453-112">Definire il modo in cui i dati del buffer dei vertici verranno trasmessi nella fase IA usando un oggetto di layout di input.</span><span class="sxs-lookup"><span data-stu-id="5f453-112">Define how the vertex buffer data will be streamed into the IA stage by using an input-layout object.</span></span> |
| [<span data-ttu-id="5f453-113">Associare oggetti alla fase Input-Assembler</span><span class="sxs-lookup"><span data-stu-id="5f453-113">Bind Objects to the Input-Assembler Stage</span></span>](#bind-objects-to-the-input-assembler-stage) | <span data-ttu-id="5f453-114">Associare gli oggetti creati (buffer di input e l'oggetto layout di input) alla fase IA.</span><span class="sxs-lookup"><span data-stu-id="5f453-114">Bind the created objects (input buffers and the input-layout object) to the IA stage.</span></span>                 |
| [<span data-ttu-id="5f453-115">Specificare il tipo primitivo</span><span class="sxs-lookup"><span data-stu-id="5f453-115">Specify the Primitive Type</span></span>](#specify-the-primitive-type)                               | <span data-ttu-id="5f453-116">Identificare il modo in cui i vertici verranno assemblati in primitive.</span><span class="sxs-lookup"><span data-stu-id="5f453-116">Identify how the vertices will be assembled into primitives.</span></span>                                          |
| [<span data-ttu-id="5f453-117">Metodi di richiamo della chiamata</span><span class="sxs-lookup"><span data-stu-id="5f453-117">Call Draw Methods</span></span>](#call-draw-methods)                                                 | <span data-ttu-id="5f453-118">Inviare i dati associati alla fase IA tramite la pipeline.</span><span class="sxs-lookup"><span data-stu-id="5f453-118">Send the data bound to the IA stage through the pipeline.</span></span>                                             |



 

<span data-ttu-id="5f453-119">Dopo aver compreso questi passaggi, passare a [utilizzando System-Generated valori](d3d10-graphics-programming-guide-input-assembler-stage-using.md).</span><span class="sxs-lookup"><span data-stu-id="5f453-119">After you understand these steps, move on to [Using System-Generated Values](d3d10-graphics-programming-guide-input-assembler-stage-using.md).</span></span>

## <a name="create-input-buffers"></a><span data-ttu-id="5f453-120">Creare buffer di input</span><span class="sxs-lookup"><span data-stu-id="5f453-120">Create Input Buffers</span></span>

<span data-ttu-id="5f453-121">Sono disponibili due tipi di buffer di input: i buffer dei [vertici](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) e gli indici.</span><span class="sxs-lookup"><span data-stu-id="5f453-121">There are two types of input buffers: [vertex buffers](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types) and index buffers.</span></span> <span data-ttu-id="5f453-122">I buffer vertex forniscono i dati dei vertici alla fase IA.</span><span class="sxs-lookup"><span data-stu-id="5f453-122">Vertex buffers supply vertex data to the IA stage.</span></span> <span data-ttu-id="5f453-123">I buffer di indice sono facoltativi. forniscono indici ai vertici dal buffer dei vertici.</span><span class="sxs-lookup"><span data-stu-id="5f453-123">Index buffers are optional; they provide indices to vertices from the vertex buffer.</span></span> <span data-ttu-id="5f453-124">È possibile creare uno o più buffer vertex e, facoltativamente, un buffer di indice.</span><span class="sxs-lookup"><span data-stu-id="5f453-124">You may create one or more vertex buffers and, optionally, an index buffer.</span></span>

<span data-ttu-id="5f453-125">Dopo aver creato le risorse del buffer, è necessario creare un oggetto di layout di input per descrivere il layout dei dati alla fase IA, quindi è necessario associare le risorse del buffer alla fase IA.</span><span class="sxs-lookup"><span data-stu-id="5f453-125">After you create the buffer resources, you need to create an input-layout object to describe the data layout to the IA stage, and then you need to bind the buffer resources to the IA stage.</span></span> <span data-ttu-id="5f453-126">La creazione e l'associazione dei buffer non sono necessari se gli shader non usano i buffer.</span><span class="sxs-lookup"><span data-stu-id="5f453-126">Creating and binding buffers is not necessary if your shaders don't use buffers.</span></span> <span data-ttu-id="5f453-127">Per un esempio di un vertice semplice e pixel shader che disegna un singolo triangolo, vedere [uso della fase di Input-Assembler senza buffer](d3d10-graphics-programming-guide-input-assembler-stage-no-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="5f453-127">For an example of a simple vertex and pixel shader that draws a single triangle, see [Using the Input-Assembler Stage without Buffers](d3d10-graphics-programming-guide-input-assembler-stage-no-buffers.md).</span></span>

<span data-ttu-id="5f453-128">Per informazioni sulla creazione di un buffer vertex, vedere [creare un buffer vertex](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating).</span><span class="sxs-lookup"><span data-stu-id="5f453-128">For help with creating a vertex buffer, see [Create a Vertex Buffer](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating).</span></span> <span data-ttu-id="5f453-129">Per informazioni sulla creazione di un buffer di indice, vedere creare un buffer di indice.</span><span class="sxs-lookup"><span data-stu-id="5f453-129">For help with creating an index buffer, see Create an Index Buffer.</span></span>

## <a name="create-the-input-layout-object"></a><span data-ttu-id="5f453-130">Creare l'oggetto Input-Layout</span><span class="sxs-lookup"><span data-stu-id="5f453-130">Create the Input-Layout Object</span></span>

<span data-ttu-id="5f453-131">L'oggetto di layout di input incapsula lo stato di input della fase IA.</span><span class="sxs-lookup"><span data-stu-id="5f453-131">The input-layout object encapsulates the input state of the IA stage.</span></span> <span data-ttu-id="5f453-132">Include una descrizione dei dati di input associati alla fase IA.</span><span class="sxs-lookup"><span data-stu-id="5f453-132">This includes a description of the input data that is bound to the IA stage.</span></span> <span data-ttu-id="5f453-133">I dati vengono trasmessi alla fase IA dalla memoria, da uno o più buffer dei vertici.</span><span class="sxs-lookup"><span data-stu-id="5f453-133">The data is streamed into the IA stage from memory, from one or more vertex buffers.</span></span> <span data-ttu-id="5f453-134">La descrizione identifica i dati di input associati da uno o più buffer vertex e consente al runtime di controllare i tipi di dati di input in base ai tipi di parametro di input dello shader.</span><span class="sxs-lookup"><span data-stu-id="5f453-134">The description identifies the input data that is bound from one or more vertex buffers and gives the runtime the ability to check the input data types against the shader input parameter types.</span></span> <span data-ttu-id="5f453-135">Questo controllo del tipo non solo verifica che i tipi siano compatibili, ma anche che ogni elemento richiesto dallo shader sia disponibile nelle risorse del buffer.</span><span class="sxs-lookup"><span data-stu-id="5f453-135">This type checking not only verifies that the types are compatible, but also that each of the elements that the shader requires is available in the buffer resources.</span></span>

<span data-ttu-id="5f453-136">Viene creato un oggetto di layout di input da una matrice di descrizioni di elementi di input e un puntatore allo shader compilato (vedere [**ID3D11Device:: CreateInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout)).</span><span class="sxs-lookup"><span data-stu-id="5f453-136">An input-layout object is created from an array of input-element descriptions and a pointer to the compiled shader (see [**ID3D11Device::CreateInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createinputlayout)).</span></span> <span data-ttu-id="5f453-137">La matrice contiene uno o più elementi di input. ogni elemento di input descrive un singolo elemento di dati vertex da un singolo buffer del vertice.</span><span class="sxs-lookup"><span data-stu-id="5f453-137">The array contains one or more input elements; each input element describes a single vertex-data element from a single vertex buffer.</span></span> <span data-ttu-id="5f453-138">L'intero set di descrizioni degli elementi di input descrive tutti gli elementi dei dati di vertice di tutti i vertex buffer che verranno associati alla fase di assemblaggio dell'input.</span><span class="sxs-lookup"><span data-stu-id="5f453-138">The entire set of input-element descriptions describes all of the vertex-data elements from all of the vertex buffers that will be bound to the IA stage.</span></span>

<span data-ttu-id="5f453-139">Nella descrizione del layout seguente viene descritto un singolo buffer del vertice che contiene tre elementi di dati dei vertici:</span><span class="sxs-lookup"><span data-stu-id="5f453-139">The following layout description describes a single vertex buffer that contains three vertex-data elements:</span></span>


```
D3D11_INPUT_ELEMENT_DESC layout[] =
{
    { L"POSITION", 0, DXGI_FORMAT_R32G32B32_FLOAT, 0, 0, 
          D3D11_INPUT_PER_VERTEX_DATA, 0 },
    { L"TEXCOORD", 0, DXGI_FORMAT_R32G32_FLOAT, 0, 12, 
          D3D11_INPUT_PER_VERTEX_DATA, 0 },
    { L"NORMAL", 0, DXGI_FORMAT_R32G32B32_FLOAT, 0, 20, 
          D3D11_INPUT_PER_VERTEX_DATA, 0 },
};
```



<span data-ttu-id="5f453-140">Una descrizione dell'elemento di input descrive ogni elemento contenuto da un singolo vertice in un buffer del vertice, incluse le dimensioni, il tipo, la posizione e lo scopo.</span><span class="sxs-lookup"><span data-stu-id="5f453-140">An input-element description describes each element contained by a single vertex in a vertex buffer, including size, type, location, and purpose.</span></span> <span data-ttu-id="5f453-141">Ogni riga identifica il tipo di dati utilizzando la semantica, l'indice semantico e il formato dati.</span><span class="sxs-lookup"><span data-stu-id="5f453-141">Each row identifies the type of data by using the semantic, the semantic index, and the data format.</span></span> <span data-ttu-id="5f453-142">Una [semantica](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) è una stringa di testo che consente di identificare la modalità di utilizzo dei dati.</span><span class="sxs-lookup"><span data-stu-id="5f453-142">A [semantic](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics) is a text string that identifies how the data will be used.</span></span> <span data-ttu-id="5f453-143">In questo esempio, la prima riga identifica i dati di posizione a 3 componenti (ad esempio,*XYZ*); la seconda riga identifica i dati di trama a 2 componenti (ad esempio,*UV*); e la terza riga identifica i dati normali.</span><span class="sxs-lookup"><span data-stu-id="5f453-143">In this example, the first row identifies 3-component position data (*xyz*, for example); the second row identifies 2-component texture data (*UV*, for example); and the third row identifies normal data.</span></span>

<span data-ttu-id="5f453-144">In questo esempio di descrizione di un elemento di input, l'indice semantico, ovvero il secondo parametro, viene impostato su zero per tutte e tre le righe.</span><span class="sxs-lookup"><span data-stu-id="5f453-144">In this example of an input-element description, the semantic index (which is the second parameter) is set to zero for all three rows.</span></span> <span data-ttu-id="5f453-145">L'indice semantico consente di distinguere tra due righe che utilizzano la stessa semantica.</span><span class="sxs-lookup"><span data-stu-id="5f453-145">The semantic index helps distinguish between two rows that use the same semantics.</span></span> <span data-ttu-id="5f453-146">Poiché in questo esempio non è presente alcuna semantica simile, l'indice semantico può essere impostato sul valore predefinito, pari a zero.</span><span class="sxs-lookup"><span data-stu-id="5f453-146">Since there are no similar semantics in this example, the semantic index can be set to its default value, zero.</span></span>

<span data-ttu-id="5f453-147">Il terzo parametro è il *formato*.</span><span class="sxs-lookup"><span data-stu-id="5f453-147">The third parameter is the *format*.</span></span> <span data-ttu-id="5f453-148">Il formato (vedere [**DXGI \_ Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)) specifica il numero di componenti per ogni elemento e il tipo di dati, che definisce le dimensioni dei dati per ogni elemento.</span><span class="sxs-lookup"><span data-stu-id="5f453-148">The format (see [**DXGI\_FORMAT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)) specifies the number of components per element, and the data type, which defines the size of the data for each element.</span></span> <span data-ttu-id="5f453-149">Il formato può essere digitato completamente al momento della creazione della risorsa oppure è possibile creare una risorsa usando un **\_ formato DXGI**, che identifica il numero di componenti in un elemento, ma lascia il tipo di dati non definito.</span><span class="sxs-lookup"><span data-stu-id="5f453-149">The format can be fully typed at the time of resource creation, or you may create a resource by using a **DXGI\_FORMAT**, which identifies the number of components in an element, but leaves the data type undefined.</span></span>

### <a name="input-slots"></a><span data-ttu-id="5f453-150">Slot di input</span><span class="sxs-lookup"><span data-stu-id="5f453-150">Input Slots</span></span>

<span data-ttu-id="5f453-151">I dati entrano nella fase IA tramite input detti *slot di input*, come illustrato nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="5f453-151">Data enters the IA stage through inputs called *input slots*, as shown in the following illustration.</span></span> <span data-ttu-id="5f453-152">La fase IA ha *n* slot di input, progettati per ospitare fino a *n* buffer di vertici che forniscono dati di input.</span><span class="sxs-lookup"><span data-stu-id="5f453-152">The IA stage has *n* input slots, which are designed to accommodate up to *n* vertex buffers that provide input data.</span></span> <span data-ttu-id="5f453-153">Ogni buffer dei vertici deve essere assegnato a uno slot diverso; Queste informazioni vengono archiviate nella dichiarazione di layout di input quando viene creato l'oggetto di layout di input.</span><span class="sxs-lookup"><span data-stu-id="5f453-153">Each vertex buffer must be assigned to a different slot; this information is stored in the input-layout declaration when the input-layout object is created.</span></span> <span data-ttu-id="5f453-154">È anche possibile specificare un offset dall'inizio di ogni buffer al primo elemento nel buffer da leggere.</span><span class="sxs-lookup"><span data-stu-id="5f453-154">You may also specify an offset from the start of each buffer to the first element in the buffer to be read.</span></span>

![illustrazione degli slot di input per la fase IA](images/d3d10-ia-slots.png)

<span data-ttu-id="5f453-156">I due parametri successivi sono lo *slot di input* e l' *offset di input*.</span><span class="sxs-lookup"><span data-stu-id="5f453-156">The next two parameters are the *input slot* and the *input offset*.</span></span> <span data-ttu-id="5f453-157">Quando si usano più buffer, è possibile associarli a uno o più slot di input.</span><span class="sxs-lookup"><span data-stu-id="5f453-157">When you use multiple buffers, you can bind them to one or more input slots.</span></span> <span data-ttu-id="5f453-158">L'offset di input è il numero di byte tra l'inizio del buffer e l'inizio dei dati.</span><span class="sxs-lookup"><span data-stu-id="5f453-158">The input offset is the number of bytes between the start of the buffer and the beginning of the data.</span></span>

### <a name="reusing-input-layout-objects"></a><span data-ttu-id="5f453-159">Riutilizzo di oggetti Input-Layout</span><span class="sxs-lookup"><span data-stu-id="5f453-159">Reusing Input-Layout Objects</span></span>

<span data-ttu-id="5f453-160">Ogni oggetto di layout di input viene creato in base a una firma dello shader. Ciò consente all'API di convalidare gli elementi input-layout-Object rispetto alla firma di input shader per assicurarsi che esista una corrispondenza esatta tra tipi e semantica.</span><span class="sxs-lookup"><span data-stu-id="5f453-160">Each input-layout object is created based on a shader signature; this allows the API to validate the input-layout-object elements against the shader-input signature to make sure that there is an exact match of types and semantics.</span></span> <span data-ttu-id="5f453-161">È possibile creare un singolo oggetto layout di input per molti shader, purché tutte le firme di input shader corrispondano esattamente.</span><span class="sxs-lookup"><span data-stu-id="5f453-161">You can create a single input-layout object for many shaders, as long as all of the shader-input signatures exactly match.</span></span>

## <a name="bind-objects-to-the-input-assembler-stage"></a><span data-ttu-id="5f453-162">Associare oggetti alla fase Input-Assembler</span><span class="sxs-lookup"><span data-stu-id="5f453-162">Bind Objects to the Input-Assembler Stage</span></span>

<span data-ttu-id="5f453-163">Dopo aver creato le risorse del buffer dei vertici e un oggetto layout di input, è possibile associarle alla fase IA chiamando [**sul ID3D11DeviceContext:: IASetVertexBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers) e [**sul ID3D11DeviceContext:: IASetInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetinputlayout).</span><span class="sxs-lookup"><span data-stu-id="5f453-163">After you create vertex buffer resources and an input layout object, you can bind them to the IA stage by calling [**ID3D11DeviceContext::IASetVertexBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers) and [**ID3D11DeviceContext::IASetInputLayout**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetinputlayout).</span></span> <span data-ttu-id="5f453-164">Nell'esempio seguente viene illustrata l'associazione di un singolo vertex buffer e di un oggetto di layout di input alla fase IA:</span><span class="sxs-lookup"><span data-stu-id="5f453-164">The following example shows the binding of a single vertex buffer and an input-layout object to the IA stage:</span></span>


```
UINT stride = sizeof( SimpleVertex );
UINT offset = 0;
g_pd3dDevice->IASetVertexBuffers( 
    0,                // the first input slot for binding
    1,                // the number of buffers in the array
    &g_pVertexBuffer, // the array of vertex buffers
    &stride,          // array of stride values, one for each buffer
    &offset );        // array of offset values, one for each buffer

// Set the input layout
g_pd3dDevice->IASetInputLayout( g_pVertexLayout );
```



<span data-ttu-id="5f453-165">Per l'associazione dell'oggetto di layout di input è necessario solo un puntatore all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="5f453-165">Binding the input-layout object only requires a pointer to the object.</span></span>

<span data-ttu-id="5f453-166">Nell'esempio precedente viene associato un singolo buffer del vertice; Tuttavia, più buffer dei vertici possono essere associati da una singola chiamata a [**sul ID3D11DeviceContext:: IASetVertexBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers)e il codice seguente mostra tale chiamata per associare tre buffer di vertici:</span><span class="sxs-lookup"><span data-stu-id="5f453-166">In the preceding example, a single vertex buffer is bound; however, multiple vertex buffers can be bound by a single call to [**ID3D11DeviceContext::IASetVertexBuffers**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetvertexbuffers), and the following code shows such a call to bind three vertex buffers:</span></span>


```
UINT strides[3];
strides[0] = sizeof(SimpleVertex1);
strides[1] = sizeof(SimpleVertex2);
strides[2] = sizeof(SimpleVertex3);
UINT offsets[3] = { 0, 0, 0 };
g_pd3dDevice->IASetVertexBuffers( 
    0,                 //first input slot for binding
    3,                 //number of buffers in the array
    &g_pVertexBuffers, //array of three vertex buffers
    &strides,          //array of stride values, one for each buffer
    &offsets );        //array of offset values, one for each buffer
```



<span data-ttu-id="5f453-167">Un buffer di indice è associato alla fase IA chiamando [**sul ID3D11DeviceContext:: IASetIndexBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetindexbuffer).</span><span class="sxs-lookup"><span data-stu-id="5f453-167">An index buffer is bound to the IA stage by calling [**ID3D11DeviceContext::IASetIndexBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetindexbuffer).</span></span>

## <a name="specify-the-primitive-type"></a><span data-ttu-id="5f453-168">Specificare il tipo primitivo</span><span class="sxs-lookup"><span data-stu-id="5f453-168">Specify the Primitive Type</span></span>

<span data-ttu-id="5f453-169">Una volta associati i buffer di input, è necessario che nella fase IA venga indicato come assemblare i vertici in primitive.</span><span class="sxs-lookup"><span data-stu-id="5f453-169">After the input buffers have been bound, the IA stage must be told how to assemble the vertices into primitives.</span></span> <span data-ttu-id="5f453-170">Questa operazione viene eseguita specificando il [tipo primitivo](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-primitive-topologies) chiamando [**sul ID3D11DeviceContext:: IASetPrimitiveTopology**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology); il codice seguente chiama questa funzione per definire i dati come un elenco di triangolo senza adiacenza:</span><span class="sxs-lookup"><span data-stu-id="5f453-170">This is done by specifying the [primitive type](/windows/desktop/direct3d11/d3d10-graphics-programming-guide-primitive-topologies) by calling [**ID3D11DeviceContext::IASetPrimitiveTopology**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-iasetprimitivetopology); the following code calls this function to define the data as a triangle list without adjacency:</span></span>


```
g_pd3dDevice->IASetPrimitiveTopology( D3D_PRIMITIVE_TOPOLOGY_TRIANGLELIST );
```



<span data-ttu-id="5f453-171">I restanti tipi primitivi sono elencati nella [**\_ \_ topologia primitiva D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_primitive_topology).</span><span class="sxs-lookup"><span data-stu-id="5f453-171">The rest of the primitive types are listed in [**D3D\_PRIMITIVE\_TOPOLOGY**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_primitive_topology).</span></span>

## <a name="call-draw-methods"></a><span data-ttu-id="5f453-172">Metodi di richiamo della chiamata</span><span class="sxs-lookup"><span data-stu-id="5f453-172">Call Draw Methods</span></span>

<span data-ttu-id="5f453-173">Dopo aver associato le risorse di input alla pipeline, un'applicazione chiama un metodo di disegnare per eseguire il rendering delle primitive.</span><span class="sxs-lookup"><span data-stu-id="5f453-173">After input resources have been bound to the pipeline, an application calls a draw method to render primitives.</span></span> <span data-ttu-id="5f453-174">Sono disponibili diversi metodi di estrazione, illustrati nella tabella seguente: Alcuni usano i buffer di indice, alcuni usano i dati dell'istanza e alcuni riutilizzano i dati dalla fase di output di streaming come input per la fase di input-assembler.</span><span class="sxs-lookup"><span data-stu-id="5f453-174">There are several draw methods, which are shown in the following table; some use index buffers, some use instance data, and some reuse data from the streaming-output stage as input to the input-assembler stage.</span></span>



| <span data-ttu-id="5f453-175">Metodi di estrazione</span><span class="sxs-lookup"><span data-stu-id="5f453-175">Draw Methods</span></span>                                                                                  | <span data-ttu-id="5f453-176">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5f453-176">Description</span></span>                                                                                            |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5f453-177">**Sul ID3D11DeviceContext::D RAW**</span><span class="sxs-lookup"><span data-stu-id="5f453-177">**ID3D11DeviceContext::Draw**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw)                                 | <span data-ttu-id="5f453-178">Creare primitive non indicizzate non indicizzate.</span><span class="sxs-lookup"><span data-stu-id="5f453-178">Draw non-indexed, non-instanced primitives.</span></span>                                                            |
| [<span data-ttu-id="5f453-179">**Sul ID3D11DeviceContext::D rawInstanced**</span><span class="sxs-lookup"><span data-stu-id="5f453-179">**ID3D11DeviceContext::DrawInstanced**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawinstanced)               | <span data-ttu-id="5f453-180">Creare primitive con istanze non indicizzate.</span><span class="sxs-lookup"><span data-stu-id="5f453-180">Draw non-indexed, instanced primitives.</span></span>                                                                |
| [<span data-ttu-id="5f453-181">**Sul ID3D11DeviceContext::D rawIndexed**</span><span class="sxs-lookup"><span data-stu-id="5f453-181">**ID3D11DeviceContext::DrawIndexed**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexed)                   | <span data-ttu-id="5f453-182">Creare primitive indicizzate senza istanze.</span><span class="sxs-lookup"><span data-stu-id="5f453-182">Draw indexed, non-instanced primitives.</span></span>                                                                |
| [<span data-ttu-id="5f453-183">**Sul ID3D11DeviceContext::D rawIndexedInstanced**</span><span class="sxs-lookup"><span data-stu-id="5f453-183">**ID3D11DeviceContext::DrawIndexedInstanced**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced) | <span data-ttu-id="5f453-184">Creare primitive con indicizzazione e istanze.</span><span class="sxs-lookup"><span data-stu-id="5f453-184">Draw indexed, instanced primitives.</span></span>                                                                    |
| [<span data-ttu-id="5f453-185">**Sul ID3D11DeviceContext::D rawAuto**</span><span class="sxs-lookup"><span data-stu-id="5f453-185">**ID3D11DeviceContext::DrawAuto**</span></span>](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawauto)                         | <span data-ttu-id="5f453-186">Tracciare primitive non indicizzate non indicizzate dai dati di input provenienti dalla fase di streaming-output.</span><span class="sxs-lookup"><span data-stu-id="5f453-186">Draw non-indexed, non-instanced primitives from input data that comes from the streaming-output stage.</span></span> |



 

<span data-ttu-id="5f453-187">Ogni metodo di disegnare esegue il rendering di un singolo tipo di topologia.</span><span class="sxs-lookup"><span data-stu-id="5f453-187">Each draw method renders a single topology type.</span></span> <span data-ttu-id="5f453-188">Durante il rendering, le primitive incomplete (quelle prive di vertici sufficienti, privi di indici, primitive parziali e così via) vengono ignorate automaticamente.</span><span class="sxs-lookup"><span data-stu-id="5f453-188">During rendering, incomplete primitives (those without enough vertices, lacking indices, partial primitives, and so on) are silently discarded.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5f453-189">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5f453-189">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f453-190">Fase input-assembler</span><span class="sxs-lookup"><span data-stu-id="5f453-190">Input-Assembler Stage</span></span>](d3d10-graphics-programming-guide-input-assembler-stage.md)
</dt> </dl>

 

 