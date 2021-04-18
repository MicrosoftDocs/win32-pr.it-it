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
# <a name="d3dfvf"></a>D3DFVF

Le costanti di formato vertex flessibili o i codici FVF vengono usati per descrivere il contenuto dei vertici con interfoliazione in un singolo flusso di dati che verrà elaborato dalla pipeline a funzione fissa.

## <a name="vertex-data-flags"></a>Flag di dati dei vertici

I flag seguenti descrivono un formato vertici. Per informazioni sui formati dei vertici, vedere [codici FVF della funzione fissa (Direct3D 9)](fixed-function-fvf-codes.md).



|                                     |                                                                                                                                                                                                                                                                                                                                                                         |                                                                                                           |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| \#definire                            | Descrizione                                                                                                                                                                                                                                                                                                                                                             | Ordine e tipo di dati                                                                                       |
| D3DFVF \_ diffuse                     | Il formato del vertice include un componente colore diffuso.                                                                                                                                                                                                                                                                                                                       | DWORD in ordine ARGB. Vedere [**D3DCOLOR \_ ARGB**](d3dcolor-argb.md).                                         |
| D3DFVF \_ normale                      | Il formato del vertice include un vettore di normale vertice. Questo flag non può essere usato con il \_ flag XYZRHW di D3DFVF.                                                                                                                                                                                                                                                                   | float, float, float                                                                                       |
| \_PSIZE D3DFVF                       | Formato vertice specificato in dimensioni punto. Questa dimensione è espressa in unità di spazio della fotocamera per i vertici che non sono trasformati e illuminati e in unità di spazio del dispositivo per i vertici trasformati e illuminati.                                                                                                                                                                          | float                                                                                                     |
| D3DFVF \_ speculare                    | Il formato del vertice include un componente colore speculare.                                                                                                                                                                                                                                                                                                                      | DWORD in ordine ARGB. Vedere [**D3DCOLOR \_ ARGB**](d3dcolor-argb.md).                                         |
| D3DFVF \_ XYZ                         | Il formato del vertice include la posizione di un vertice non trasformato. Questo flag non può essere usato con il \_ flag XYZRHW di D3DFVF.                                                                                                                                                                                                                                                  | float, float, float.                                                                                      |
| \_XYZRHW D3DFVF                      | Il formato del vertice include la posizione di un vertice trasformato. Non è possibile usare questo flag con i \_ flag normali D3DFVF XYZ o D3DFVF \_ .                                                                                                                                                                                                                                     | float, float, float, float.                                                                               |
| D3DFVF \_ XYZB1 tramite D3DFVF \_ XYZB5 | Il formato vertici contiene i dati di posizione e un numero corrispondente di valori di ponderazione (beta) da usare per le operazioni di fusione dei vertici a più matrici. Attualmente, Direct3D può unire fino a tre valori di ponderazione e quattro matrici di Blend. Per ulteriori informazioni sull'utilizzo di matrici di fusione, vedere [indexed Vertex blending (Direct3D 9)](indexed-vertex-blending.md). | 1, 2 o 3 float. Quando \_ \_ si usa D3DFVF LASTBETA UBYTE4, l'ultimo peso della fusione viene considerato come un valore DWORD. |
| \_XYZW D3DFVF                        | Il formato del vertice contiene dati trasformati e ritagliati (x, y, z, w). ProcessVertices non richiama il Clipper, bensì l'output dei dati nelle coordinate di ritaglio. Questa costante è progettata per e può essere usata solo con, la pipeline di vertici programmabile.                                                                                                                 | float, float, float, float                                                                                |



 

## <a name="texture-flags"></a>Flag di trama

I flag seguenti descrivono i flag di trama utilizzati dalla pipeline a funzione fissa.



|                                   |                                                                                                                                                                                                                                                                                    |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \#definire                          | Descrizione                                                                                                                                                                                                                                                                        |
| D3DFVF \_ TEX0-D3DFVF \_ TEX8       | Numero di set di coordinate di trama per questo vertice. I valori effettivi per questi flag non sono sequenziali.                                                                                                                                                                           |
| D3DFVF \_ TEXCOORDSIZEN (coordIndex) | Definire un set di dati di coordinate di trama. n indica la dimensione delle coordinate di trama. coordIndex indica il numero di indice delle coordinate di trama. Vedere [**D3DFVF \_ TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) e [coordinate di trama e fasi della trama](texture-coordinates.md). |



 

## <a name="mask-flags"></a>Flag maschera

I flag seguenti descrivono i flag della maschera usati dalla pipeline a funzione fissa.



|                                      |                                                       |
|--------------------------------------|-------------------------------------------------------|
| \#definire                             | Descrizione                                           |
| \_Maschera posizione \_ D3DFVF               | Maschera per i bit di posizione.                               |
| D3DFVF \_ RESERVED0, D3DFVF \_ RESERVED2 | Mascherare i valori per i bit riservati in FVF. Non usare. |
| \_Maschera D3DFVF TEXCOUNT \_               | Valore della maschera per i bit del flag di trama.                     |



 

## <a name="miscellaneous-flags"></a>Flag varie

I flag seguenti descrivono un'ampia gamma di flag utilizzati dalla pipeline a funzione fissa.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>#definire</td>
<td>Descrizione</td>
</tr>
<tr class="even">
<td>D3DFVF_LASTBETA_D3DCOLOR</td>
<td>L'ultimo campo beta nei dati della posizione del vertice sarà di tipo D3DCOLOR. I dati nei campi beta vengono usati con la personalizzazione della tavolozza della tabella per specificare gli indici della matrice.</td>
</tr>
<tr class="odd">
<td>D3DFVF_LASTBETA_UBYTE4</td>
<td>L'ultimo campo beta nei dati della posizione del vertice sarà di tipo UBYTE4. I dati nei campi beta vengono usati con la personalizzazione della tavolozza della tabella per specificare gli indici della matrice. <span data-codelanguage=""></span>
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

<p>Dato che FVF è dichiarato come: D3DFVF_XYZB5 | D3DFVF_LASTBETA_UBYTE4. Weight e MatrixIndices sono inclusi nella versione beta [5], dove D3DFVF_LASTBETA_UBYTE4 dice di interpretare l'ultimo DWORD in beta [5] come tipo UBYTE4.</p></td>
</tr>
<tr class="even">
<td>D3DFVF_TEXCOUNT_SHIFT</td>
<td>Numero di bit in base al quale spostare un valore intero che identifica il numero di coordinate di trama per un vertice. Questo valore può essere usato come illustrato di seguito.
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



 

### <a name="examples"></a>Esempio

Negli esempi seguenti vengono illustrate altre combinazioni di flag comuni.


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



## <a name="constant-information"></a>Informazioni sulle costanti



|                          |             |
|--------------------------|-------------|
| Intestazione                   | d3d9types. h |
| Sistema operativo minimo | Windows 98  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[Codici FVF della funzione fissa (Direct3D 9)](fixed-function-fvf-codes.md)
</dt> <dt>

[Blending Geometry (Direct3D 9)](geometry-blending.md)
</dt> </dl>

 

 



