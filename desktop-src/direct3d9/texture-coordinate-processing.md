---
description: Il diagramma seguente mostra il percorso tracciato dalle coordinate della trama dall'origine, tramite l'elaborazione e fino al rasterizzatore.
ms.assetid: a6126946-8f75-4b3a-b017-d1014e917e9c
title: Elaborazione delle coordinate della trama (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72ce5a002e7171f97ab60c0af3cd5e8228cb8222ba70b8e718f2d93c28cebf33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044225"
---
# <a name="texture-coordinate-processing-direct3d-9"></a>Elaborazione delle coordinate della trama (Direct3D 9)

Il diagramma seguente mostra il percorso tracciato dalle coordinate della trama dall'origine, tramite l'elaborazione e fino al rasterizzatore.

![diagramma del percorso per le coordinate della trama da un'origine al rasterizzatore](images/tex-processing.png)

Esistono due origini da cui il sistema può disegnare le coordinate della trama. Per una determinata fase di trama, è possibile usare le coordinate della trama incluse nel formato vertice (da D3DFVF \_ TEX1 a D3DFVF TEX8) oppure è possibile usare le coordinate di trama generate automaticamente da \_ Direct3D. Per informazioni dettagliate su quest'ultimo caso, vedere [Coordinate di trama generate automaticamente (Direct3D 9).](automatically-generated-texture-coordinates.md) Se lo stato della fase della trama TEXTURETRANSFORMFLAGS D3DTSS per la fase di trama corrente è impostato su \_ D3DTTFF DISABLE (impostazione predefinita), le coordinate di input non vengono \_ trasformate. Se la proprietà TEXTURETRANSFORMFLAGS> D3DTSS è impostata su qualsiasi altro valore, la matrice di trasformazione per tale fase viene applicata \_ alle coordinate di input.

Il [**tipo enumerato D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) definisce valori validi per lo stato della fase di trama \_ TEXTURETRANSFORMFLAGS D3DTSS. Ad eccezione del flag DISABLE D3DTTFF, che ignora la trasformazione delle coordinate di trama, i valori definiti in questa enumerazione configurano il numero di coordinate di output passate dal sistema al \_ rasterizzatore. I flag DA D3DTTFF COUNT1 a D3DTTFF COUNT4 indicano al sistema di passare uno, due, tre o quattro elementi dalle coordinate di output al \_ \_ rasterizzatore.

Il flag D3DTTFF PROJECTED è speciale: indica al sistema che le coordinate della \_ trama sono per una trama proiettata. Combinare il flag D3DTTFF PROJECTED con un altro membro di \_ [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) per indicare al rasterizzatore di dividere tutti gli elementi per l'ultimo elemento prima della rasterizzazione. Ad esempio, quando si usano in modo esplicito coordinate di trama a tre elementi o quando la trasformazione produce una coordinata di trama a tre elementi, è possibile combinare i flag D3DTTFF COUNT3 e D3DTTFF PROJECTED per fare in modo che il rasterizzatore divida i primi due elementi per l'ultimo, producendo le coordinate di trama 2D necessarie per affrontare una \_ \_ trama 2D.

> [!Note]  
> Ad eccezione delle mappe dell'ambiente cubico e delle trame del volume, i rasterizzatori non possono risolvere le trame usando le coordinate della trama con più di due elementi. Se si specificano più elementi di quelli che possono essere usati per la trama corrente per tale fase, gli elementi estranei vengono ignorati. Questo vale anche quando si usano coordinate di trama 2D per una trama 1D.

 

Altre informazioni sono contenute negli argomenti seguenti.

-   [Coordinate di trama generate automaticamente (Direct3D 9)](automatically-generated-texture-coordinates.md)
-   [Trasformazioni delle coordinate di trama (Direct3D 9)](texture-coordinate-transformations.md)
-   [Effetti speciali (Direct3D 9)](special-effects.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Coordinate della trama](texture-coordinates.md)
</dt> </dl>

 

 
