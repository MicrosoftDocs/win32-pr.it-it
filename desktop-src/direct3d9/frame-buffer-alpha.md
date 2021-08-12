---
description: La fusione alfa del buffer dei frame è leggermente diversa da quella dei vertici alfa, alfa materiale e alfa della trama.
ms.assetid: 3664215d-ad03-400e-beab-b0421cf6b693
title: Frame Buffer Alpha (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec091e8cc42d6b21142d3b9372f6d2931ba25d1dfe12aa7717e0b09acf0b0718
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118297496"
---
# <a name="frame-buffer-alpha-direct3d-9"></a>Frame Buffer Alpha (Direct3D 9)

La fusione alfa del buffer dei frame è leggermente diversa da quella dei vertici alfa, alfa materiale e alfa della trama. Vertice, materiale e alfa della trama impostano valori di trasparenza che vengono usati solo per la primitiva corrente e di per sé non hanno alcun effetto su altre primitive. La fusione alfa del buffer dei frame controlla il modo in cui la primitiva corrente viene combinata con i pixel esistenti nel buffer dei frame per produrre un colore finale in pixel.

Quando si esegue la fusione alfa, vengono combinati due colori: un colore di origine e un colore di destinazione. Il colore di origine deriva dall'oggetto trasparente, il colore di destinazione è il colore già presente nella posizione in pixel. Il colore di destinazione è il risultato del rendering di un altro oggetto che si trova dietro l'oggetto trasparente, ad esempio l'oggetto che sarà visibile tramite l'oggetto trasparente. La fusione alfa usa una formula per controllare il rapporto tra gli oggetti di origine e di destinazione.


```
Final Color = ObjectColor * SourceBlendFactor + PixelColor * DestinationBlendFactor 
```



ObjectColor è il contributo della primitiva di cui viene eseguito il rendering nella posizione in pixel corrente. PixelColor è il contributo dal buffer dei frame nella posizione in pixel corrente.

Il set di fattori di fusione alfa che è possibile usare è elencato di seguito.



| Fattore di modalità blend         | Descrizione                                                                                                                                                                              |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DBLEND \_ ZERO            | (0, 0, 0, 0)                                                                                                                                                                             |
| D3DBLEND \_ ONE             | (1, 1, 1, 1)                                                                                                                                                                             |
| D3DBLEND \_ SRCCOLOR        | (Rs, Gs, Bs, As)                                                                                                                                                                         |
| D3DBLEND \_ INVSRCCOLOR     | (1-Rs, 1-Gs, 1-Bs, 1-As)                                                                                                                                                                 |
| D3DBLEND \_ SRCALPHA        | (As, As, As, As)                                                                                                                                                                         |
| D3DBLEND \_ INVSRCALPHA     | (1-As, 1-As, 1-As, 1-As)                                                                                                                                                                 |
| D3DBLEND \_ DESTALPHA       | (Ad, Ad, Ad, Ad)                                                                                                                                                                         |
| D3DBLEND \_ INVDESTALPHA    | (1-Ad, 1-Ad, 1-Ad, 1-Ad)                                                                                                                                                                 |
| D3DBLEND \_ DESTCOLOR       | (Rd, Gd, Bd, Ad)                                                                                                                                                                         |
| D3DBLEND \_ INVDESTCOLOR    | (1-Rd, 1-Gd, 1-Bd, 1-Ad)                                                                                                                                                                 |
| D3DBLEND \_ SRCALPHASAT     | (f, f, f, 1); f = min(As, 1-Ad)                                                                                                                                                          |
| D3DBLEND \_ BOTHSRCALPHA    | Obsoleto per DirectX 6 e versioni successive. È possibile ottenere lo stesso effetto impostando i fattori di blend di origine e destinazione su D3DBLEND \_ SRCALPHA e D3DBLEND \_ INVSRCALPHA in chiamate separate. |
| D3DBLEND \_ BOTHINVSRCALPHA | Obsoleto per DirectX 6. È possibile ottenere lo stesso effetto impostando i fattori di blend di origine e destinazione su D3DBLEND \_ INVSRCALPHA e D3DBLEND \_ SRCALPHA in chiamate separate.           |
| D3DBLEND \_ BLENDFACTOR     | Usare color.r, color.g, color.b e color.a ottenuti dall'impostazione D3DRS \_ BLENDFACTOR.                                                                                                 |
| D3DBLEND \_ INVBLENDFACTOR  | Usare 1-color.r, 1-color.g, 1-color.b e 1-color.a ottenuti dall'impostazione D3DRS \_ BLENDFACTOR.                                                                                         |



 

Direct3D usa lo stato di rendering D3DRS \_ ALPHABLENDENABLE per abilitare la fusione della trasparenza alfa. Il tipo di fusione alfa eseguita dipende dagli stati di rendering D3DRS \_ SRCBLEND e D3DRS \_ DESTBLEND. Gli stati di blend di origine e di destinazione vengono usati in coppie. Il frammento di codice seguente imposta lo stato di blend di origine su D3DBLEND SRCCOLOR e lo stato di blend di destinazione su \_ D3DBLEND \_ INVSRCCOLOR.


```
// This code fragment assumes that lpD3DDevice is a 
//   valid pointer to a device.

// Enable alpha blending.
lpD3DDevice->SetRenderState(D3DRS_ALPHABLENDENABLE, 
                            TRUE);

// Set the source blend state.
lpD3DDevice->SetRenderState(D3DRS_SRCBLEND, 
                            D3DBLEND_SRCCOLOR);

// Set the destination blend state.
lpD3DDevice->SetRenderState(D3DRS_DESTBLEND, 
                            D3DBLEND_INVSRCCOLOR);
```



Questo codice esegue una fusione lineare tra il colore di origine (il colore della primitiva di cui viene eseguito il rendering nella posizione corrente) e il colore di destinazione (il colore nella posizione corrente nel buffer dei frame). L'aspetto risultante è simile a una lente colorata in quanto parte del colore dell'oggetto di destinazione sembra essere trasmessa tramite l'oggetto di origine; il resto sembra essere inassato.

Molti di questi fattori di fusione richiedono valori alfa nella trama per funzionare correttamente. Pertanto, quando si usa vertice o alfa materiale, l'applicazione è limitata alle modalità che produrranno risultati interessanti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Fusione alfa](alpha-blending.md)
</dt> </dl>

 

 



