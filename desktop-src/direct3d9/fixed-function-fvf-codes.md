---
description: Un codice FVF descrive il contenuto dei vertici archiviati con interfoliazione in un singolo flusso di dati.
ms.assetid: 1a616f42-ec24-44ab-872f-7ea43646dd00
title: Codici FVF della funzione fissa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd10b655c0692881e5d93b6c716ec9bcd8a76c45
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303678"
---
# <a name="fixed-function-fvf-codes-direct3d-9"></a><span data-ttu-id="27b89-103">Codici FVF della funzione fissa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="27b89-103">Fixed Function FVF Codes (Direct3D 9)</span></span>

<span data-ttu-id="27b89-104">Un codice FVF descrive il contenuto dei vertici archiviati con interfoliazione in un singolo flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="27b89-104">A FVF code describes the contents of vertices stored interleaved in a single data stream.</span></span> <span data-ttu-id="27b89-105">In genere specifica i dati che devono essere elaborati dalla pipeline di elaborazione del vertice della funzione fissa.</span><span class="sxs-lookup"><span data-stu-id="27b89-105">It generally specifies data to be processed by the fixed function vertex processing pipeline.</span></span> <span data-ttu-id="27b89-106">Si tratta di una dichiarazione di vertice di tipo precedente; per visualizzare lo stile di dichiarazione del vertice corrente, vedere [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span><span class="sxs-lookup"><span data-stu-id="27b89-106">This is an older-style vertex declaration; to see the current vertex declaration style, see [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span></span>

<span data-ttu-id="27b89-107">Le applicazioni Direct3D possono definire i vertici del modello in diversi modi.</span><span class="sxs-lookup"><span data-stu-id="27b89-107">Direct3D applications can define model vertices in several different ways.</span></span> <span data-ttu-id="27b89-108">Il supporto per le definizioni dei vertici flessibili, noti anche come formati di vertici flessibili o codici di formato vertice flessibili, consente all'applicazione di usare solo i componenti Vertex necessari, eliminando i componenti che non vengono usati.</span><span class="sxs-lookup"><span data-stu-id="27b89-108">Support for flexible vertex definitions, also known as flexible vertex formats or flexible vertex format codes, makes it possible for your application to use only the vertex components it needs, eliminating those components that aren't used.</span></span> <span data-ttu-id="27b89-109">Utilizzando solo i componenti Vertex necessari, l'applicazione può conservare la memoria e ridurre al minimo la larghezza di banda di elaborazione necessaria per il rendering dei modelli.</span><span class="sxs-lookup"><span data-stu-id="27b89-109">By using only the needed vertex components, your application can conserve memory and minimize the processing bandwidth required to render models.</span></span> <span data-ttu-id="27b89-110">Viene descritto il modo in cui i vertici vengono formattati utilizzando una combinazione di codici [D3DFVF](d3dfvf.md) .</span><span class="sxs-lookup"><span data-stu-id="27b89-110">You describe how your vertices are formatted by using a combination of [D3DFVF](d3dfvf.md) codes.</span></span>

<span data-ttu-id="27b89-111">La specifica FVF include i formati per le dimensioni dei punti, specificati da D3DFVF \_ PSIZE.</span><span class="sxs-lookup"><span data-stu-id="27b89-111">The FVF specification includes formats for point size, specified by D3DFVF\_PSIZE.</span></span> <span data-ttu-id="27b89-112">Questa dimensione è espressa in unità di spazio della fotocamera per i vertici non trasformati e illuminati (TL) e in unità di spazio del dispositivo per i vertici TL.</span><span class="sxs-lookup"><span data-stu-id="27b89-112">This size is expressed in camera space units for non-transformed and lit (TL) vertices, and in device-space units for TL vertices.</span></span>

<span data-ttu-id="27b89-113">I metodi di rendering dell'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) forniscono applicazioni C++ con metodi che accettano una combinazione di questi flag e li usano per determinare come eseguire il rendering delle primitive.</span><span class="sxs-lookup"><span data-stu-id="27b89-113">The rendering methods of the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface provide C++ applications with methods that accept a combination of these flags, and use them to determine how to render primitives.</span></span> <span data-ttu-id="27b89-114">Fondamentalmente, questi flag indicano al sistema i componenti dei vertici, ovvero la posizione, i pesi di fusione dei vertici, le normali, i colori e il numero e il formato delle coordinate di trama. l'applicazione usa e, indirettamente, le parti della pipeline di rendering a cui si vuole applicare Direct3D.</span><span class="sxs-lookup"><span data-stu-id="27b89-114">Basically, these flags tell the system which vertex components - position, vertex blending weights, normal, colors, and the number and format of texture coordinates - your application uses and, indirectly, which parts of the rendering pipeline you want Direct3D to apply to them.</span></span> <span data-ttu-id="27b89-115">Inoltre, la presenza o l'assenza di un particolare flag di formato vertice comunica al sistema quali campi del componente Vertex sono presenti in memoria e che sono stati omessi.</span><span class="sxs-lookup"><span data-stu-id="27b89-115">In addition, the presence or absence of a particular vertex format flag communicates to the system which vertex component fields are present in memory and which you've omitted.</span></span>

<span data-ttu-id="27b89-116">Per determinare le limitazioni dei dispositivi, è possibile eseguire una query su un dispositivo per i valori di D3DFVFCAPS \_ DONOTSTRIPELEMENTS e D3DFVFCAPS \_ TEXCOORDCOUNTMASK nel membro FVFCaps di [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="27b89-116">To determine device limitations, you can query a device for the values of D3DFVFCAPS\_DONOTSTRIPELEMENTS and D3DFVFCAPS\_TEXCOORDCOUNTMASK in the FVFCaps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

<span data-ttu-id="27b89-117">Le coordinate di trama possono essere dichiarate in formati diversi, consentendo la ricerca di trame usando il numero di coordinate di una coordinata o di quattro coordinate di trama (per le coordinate di trama proiettate 2D).</span><span class="sxs-lookup"><span data-stu-id="27b89-117">Texture coordinates can be declared in different formats, allowing textures to be addressed using as few as one coordinate or as many as four texture coordinates (for 2D projected texture coordinates).</span></span> <span data-ttu-id="27b89-118">Per altre informazioni, vedere [formati di coordinate di trama (Direct3D 9)](texture-coordinate-formats.md).</span><span class="sxs-lookup"><span data-stu-id="27b89-118">For more information, see [Texture Coordinate Formats (Direct3D 9)](texture-coordinate-formats.md).</span></span> <span data-ttu-id="27b89-119">Usare il set di macro [**D3DFVF \_ TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) per creare modelli di bit che identifichino i formati di coordinate di trama usati dal formato del vertice.</span><span class="sxs-lookup"><span data-stu-id="27b89-119">Use the [**D3DFVF\_TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) set of macros to create bit patterns that identify the texture coordinate formats that your vertex format uses.</span></span>

<span data-ttu-id="27b89-120">Nessuna applicazione userà tutti i componenti.</span><span class="sxs-lookup"><span data-stu-id="27b89-120">No application will use every component.</span></span> <span data-ttu-id="27b89-121">I campi uniformi W (RHW) e i normali vertici si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="27b89-121">The reciprocal homogeneous W (RHW) and vertex normal fields are mutually exclusive.</span></span> <span data-ttu-id="27b89-122">E la maggior parte delle applicazioni tentano di usare tutti e otto i set di coordinate di trama, ma Direct3D ha questa capacità.</span><span class="sxs-lookup"><span data-stu-id="27b89-122">Nor will most applications try to use all eight sets of texture coordinates, but Direct3D has this capacity.</span></span> <span data-ttu-id="27b89-123">Esistono diverse restrizioni sui flag che è possibile usare con altri flag.</span><span class="sxs-lookup"><span data-stu-id="27b89-123">There are several restrictions on which flags you can use with other flags.</span></span> <span data-ttu-id="27b89-124">Ad esempio, non è possibile usare \_ insieme i flag D3DFVF XYZ e D3DFVF \_ XYZRHW, in quanto ciò indicherebbe che l'applicazione sta descrivendo la posizione di un vertice con i vertici non trasformati e trasformati.</span><span class="sxs-lookup"><span data-stu-id="27b89-124">For example, you cannot use the D3DFVF\_XYZ and D3DFVF\_XYZRHW flags together, as this would indicate that your application is describing a vertex's position with both untransformed and transformed vertices.</span></span>

<span data-ttu-id="27b89-125">Per usare la combinazione di vertici indicizzati, \_ il \_ flag D3DFVF LASTBETA UBYTE4 dovrebbe essere visualizzato alla fine della dichiarazione FVF.</span><span class="sxs-lookup"><span data-stu-id="27b89-125">To use indexed vertex blending, the D3DFVF\_LASTBETA\_UBYTE4 flag should appear at the end of the FVF declaration.</span></span> <span data-ttu-id="27b89-126">La presenza di questo flag indica che il quinto peso di fusione verrà considerato come DWORD anziché come float.</span><span class="sxs-lookup"><span data-stu-id="27b89-126">The presence of this flag indicates that the fifth blending weight will be treated as a DWORD instead of float.</span></span> <span data-ttu-id="27b89-127">Per ulteriori informazioni, vedere la pagina relativa alla [fusione dei vertici indicizzati (Direct3D 9)](indexed-vertex-blending.md).</span><span class="sxs-lookup"><span data-stu-id="27b89-127">For more information, see [Indexed Vertex Blending (Direct3D 9)](indexed-vertex-blending.md).</span></span>

<span data-ttu-id="27b89-128">Gli esempi di codice seguenti illustrano la differenza tra un codice FVF che usa \_ il \_ flag D3DFVF LASTBETA UBYTE4 e uno che non lo è.</span><span class="sxs-lookup"><span data-stu-id="27b89-128">The following code samples shows the difference between an FVF code that uses the D3DFVF\_LASTBETA\_UBYTE4 flag and one that doesn't.</span></span> <span data-ttu-id="27b89-129">Il flag D3DFVF \_ XYZB3 è presente quando vengono usati quattro indici di fusione perché si sottrae sempre la somma dei primi tre dal numero uno per ottenere il quarto (Blend ₄ = 1-(Blend ₁ + Blend ₂ + Blend ₃)).</span><span class="sxs-lookup"><span data-stu-id="27b89-129">The flag D3DFVF\_XYZB3 is present when four blending indices are used because you always subtract the sum of the first three from the number one to obtain the fourth (blend₄ = 1 - (blend₁ + blend₂ + blend₃)).</span></span>


```
#define D3DFVF_BLENDVERTEX (D3DFVF_XYZB3|D3DFVF_NORMAL|D3DFVF_TEX1)

struct BLENDVERTEX
{
    D3DXVECTOR3 v;       // Referenced as v0 in the vertex shader
    FLOAT       blend1;  // Referenced as v1.x in the vertex shader
    FLOAT       blend2;  // Referenced as v1.y in the vertex shader
    FLOAT       blend3;  // Referenced as v1.z in the vertex shader
                         // v1.w = 1.0 - (v1.x + v1.y + v1.z)
    D3DXVECTOR3 n;       // Referenced as v3 in the vertex shader
    FLOAT       tu, tv;  // Referenced as v7 in the vertex shader
};
```



<span data-ttu-id="27b89-130">Il FVF definito di seguito usa il \_ flag D3DFVF Last \_ UBYTE4.</span><span class="sxs-lookup"><span data-stu-id="27b89-130">The FVF defined below uses the D3DFVF\_LAST\_UBYTE4 flag.</span></span>


```
#define D3DFVF_BLENDVERTEX (D3DFVF_XYZB4 | D3DFVF_LASTBETA_UBYTE4 |D3DFVF_NORMAL|D3DFVF_TEX1)

struct BLENDVERTEX
{
    D3DXVECTOR3 v;       // Referenced as v0 in the vertex shader
    FLOAT       blend1;  // Referenced as v1.x in the vertex shader
    FLOAT       blend2;  // Referenced as v1.y in the vertex shader
    FLOAT       blend3;  // Referenced as v1.z in the vertex shader
                         // v1.w = 1.0 - (v1.x + v1.y + v1.z)
    DWORD       indices; // Referenced as v2.xyzw in the vertex shader 
    D3DXVECTOR3 n;       // Referenced as v3 in the vertex shader
    FLOAT       tu, tv;  // Referenced as v7 in the vertex shader
};
```



## <a name="related-topics"></a><span data-ttu-id="27b89-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="27b89-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27b89-132">Dichiarazione vertici</span><span class="sxs-lookup"><span data-stu-id="27b89-132">Vertex Declaration</span></span>](vertex-declaration.md)
</dt> </dl>

 

 
