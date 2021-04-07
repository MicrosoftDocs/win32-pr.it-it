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
# <a name="texture-coordinate-formats-direct3d-9"></a>Formati di coordinate di trama (Direct3D 9)

Le coordinate di trama in Direct3D possono includere uno, due, tre o quattro elementi a virgola mobile per indirizzare le trame con diversi livelli di dimensione. Una trama 1D, ovvero una superficie di trama con dimensioni di Texel 1 per n, viene richiamata da una coordinata di trama. Il caso più comune, le trame 2D, vengono risolte con due coordinate di trama comunemente chiamate u e v. Direct3D supporta due tipi di trame 3D, mappe dell'ambiente cubico e trame del volume. Le mappe dell'ambiente cubi non sono realmente 3D, ma vengono risolte con un vettore di 3 elementi. Per informazioni dettagliate, vedere [mapping di ambienti cubici (Direct3D 9)](cubic-environment-mapping.md).

Come descritto in [codici FVF a funzione fissa (Direct3D 9)](fixed-function-fvf-codes.md), le applicazioni codificano le coordinate di trama nel formato vertice. Il formato Vertex può includere più set di coordinate di trama. Usare D3DFVF \_ TEX0 tramite D3DFVF \_ TEX8 [D3DFVF](d3dfvf.md) per descrivere un formato di vertice che non includa coordinate di trama o un numero di otto set.

Ogni set di coordinate di trama può includere tra uno e quattro elementi. I \_ flag D3DFVF TEXTUREFORMAT1 through D3DFVF \_ TEXTUREFORMAT4 descrivono il numero di elementi in una coordinata di trama in un set, ma questi flag non vengono usati da soli. Piuttosto, il set di macro [**D3DFVF \_ TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) usa questi flag per creare modelli di bit che descrivono il numero di elementi usati da un particolare set di coordinate di trama nel formato vertice. Queste macro accettano un singolo parametro che identifica l'indice del set di coordinate il cui numero di elementi viene definito. Nell'esempio seguente viene illustrata la modalità di utilizzo di queste macro.


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
> Ad eccezione delle mappe dell'ambiente cubica e delle trame dei volumi, i rasterizzatori non possono indirizzare le trame usando più di due elementi. Le applicazioni possono fornire fino a tre elementi per una coordinata di trama, ma solo se la trama è una mappa cubo, una trama del volume o il \_ flag di trasformazione della trama proiettata D3DTTFF. Il \_ flag proiettato D3DTTFF fa sì che il rasterizzatore divida i primi due elementi per il terzo elemento (o n). Per altre informazioni, vedere [trasformazioni di coordinate di trama (Direct3D 9)](texture-coordinate-transformations.md).

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Coordinate di trama](texture-coordinates.md)
</dt> </dl>

 

 



