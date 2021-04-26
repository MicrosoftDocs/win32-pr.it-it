---
description: 'I flag seguenti vengono usati per specificare le opzioni di rendering dello sprite per il parametro flags nel metodo Begin:'
ms.assetid: 195ee969-30e8-4828-a0be-f0d2a82e247c
title: D3DXSPRITE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe4dbf3e80e7cf6f7884d778860f9de61f5193f5
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997318"
---
# <a name="d3dxsprite"></a>D3DXSPRITE

I flag seguenti vengono usati per specificare le opzioni di rendering dello sprite per il parametro flags nel [**metodo Begin:**](id3dxsprite--begin.md)



| \#Definire                             | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DXSPRITE \_ DONOTSAVESTATE           | Lo stato del dispositivo non deve essere salvato o ripristinato quando [**viene chiamato Begin**](id3dxsprite--begin.md) o End. [](id3dxsprite--end.md)                                                                                                                                                                                                                                                                                            |
| D3DXSPRITE \_ DONOTMODIFY \_ RENDERSTATE | Lo stato di rendering del dispositivo non deve essere modificato quando [**viene chiamato Begin.**](id3dxsprite--begin.md) Si presuppone che il dispositivo sia in uno stato valido per disegnare vertici contenenti UsageIndex = 0 nei dati D3DDECLUSAGE \_ POSITION, D3DDECLUSAGE \_ TEXCOORD e D3DDECLUSAGE \_ COLOR.                                                                                                                                                     |
| SPAZIO OGGETTI D3DXSPRITE \_              | Le trasformazioni di mondo, visualizzazione e proiezione non vengono modificate. Le trasformazioni attualmente impostate sul dispositivo vengono usate per trasformare gli sprite quando vengono disegnati gli sprite in batch (quando viene chiamato [**Flush**](id3dxsprite--flush.md) o [**End).**](id3dxsprite--end.md) Se questo flag non viene specificato, le trasformazioni world, view e projection vengono modificate in modo che gli sprite siano disegnati nelle coordinate dello spazio dello schermo.              |
| D3DXSPRITE \_ BILLBOARD                | Ogni sprite verrà ruotato intorno al centro in modo che sia rivolto verso il visualizzatore. [**È necessario chiamare prima SetWorldViewLH**](id3dxsprite--setworldviewlh.md) o [**SetWorldViewRH.**](id3dxsprite--setworldviewrh.md)                                                                                                                                                                                                                |
| D3DXSPRITE \_ ALPHABLEND               | Abilita la fusione alfa con D3DRS \_ ALPHATESTENABLE impostato su **TRUE** (per alfa diverso da zero). D3DBLEND SRCALPHA sarà lo stato di blend di origine \_ e D3DBLEND INVSRCALPHA sarà lo stato di blend di destinazione nelle chiamate a \_ [**SetRenderState**](/windows/desktop/api). Vedere [Alpha Blending State (Direct3D 9) (Stato di fusione alfa - Direct3D 9).](alpha-blending-state.md) [**ID3DXFont**](id3dxfont.md) prevede che questo flag sia impostato durante il disegno di testo. |
| TRAMA DI ORDINAMENTO D3DXSPRITE \_ \_            | Ordinare gli sprite in base alla trama prima del disegno. Ciò può migliorare le prestazioni quando si disegnano sprite non sovrapposti di profondità uniforme. È anche possibile combinare D3DXSPRITE SORT TEXTURE con \_ \_ D3DXSPRITE \_ SORT \_ DEPTH FRONTTOBACK o \_ D3DXSPRITE \_ SORT DEPTH \_ \_ BACKTOFRONT. In questo modo, l'elenco degli sprite verrà ordinato per profondità per primo e per secondo per trama.<br/>                                                                           |
| D3DXSPRITE \_ SORT \_ DEPTH \_ FRONTTOBACK | Gli sprite vengono ordinati in base alla profondità in ordine front-to-back prima del disegno. Questa procedura è consigliata quando si disegnano sprite opachi di profondità variabili. È possibile combinare D3DXSPRITE \_ SORT \_ DEPTH FRONTTOBACK con \_ D3DXSPRITE SORT TEXTURE per ordinare prima in base alla profondità e secondo \_ \_ per trama.<br/>                                                                                                                                   |
| D3DXSPRITE \_ SORT \_ DEPTH \_ BACKTOFRONT | Gli sprite vengono ordinati in base alla profondità in ordine di ritorno anteriore prima del disegno. Questa procedura è consigliata quando si disegnano sprite trasparenti di profondità variabili. È possibile combinare D3DXSPRITE \_ SORT \_ DEPTH BACKTOFRONT con \_ D3DXSPRITE SORT TEXTURE per ordinare prima in base alla profondità e secondo \_ \_ per trama.<br/>                                                                                                                              |
| D3DXSPRITE \_ DO \_ NOT \_ ADDREF \_ TEXTURE | Disabilita la chiamata di AddRef() a ogni disegno e Release() su Flush() per ottenere prestazioni migliori.                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="constant-information"></a>Informazioni sulle costanti



|                          |             |
|--------------------------|-------------|
| Intestazione                   | d3dx9core.h |
| Sistema operativo minimo | Windows 98  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti D3DX](dx9-graphics-reference-d3dx-constants.md)
</dt> </dl>

 

 




