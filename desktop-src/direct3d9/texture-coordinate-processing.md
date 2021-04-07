---
description: Il diagramma seguente illustra il percorso adottato dalle coordinate di trama dalla relativa origine, tramite l'elaborazione e al rasterizzatore.
ms.assetid: a6126946-8f75-4b3a-b017-d1014e917e9c
title: Elaborazione delle coordinate di trama (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a161d3675a5859702368a62719124aa029ee455
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104049038"
---
# <a name="texture-coordinate-processing-direct3d-9"></a>Elaborazione delle coordinate di trama (Direct3D 9)

Il diagramma seguente illustra il percorso adottato dalle coordinate di trama dalla relativa origine, tramite l'elaborazione e al rasterizzatore.

![diagramma del percorso per le coordinate di trama da un'origine al rasterizzatore](images/tex-processing.png)

Esistono due origini da cui il sistema può creare coordinate di trama. Per una determinata fase di trama, è possibile usare le coordinate di trama incluse nel formato del vertice (D3DFVF \_ TEX1 tramite D3DFVF \_ TEX8) oppure è possibile usare le coordinate di trama generate automaticamente da Direct3D. Per informazioni dettagliate sul secondo caso, vedere [coordinate di trama generate automaticamente (Direct3D 9)](automatically-generated-texture-coordinates.md). Se lo \_ stato della fase della trama D3DTSS TEXTURETRANSFORMFLAGS per la fase di trama corrente è impostato su D3DTTFF \_ Disable (impostazione predefinita), le coordinate di input non vengono trasformate. Se D3DTSS \_ TEXTURETRANSFORMFLAGS> è impostato su qualsiasi altro valore, la matrice di trasformazione per tale fase viene applicata alle coordinate di input.

Il tipo enumerato [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) definisce valori validi per lo \_ stato della fase della trama TEXTURETRANSFORMFLAGS di D3DTSS. Ad eccezione del \_ flag di disabilitazione di D3DTTFF, che ignora la trasformazione delle coordinate di trama, i valori definiti in questa enumerazione configurano il numero di coordinate di output passate dal sistema al rasterizzatore. I \_ flag D3DTTFF COUNT1 through D3DTTFF \_ COUNT4 indicano al sistema di passare uno, due, tre o quattro elementi dalle coordinate di output al rasterizzatore.

Il \_ flag D3DTTFF proiettato è speciale: indica al sistema che le coordinate di trama si riferiscono a una trama proiettata. Combinare il \_ flag D3DTTFF proiettato con un altro membro di [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) per indicare al rasterizzatore di dividere tutti gli elementi in base all'ultimo elemento prima che la rasterizzazione avvenga. Ad esempio, quando si usano in modo esplicito le coordinate di trama a tre elementi o quando la trasformazione produce una coordinata di trama a tre elementi, è possibile combinare i \_ flag D3DTTFF COUNT3 e D3DTTFF \_ proiettati per fare in modo che il rasterizzatore divida i primi due elementi per ultimo, producendo coordinate di trama 2D necessarie per indirizzare una trama 2D.

> [!Note]  
> Ad eccezione delle mappe dell'ambiente cubica e delle trame dei volumi, i rasterizzatori non possono indirizzare le trame usando coordinate di trama con più di due elementi. Se si specificano più elementi di quelli che possono essere usati per indirizzare la trama corrente per tale fase, gli elementi estranei vengono ignorati. Questo vale anche quando si usano le coordinate di trama 2D per una trama 1D.

 

Informazioni aggiuntive sono contenute negli argomenti seguenti.

-   [Coordinate di trama generate automaticamente (Direct3D 9)](automatically-generated-texture-coordinates.md)
-   [Trasformazioni di coordinate di trama (Direct3D 9)](texture-coordinate-transformations.md)
-   [Effetti speciali (Direct3D 9)](special-effects.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Coordinate di trama](texture-coordinates.md)
</dt> </dl>

 

 
