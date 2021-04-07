---
description: Le coordinate di trama in Direct3D possono includere uno, due, tre o quattro elementi a virgola mobile per indirizzare le trame con diversi livelli di dimensione.
ms.assetid: d841af62-41b0-4b80-960b-4630b9a7210c
title: Formati di coordinate di trama (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c95eada1cf21f0a4db38589794b08b88023e72d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747615"
---
# <a name="texture-coordinate-formats-direct3d-9"></a><span data-ttu-id="20896-103">Formati di coordinate di trama (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="20896-103">Texture Coordinate Formats (Direct3D 9)</span></span>

<span data-ttu-id="20896-104">Le coordinate di trama in Direct3D possono includere uno, due, tre o quattro elementi a virgola mobile per indirizzare le trame con diversi livelli di dimensione.</span><span class="sxs-lookup"><span data-stu-id="20896-104">Texture coordinates in Direct3D can include one, two, three, or four floating point elements to address textures with varying levels of dimension.</span></span> <span data-ttu-id="20896-105">Una trama 1D, ovvero una superficie di trama con dimensioni di Texel 1 per n, viene richiamata da una coordinata di trama.</span><span class="sxs-lookup"><span data-stu-id="20896-105">A 1D texture - a texture surface with dimensions of 1-by-n texels - is addressed by one texture coordinate.</span></span> <span data-ttu-id="20896-106">Il caso più comune, le trame 2D, vengono risolte con due coordinate di trama comunemente chiamate u e v.</span><span class="sxs-lookup"><span data-stu-id="20896-106">The most common case, 2D textures, are addressed with two texture coordinates commonly called u and v.</span></span> <span data-ttu-id="20896-107">Direct3D supporta due tipi di trame 3D, mappe dell'ambiente cubico e trame del volume.</span><span class="sxs-lookup"><span data-stu-id="20896-107">Direct3D supports two types of 3D textures, cubic-environment maps and volume textures.</span></span> <span data-ttu-id="20896-108">Le mappe dell'ambiente cubi non sono realmente 3D, ma vengono risolte con un vettore di 3 elementi.</span><span class="sxs-lookup"><span data-stu-id="20896-108">Cubic environment maps aren't truly 3D, but they are addressed with a 3-element vector.</span></span> <span data-ttu-id="20896-109">Per informazioni dettagliate, vedere [mapping di ambienti cubici (Direct3D 9)](cubic-environment-mapping.md).</span><span class="sxs-lookup"><span data-stu-id="20896-109">For details, see [Cubic Environment Mapping (Direct3D 9)](cubic-environment-mapping.md).</span></span>

<span data-ttu-id="20896-110">Come descritto in [codici FVF a funzione fissa (Direct3D 9)](fixed-function-fvf-codes.md), le applicazioni codificano le coordinate di trama nel formato vertice.</span><span class="sxs-lookup"><span data-stu-id="20896-110">As described in [Fixed Function FVF Codes (Direct3D 9)](fixed-function-fvf-codes.md), applications encode texture coordinates in the vertex format.</span></span> <span data-ttu-id="20896-111">Il formato Vertex può includere più set di coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="20896-111">The vertex format can include multiple sets of texture coordinates.</span></span> <span data-ttu-id="20896-112">Usare D3DFVF \_ TEX0 tramite D3DFVF \_ TEX8 [D3DFVF](d3dfvf.md) per descrivere un formato di vertice che non includa coordinate di trama o un numero di otto set.</span><span class="sxs-lookup"><span data-stu-id="20896-112">Use the D3DFVF\_TEX0 through D3DFVF\_TEX8 [D3DFVF](d3dfvf.md) to describe a vertex format that includes no texture coordinates, or as many as eight sets.</span></span>

<span data-ttu-id="20896-113">Ogni set di coordinate di trama può includere tra uno e quattro elementi.</span><span class="sxs-lookup"><span data-stu-id="20896-113">Each texture coordinate set can have between one and four elements.</span></span> <span data-ttu-id="20896-114">I \_ flag D3DFVF TEXTUREFORMAT1 through D3DFVF \_ TEXTUREFORMAT4 descrivono il numero di elementi in una coordinata di trama in un set, ma questi flag non vengono usati da soli.</span><span class="sxs-lookup"><span data-stu-id="20896-114">The D3DFVF\_TEXTUREFORMAT1 through D3DFVF\_TEXTUREFORMAT4 flags describe the number of elements in a texture coordinate in a set, but these flags aren't used by themselves.</span></span> <span data-ttu-id="20896-115">Piuttosto, il set di macro [**D3DFVF \_ TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) usa questi flag per creare modelli di bit che descrivono il numero di elementi usati da un particolare set di coordinate di trama nel formato vertice.</span><span class="sxs-lookup"><span data-stu-id="20896-115">Rather, the [**D3DFVF\_TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) set of macros use these flags to create bit patterns that describe the number of elements used by a particular set of texture coordinates in the vertex format.</span></span> <span data-ttu-id="20896-116">Queste macro accettano un singolo parametro che identifica l'indice del set di coordinate il cui numero di elementi viene definito.</span><span class="sxs-lookup"><span data-stu-id="20896-116">These macros accept a single parameter that identifies the index of the coordinate set whose number of elements is being defined.</span></span> <span data-ttu-id="20896-117">Nell'esempio seguente viene illustrata la modalità di utilizzo di queste macro.</span><span class="sxs-lookup"><span data-stu-id="20896-117">The following example illustrates how these macros are used.</span></span>


```
// This vertex format contains two sets of texture coordinates.
// The first set (index 0) has 2 elements, and the second set 
// has 1 element. The description for this vertex format would be: 
//     dwFVF = D3DFVF_XYZ  | D3DFVF_NORMAL | D3DFVF_DIFFUSE | D3DFVF_TEX2 |
//             D3DFVF_TEXCOORDSIZE2(0) | D3DFVF_TEXCOORDSIZE1(1); 
//
typedef struct CVF
{
    D3DVECTOR position;
    D3DVECTOR normal;
    D3DCOLOR  diffuse;
    float     u, v;   // 1st set, 2D
    float     t;      // 2nd set, 1D
} CustomVertexFormat;
```



> [!Note]  
> <span data-ttu-id="20896-118">Ad eccezione delle mappe dell'ambiente cubica e delle trame dei volumi, i rasterizzatori non possono indirizzare le trame usando più di due elementi.</span><span class="sxs-lookup"><span data-stu-id="20896-118">With the exception of cubic-environment maps and volume textures, rasterizers cannot address textures by using any more than two elements.</span></span> <span data-ttu-id="20896-119">Le applicazioni possono fornire fino a tre elementi per una coordinata di trama, ma solo se la trama è una mappa cubo, una trama del volume o il \_ flag di trasformazione della trama proiettata D3DTTFF.</span><span class="sxs-lookup"><span data-stu-id="20896-119">Applications can supply up to three elements for a texture coordinate, but only if the texture is a cube map, a volume texture, or the D3DTTFF\_PROJECTED texture transform flag is used.</span></span> <span data-ttu-id="20896-120">Il \_ flag proiettato D3DTTFF fa sì che il rasterizzatore divida i primi due elementi per il terzo elemento (o n).</span><span class="sxs-lookup"><span data-stu-id="20896-120">The D3DTTFF\_PROJECTED flag causes the rasterizer to divide the first two elements by the third (or n) element.</span></span> <span data-ttu-id="20896-121">Per altre informazioni, vedere [trasformazioni di coordinate di trama (Direct3D 9)](texture-coordinate-transformations.md).</span><span class="sxs-lookup"><span data-stu-id="20896-121">For more information, see [Texture Coordinate Transformations (Direct3D 9)](texture-coordinate-transformations.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="20896-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="20896-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20896-123">Coordinate di trama</span><span class="sxs-lookup"><span data-stu-id="20896-123">Texture Coordinates</span></span>](texture-coordinates.md)
</dt> </dl>

 

 



