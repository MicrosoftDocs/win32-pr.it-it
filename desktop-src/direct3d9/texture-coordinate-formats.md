---
description: Le coordinate di trama in Direct3D possono includere uno, due, tre o quattro elementi a virgola mobile per indirizzare le trame con diversi livelli di dimensione.
ms.assetid: d841af62-41b0-4b80-960b-4630b9a7210c
title: Formati delle coordinate della trama (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c48ec28b9c99357fe8825f5ff79da3c8869719389c4a4bc4874c5740fc71f42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118519884"
---
# <a name="texture-coordinate-formats-direct3d-9"></a>Formati delle coordinate della trama (Direct3D 9)

Le coordinate di trama in Direct3D possono includere uno, due, tre o quattro elementi a virgola mobile per indirizzare le trame con diversi livelli di dimensione. Una trama 1D, una superficie di trama con dimensioni di texel 1 per n, è indirizzata da una coordinata di trama. Il caso più comune, le trame 2D, viene indirizzato con due coordinate di trama comunemente denominate you e v. Direct3D supporta due tipi di trame 3D, mappe di ambiente cubico e trame di volume. Le mappe di ambiente cubiche non sono realmente 3D, ma sono indirizzate con un vettore a 3 elementi. Per informazioni dettagliate, [vedere Cubic Environment Mapping (Direct3D 9)](cubic-environment-mapping.md).

Come descritto in Codici FVF a funzione fissa [(Direct3D 9),](fixed-function-fvf-codes.md)le applicazioni codificano le coordinate di trama nel formato vertice. Il formato vertice può includere più set di coordinate di trama. Usare da D3DFVF \_ TEX0 a D3DFVF \_ TEX8 [D3DFVF](d3dfvf.md) per descrivere un formato di vertice che non include coordinate di trama o fino a otto set.

Ogni set di coordinate di trama può avere tra uno e quattro elementi. I \_ flag TEXTUREFORMAT1 e D3DFVF TEXTUREFORMAT4 descrivono il numero di elementi in una coordinata di trama in un set, ma questi flag non vengono usati \_ da soli. Il set di macro [**D3DFVF \_ TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) usa invece questi flag per creare modelli di bit che descrivono il numero di elementi usati da un particolare set di coordinate di trama nel formato vertice. Queste macro accettano un singolo parametro che identifica l'indice del set di coordinate di cui viene definito il numero di elementi. Nell'esempio seguente viene illustrato l'utilizzo di queste macro.


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
> Ad eccezione delle mappe di ambiente cubico e delle trame di volume, i rasterizzatori non possono risolvere le trame usando più di due elementi. Le applicazioni possono fornire fino a tre elementi per una coordinata di trama, ma solo se la trama è una mappa cubo, una trama di volume o il flag di trasformazione della trama D3DTTFF \_ PROJECTED. Il flag D3DTTFF PROJECTED fa sì che il rasterizzatore divida i primi due elementi per \_ il terzo (o n) elemento. Per altre informazioni, vedere [Trasformazioni delle coordinate di trama (Direct3D 9).](texture-coordinate-transformations.md)

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Coordinate della trama](texture-coordinates.md)
</dt> </dl>

 

 



