---
description: Le costanti di formato dei vertici flessibili, o codici FVF, vengono usate per descrivere il contenuto dei vertici interfoliati in un singolo flusso di dati che verrà elaborato dalla pipeline a funzione fissa.
ms.assetid: 85d9f5b2-8e4a-4f92-a587-eae5b293778c
title: D3DFVF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25a12b4f6008023a388bd204440a0b544db85c19
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999438"
---
# <a name="d3dfvf"></a><span data-ttu-id="3e33a-103">D3DFVF</span><span class="sxs-lookup"><span data-stu-id="3e33a-103">D3DFVF</span></span>

<span data-ttu-id="3e33a-104">Le costanti di formato dei vertici flessibili, o codici FVF, vengono usate per descrivere il contenuto dei vertici interfoliati in un singolo flusso di dati che verrà elaborato dalla pipeline a funzione fissa.</span><span class="sxs-lookup"><span data-stu-id="3e33a-104">Flexible Vertex Format Constants, or FVF codes, are used to describe the contents of vertices interleaved in a single data stream that will be processed by the fixed-function pipeline.</span></span>

## <a name="vertex-data-flags"></a><span data-ttu-id="3e33a-105">Flag di dati dei vertici</span><span class="sxs-lookup"><span data-stu-id="3e33a-105">Vertex Data Flags</span></span>

<span data-ttu-id="3e33a-106">I flag seguenti descrivono un formato di vertice.</span><span class="sxs-lookup"><span data-stu-id="3e33a-106">The following flags describe a vertex format.</span></span> <span data-ttu-id="3e33a-107">Per informazioni sui formati dei vertici, vedere Codici FVF delle funzioni [fisse (Direct3D 9).](fixed-function-fvf-codes.md)</span><span class="sxs-lookup"><span data-stu-id="3e33a-107">For information regarding vertex formats, see [Fixed Function FVF Codes (Direct3D 9)](fixed-function-fvf-codes.md).</span></span>



| <span data-ttu-id="3e33a-108">\#Definire</span><span class="sxs-lookup"><span data-stu-id="3e33a-108">\#define</span></span>                            | <span data-ttu-id="3e33a-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3e33a-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                             | <span data-ttu-id="3e33a-110">Ordine e tipo dei dati</span><span class="sxs-lookup"><span data-stu-id="3e33a-110">Data order and type</span></span>                                                                                       |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e33a-111">D3DFVF \_ DIFFUSE</span><span class="sxs-lookup"><span data-stu-id="3e33a-111">D3DFVF\_DIFFUSE</span></span>                     | <span data-ttu-id="3e33a-112">Il formato vertice include un componente di colore diffuso.</span><span class="sxs-lookup"><span data-stu-id="3e33a-112">Vertex format includes a diffuse color component.</span></span>                                                                                                                                                                                                                                                                                                                       | <span data-ttu-id="3e33a-113">DWORD in ordine ARGB.</span><span class="sxs-lookup"><span data-stu-id="3e33a-113">DWORD in ARGB order.</span></span> <span data-ttu-id="3e33a-114">Vedere [**D3DCOLOR \_ ARGB**](d3dcolor-argb.md).</span><span class="sxs-lookup"><span data-stu-id="3e33a-114">See [**D3DCOLOR\_ARGB**](d3dcolor-argb.md).</span></span>                                         |
| <span data-ttu-id="3e33a-115">D3DFVF \_ NORMAL</span><span class="sxs-lookup"><span data-stu-id="3e33a-115">D3DFVF\_NORMAL</span></span>                      | <span data-ttu-id="3e33a-116">Il formato vertice include un vettore normale dei vertici.</span><span class="sxs-lookup"><span data-stu-id="3e33a-116">Vertex format includes a vertex normal vector.</span></span> <span data-ttu-id="3e33a-117">Questo flag non può essere usato con il flag D3DFVF \_ XYZRHW.</span><span class="sxs-lookup"><span data-stu-id="3e33a-117">This flag cannot be used with the D3DFVF\_XYZRHW flag.</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="3e33a-118">float, float, float</span><span class="sxs-lookup"><span data-stu-id="3e33a-118">float, float, float</span></span>                                                                                       |
| <span data-ttu-id="3e33a-119">D3DFVF \_ PSIZE</span><span class="sxs-lookup"><span data-stu-id="3e33a-119">D3DFVF\_PSIZE</span></span>                       | <span data-ttu-id="3e33a-120">Formato del vertice specificato in dimensioni in punti.</span><span class="sxs-lookup"><span data-stu-id="3e33a-120">Vertex format specified in point size.</span></span> <span data-ttu-id="3e33a-121">Queste dimensioni sono espresse in unità dello spazio della fotocamera per i vertici che non vengono trasformati e accesi e in unità di spazio del dispositivo per i vertici trasformati e accesi.</span><span class="sxs-lookup"><span data-stu-id="3e33a-121">This size is expressed in camera space units for vertices that are not transformed and lit, and in device-space units for transformed and lit vertices.</span></span>                                                                                                                                                                          | <span data-ttu-id="3e33a-122">float</span><span class="sxs-lookup"><span data-stu-id="3e33a-122">float</span></span>                                                                                                     |
| <span data-ttu-id="3e33a-123">D3DFVF \_ SPECULAR</span><span class="sxs-lookup"><span data-stu-id="3e33a-123">D3DFVF\_SPECULAR</span></span>                    | <span data-ttu-id="3e33a-124">Il formato vertice include un componente di colore speculare.</span><span class="sxs-lookup"><span data-stu-id="3e33a-124">Vertex format includes a specular color component.</span></span>                                                                                                                                                                                                                                                                                                                      | <span data-ttu-id="3e33a-125">DWORD in ordine ARGB.</span><span class="sxs-lookup"><span data-stu-id="3e33a-125">DWORD in ARGB order.</span></span> <span data-ttu-id="3e33a-126">Vedere [**D3DCOLOR \_ ARGB.**](d3dcolor-argb.md)</span><span class="sxs-lookup"><span data-stu-id="3e33a-126">See [**D3DCOLOR\_ARGB**](d3dcolor-argb.md).</span></span>                                         |
| <span data-ttu-id="3e33a-127">D3DFVF \_ XYZ</span><span class="sxs-lookup"><span data-stu-id="3e33a-127">D3DFVF\_XYZ</span></span>                         | <span data-ttu-id="3e33a-128">Il formato vertice include la posizione di un vertice non trasformato.</span><span class="sxs-lookup"><span data-stu-id="3e33a-128">Vertex format includes the position of an untransformed vertex.</span></span> <span data-ttu-id="3e33a-129">Questo flag non può essere usato con il flag D3DFVF \_ XYZRHW.</span><span class="sxs-lookup"><span data-stu-id="3e33a-129">This flag cannot be used with the D3DFVF\_XYZRHW flag.</span></span>                                                                                                                                                                                                                                                  | <span data-ttu-id="3e33a-130">float, float, float.</span><span class="sxs-lookup"><span data-stu-id="3e33a-130">float, float, float.</span></span>                                                                                      |
| <span data-ttu-id="3e33a-131">D3DFVF \_ XYZRHW</span><span class="sxs-lookup"><span data-stu-id="3e33a-131">D3DFVF\_XYZRHW</span></span>                      | <span data-ttu-id="3e33a-132">Il formato vertice include la posizione di un vertice trasformato.</span><span class="sxs-lookup"><span data-stu-id="3e33a-132">Vertex format includes the position of a transformed vertex.</span></span> <span data-ttu-id="3e33a-133">Questo flag non può essere usato con i flag D3DFVF \_ XYZ o D3DFVF \_ NORMAL.</span><span class="sxs-lookup"><span data-stu-id="3e33a-133">This flag cannot be used with the D3DFVF\_XYZ or D3DFVF\_NORMAL flags.</span></span>                                                                                                                                                                                                                                     | <span data-ttu-id="3e33a-134">float, float, float, float.</span><span class="sxs-lookup"><span data-stu-id="3e33a-134">float, float, float, float.</span></span>                                                                               |
| <span data-ttu-id="3e33a-135">Da D3DFVF \_ XYZB1 a D3DFVF \_ XYZB5</span><span class="sxs-lookup"><span data-stu-id="3e33a-135">D3DFVF\_XYZB1 through D3DFVF\_XYZB5</span></span> | <span data-ttu-id="3e33a-136">Il formato vertice contiene i dati sulla posizione e un numero corrispondente di valori di ponderazione (beta) da usare per le operazioni di fusione dei vertici multimatrix.</span><span class="sxs-lookup"><span data-stu-id="3e33a-136">Vertex format contains position data, and a corresponding number of weighting (beta) values to use for multimatrix vertex blending operations.</span></span> <span data-ttu-id="3e33a-137">Attualmente, Direct3D può essere misto con un massimo di tre valori di ponderazione e quattro matrici di fusione.</span><span class="sxs-lookup"><span data-stu-id="3e33a-137">Currently, Direct3D can blend with up to three weighting values and four blending matrices.</span></span> <span data-ttu-id="3e33a-138">Per altre informazioni sull'uso delle matrici di blending, vedere [Indexed Vertex Blending (Direct3D 9) (Blending vertici indicizzati (Direct3D 9)](indexed-vertex-blending.md)).</span><span class="sxs-lookup"><span data-stu-id="3e33a-138">For more information about using blending matrices, see [Indexed Vertex Blending (Direct3D 9)](indexed-vertex-blending.md).</span></span> | <span data-ttu-id="3e33a-139">1, 2 o 3 float.</span><span class="sxs-lookup"><span data-stu-id="3e33a-139">1, 2, or 3 floats.</span></span> <span data-ttu-id="3e33a-140">Quando si usa D3DFVF \_ LASTBETA UBYTE4, l'ultimo peso di fusione viene \_ considerato come DWORD.</span><span class="sxs-lookup"><span data-stu-id="3e33a-140">When D3DFVF\_LASTBETA\_UBYTE4 is used, the last blending weight is treated as a DWORD.</span></span> |
| <span data-ttu-id="3e33a-141">D3DFVF \_ XYZW</span><span class="sxs-lookup"><span data-stu-id="3e33a-141">D3DFVF\_XYZW</span></span>                        | <span data-ttu-id="3e33a-142">Il formato vertice contiene dati trasformati e ritagliati (x, y, z, w).</span><span class="sxs-lookup"><span data-stu-id="3e33a-142">Vertex format contains transformed and clipped (x, y, z, w) data.</span></span> <span data-ttu-id="3e33a-143">ProcessVertices non richiama il clipper, ma restituisce i dati nelle coordinate del clip.</span><span class="sxs-lookup"><span data-stu-id="3e33a-143">ProcessVertices does not invoke the clipper, instead outputting data in clip coordinates.</span></span> <span data-ttu-id="3e33a-144">Questa costante è progettata per e può essere usata solo con la pipeline dei vertici programmabili.</span><span class="sxs-lookup"><span data-stu-id="3e33a-144">This constant is designed for, and can only be used with, the programmable vertex pipeline.</span></span>                                                                                                                 | <span data-ttu-id="3e33a-145">float, float, float, float</span><span class="sxs-lookup"><span data-stu-id="3e33a-145">float, float, float, float</span></span>                                                                                |



 

## <a name="texture-flags"></a><span data-ttu-id="3e33a-146">Flag di trama</span><span class="sxs-lookup"><span data-stu-id="3e33a-146">Texture Flags</span></span>

<span data-ttu-id="3e33a-147">I flag seguenti descrivono i flag di trama usati dalla pipeline a funzione fissa.</span><span class="sxs-lookup"><span data-stu-id="3e33a-147">The following flags describe texture flags used by the fixed-function pipeline.</span></span>



| <span data-ttu-id="3e33a-148">\#Definire</span><span class="sxs-lookup"><span data-stu-id="3e33a-148">\#define</span></span>                          | <span data-ttu-id="3e33a-149">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3e33a-149">Description</span></span>                                                                                                                                                                                                                                                                        |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e33a-150">D3DFVF \_ TEX0 - D3DFVF \_ TEX8</span><span class="sxs-lookup"><span data-stu-id="3e33a-150">D3DFVF\_TEX0 - D3DFVF\_TEX8</span></span>       | <span data-ttu-id="3e33a-151">Numero di set di coordinate di trama per questo vertice.</span><span class="sxs-lookup"><span data-stu-id="3e33a-151">Number of texture coordinate sets for this vertex.</span></span> <span data-ttu-id="3e33a-152">I valori effettivi per questi flag non sono sequenziali.</span><span class="sxs-lookup"><span data-stu-id="3e33a-152">The actual values for these flags are not sequential.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="3e33a-153">D3DFVF \_ TEXCOORDSIZEN(coordIndex)</span><span class="sxs-lookup"><span data-stu-id="3e33a-153">D3DFVF\_TEXCOORDSIZEN(coordIndex)</span></span> | <span data-ttu-id="3e33a-154">Definire un set di dati delle coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="3e33a-154">Define a texture coordinate data set.</span></span> <span data-ttu-id="3e33a-155">n indica la dimensione delle coordinate della trama.</span><span class="sxs-lookup"><span data-stu-id="3e33a-155">n indicates the dimension of the texture coordinates.</span></span> <span data-ttu-id="3e33a-156">coordIndex indica il numero di indice delle coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="3e33a-156">coordIndex indicates texture coordinate index number.</span></span> <span data-ttu-id="3e33a-157">Vedere [**D3DFVF \_ TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) e [Coordinate trama e Fasi trama](texture-coordinates.md).</span><span class="sxs-lookup"><span data-stu-id="3e33a-157">See [**D3DFVF\_TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) and [Texture coordinates and Texture Stages](texture-coordinates.md).</span></span> |



 

## <a name="mask-flags"></a><span data-ttu-id="3e33a-158">Flag di maschera</span><span class="sxs-lookup"><span data-stu-id="3e33a-158">Mask Flags</span></span>

<span data-ttu-id="3e33a-159">I flag seguenti descrivono i flag di maschera usati dalla pipeline di funzioni fisse.</span><span class="sxs-lookup"><span data-stu-id="3e33a-159">The following flags describe mask flags used by the fixed-function pipeline.</span></span>



| <span data-ttu-id="3e33a-160">\#Definire</span><span class="sxs-lookup"><span data-stu-id="3e33a-160">\#define</span></span>                             | <span data-ttu-id="3e33a-161">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3e33a-161">Description</span></span>                                           |
|--------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="3e33a-162">MASCHERA DI POSIZIONE D3DFVF \_ \_</span><span class="sxs-lookup"><span data-stu-id="3e33a-162">D3DFVF\_POSITION\_MASK</span></span>               | <span data-ttu-id="3e33a-163">Maschera per i bit di posizione.</span><span class="sxs-lookup"><span data-stu-id="3e33a-163">Mask for position bits.</span></span>                               |
| <span data-ttu-id="3e33a-164">D3DFVF \_ RESERVED0, D3DFVF \_ RESERVED2</span><span class="sxs-lookup"><span data-stu-id="3e33a-164">D3DFVF\_RESERVED0, D3DFVF\_RESERVED2</span></span> | <span data-ttu-id="3e33a-165">Mascherare i valori per i bit riservati in FVF.</span><span class="sxs-lookup"><span data-stu-id="3e33a-165">Mask values for reserved bits in the FVF.</span></span> <span data-ttu-id="3e33a-166">Non usare.</span><span class="sxs-lookup"><span data-stu-id="3e33a-166">Do not use.</span></span> |
| <span data-ttu-id="3e33a-167">MASCHERA D3DFVF \_ TEXCOUNT \_</span><span class="sxs-lookup"><span data-stu-id="3e33a-167">D3DFVF\_TEXCOUNT\_MASK</span></span>               | <span data-ttu-id="3e33a-168">Valore della maschera per i bit del flag di trama.</span><span class="sxs-lookup"><span data-stu-id="3e33a-168">Mask value for texture flag bits.</span></span>                     |



 

## <a name="miscellaneous-flags"></a><span data-ttu-id="3e33a-169">Flag vari</span><span class="sxs-lookup"><span data-stu-id="3e33a-169">Miscellaneous Flags</span></span>

<span data-ttu-id="3e33a-170">I flag seguenti descrivono un'ampia gamma di flag usati dalla pipeline a funzione fissa.</span><span class="sxs-lookup"><span data-stu-id="3e33a-170">The following flags describe a variety of flags used by the fixed-function pipeline.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3e33a-171">#Definire</span><span class="sxs-lookup"><span data-stu-id="3e33a-171">#define</span></span></td>
<td><span data-ttu-id="3e33a-172">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3e33a-172">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3e33a-173">D3DFVF_LASTBETA_D3DCOLOR</span><span class="sxs-lookup"><span data-stu-id="3e33a-173">D3DFVF_LASTBETA_D3DCOLOR</span></span></td>
<td><span data-ttu-id="3e33a-174">L'ultimo campo beta nei dati della posizione del vertice sarà di tipo D3DCOLOR.</span><span class="sxs-lookup"><span data-stu-id="3e33a-174">The last beta field in the vertex position data will be of type D3DCOLOR.</span></span> <span data-ttu-id="3e33a-175">I dati nei campi beta vengono usati con l'interfaccia della tavolozza della matrice per specificare gli indici della matrice.</span><span class="sxs-lookup"><span data-stu-id="3e33a-175">The data in the beta fields are used with matrix palette skinning to specify matrix indices.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3e33a-176">D3DFVF_LASTBETA_UBYTE4</span><span class="sxs-lookup"><span data-stu-id="3e33a-176">D3DFVF_LASTBETA_UBYTE4</span></span></td>
<td><span data-ttu-id="3e33a-177">L'ultimo campo beta nei dati della posizione dei vertici sarà di tipo UBYTE4.</span><span class="sxs-lookup"><span data-stu-id="3e33a-177">The last beta field in the vertex position data will be of type UBYTE4.</span></span> <span data-ttu-id="3e33a-178">I dati nei campi beta vengono usati con l'interfaccia della tavolozza della matrice per specificare gli indici della matrice.</span><span class="sxs-lookup"><span data-stu-id="3e33a-178">The data in the beta fields are used with matrix palette skinning to specify matrix indices.</span></span> <span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>// Given the following vertex data definition: 
struct VERTEXPOSITION
{
   float pos[3];
   union 
   {
      float beta[5];
      struct
      {
         float weights[4];
         DWORD MatrixIndices;  // Used as UBYTEs
      }
   }
};</code></pre></td>
</tr>
</tbody>
</table>

<p><span data-ttu-id="3e33a-179">Dato che FVF è dichiarato come: D3DFVF_XYZB5 | D3DFVF_LASTBETA_UBYTE4.</span><span class="sxs-lookup"><span data-stu-id="3e33a-179">Given the FVF is declared as: D3DFVF_XYZB5 | D3DFVF_LASTBETA_UBYTE4.</span></span> <span data-ttu-id="3e33a-180">Weight e MatrixIndices sono inclusi nella versione beta[5], dove D3DFVF_LASTBETA_UBYTE4 indica di interpretare l'ultima DWORD in beta[5] come tipo UBYTE4.</span><span class="sxs-lookup"><span data-stu-id="3e33a-180">Weight and MatrixIndices are included in beta[5], where D3DFVF_LASTBETA_UBYTE4 says to interpret the last DWORD in beta[5] as type UBYTE4.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3e33a-181">D3DFVF_TEXCOUNT_SHIFT</span><span class="sxs-lookup"><span data-stu-id="3e33a-181">D3DFVF_TEXCOUNT_SHIFT</span></span></td>
<td><span data-ttu-id="3e33a-182">Numero di bit in base al quale spostare un valore intero che identifica il numero di coordinate di trama per un vertice.</span><span class="sxs-lookup"><span data-stu-id="3e33a-182">The number of bits by which to shift an integer value that identifies the number of texture coordinates for a vertex.</span></span> <span data-ttu-id="3e33a-183">Questo valore può essere usato come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="3e33a-183">This value might be used as shown below.</span></span>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>DWORD dwNumTextures = 1;  // Vertex has only one set of coordinates.

// Shift the value for use when creating a 
//   flexible vertex format (FVF) combination.
dwFVF = dwNumTextures << D3DFVF_TEXCOUNT_SHIFT;

// Now, create an FVF combination using the shifted value.</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

### <a name="examples"></a><span data-ttu-id="3e33a-184">Esempio</span><span class="sxs-lookup"><span data-stu-id="3e33a-184">Examples</span></span>

<span data-ttu-id="3e33a-185">Gli esempi seguenti illustrano altre combinazioni di flag comuni.</span><span class="sxs-lookup"><span data-stu-id="3e33a-185">The following examples show other common flag combinations.</span></span>


```
// Untransformed vertex for lit, untextured, Gouraud-shaded content.
dwFVF = ( D3DFVF_XYZ | D3DFVF_DIFFUSE );
```




```
// Untransformed vertex for unlit, untextured, Gouraud-shaded 
//   content with diffuse material color specified per vertex.
dwFVF = ( D3DFVF_XYZ | D3DFVF_NORMAL | D3DFVF_DIFFUSE );
```




```
// Untransformed vertex for light-map-based lighting.
dwFVF = ( D3DFVF_XYZ | D3DFVF_TEX2 );
```




```
// Transformed vertex for light-map-based lighting with shared rhw.
dwFVF = ( D3DFVF_XYZRHW | D3DFVF_TEX2 );
```




```
// Heavyweight vertex for unlit, colored content with two 
//   sets of texture coordinates.
dwFVF = ( D3DFVF_XYZ | D3DFVF_NORMAL | D3DFVF_DIFFUSE | 
          D3DFVF_SPECULAR | D3DFVF_TEX2 );
```



## <a name="constant-information"></a><span data-ttu-id="3e33a-186">Informazioni costanti</span><span class="sxs-lookup"><span data-stu-id="3e33a-186">Constant Information</span></span>



|                          |             |
|--------------------------|-------------|
| <span data-ttu-id="3e33a-187">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3e33a-187">Header</span></span>                   | <span data-ttu-id="3e33a-188">d3d9types.h</span><span class="sxs-lookup"><span data-stu-id="3e33a-188">d3d9types.h</span></span> |
| <span data-ttu-id="3e33a-189">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="3e33a-189">Minimum operating system</span></span> | <span data-ttu-id="3e33a-190">Windows 98</span><span class="sxs-lookup"><span data-stu-id="3e33a-190">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="3e33a-191">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3e33a-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e33a-192">Costanti Direct3D</span><span class="sxs-lookup"><span data-stu-id="3e33a-192">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[<span data-ttu-id="3e33a-193">Codici FVF delle funzioni fisse (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="3e33a-193">Fixed Function FVF Codes (Direct3D 9)</span></span>](fixed-function-fvf-codes.md)
</dt> <dt>

[<span data-ttu-id="3e33a-194">Blending geometrico (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="3e33a-194">Geometry Blending (Direct3D 9)</span></span>](geometry-blending.md)
</dt> </dl>

 

 



