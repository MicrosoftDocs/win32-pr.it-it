---
description: Il valore alfa di un colore ne controlla la trasparenza. L'abilitazione della fusione alfa consente di unire colori, materiali e trame su una superficie con trasparenza su un'altra superficie.
ms.assetid: e8e925d5-262d-45c0-be9f-21c9a103d7b7
title: Stato di fusione alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc4bd012340fae9e7597479d846d18db37c32d6f95a42118ba7444ad63a2e1cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045209"
---
# <a name="alpha-blending-state-direct3d-9"></a>Stato di fusione alfa (Direct3D 9)

Il valore alfa di un colore ne controlla la trasparenza. L'abilitazione della fusione alfa consente di unire colori, materiali e trame su una superficie con trasparenza su un'altra superficie.

Per altre informazioni, vedere [Alpha Texture Blending (Direct3D 9) e](alpha-texture-blending.md) Texture [Blending (Direct3D 9) (Fusione di trame -Direct3D 9).](texture-blending.md)

Le applicazioni scritte in C++ usano lo stato di rendering [**D3DRS \_ ALPHABLENDENABLE**](./d3drenderstatetype.md) per abilitare la fusione della trasparenza alfa. L'API Direct3D consente molti tipi di fusione alfa. È tuttavia importante notare che l'hardware 3D dell'utente potrebbe non supportare tutti gli stati di fusione consentiti da Direct3D.

Il tipo di fusione alfa eseguita dipende dagli stati di rendering [**D3DRS \_ SRCBLEND**](./d3drenderstatetype.md) e **D3DRS \_ DESTBLEND.** Gli stati di blend di origine e di destinazione vengono usati in coppie. L'esempio di codice seguente illustra come lo stato di blend di origine è impostato su D3DBLEND SRCCOLOR e lo stato di blend di destinazione è impostato su \_ D3DBLEND \_ INVSRCCOLOR.


```
// This code example assumes that d3dDevice is a
// valid pointer to an IDirect3DDevice9 interface.

// Set the source blend state.
d3dDevice->SetRenderState(D3DRS_SRCBLEND, D3DBLEND_SRCCOLOR);

// Set the destination blend state.

d3dDevice->SetRenderState(D3DRS_DESTBLEND, D3DBLEND_INVSRCCOLOR);
```



La modifica degli stati di blend di origine e di destinazione può dare l'aspetto di oggetti emissivi in un'aria nebbiosa o tura. Ad esempio, se l'applicazione modella i campi di forza, i campi di forza o gli oggetti radianti simili in un ambiente nebbioso, impostare gli stati di fusione di origine e di destinazione su D3DBLEND \_ ONE.

Un'altra applicazione della fusione alfa è il controllo dell'illuminazione in una scena 3D, detta anche mapping della luce. Impostando lo stato di blend di origine su D3DBLEND ZERO e lo stato di blend di destinazione su \_ D3DBLEND SRCALPHA, una scena viene scura in base alle informazioni \_ alfa di origine. La primitiva di origine viene usata come mappa di luce che ridimensiona il contenuto del buffer dei fotogrammi per scurirlo quando appropriato. In questo modo viene generato il mapping di luce monocromatica.

È possibile ottenere il mapping della luce del colore impostando lo stato di fusione alfa di origine su D3DBLEND ZERO e lo stato di sfumatura di destinazione \_ su D3DBLEND \_ SRCCOLOR.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Stati di rendering](render-states.md)
</dt> </dl>

 

 
