---
description: Le costanti di formato dei vertici flessibili, o codici FVF, vengono usate per descrivere il contenuto dei vertici interfoliati in un singolo flusso di dati che verrà elaborato dalla pipeline a funzione fissa.
ms.assetid: 85d9f5b2-8e4a-4f92-a587-eae5b293778c
title: D3DFVF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56136b57aa0af7e8a7d4050f9feb6e1e3e92f3b6
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122629740"
---
# <a name="d3dfvf"></a>D3DFVF

Le costanti di formato dei vertici flessibili, o codici FVF, vengono usate per descrivere il contenuto dei vertici interfoliati in un singolo flusso di dati che verrà elaborato dalla pipeline a funzione fissa.

## <a name="vertex-data-flags"></a>Flag di dati dei vertici

I flag seguenti descrivono un formato di vertice. Per informazioni sui formati dei vertici, vedere Codici FVF delle funzioni [fisse (Direct3D 9).](fixed-function-fvf-codes.md)



| \#Definire                            | Descrizione                                                                                                                                                                                                                                                                                                                                                             | Ordine e tipo dei dati                                                                                       |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| D3DFVF \_ DIFFUSE                     | Il formato vertice include un componente di colore diffuso.                                                                                                                                                                                                                                                                                                                       | DWORD in ordine ARGB. Vedere [**D3DCOLOR \_ ARGB**](d3dcolor-argb.md).                                         |
| D3DFVF \_ NORMAL                      | Il formato vertice include un vettore normale dei vertici. Questo flag non può essere usato con il flag D3DFVF \_ XYZRHW.                                                                                                                                                                                                                                                                   | float, float, float                                                                                       |
| D3DFVF \_ PSIZE                       | Formato del vertice specificato in dimensioni in punti. Queste dimensioni sono espresse in unità dello spazio della fotocamera per i vertici non trasformati e accesi e in unità spazio dispositivo per vertici trasformati e accesi.                                                                                                                                                                          | float                                                                                                     |
| SPECULARE D3DFVF \_                    | Il formato vertice include un componente di colore speculare.                                                                                                                                                                                                                                                                                                                      | DWORD in ordine ARGB. Vedere [**D3DCOLOR \_ ARGB**](d3dcolor-argb.md).                                         |
| D3DFVF \_ XYZ                         | Il formato vertice include la posizione di un vertice non trasformato. Questo flag non può essere usato con il flag D3DFVF \_ XYZRHW.                                                                                                                                                                                                                                                  | float, float, float.                                                                                      |
| D3DFVF \_ XYZRHW                      | Il formato vertice include la posizione di un vertice trasformato. Questo flag non può essere usato con i flag D3DFVF \_ XYZ o D3DFVF \_ NORMAL.                                                                                                                                                                                                                                     | float, float, float, float.                                                                               |
| Da D3DFVF \_ XYZB1 a D3DFVF \_ XYZB5 | Il formato vertice contiene i dati di posizione e un numero corrispondente di valori di ponderazione (beta) da usare per le operazioni di fusione dei vertici multimatrix. Attualmente Direct3D può essere misto con un massimo di tre valori di ponderazione e quattro matrici di fusione. Per altre informazioni sull'uso delle matrici di fusione, vedere [Indexed Vertex Blending (Direct3D 9)](indexed-vertex-blending.md). | 1, 2 o 3 float. Quando si usa D3DFVF \_ LASTBETA UBYTE4, l'ultimo peso di \_ fusione viene considerato come DWORD. |
| D3DFVF \_ XYZW                        | Il formato vertice contiene dati trasformati e ritagliati (x, y, z, w). ProcessVertices non richiama il clipper, ma restituisce i dati nelle coordinate del clip. Questa costante è progettata per e può essere usata solo con la pipeline dei vertici programmabili.                                                                                                                 | float, float, float, float                                                                                |



 

## <a name="texture-flags"></a>Flag di trama

I flag seguenti descrivono i flag di trama usati dalla pipeline a funzione fissa.



| \#Definire                          | Descrizione                                                                                                                                                                                                                                                                        |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DFVF \_ TEX0 - D3DFVF \_ TEX8       | Numero di set di coordinate di trama per questo vertice. I valori effettivi per questi flag non sono sequenziali.                                                                                                                                                                           |
| D3DFVF \_ TEXCOORDSIZEN(coordIndex) | Definire un set di dati delle coordinate di trama. n indica la dimensione delle coordinate della trama. coordIndex indica il numero di indice delle coordinate di trama. Vedere [**D3DFVF \_ TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) e [Coordinate trama e Fasi trama](texture-coordinates.md). |



 

## <a name="mask-flags"></a>Flag di maschera

I flag seguenti descrivono i flag di maschera usati dalla pipeline di funzioni fisse.



| \#Definire                             | Descrizione                                           |
|--------------------------------------|-------------------------------------------------------|
| MASCHERA DI POSIZIONE D3DFVF \_ \_               | Maschera per i bit di posizione.                               |
| D3DFVF \_ RESERVED0, D3DFVF \_ RESERVED2 | Mascherare i valori per i bit riservati in FVF. Non usare. |
| MASCHERA D3DFVF \_ TEXCOUNT \_               | Valore della maschera per i bit del flag di trama.                     |



 

## <a name="miscellaneous-flags"></a>Flag vari

I flag seguenti descrivono un'ampia gamma di flag usati dalla pipeline a funzione fissa.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>#Definire</td>
<td>Descrizione</td>
</tr>
<tr class="even">
<td>D3DFVF_LASTBETA_D3DCOLOR</td>
<td>L'ultimo campo beta nei dati della posizione del vertice sarà di tipo D3DCOLOR. I dati nei campi beta vengono usati con l'interfaccia della tavolozza della matrice per specificare gli indici della matrice.</td>
</tr>
<tr class="odd">
<td>D3DFVF_LASTBETA_UBYTE4</td>
<td>L'ultimo campo beta nei dati della posizione dei vertici sarà di tipo UBYTE4. I dati nei campi beta vengono usati con l'interfaccia della tavolozza della matrice per specificare gli indici della matrice. <span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
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

<p>Dato che FVF è dichiarato come: D3DFVF_XYZB5 | D3DFVF_LASTBETA_UBYTE4. Weight e MatrixIndices sono inclusi in beta[5], dove D3DFVF_LASTBETA_UBYTE4 indica di interpretare l'ultima DWORD in beta[5] come tipo UBYTE4.</p></td>
</tr>
<tr class="even">
<td>D3DFVF_TEXCOUNT_SHIFT</td>
<td>Numero di bit in base al quale spostare un valore intero che identifica il numero di coordinate di trama per un vertice. Questo valore può essere usato come illustrato di seguito.
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
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



 

### <a name="examples"></a>Esempio

Gli esempi seguenti illustrano altre combinazioni di flag comuni.


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



## <a name="constant-information"></a>Informazioni costanti



| Requisito                         | Valore            |
|--------------------------|-------------|
| Intestazione                   | d3d9types.h |
| Sistema operativo minimo | Windows 98  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[Codici FVF delle funzioni fisse (Direct3D 9)](fixed-function-fvf-codes.md)
</dt> <dt>

[Fusione geometry (Direct3D 9)](geometry-blending.md)
</dt> </dl>

 

 



