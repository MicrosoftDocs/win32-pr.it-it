---
description: Le costanti di formato vertex flessibili o i codici FVF vengono usati per descrivere il contenuto dei vertici con interfoliazione in un singolo flusso di dati che verrà elaborato dalla pipeline a funzione fissa.
ms.assetid: 85d9f5b2-8e4a-4f92-a587-eae5b293778c
title: D3DFVF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d4bfc1dcabdb6991b49af967bb596fd4c1e3bdd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305048"
---
# <a name="d3dfvf"></a><span data-ttu-id="effdb-103">D3DFVF</span><span class="sxs-lookup"><span data-stu-id="effdb-103">D3DFVF</span></span>

<span data-ttu-id="effdb-104">Le costanti di formato vertex flessibili o i codici FVF vengono usati per descrivere il contenuto dei vertici con interfoliazione in un singolo flusso di dati che verrà elaborato dalla pipeline a funzione fissa.</span><span class="sxs-lookup"><span data-stu-id="effdb-104">Flexible Vertex Format Constants, or FVF codes, are used to describe the contents of vertices interleaved in a single data stream that will be processed by the fixed-function pipeline.</span></span>

## <a name="vertex-data-flags"></a><span data-ttu-id="effdb-105">Flag di dati dei vertici</span><span class="sxs-lookup"><span data-stu-id="effdb-105">Vertex Data Flags</span></span>

<span data-ttu-id="effdb-106">I flag seguenti descrivono un formato vertici.</span><span class="sxs-lookup"><span data-stu-id="effdb-106">The following flags describe a vertex format.</span></span> <span data-ttu-id="effdb-107">Per informazioni sui formati dei vertici, vedere [codici FVF della funzione fissa (Direct3D 9)](fixed-function-fvf-codes.md).</span><span class="sxs-lookup"><span data-stu-id="effdb-107">For information regarding vertex formats, see [Fixed Function FVF Codes (Direct3D 9)](fixed-function-fvf-codes.md).</span></span>



|                                     |                                                                                                                                                                                                                                                                                                                                                                         |                                                                                                           |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="effdb-108">\#definire</span><span class="sxs-lookup"><span data-stu-id="effdb-108">\#define</span></span>                            | <span data-ttu-id="effdb-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="effdb-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                             | <span data-ttu-id="effdb-110">Ordine e tipo di dati</span><span class="sxs-lookup"><span data-stu-id="effdb-110">Data order and type</span></span>                                                                                       |
| <span data-ttu-id="effdb-111">D3DFVF \_ diffuse</span><span class="sxs-lookup"><span data-stu-id="effdb-111">D3DFVF\_DIFFUSE</span></span>                     | <span data-ttu-id="effdb-112">Il formato del vertice include un componente colore diffuso.</span><span class="sxs-lookup"><span data-stu-id="effdb-112">Vertex format includes a diffuse color component.</span></span>                                                                                                                                                                                                                                                                                                                       | <span data-ttu-id="effdb-113">DWORD in ordine ARGB.</span><span class="sxs-lookup"><span data-stu-id="effdb-113">DWORD in ARGB order.</span></span> <span data-ttu-id="effdb-114">Vedere [**D3DCOLOR \_ ARGB**](d3dcolor-argb.md).</span><span class="sxs-lookup"><span data-stu-id="effdb-114">See [**D3DCOLOR\_ARGB**](d3dcolor-argb.md).</span></span>                                         |
| <span data-ttu-id="effdb-115">D3DFVF \_ normale</span><span class="sxs-lookup"><span data-stu-id="effdb-115">D3DFVF\_NORMAL</span></span>                      | <span data-ttu-id="effdb-116">Il formato del vertice include un vettore di normale vertice.</span><span class="sxs-lookup"><span data-stu-id="effdb-116">Vertex format includes a vertex normal vector.</span></span> <span data-ttu-id="effdb-117">Questo flag non può essere usato con il \_ flag XYZRHW di D3DFVF.</span><span class="sxs-lookup"><span data-stu-id="effdb-117">This flag cannot be used with the D3DFVF\_XYZRHW flag.</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="effdb-118">float, float, float</span><span class="sxs-lookup"><span data-stu-id="effdb-118">float, float, float</span></span>                                                                                       |
| <span data-ttu-id="effdb-119">\_PSIZE D3DFVF</span><span class="sxs-lookup"><span data-stu-id="effdb-119">D3DFVF\_PSIZE</span></span>                       | <span data-ttu-id="effdb-120">Formato vertice specificato in dimensioni punto.</span><span class="sxs-lookup"><span data-stu-id="effdb-120">Vertex format specified in point size.</span></span> <span data-ttu-id="effdb-121">Questa dimensione è espressa in unità di spazio della fotocamera per i vertici che non sono trasformati e illuminati e in unità di spazio del dispositivo per i vertici trasformati e illuminati.</span><span class="sxs-lookup"><span data-stu-id="effdb-121">This size is expressed in camera space units for vertices that are not transformed and lit, and in device-space units for transformed and lit vertices.</span></span>                                                                                                                                                                          | <span data-ttu-id="effdb-122">float</span><span class="sxs-lookup"><span data-stu-id="effdb-122">float</span></span>                                                                                                     |
| <span data-ttu-id="effdb-123">D3DFVF \_ speculare</span><span class="sxs-lookup"><span data-stu-id="effdb-123">D3DFVF\_SPECULAR</span></span>                    | <span data-ttu-id="effdb-124">Il formato del vertice include un componente colore speculare.</span><span class="sxs-lookup"><span data-stu-id="effdb-124">Vertex format includes a specular color component.</span></span>                                                                                                                                                                                                                                                                                                                      | <span data-ttu-id="effdb-125">DWORD in ordine ARGB.</span><span class="sxs-lookup"><span data-stu-id="effdb-125">DWORD in ARGB order.</span></span> <span data-ttu-id="effdb-126">Vedere [**D3DCOLOR \_ ARGB**](d3dcolor-argb.md).</span><span class="sxs-lookup"><span data-stu-id="effdb-126">See [**D3DCOLOR\_ARGB**](d3dcolor-argb.md).</span></span>                                         |
| <span data-ttu-id="effdb-127">D3DFVF \_ XYZ</span><span class="sxs-lookup"><span data-stu-id="effdb-127">D3DFVF\_XYZ</span></span>                         | <span data-ttu-id="effdb-128">Il formato del vertice include la posizione di un vertice non trasformato.</span><span class="sxs-lookup"><span data-stu-id="effdb-128">Vertex format includes the position of an untransformed vertex.</span></span> <span data-ttu-id="effdb-129">Questo flag non può essere usato con il \_ flag XYZRHW di D3DFVF.</span><span class="sxs-lookup"><span data-stu-id="effdb-129">This flag cannot be used with the D3DFVF\_XYZRHW flag.</span></span>                                                                                                                                                                                                                                                  | <span data-ttu-id="effdb-130">float, float, float.</span><span class="sxs-lookup"><span data-stu-id="effdb-130">float, float, float.</span></span>                                                                                      |
| <span data-ttu-id="effdb-131">\_XYZRHW D3DFVF</span><span class="sxs-lookup"><span data-stu-id="effdb-131">D3DFVF\_XYZRHW</span></span>                      | <span data-ttu-id="effdb-132">Il formato del vertice include la posizione di un vertice trasformato.</span><span class="sxs-lookup"><span data-stu-id="effdb-132">Vertex format includes the position of a transformed vertex.</span></span> <span data-ttu-id="effdb-133">Non è possibile usare questo flag con i \_ flag normali D3DFVF XYZ o D3DFVF \_ .</span><span class="sxs-lookup"><span data-stu-id="effdb-133">This flag cannot be used with the D3DFVF\_XYZ or D3DFVF\_NORMAL flags.</span></span>                                                                                                                                                                                                                                     | <span data-ttu-id="effdb-134">float, float, float, float.</span><span class="sxs-lookup"><span data-stu-id="effdb-134">float, float, float, float.</span></span>                                                                               |
| <span data-ttu-id="effdb-135">D3DFVF \_ XYZB1 tramite D3DFVF \_ XYZB5</span><span class="sxs-lookup"><span data-stu-id="effdb-135">D3DFVF\_XYZB1 through D3DFVF\_XYZB5</span></span> | <span data-ttu-id="effdb-136">Il formato vertici contiene i dati di posizione e un numero corrispondente di valori di ponderazione (beta) da usare per le operazioni di fusione dei vertici a più matrici.</span><span class="sxs-lookup"><span data-stu-id="effdb-136">Vertex format contains position data, and a corresponding number of weighting (beta) values to use for multimatrix vertex blending operations.</span></span> <span data-ttu-id="effdb-137">Attualmente, Direct3D può unire fino a tre valori di ponderazione e quattro matrici di Blend.</span><span class="sxs-lookup"><span data-stu-id="effdb-137">Currently, Direct3D can blend with up to three weighting values and four blending matrices.</span></span> <span data-ttu-id="effdb-138">Per ulteriori informazioni sull'utilizzo di matrici di fusione, vedere [indexed Vertex blending (Direct3D 9)](indexed-vertex-blending.md).</span><span class="sxs-lookup"><span data-stu-id="effdb-138">For more information about using blending matrices, see [Indexed Vertex Blending (Direct3D 9)](indexed-vertex-blending.md).</span></span> | <span data-ttu-id="effdb-139">1, 2 o 3 float.</span><span class="sxs-lookup"><span data-stu-id="effdb-139">1, 2, or 3 floats.</span></span> <span data-ttu-id="effdb-140">Quando \_ \_ si usa D3DFVF LASTBETA UBYTE4, l'ultimo peso della fusione viene considerato come un valore DWORD.</span><span class="sxs-lookup"><span data-stu-id="effdb-140">When D3DFVF\_LASTBETA\_UBYTE4 is used, the last blending weight is treated as a DWORD.</span></span> |
| <span data-ttu-id="effdb-141">\_XYZW D3DFVF</span><span class="sxs-lookup"><span data-stu-id="effdb-141">D3DFVF\_XYZW</span></span>                        | <span data-ttu-id="effdb-142">Il formato del vertice contiene dati trasformati e ritagliati (x, y, z, w).</span><span class="sxs-lookup"><span data-stu-id="effdb-142">Vertex format contains transformed and clipped (x, y, z, w) data.</span></span> <span data-ttu-id="effdb-143">ProcessVertices non richiama il Clipper, bensì l'output dei dati nelle coordinate di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="effdb-143">ProcessVertices does not invoke the clipper, instead outputting data in clip coordinates.</span></span> <span data-ttu-id="effdb-144">Questa costante è progettata per e può essere usata solo con, la pipeline di vertici programmabile.</span><span class="sxs-lookup"><span data-stu-id="effdb-144">This constant is designed for, and can only be used with, the programmable vertex pipeline.</span></span>                                                                                                                 | <span data-ttu-id="effdb-145">float, float, float, float</span><span class="sxs-lookup"><span data-stu-id="effdb-145">float, float, float, float</span></span>                                                                                |



 

## <a name="texture-flags"></a><span data-ttu-id="effdb-146">Flag di trama</span><span class="sxs-lookup"><span data-stu-id="effdb-146">Texture Flags</span></span>

<span data-ttu-id="effdb-147">I flag seguenti descrivono i flag di trama utilizzati dalla pipeline a funzione fissa.</span><span class="sxs-lookup"><span data-stu-id="effdb-147">The following flags describe texture flags used by the fixed-function pipeline.</span></span>



|                                   |                                                                                                                                                                                                                                                                                    |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="effdb-148">\#definire</span><span class="sxs-lookup"><span data-stu-id="effdb-148">\#define</span></span>                          | <span data-ttu-id="effdb-149">Descrizione</span><span class="sxs-lookup"><span data-stu-id="effdb-149">Description</span></span>                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="effdb-150">D3DFVF \_ TEX0-D3DFVF \_ TEX8</span><span class="sxs-lookup"><span data-stu-id="effdb-150">D3DFVF\_TEX0 - D3DFVF\_TEX8</span></span>       | <span data-ttu-id="effdb-151">Numero di set di coordinate di trama per questo vertice.</span><span class="sxs-lookup"><span data-stu-id="effdb-151">Number of texture coordinate sets for this vertex.</span></span> <span data-ttu-id="effdb-152">I valori effettivi per questi flag non sono sequenziali.</span><span class="sxs-lookup"><span data-stu-id="effdb-152">The actual values for these flags are not sequential.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="effdb-153">D3DFVF \_ TEXCOORDSIZEN (coordIndex)</span><span class="sxs-lookup"><span data-stu-id="effdb-153">D3DFVF\_TEXCOORDSIZEN(coordIndex)</span></span> | <span data-ttu-id="effdb-154">Definire un set di dati di coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="effdb-154">Define a texture coordinate data set.</span></span> <span data-ttu-id="effdb-155">n indica la dimensione delle coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="effdb-155">n indicates the dimension of the texture coordinates.</span></span> <span data-ttu-id="effdb-156">coordIndex indica il numero di indice delle coordinate di trama.</span><span class="sxs-lookup"><span data-stu-id="effdb-156">coordIndex indicates texture coordinate index number.</span></span> <span data-ttu-id="effdb-157">Vedere [**D3DFVF \_ TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) e [coordinate di trama e fasi della trama](texture-coordinates.md).</span><span class="sxs-lookup"><span data-stu-id="effdb-157">See [**D3DFVF\_TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) and [Texture coordinates and Texture Stages](texture-coordinates.md).</span></span> |



 

## <a name="mask-flags"></a><span data-ttu-id="effdb-158">Flag maschera</span><span class="sxs-lookup"><span data-stu-id="effdb-158">Mask Flags</span></span>

<span data-ttu-id="effdb-159">I flag seguenti descrivono i flag della maschera usati dalla pipeline a funzione fissa.</span><span class="sxs-lookup"><span data-stu-id="effdb-159">The following flags describe mask flags used by the fixed-function pipeline.</span></span>



|                                      |                                                       |
|--------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="effdb-160">\#definire</span><span class="sxs-lookup"><span data-stu-id="effdb-160">\#define</span></span>                             | <span data-ttu-id="effdb-161">Descrizione</span><span class="sxs-lookup"><span data-stu-id="effdb-161">Description</span></span>                                           |
| <span data-ttu-id="effdb-162">\_Maschera posizione \_ D3DFVF</span><span class="sxs-lookup"><span data-stu-id="effdb-162">D3DFVF\_POSITION\_MASK</span></span>               | <span data-ttu-id="effdb-163">Maschera per i bit di posizione.</span><span class="sxs-lookup"><span data-stu-id="effdb-163">Mask for position bits.</span></span>                               |
| <span data-ttu-id="effdb-164">D3DFVF \_ RESERVED0, D3DFVF \_ RESERVED2</span><span class="sxs-lookup"><span data-stu-id="effdb-164">D3DFVF\_RESERVED0, D3DFVF\_RESERVED2</span></span> | <span data-ttu-id="effdb-165">Mascherare i valori per i bit riservati in FVF.</span><span class="sxs-lookup"><span data-stu-id="effdb-165">Mask values for reserved bits in the FVF.</span></span> <span data-ttu-id="effdb-166">Non usare.</span><span class="sxs-lookup"><span data-stu-id="effdb-166">Do not use.</span></span> |
| <span data-ttu-id="effdb-167">\_Maschera D3DFVF TEXCOUNT \_</span><span class="sxs-lookup"><span data-stu-id="effdb-167">D3DFVF\_TEXCOUNT\_MASK</span></span>               | <span data-ttu-id="effdb-168">Valore della maschera per i bit del flag di trama.</span><span class="sxs-lookup"><span data-stu-id="effdb-168">Mask value for texture flag bits.</span></span>                     |



 

## <a name="miscellaneous-flags"></a><span data-ttu-id="effdb-169">Flag varie</span><span class="sxs-lookup"><span data-stu-id="effdb-169">Miscellaneous Flags</span></span>

<span data-ttu-id="effdb-170">I flag seguenti descrivono un'ampia gamma di flag utilizzati dalla pipeline a funzione fissa.</span><span class="sxs-lookup"><span data-stu-id="effdb-170">The following flags describe a variety of flags used by the fixed-function pipeline.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="effdb-171">#definire</span><span class="sxs-lookup"><span data-stu-id="effdb-171">#define</span></span></td>
<td><span data-ttu-id="effdb-172">Descrizione</span><span class="sxs-lookup"><span data-stu-id="effdb-172">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="effdb-173">D3DFVF_LASTBETA_D3DCOLOR</span><span class="sxs-lookup"><span data-stu-id="effdb-173">D3DFVF_LASTBETA_D3DCOLOR</span></span></td>
<td><span data-ttu-id="effdb-174">L'ultimo campo beta nei dati della posizione del vertice sarà di tipo D3DCOLOR.</span><span class="sxs-lookup"><span data-stu-id="effdb-174">The last beta field in the vertex position data will be of type D3DCOLOR.</span></span> <span data-ttu-id="effdb-175">I dati nei campi beta vengono usati con la personalizzazione della tavolozza della tabella per specificare gli indici della matrice.</span><span class="sxs-lookup"><span data-stu-id="effdb-175">The data in the beta fields are used with matrix palette skinning to specify matrix indices.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="effdb-176">D3DFVF_LASTBETA_UBYTE4</span><span class="sxs-lookup"><span data-stu-id="effdb-176">D3DFVF_LASTBETA_UBYTE4</span></span></td>
<td><span data-ttu-id="effdb-177">L'ultimo campo beta nei dati della posizione del vertice sarà di tipo UBYTE4.</span><span class="sxs-lookup"><span data-stu-id="effdb-177">The last beta field in the vertex position data will be of type UBYTE4.</span></span> <span data-ttu-id="effdb-178">I dati nei campi beta vengono usati con la personalizzazione della tavolozza della tabella per specificare gli indici della matrice.</span><span class="sxs-lookup"><span data-stu-id="effdb-178">The data in the beta fields are used with matrix palette skinning to specify matrix indices.</span></span> <span data-codelanguage=""></span>
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

<p><span data-ttu-id="effdb-179">Dato che FVF è dichiarato come: D3DFVF_XYZB5 | D3DFVF_LASTBETA_UBYTE4.</span><span class="sxs-lookup"><span data-stu-id="effdb-179">Given the FVF is declared as: D3DFVF_XYZB5 | D3DFVF_LASTBETA_UBYTE4.</span></span> <span data-ttu-id="effdb-180">Weight e MatrixIndices sono inclusi nella versione beta [5], dove D3DFVF_LASTBETA_UBYTE4 dice di interpretare l'ultimo DWORD in beta [5] come tipo UBYTE4.</span><span class="sxs-lookup"><span data-stu-id="effdb-180">Weight and MatrixIndices are included in beta[5], where D3DFVF_LASTBETA_UBYTE4 says to interpret the last DWORD in beta[5] as type UBYTE4.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="effdb-181">D3DFVF_TEXCOUNT_SHIFT</span><span class="sxs-lookup"><span data-stu-id="effdb-181">D3DFVF_TEXCOUNT_SHIFT</span></span></td>
<td><span data-ttu-id="effdb-182">Numero di bit in base al quale spostare un valore intero che identifica il numero di coordinate di trama per un vertice.</span><span class="sxs-lookup"><span data-stu-id="effdb-182">The number of bits by which to shift an integer value that identifies the number of texture coordinates for a vertex.</span></span> <span data-ttu-id="effdb-183">Questo valore può essere usato come illustrato di seguito.</span><span class="sxs-lookup"><span data-stu-id="effdb-183">This value might be used as shown below.</span></span>
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



 

### <a name="examples"></a><span data-ttu-id="effdb-184">Esempio</span><span class="sxs-lookup"><span data-stu-id="effdb-184">Examples</span></span>

<span data-ttu-id="effdb-185">Negli esempi seguenti vengono illustrate altre combinazioni di flag comuni.</span><span class="sxs-lookup"><span data-stu-id="effdb-185">The following examples show other common flag combinations.</span></span>


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



## <a name="constant-information"></a><span data-ttu-id="effdb-186">Informazioni sulle costanti</span><span class="sxs-lookup"><span data-stu-id="effdb-186">Constant Information</span></span>



|                          |             |
|--------------------------|-------------|
| <span data-ttu-id="effdb-187">Intestazione</span><span class="sxs-lookup"><span data-stu-id="effdb-187">Header</span></span>                   | <span data-ttu-id="effdb-188">d3d9types. h</span><span class="sxs-lookup"><span data-stu-id="effdb-188">d3d9types.h</span></span> |
| <span data-ttu-id="effdb-189">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="effdb-189">Minimum operating system</span></span> | <span data-ttu-id="effdb-190">Windows 98</span><span class="sxs-lookup"><span data-stu-id="effdb-190">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="effdb-191">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="effdb-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="effdb-192">Costanti Direct3D</span><span class="sxs-lookup"><span data-stu-id="effdb-192">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[<span data-ttu-id="effdb-193">Codici FVF della funzione fissa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="effdb-193">Fixed Function FVF Codes (Direct3D 9)</span></span>](fixed-function-fvf-codes.md)
</dt> <dt>

[<span data-ttu-id="effdb-194">Blending Geometry (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="effdb-194">Geometry Blending (Direct3D 9)</span></span>](geometry-blending.md)
</dt> </dl>

 

 



