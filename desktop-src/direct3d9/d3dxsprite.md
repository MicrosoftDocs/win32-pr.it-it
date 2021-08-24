---
description: 'I flag seguenti vengono usati per specificare le opzioni di rendering dello sprite per il parametro flags nel metodo Begin:'
ms.assetid: 195ee969-30e8-4828-a0be-f0d2a82e247c
title: D3DXSPRITE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59e2247f414636039906277f882fb9dfc95f6b6b33aa29de2ac51a722c045901
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119749761"
---
# <a name="d3dxsprite"></a>D3DXSPRITE

I flag seguenti vengono usati per specificare le opzioni di rendering dello sprite per il parametro flags nel [**metodo Begin:**](id3dxsprite--begin.md)



| \#Definire                             | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DXSPRITE \_ DONOTSAVESTATE           | Lo stato del dispositivo non deve essere salvato o ripristinato quando [**viene chiamato Begin**](id3dxsprite--begin.md) [**o**](id3dxsprite--end.md) End.                                                                                                                                                                                                                                                                                            |
| D3DXSPRITE \_ DONOTMODIFY \_ RENDERSTATE | Lo stato di rendering del dispositivo non deve essere modificato quando [**viene chiamato Begin.**](id3dxsprite--begin.md) Si presuppone che il dispositivo sia in uno stato valido per disegnare vertici contenenti UsageIndex = 0 nei dati D3DDECLUSAGE \_ POSITION, D3DDECLUSAGE \_ TEXCOORD e D3DDECLUSAGE \_ COLOR.                                                                                                                                                     |
| SPAZIO OGGETTI D3DXSPRITE \_              | Le trasformazioni di mondo, visualizzazione e proiezione non vengono modificate. Le trasformazioni attualmente impostate sul dispositivo vengono usate per trasformare gli sprite quando vengono disegnati gli sprite in batch (quando viene chiamato [**Flush**](id3dxsprite--flush.md) o [**End).**](id3dxsprite--end.md) Se questo flag non viene specificato, le trasformazioni world, view e projection vengono modificate in modo che gli sprite siano disegnati nelle coordinate dello spazio dello schermo.              |
| D3DXSPRITE \_ BILLBOARD                | Ogni sprite verrà ruotato intorno al centro in modo che sia rivolto verso il visualizzatore. [**È necessario chiamare prima SetWorldViewLH**](id3dxsprite--setworldviewlh.md) o [**SetWorldViewRH.**](id3dxsprite--setworldviewrh.md)                                                                                                                                                                                                                |
| D3DXSPRITE \_ ALPHABLEND               | Abilita la fusione alfa con D3DRS \_ ALPHATESTENABLE impostato su **TRUE** (per alfa diverso da zero). D3DBLEND SRCALPHA sarà lo stato di blend di origine \_ e D3DBLEND INVSRCALPHA sarà lo stato di blend di destinazione nelle chiamate a \_ [**SetRenderState**](/windows/desktop/api). Vedere [Alpha Blending State (Direct3D 9)](alpha-blending-state.md). [**ID3DXFont**](id3dxfont.md) prevede che questo flag sia impostato durante il disegno del testo. |
| TRAMA DI ORDINAMENTO D3DXSPRITE \_ \_            | Ordinare gli sprite in base alla trama prima del disegno. Ciò può migliorare le prestazioni quando si disegnano sprite non sovrapposti di profondità uniforme. È anche possibile combinare D3DXSPRITE SORT TEXTURE con \_ \_ D3DXSPRITE \_ SORT \_ DEPTH FRONTTOBACK o \_ D3DXSPRITE \_ SORT DEPTH \_ \_ BACKTOFRONT. In questo modo l'elenco di sprite verrà ordinato in base alla profondità prima e alla trama secondo.<br/>                                                                           |
| D3DXSPRITE \_ SORT \_ DEPTH \_ FRONTTOBACK | Gli sprite vengono ordinati in base alla profondità in ordine front-to-back prima del disegno. Questa procedura è consigliata quando si disegnano sprite opache di profondità variabili. È possibile combinare D3DXSPRITE \_ SORT \_ DEPTH FRONTTOBACK con \_ D3DXSPRITE SORT TEXTURE per ordinare prima in base alla profondità e il secondo in base \_ \_ alla trama.<br/>                                                                                                                                   |
| BACKTOFRONT DELLA PROFONDITÀ DI ORDINAMENTO D3DXSPRITE \_ \_ \_ | Gli sprite vengono ordinati in base alla profondità in ordine back-to-front prima del disegno. Questa procedura è consigliata quando si disegnano sprite trasparenti di profondità variabili. È possibile combinare D3DXSPRITE \_ SORT \_ DEPTH BACKTOFRONT con \_ D3DXSPRITE SORT TEXTURE per ordinare prima per profondità \_ e secondo per \_ trama.<br/>                                                                                                                              |
| D3DXSPRITE \_ NON \_ \_ ADDREF \_ TEXTURE | Disabilita la chiamata di AddRef() a ogni disegno e di Release() su Flush() per ottenere prestazioni migliori.                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="constant-information"></a>Informazioni costanti



| Requisito                         | Valore            |
|--------------------------|-------------|
| Intestazione                   | d3dx9core.h |
| Sistema operativo minimo | Windows 98  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti D3DX](dx9-graphics-reference-d3dx-constants.md)
</dt> </dl>

 

 




