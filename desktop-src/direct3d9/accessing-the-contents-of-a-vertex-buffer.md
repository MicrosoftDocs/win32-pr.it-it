---
description: Gli oggetti vertex buffer consentono alle applicazioni di accedere direttamente alla memoria allocata per i dati dei vertici.
ms.assetid: 63d255b7-fa7d-411b-9cdb-52113f30c933
title: Accesso al contenuto di un buffer vertex (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1b5e4a4986e064d3736f83567f5dd6d479d0dbc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304883"
---
# <a name="accessing-the-contents-of-a-vertex-buffer-direct3d-9"></a><span data-ttu-id="53c39-103">Accesso al contenuto di un buffer vertex (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="53c39-103">Accessing the Contents of a Vertex Buffer (Direct3D 9)</span></span>

<span data-ttu-id="53c39-104">Gli oggetti vertex buffer consentono alle applicazioni di accedere direttamente alla memoria allocata per i dati dei vertici.</span><span class="sxs-lookup"><span data-stu-id="53c39-104">Vertex buffer objects enable applications to directly access the memory allocated for vertex data.</span></span> <span data-ttu-id="53c39-105">È possibile recuperare un puntatore alla memoria del buffer dei vertici chiamando il metodo [**IDirect3DVertexBuffer9:: Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock) e quindi accedendo alla memoria in base alle esigenze per riempire il buffer con i nuovi dati dei vertici o per leggere i dati già contenuti.</span><span class="sxs-lookup"><span data-stu-id="53c39-105">You can retrieve a pointer to vertex buffer memory by calling the [**IDirect3DVertexBuffer9::Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock) method, and then accessing the memory as needed to fill the buffer with new vertex data or to read any data it already contains.</span></span> <span data-ttu-id="53c39-106">Il metodo **IDirect3DVertexBuffer9:: Lock** accetta quattro parametri.</span><span class="sxs-lookup"><span data-stu-id="53c39-106">The **IDirect3DVertexBuffer9::Lock** method accepts four parameters.</span></span> <span data-ttu-id="53c39-107">Il primo, *OffsetToLock*, è l'offset nei dati del vertice.</span><span class="sxs-lookup"><span data-stu-id="53c39-107">The first, *OffsetToLock*, is the offset into the vertex data.</span></span> <span data-ttu-id="53c39-108">Il secondo parametro è la dimensione, espressa in byte, dei dati del vertice.</span><span class="sxs-lookup"><span data-stu-id="53c39-108">The second parameter is the size, measured in bytes, of the vertex data.</span></span> <span data-ttu-id="53c39-109">Il terzo parametro accettato è l'indirizzo di un puntatore che punta ai dati del vertice, se la chiamata ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="53c39-109">The third parameter accepted is the address of a pointer that points to the vertex data, if the call succeeds.</span></span>

<span data-ttu-id="53c39-110">L'ultimo parametro, *Flags*, indica al sistema la modalità di blocco della memoria.</span><span class="sxs-lookup"><span data-stu-id="53c39-110">The last parameter, *Flags*, tells the system how the memory should be locked.</span></span> <span data-ttu-id="53c39-111">Specificare le costanti per il parametro *Flags* in base alla modalità di accesso ai dati dei vertici.</span><span class="sxs-lookup"><span data-stu-id="53c39-111">Specify constants for the *Flags* parameter according to the way the vertex data will be accessed.</span></span> <span data-ttu-id="53c39-112">Verificare che il valore scelto per [**D3DUSAGE**](d3dusage.md) corrisponda al valore scelto per [D3DLOCK](d3dlock.md).</span><span class="sxs-lookup"><span data-stu-id="53c39-112">Make sure the value chosen for [**D3DUSAGE**](d3dusage.md) matches the value chosen for [D3DLOCK](d3dlock.md).</span></span> <span data-ttu-id="53c39-113">Se, ad esempio, si crea un buffer vertex con solo accesso in scrittura, non è sensato provare a leggere i dati specificando D3DLOCK \_ ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="53c39-113">For example, if you are creating a vertex buffer with write access only, it doesn't make sense to try to read the data by specifying D3DLOCK\_READONLY.</span></span> <span data-ttu-id="53c39-114">L'utilizzo di questi flag consente al driver di bloccare la memoria e fornire le migliori prestazioni, dato il tipo di accesso richiesto.</span><span class="sxs-lookup"><span data-stu-id="53c39-114">Wisely using these flags allows the driver to lock the memory and provide the best performance, given the requested access type.</span></span>

<span data-ttu-id="53c39-115">Dopo aver completato la compilazione o la lettura dei dati dei vertici, chiamare il metodo [**IDirect3DVertexBuffer9:: Unlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-unlock) , come illustrato nell'esempio di codice seguente.</span><span class="sxs-lookup"><span data-stu-id="53c39-115">After you finish filling or reading the vertex data, call the [**IDirect3DVertexBuffer9::Unlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-unlock) method, as shown in the following code example.</span></span>


```
// This code example assumes the g_pVB is a variable of type 
//   LPDIRECT3DVERTEXBUFFER9 and that g_Vertices has been  
//   properly initialized with vertices

// Lock the buffer to gain access to the vertices 
VOID* pVertices;

if(FAILED(g_pVB->Lock(0, sizeof(g_Vertices), 
        (BYTE**)&pVertices, 0 ) ) ) 
    return E_FAIL;

memcpy(pVertices, g_Vertices, sizeof(g_Vertices));
g_pVB->Unlock();
```



<span data-ttu-id="53c39-116">Se si crea un buffer vertex con il \_ flag WRITEONLY di D3DUSAGE, non usare il flag di blocco di sola \_ lettura D3DLOCK.</span><span class="sxs-lookup"><span data-stu-id="53c39-116">If you create a vertex buffer with the D3DUSAGE\_WRITEONLY flag, do not use the D3DLOCK\_READONLY locking flag.</span></span> <span data-ttu-id="53c39-117">Usare il \_ flag di sola lettura D3DLOCK se l'applicazione viene letta solo dalla memoria del buffer dei vertici.</span><span class="sxs-lookup"><span data-stu-id="53c39-117">Use the D3DLOCK\_READONLY flag if your application will read only from the vertex buffer memory.</span></span> <span data-ttu-id="53c39-118">L'inclusione di questo flag consente a Direct3D di ottimizzare le procedure interne per migliorare l'efficienza, dato che l'accesso alla memoria sarà di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="53c39-118">Including this flag enables Direct3D to optimize its internal procedures to improve efficiency, given that access to the memory will be read-only.</span></span>

<span data-ttu-id="53c39-119">Per [](performance-optimizations.md) informazioni sull'uso di D3DLOCK \_ scarto o D3DLOCK \_ sovrascrittura per il parametro Flags di [**IDirect3DVertexBuffer9:: Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock), vedere uso dei buffer di indice e dei vertici dinamici.</span><span class="sxs-lookup"><span data-stu-id="53c39-119">See [Using Dynamic Vertex and Index Buffers](performance-optimizations.md) for information about using D3DLOCK\_DISCARD or D3DLOCK\_NOOVERWRITE for the Flags parameter of [**IDirect3DVertexBuffer9::Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock).</span></span>

<span data-ttu-id="53c39-120">In C++, poiché si accede direttamente alla memoria allocata per il buffer dei vertici, assicurarsi che l'applicazione acceda correttamente alla memoria allocata.</span><span class="sxs-lookup"><span data-stu-id="53c39-120">In C++, because you directly access the memory allocated for the vertex buffer, make sure your application properly accesses the allocated memory.</span></span> <span data-ttu-id="53c39-121">In caso contrario, si rischia il rendering della memoria non valida.</span><span class="sxs-lookup"><span data-stu-id="53c39-121">Otherwise, you risk rendering that memory invalid.</span></span> <span data-ttu-id="53c39-122">Usare lo stride del formato Vertex usato dall'applicazione per spostarsi da un vertice nel buffer allocato a un altro.</span><span class="sxs-lookup"><span data-stu-id="53c39-122">Use the stride of the vertex format that your application uses to move from one vertex in the allocated buffer to another.</span></span> <span data-ttu-id="53c39-123">La memoria del buffer dei vertici è una semplice matrice di vertici specificati in FVF.</span><span class="sxs-lookup"><span data-stu-id="53c39-123">The vertex buffer memory is a simple array of vertices specified in FVF.</span></span> <span data-ttu-id="53c39-124">Utilizzare lo stride della struttura del formato Vertex definito.</span><span class="sxs-lookup"><span data-stu-id="53c39-124">Use the stride of whatever vertex format structure you define.</span></span> <span data-ttu-id="53c39-125">È possibile calcolare lo stride di ogni vertice in fase di esecuzione esaminando i [D3DFVF](d3dfvf.md) contenuti nella descrizione del buffer dei vertici.</span><span class="sxs-lookup"><span data-stu-id="53c39-125">You can calculate the stride of each vertex at run time by examining the [D3DFVF](d3dfvf.md) contained in the vertex buffer description.</span></span> <span data-ttu-id="53c39-126">Nella tabella seguente vengono illustrate le dimensioni di ogni componente vertice.</span><span class="sxs-lookup"><span data-stu-id="53c39-126">The following table shows the size for each vertex component.</span></span>



| <span data-ttu-id="53c39-127">Flag di formato vertici</span><span class="sxs-lookup"><span data-stu-id="53c39-127">Vertex Format Flag</span></span> | <span data-ttu-id="53c39-128">Dimensione</span><span class="sxs-lookup"><span data-stu-id="53c39-128">Size</span></span>              |
|--------------------|-------------------|
| <span data-ttu-id="53c39-129">D3DFVF \_ diffuse</span><span class="sxs-lookup"><span data-stu-id="53c39-129">D3DFVF\_DIFFUSE</span></span>    | <span data-ttu-id="53c39-130">sizeof (DWORD)</span><span class="sxs-lookup"><span data-stu-id="53c39-130">sizeof(DWORD)</span></span>     |
| <span data-ttu-id="53c39-131">D3DFVF \_ normale</span><span class="sxs-lookup"><span data-stu-id="53c39-131">D3DFVF\_NORMAL</span></span>     | <span data-ttu-id="53c39-132">sizeof (float) x 3</span><span class="sxs-lookup"><span data-stu-id="53c39-132">sizeof(float) x 3</span></span> |
| <span data-ttu-id="53c39-133">D3DFVF \_ speculare</span><span class="sxs-lookup"><span data-stu-id="53c39-133">D3DFVF\_SPECULAR</span></span>   | <span data-ttu-id="53c39-134">sizeof (DWORD)</span><span class="sxs-lookup"><span data-stu-id="53c39-134">sizeof(DWORD)</span></span>     |
| <span data-ttu-id="53c39-135">\_TEXN D3DFVF</span><span class="sxs-lookup"><span data-stu-id="53c39-135">D3DFVF\_TEXn</span></span>       | <span data-ttu-id="53c39-136">sizeof (float) x n</span><span class="sxs-lookup"><span data-stu-id="53c39-136">sizeof(float) x n</span></span> |
| <span data-ttu-id="53c39-137">D3DFVF \_ XYZ</span><span class="sxs-lookup"><span data-stu-id="53c39-137">D3DFVF\_XYZ</span></span>        | <span data-ttu-id="53c39-138">sizeof (float) x 3</span><span class="sxs-lookup"><span data-stu-id="53c39-138">sizeof(float) x 3</span></span> |
| <span data-ttu-id="53c39-139">\_XYZRHW D3DFVF</span><span class="sxs-lookup"><span data-stu-id="53c39-139">D3DFVF\_XYZRHW</span></span>     | <span data-ttu-id="53c39-140">sizeof (float) x 4</span><span class="sxs-lookup"><span data-stu-id="53c39-140">sizeof(float) x 4</span></span> |



 

<span data-ttu-id="53c39-141">Il numero di coordinate di trama presenti nel formato vertici è descritto dai \_ flag D3DFVF Tex n (dove n è un valore compreso tra 0 e 8).</span><span class="sxs-lookup"><span data-stu-id="53c39-141">The number of texture coordinates present in the vertex format is described by the D3DFVF\_TEX n flags (where n is a value from 0 to 8).</span></span> <span data-ttu-id="53c39-142">Moltiplicare il numero di set di coordinate di trama per la dimensione di un set di coordinate di trama, che può variare da uno a quattro float, per calcolare la memoria necessaria per quel numero di coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="53c39-142">Multiply the number of texture coordinate sets by the size of one set of texture coordinates, which can range from one to four floats, to calculate the memory required for that number of texture coordinates.</span></span>

<span data-ttu-id="53c39-143">Usare lo stride totale del vertice per incrementare e decrementare il puntatore di memoria in base alle esigenze per accedere a vertici specifici.</span><span class="sxs-lookup"><span data-stu-id="53c39-143">Use the total vertex stride to increment and decrement the memory pointer as needed to access particular vertices.</span></span>

## <a name="retrieving-vertex-buffer-descriptions"></a><span data-ttu-id="53c39-144">Recupero delle descrizioni dei buffer dei vertici</span><span class="sxs-lookup"><span data-stu-id="53c39-144">Retrieving Vertex Buffer Descriptions</span></span>

<span data-ttu-id="53c39-145">È possibile recuperare informazioni su un buffer vertex chiamando il metodo [**IDirect3DVertexBuffer9:: getdesc**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="53c39-145">You can retrieve information about a vertex buffer by calling the [**IDirect3DVertexBuffer9::GetDesc**](/windows/desktop/api) method.</span></span> <span data-ttu-id="53c39-146">Questo metodo compila i membri della struttura [**D3DVERTEXBUFFER \_ desc**](d3dvertexbuffer-desc.md) con le informazioni sul buffer dei vertici.</span><span class="sxs-lookup"><span data-stu-id="53c39-146">This method fills the members of the [**D3DVERTEXBUFFER\_DESC**](d3dvertexbuffer-desc.md) structure with information about the vertex buffer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="53c39-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="53c39-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="53c39-148">Buffer vertici</span><span class="sxs-lookup"><span data-stu-id="53c39-148">Vertex Buffers</span></span>](vertex-buffers.md)
</dt> </dl>

 

 
