---
description: 'I flag seguenti vengono usati per specificare le opzioni di rendering sprite per il parametro flags nel metodo Begin:'
ms.assetid: 195ee969-30e8-4828-a0be-f0d2a82e247c
title: D3DXSPRITE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c394d2606584ec5f56aa28661a2da286f000a66d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520378"
---
# <a name="d3dxsprite"></a>D3DXSPRITE

I flag seguenti vengono usati per specificare le opzioni di rendering sprite per il parametro flags nel metodo [**Begin**](id3dxsprite--begin.md) :



|                                      |                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \#definire                             | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                       |
| \_DONOTSAVESTATE D3DXSPRITE           | Lo stato del dispositivo non deve essere salvato o ripristinato quando viene chiamato il metodo [**Begin**](id3dxsprite--begin.md) o [**end**](id3dxsprite--end.md) .                                                                                                                                                                                                                                                                                            |
| D3DXSPRITE \_ DONOTMODIFY \_ RENDERSTATE | Lo stato di rendering del dispositivo non deve essere modificato quando viene chiamato il metodo [**Begin**](id3dxsprite--begin.md) . Si presuppone che il dispositivo sia in uno stato valido per creare vertici contenenti UsageIndex = 0 nella posizione D3DDECLUSAGE \_ , D3DDECLUSAGE \_ TEXCOORD e D3DDECLUSAGE \_ color data.                                                                                                                                                     |
| \_OBJECTSPACE D3DXSPRITE              | Le trasformazioni del mondo, della vista e della proiezione non vengono modificate. Le trasformazioni attualmente impostate sul dispositivo vengono usate per trasformare gli sprite quando vengono disegnati gli sprite in batch (quando viene chiamato [**Flush**](id3dxsprite--flush.md) o [**end**](id3dxsprite--end.md) ). Se questo flag non è specificato, le trasformazioni World, View e Projection vengono modificate in modo che gli sprite vengano disegnati in coordinate dello spazio dello schermo.              |
| \_Tabellone D3DXSPRITE                | Ogni sprite verrà ruotato attorno al centro, in modo che sia rivolte al visualizzatore. È necessario chiamare prima [**SetWorldViewLH**](id3dxsprite--setworldviewlh.md) o [**SetWorldViewRH**](id3dxsprite--setworldviewrh.md) .                                                                                                                                                                                                                |
| \_AlphaBlend D3DXSPRITE               | Abilita la fusione alfa con D3DRS \_ ALPHATESTENABLE impostato su **true** (per un valore alfa diverso da zero). D3DBLEND \_ SRCALPHA sarà lo stato di Blend di origine e D3DBLEND \_ INVSRCALPHA sarà lo stato di Blend di destinazione nelle chiamate a [**SetRenderState**](/windows/desktop/api). Vedere [stato di fusione alfa (Direct3D 9)](alpha-blending-state.md). [**ID3DXFont**](id3dxfont.md) prevede l'impostazione di questo flag durante il disegno del testo. |
| \_Trama di ordinamento D3DXSPRITE \_            | Ordina gli sprite per trama prima del disegno. Questo può migliorare le prestazioni quando si disegnano sprite non sovrapposti di profondità uniforme. È anche possibile combinare \_ \_ la texture di ordinamento di D3DXSPRITE con D3DXSPRITE \_ Sort \_ Depth \_ FRONTTOBACK o D3DXSPRITE \_ Sort \_ Depth \_ BACKTOFRONT. In questo modo l'elenco degli sprite viene ordinato per primo e per la trama secondo.<br/>                                                                           |
| \_Profondità di ordinamento D3DXSPRITE \_ \_ FRONTTOBACK | Gli sprite sono ordinati in base alla profondità nell'ordine da inizio a indietro prima del disegno. Questa procedura è consigliata quando si disegnano sprite opachi di profondità variabili. È possibile combinare D3DXSPRITE \_ di \_ profondità di ordinamento \_ FRONTTOBACK con D3DXSPRITE \_ Ordina \_ trama per eseguire l'ordinamento prima in base alla profondità e secondo per trama.<br/>                                                                                                                                   |
| \_Profondità di ordinamento D3DXSPRITE \_ \_ BACKTOFRONT | Gli sprite sono ordinati in base alla profondità nell'ordine back-to-front prima del disegno. Questa procedura è consigliata per la creazione di sprite trasparenti di profondità variabili. È possibile combinare D3DXSPRITE \_ di \_ profondità di ordinamento \_ BACKTOFRONT con D3DXSPRITE \_ Ordina \_ trama per eseguire l'ordinamento prima in base alla profondità e secondo per trama.<br/>                                                                                                                              |
| D3DXSPRITE \_ \_ non \_ ADDREF \_ trama | Disabilita la chiamata a AddRef () a ogni estrazione e la versione () in Flush () per ottenere prestazioni migliori.                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="constant-information"></a>Informazioni sulle costanti



|                          |             |
|--------------------------|-------------|
| Intestazione                   | d3dx9core. h |
| Sistema operativo minimo | Windows 98  |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Costanti D3DX](dx9-graphics-reference-d3dx-constants.md)
</dt> </dl>

 

 




