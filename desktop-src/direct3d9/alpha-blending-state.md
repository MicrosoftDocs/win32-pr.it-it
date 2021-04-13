---
description: Il valore alfa di un colore ne controlla la trasparenza. L'abilitazione della fusione alfa consente la fusione di colori, materiali e trame in una superficie con trasparenza su un'altra superficie.
ms.assetid: e8e925d5-262d-45c0-be9f-21c9a103d7b7
title: Stato di fusione alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 884ecad07fb9aefba08a0abbab92969937ec6361
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401460"
---
# <a name="alpha-blending-state-direct3d-9"></a>Stato di fusione alfa (Direct3D 9)

Il valore alfa di un colore ne controlla la trasparenza. L'abilitazione della fusione alfa consente la fusione di colori, materiali e trame in una superficie con trasparenza su un'altra superficie.

Per altre informazioni, vedere [Alpha texture blending (Direct3D 9)](alpha-texture-blending.md) e [blending di trame (Direct3D 9)](texture-blending.md).

Le applicazioni scritte in C++ usano lo stato di rendering [**\_ ALPHABLENDENABLE di D3DRS**](./d3drenderstatetype.md) per abilitare la sfumatura di trasparenza alfa. L'API Direct3D consente molti tipi di fusione alfa. Tuttavia, è importante notare che l'hardware 3D dell'utente potrebbe non supportare tutti gli Stati di fusione consentiti da Direct3D.

Il tipo di fusione alfa eseguita dipende dagli Stati di rendering [**D3DRS \_ SRCBLEND**](./d3drenderstatetype.md) e **D3DRS \_ DESTBLEND** . Gli Stati di Blend di origine e di destinazione vengono utilizzati nelle coppie. Nell'esempio di codice riportato di seguito viene illustrato il modo in cui lo stato di Blend di origine è impostato su D3DBLEND \_ SRCCOLOR e lo stato di Blend di destinazione è impostato su D3DBLEND \_ INVSRCCOLOR.


```
// This code example assumes that d3dDevice is a
// valid pointer to an IDirect3DDevice9 interface.

// Set the source blend state.
d3dDevice->SetRenderState(D3DRS_SRCBLEND, D3DBLEND_SRCCOLOR);

// Set the destination blend state.

d3dDevice->SetRenderState(D3DRS_DESTBLEND, D3DBLEND_INVSRCCOLOR);
```



La modifica degli Stati di Blend di origine e di destinazione può fornire l'aspetto degli oggetti emissivo in un'atmosfera nebbiosa o polverosa. Ad esempio, se l'applicazione modella le fiamme, forza i campi, i Beam plasmatici o gli oggetti radianti allo stesso modo in un ambiente nebbioso, impostare gli Stati di Blend di origine e di destinazione su D3DBLEND \_ One.

Un'altra applicazione di fusione alfa consiste nel controllare l'illuminazione in una scena 3D, denominata anche Light Mapping. Impostando lo stato di Blend di origine su D3DBLEND \_ zero e lo stato di Blend di destinazione su D3DBLEND \_ SRCALPHA, una scena viene offuscata in base alle informazioni alfa di origine. La primitiva di origine viene usata come mappa chiara che ridimensiona il contenuto del buffer del frame per scurirlo quando appropriato. Questo produce un mapping chiaro monocromatico.

È possibile ottenere il mapping della luce dei colori impostando lo stato di fusione alfa di origine su D3DBLEND \_ zero e lo stato di Blend di destinazione su D3DBLEND \_ SRCCOLOR.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Stati di rendering](render-states.md)
</dt> </dl>

 

 
