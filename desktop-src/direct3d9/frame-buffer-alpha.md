---
description: La fusione alfa del buffer dei frame è leggermente diversa da quella del vertice Alpha, dal materiale Alfa e dalla trama alfa.
ms.assetid: 3664215d-ad03-400e-beab-b0421cf6b693
title: Buffer frame alfa (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb310e2c66f43282e65425fd0d6c6a24961accaa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123858"
---
# <a name="frame-buffer-alpha-direct3d-9"></a>Buffer frame alfa (Direct3D 9)

La fusione alfa del buffer dei frame è leggermente diversa da quella del vertice Alpha, dal materiale Alfa e dalla trama alfa. Il vertice, il materiale e l'alfa di trama impostano i valori di trasparenza usati solo per la primitiva corrente e non hanno alcun effetto su altre primitive. La fusione alfa del buffer dei frame controlla il modo in cui la primitiva corrente viene combinata con i pixel esistenti nel buffer del frame per produrre un colore finale del pixel.

Quando si esegue la fusione alfa, vengono combinati due colori: un colore di origine e un colore di destinazione. Il colore di origine è dall'oggetto trasparente, il colore di destinazione è il colore già presente nella posizione dei pixel. Il colore di destinazione è il risultato del rendering di un altro oggetto dietro l'oggetto trasparente, ovvero l'oggetto che sarà visibile tramite l'oggetto trasparente. La fusione alfa usa una formula per controllare il rapporto tra gli oggetti di origine e di destinazione.


```
Final Color = ObjectColor * SourceBlendFactor + PixelColor * DestinationBlendFactor 
```



ObjectColor è il contributo della primitiva di cui viene eseguito il rendering nella posizione del pixel corrente. PixelColor è il contributo del buffer dei frame nella posizione del pixel corrente.

Il set di fattori di blend alfa che è possibile usare è riportato di seguito.



| Fattore modalità Blend         | Descrizione                                                                                                                                                                              |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DBLEND \_ zero            | (0, 0, 0, 0)                                                                                                                                                                             |
| D3DBLEND \_ One             | (1, 1, 1, 1)                                                                                                                                                                             |
| \_SRCCOLOR D3DBLEND        | (RS, GS, BS, As)                                                                                                                                                                         |
| \_INVSRCCOLOR D3DBLEND     | (1-RS, 1-GS, 1-BS, 1 come)                                                                                                                                                                 |
| \_SRCALPHA D3DBLEND        | (Come, come, come)                                                                                                                                                                         |
| \_INVSRCALPHA D3DBLEND     | (1-As, 1-As, 1-As, 1-As)                                                                                                                                                                 |
| \_DESTALPHA D3DBLEND       | (Ad, ad, ad, ad)                                                                                                                                                                         |
| \_INVDESTALPHA D3DBLEND    | (1-ad, 1-ad, 1-ad, 1-ad)                                                                                                                                                                 |
| \_DESTCOLOR D3DBLEND       | (Rd, GD, BD, ad)                                                                                                                                                                         |
| \_INVDESTCOLOR D3DBLEND    | (1-Rd, 1-GD, 1-BD, 1-ad)                                                                                                                                                                 |
| \_SRCALPHASAT D3DBLEND     | (f, f, f, 1); f = min (As, 1-ad)                                                                                                                                                          |
| \_BOTHSRCALPHA D3DBLEND    | Obsoleto per DirectX 6 e versioni successive. È possibile ottenere lo stesso risultato impostando i fattori di Blend di origine e di destinazione su D3DBLEND \_ SRCALPHA e D3DBLEND \_ INVSRCALPHA in chiamate separate. |
| \_BOTHINVSRCALPHA D3DBLEND | Obsoleto per DirectX 6. È possibile ottenere lo stesso risultato impostando i fattori di Blend di origine e di destinazione su D3DBLEND \_ INVSRCALPHA e D3DBLEND \_ SRCALPHA in chiamate separate.           |
| \_BLENDFACTOR D3DBLEND     | Usare color. r, color. g, color. b e color. a ottenuto dall' \_ impostazione BLENDFACTOR di D3DRS.                                                                                                 |
| \_INVBLENDFACTOR D3DBLEND  | Usare 1-color. r, 1-color. g, 1-color. b e 1-color. a ottenuto dall' \_ impostazione BLENDFACTOR di D3DRS.                                                                                         |



 

Direct3D usa lo \_ stato di rendering ALPHABLENDENABLE di D3DRS per abilitare la sfumatura di trasparenza alfa. Il tipo di fusione alfa eseguita dipende \_ dagli Stati di rendering D3DRS SRCBLEND e D3DRS \_ DESTBLEND. Gli Stati di Blend di origine e di destinazione vengono utilizzati nelle coppie. Il seguente frammento di codice imposta lo stato di Blend di origine su D3DBLEND \_ SRCCOLOR e lo stato di Blend di destinazione su D3DBLEND \_ INVSRCCOLOR.


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



Questo codice esegue una Blend lineare tra il colore di origine (il colore della primitiva di cui viene eseguito il rendering nella posizione corrente) e il colore di destinazione (il colore in corrispondenza della posizione corrente nel buffer del frame). L'aspetto risultante è simile a quello colorato in quanto il colore dell'oggetto di destinazione sembra essere trasmesso tramite l'oggetto di origine. il resto sembra essere assorbito.

Molti di questi fattori di Blend richiedono che i valori alfa nella trama funzionino correttamente. Quindi, quando si usa il vertice o il materiale Alfa, l'applicazione è limitata al modo in cui le modalità produrranno risultati interessanti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Fusione alfa](alpha-blending.md)
</dt> </dl>

 

 



