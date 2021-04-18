---
description: Questa sezione descrive gli shader che è possibile usare per il modello di flusso programmabile.
ms.assetid: 800aaa27-e1e6-4d35-8de4-7ac94d646870
title: Programmazione di uno o più flussi (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43210823911648ed11227faef44d980b60d0a335
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304065"
---
# <a name="programming-one-or-more-streams-direct3d-9"></a><span data-ttu-id="4f598-103">Programmazione di uno o più flussi (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="4f598-103">Programming One or More Streams (Direct3D 9)</span></span>

<span data-ttu-id="4f598-104">Questa sezione descrive gli shader che è possibile usare per il modello di flusso programmabile.</span><span class="sxs-lookup"><span data-stu-id="4f598-104">This section describes shaders that can be used for the programmable stream model.</span></span>

## <a name="using-streams"></a><span data-ttu-id="4f598-105">Uso di flussi</span><span class="sxs-lookup"><span data-stu-id="4f598-105">Using Streams</span></span>

<span data-ttu-id="4f598-106">DirectX 8 ha introdotto la nozione di flusso per associare i dati ai registri di input per l'uso da parte degli shader.</span><span class="sxs-lookup"><span data-stu-id="4f598-106">DirectX 8 introduced the notion of a stream to bind data to input registers for use by shaders.</span></span> <span data-ttu-id="4f598-107">Un flusso è una matrice uniforme di dati del componente, in cui ogni componente è costituito da uno o più elementi che rappresentano una singola entità, ad esempio posizione, normale, colore e così via.</span><span class="sxs-lookup"><span data-stu-id="4f598-107">A stream is a uniform array of component data, where each component consists of one or more elements that represent a single entity such as position, normal, color, and so on.</span></span> <span data-ttu-id="4f598-108">I flussi consentono ai chip grafici di eseguire un accesso diretto alla memoria da più buffer dei vertici in parallelo e forniscono anche un mapping più naturale dai dati dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4f598-108">Streams enable graphic chips to perform a direct memory access from multiple vertex buffers in parallel and also provide a more natural mapping from application data.</span></span> <span data-ttu-id="4f598-109">Abilitano anche Trivial multitexture rispetto a MultiPASS.</span><span class="sxs-lookup"><span data-stu-id="4f598-109">They also enable trivial multitexture versus multipass.</span></span> <span data-ttu-id="4f598-110">Si pensi a questo:</span><span class="sxs-lookup"><span data-stu-id="4f598-110">Think of it like this:</span></span>

-   <span data-ttu-id="4f598-111">Un vertice è costituito da n flussi.</span><span class="sxs-lookup"><span data-stu-id="4f598-111">A vertex is composed of n streams.</span></span>
-   <span data-ttu-id="4f598-112">Un flusso è costituito da elementi m.</span><span class="sxs-lookup"><span data-stu-id="4f598-112">A stream is composed of m elements.</span></span>
-   <span data-ttu-id="4f598-113">Un elemento è \[ position, color, Normal e coordinata di trama \] .</span><span class="sxs-lookup"><span data-stu-id="4f598-113">An element is \[position, color, normal, texture coordinate\].</span></span>

<span data-ttu-id="4f598-114">Il metodo [**IDirect3DDevice9:: SetStreamSource**](/windows/desktop/api) associa un buffer vertex a un flusso di dati del dispositivo, creando un'associazione tra i dati dei vertici e una delle diverse porte del flusso di dati che alimentano le funzioni di elaborazione primitive.</span><span class="sxs-lookup"><span data-stu-id="4f598-114">The [**IDirect3DDevice9::SetStreamSource**](/windows/desktop/api) method binds a vertex buffer to a device data stream, creating an association between the vertex data and one of several data stream ports that feed the primitive processing functions.</span></span> <span data-ttu-id="4f598-115">I riferimenti effettivi ai dati del flusso non si verificano fino a quando non viene chiamato un metodo di disegno, ad esempio [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive).</span><span class="sxs-lookup"><span data-stu-id="4f598-115">The actual references to the stream data do not occur until a drawing method, such as [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), is called.</span></span>

<span data-ttu-id="4f598-116">Il mapping degli elementi del vertice di input ai registri di input dei vertici per i vertex shader programmabili è definito nella dichiarazione dello shader, ma gli elementi del vertice di input non hanno una semantica specifica relativa all'utilizzo.</span><span class="sxs-lookup"><span data-stu-id="4f598-116">The mapping of the input vertex elements to the vertex input registers for programmable vertex shaders is defined in the shader declaration, but the input vertex elements do not have specific semantics about their use.</span></span> <span data-ttu-id="4f598-117">L'interpretazione degli elementi del vertice di input viene programmata usando le istruzioni dello shader.</span><span class="sxs-lookup"><span data-stu-id="4f598-117">The interpretation of the input vertex elements is programmed using the shader instructions.</span></span> <span data-ttu-id="4f598-118">La funzione vertex shader viene definita da una matrice di istruzioni applicate a ogni vertice.</span><span class="sxs-lookup"><span data-stu-id="4f598-118">The vertex shader function is defined by an array of instructions that are applied to each vertex.</span></span> <span data-ttu-id="4f598-119">I registri di output dei vertici vengono scritti in modo esplicito in, usando le istruzioni nella funzione shader.</span><span class="sxs-lookup"><span data-stu-id="4f598-119">The vertex output registers are explicitly written to, using instructions in the shader function.</span></span>

<span data-ttu-id="4f598-120">Per questa discussione, tuttavia, è preoccupante del mapping semantico degli elementi ai registri e più riguarda il motivo per l'uso dei flussi e il problema che viene risolto usando i flussi.</span><span class="sxs-lookup"><span data-stu-id="4f598-120">For this discussion, though, be less concerned with the semantic mapping of elements to registers and more concerned with the reason for using streams and what problem is solved by using streams.</span></span> <span data-ttu-id="4f598-121">Il vantaggio principale dei flussi consiste nel fatto che i dati dei vertici vengono rimossi in precedenza dai costi associati al multitexturing.</span><span class="sxs-lookup"><span data-stu-id="4f598-121">The main benefit of streams is that they remove the vertex data costs previously associated with multitexturing.</span></span> <span data-ttu-id="4f598-122">Prima dei flussi, un utente doveva duplicare i set di dati dei vertici per gestire il case singolo e multitrama senza elementi dati inutilizzati o includere elementi di dati che sarebbero stati inutilizzati tranne nel caso di multitexture.</span><span class="sxs-lookup"><span data-stu-id="4f598-122">Before streams, a user had to either duplicate vertex data sets to handle the single and multitexture case with no unused data elements, or carry data elements that would be unused except in the multitexture case.</span></span>

<span data-ttu-id="4f598-123">Di seguito è riportato un esempio di utilizzo di due set di dati dei vertici, uno per la trama singola e uno per la multitexturing.</span><span class="sxs-lookup"><span data-stu-id="4f598-123">Here is an example of using two sets of vertex data, one for single texture and one for multitexturing.</span></span>


```
struct CUSTOMVERTEX_TEX1
{
    FLOAT x, y, z;      // The untransformed position for the vertex
    DWORD diffColor;    // The vertex diffuse color    
    DWORD specColor;    // The vertex specular color
    float tu_1, tv_1;   // Texture coordinates for a single texture
};
 
struct CUSTOMVERTEX_TEX2
{
    FLOAT x, y, z;      // The untransformed position for the vertex
    DWORD diffColor;    // The vertex diffuse color    
    DWORD specColor;    // The vertex specular color
    float tu_2, tv_2;   // Texture coordinates for multitexturing
};
```



<span data-ttu-id="4f598-124">In alternativa, era necessario disporre di un singolo elemento Vertex che conteneva entrambi i set di coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="4f598-124">The alternative was to have a single vertex element that contained both sets of texture coordinates.</span></span>


```
struct CUSTOMVERTEX_TEX2
{
    FLOAT x, y, z;      // The untransformed position for the vertex
    DWORD diffColor;    // The vertex diffuse color    
    DWORD specColor;    // The vertex specular color
    float tu_1, tv_1;   // Texture coordinates for a single texture
    float tu_2, tv_2;   // Texture coordinates for multitexturing
};
```



<span data-ttu-id="4f598-125">Con questi dati dei vertici, solo una copia dei dati di posizione e colore viene mantenuta in memoria, a scapito del fatto di portare entrambi i set di coordinate di trama per il rendering anche nel caso di una singola trama.</span><span class="sxs-lookup"><span data-stu-id="4f598-125">With this vertex data, only one copy of the position and color data are carried in memory, at the expense of carrying both sets of texture coordinates around for rendering even in the single texture case.</span></span>

<span data-ttu-id="4f598-126">Ora che il compromesso è chiaro, i flussi forniscono una soluzione elegante a questo dilemma.</span><span class="sxs-lookup"><span data-stu-id="4f598-126">Now that the tradeoff is clear, streams provide an elegant fix to this dilemma.</span></span> <span data-ttu-id="4f598-127">Di seguito è riportato un set di definizioni dei vertici per supportare tre flussi: uno con la posizione e il colore, uno con il primo set di coordinate di trama e uno con il secondo set di coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="4f598-127">Here is a set of vertex definitions to support three streams: one with position and color, one with the first set of texture coordinates, and one with the second set of texture coordinates.</span></span>


```
// Multistream vertex
// Stream 0, pos, diffuse, specular
struct POSCOLORVERTEX
{
    FLOAT x, y, z;
    DWORD diffColor, specColor;
};
#define D3DFVF_POSCOLORVERTEX (D3DFVF_XYZ|D3DFVF_DIFFUSE|D3DFVF_SPECULAR)
// Stream 1, tex coord 0
struct TEXC0VERTEX
{
    FLOAT tu1, tv1;
};
#define D3DFVF_TEXC0VERTEX (D3DFVF_TEX1)

// Stream 2, tex coord 1
struct TEXC1VERTEX
{
    FLOAT tu2, tv2;
};
#define D3DFVF_TEXC1VERTEX (D3DFVF_TEX0)
```



<span data-ttu-id="4f598-128">La dichiarazione del vertice sarà la seguente:</span><span class="sxs-lookup"><span data-stu-id="4f598-128">The vertex declaration would be as follows:</span></span>


```
// Multitexture - multistream

D3DVERTEXELEMENT9 dwDecl3[] = 
{
    {0, 0,  D3DDECLTYPE_FLOAT3,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_POSITION, 0},
    {0, 12, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 0},
    {0, 16, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 1},
    {1,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 0},
    {2,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 1},
    D3DDECL_END()
};
```



<span data-ttu-id="4f598-129">A questo punto, creare l'oggetto dichiarazione vertici e impostarlo come illustrato di seguito:</span><span class="sxs-lookup"><span data-stu-id="4f598-129">Now create the vertex declaration object and set it as shown:</span></span>


```
LPDIRECT3DVERTEXDECLARATION9 m_pVertexDeclaration;
g_d3dDevice->CreateVertexDeclaration(dwDecl3, &m_pVertexDeclaration);

m_pd3dDevice->SetVertexDeclaration(m_pVertexDeclaration);
```



## <a name="examples-of-combinations"></a><span data-ttu-id="4f598-130">Esempi di combinazioni</span><span class="sxs-lookup"><span data-stu-id="4f598-130">Examples of Combinations</span></span>

### <a name="one-stream-diffuse-color"></a><span data-ttu-id="4f598-131">Colore diffuso di un flusso</span><span class="sxs-lookup"><span data-stu-id="4f598-131">One Stream Diffuse Color</span></span>

<span data-ttu-id="4f598-132">La dichiarazione dei vertici e le impostazioni di flusso per il rendering dei colori diffusi sono simili alle seguenti:</span><span class="sxs-lookup"><span data-stu-id="4f598-132">The vertex declaration and stream settings for diffuse color rendering would look like this:</span></span>


```
D3DVERTEXELEMENT9 dwDecl3[] = 
{
    {0,  0,  D3DDECLTYPE_FLOAT3,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_POSITION, 0},
    {0, 12,  D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 0 ,
    {0, 16,  D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 1},
    D3DDECL_END()
};
   m_pd3dDevice->SetStreamSource(0, m_pVBVertexShader0, 0,
                                      sizeof(CUSTOMVERTEX));
   m_pd3dDevice->SetStreamSource(1, NULL, 0, 0);
   m_pd3dDevice->SetStreamSource(2, NULL, 0, 0);
```



### <a name="two-streams-with-color-and-texture"></a><span data-ttu-id="4f598-133">Due flussi con colore e trama</span><span class="sxs-lookup"><span data-stu-id="4f598-133">Two Streams with Color and Texture</span></span>

<span data-ttu-id="4f598-134">La dichiarazione dei vertici e le impostazioni di flusso per il rendering a trama singola avranno un aspetto simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="4f598-134">The vertex declaration and stream settings for single texture rendering would look like this:</span></span>


```
D3DVERTEXELEMENT9 dwDecl3[] = 
{
    {0, 0,  D3DDECLTYPE_FLOAT3,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_POSITION, 0},
    {0, 12, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 0},
    {0, 16, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 1},

    {1,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 0},

    D3DDECL_END()
};
   m_pd3dDevice->SetStreamSource(0, m_pVBPosColor, 0,
                                           sizeof(POSCOLORVERTEX));
   m_pd3dDevice->SetStreamSource(1, m_pVBTexC0, 0,
                                           sizeof(TEXC0VERTEX));
   m_pd3dDevice->SetStreamSource(2, NULL, 0, 0);
```



### <a name="two-streams-with-color-and-two-textures"></a><span data-ttu-id="4f598-135">Due flussi con colore e due trame</span><span class="sxs-lookup"><span data-stu-id="4f598-135">Two Streams with Color and two Textures</span></span>

<span data-ttu-id="4f598-136">La dichiarazione dei vertici e le impostazioni di flusso per il rendering a più trame a due trame avranno un aspetto simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="4f598-136">The vertex declaration and stream settings for two-texture multi-texture rendering would look like this:</span></span>


```
D3DVERTEXELEMENT9 dwDecl3[] = 
{
    {0, 0,  D3DDECLTYPE_FLOAT3,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_POSITION, 0},
    {0, 12, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 0},
    {0, 16, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 1},

    {1,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 0},

    {2,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 1},
    
    D3DDECL_END()
};
 
m_pd3dDevice->SetStreamSource(0, m_pVBPosColor, 0, 
                                          sizeof(POSCOLORVERTEX));
m_pd3dDevice->SetStreamSource(1, m_pVBTexC0, 0, 
                                          sizeof(TEXC0VERTEX));
m_pd3dDevice->SetStreamSource(2, m_pVBTexC1, 0, 
                                          sizeof(TEXC1VERTEX));
```



<span data-ttu-id="4f598-137">In ogni caso, è sufficiente la chiamata [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) .</span><span class="sxs-lookup"><span data-stu-id="4f598-137">In every case, the following [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) invocation suffices.</span></span>


```
       m_pd3dDevice->DrawPrimitive(D3DPT_TRIANGLEFAN, 0, NUM_TRIS);
```



<span data-ttu-id="4f598-138">Questo mostra la flessibilità dei flussi per la risoluzione del problema di duplicazione dei dati/trasmissione di dati ridondanti sul bus (ovvero, di sprecare larghezza di banda).</span><span class="sxs-lookup"><span data-stu-id="4f598-138">This shows the flexibility of streams in solving the problem of data duplication/redundant data transmission across the bus (that is, of wasting bandwidth).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4f598-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4f598-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f598-140">Dichiarazione vertici</span><span class="sxs-lookup"><span data-stu-id="4f598-140">Vertex Declaration</span></span>](vertex-declaration.md)
</dt> </dl>

 

 
