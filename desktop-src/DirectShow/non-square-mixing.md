---
description: Combinazione non quadrata
ms.assetid: 8d27a921-5638-43ac-807d-e3bd7b9b2de8
title: Combinazione non quadrata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4674891b7b9d44cb35522b6040723bc71436d677b10a4326d9f00a269ce3aff2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102413"
---
# <a name="non-square-mixing"></a>Combinazione non quadrata

Questo argomento si applica Windows XP Service Pack 2 o versioni successive.

Quando VMR-9 combina due o più flussi, è possibile che si verifichi il ridimensionamento in due punti: quando il mixer compone i flussi di input e quando allocator-presenter esegue il rendering dell'immagine composita.

![Operazioni di combinazione di vmr](images/vmr-nonsquare-mixing.png)

Le versioni precedenti di VMR-9 componevano sempre i flussi di input usando proporzioni in pixel quadrate (1:1), anche quando era presente un solo flusso video. Se il flusso di input ha pixel non quadrati, ciò ha causato un'operazione di ridimensionamento non necessaria. Il ridimensionamento deve essere evitato il più possibile, naturalmente, perché riduce la qualità dell'immagine finale.

A partire Windows XP Service Pack 2, VMR-9 supporta due modi diversi per evitare il problema della scalabilità doppia:

-   Implementare un allocatore-presentatore personalizzato e supportare [**l'interfaccia IVMRSurfaceAllocatorEx9.**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9)
-   Usare la modalità di combinazione non quadrata.

Questa sezione descrive la modalità di combinazione non quadrata. Le applicazioni possono combinare entrambe le tecniche.

**Funzionamento della combinazione non quadrata**

In modalità di combinazione non quadrata, VMR-9 seleziona un flusso di input come dimensione di destinazione e PAR. Il mixer della macchina virtuale non ridimensiona il video da tale flusso o da qualsiasi altro flusso con le stesse dimensioni di immagine e par. Flussi dimensioni o proporzioni diverse vengono ridimensionate in modo che corrispondano al par di destinazione e alla casella di testo in base alle dimensioni dell'immagine di output finale.

La scelta dei flussi dipende dalla modalità di combinazione corrente:

-   La modalità di combinazione YUV è limitata a un flusso video sul pin 0. Gli altri segnaposto possono avere flussi di immagini secondarie o sottotitoli codificati. Pertanto, VMR-9 seleziona sempre il pin 0 per le dimensioni dell'immagine di destinazione e PAR.
-   In modalità di combinazione RGB, la macchina virtuale seleziona il flusso con le dimensioni massime dell'immagine. Se ne sono presenti più di uno, seleziona quello con l'ordine z più alto; e se è ancora presente un valore di pari livello, seleziona il flusso con il numero di pin più basso.

**Esempi di operazione**

**Esempio 1.** Il flusso 0 è di 720 x 480 pixel con proporzioni dell'immagine di 16:9. Il flusso 1 è di 640 x 480 pixel con proporzioni dell'immagine di 4:3.

In questo esempio, il flusso 0 ha le dimensioni massime dell'immagine, quindi la macchina virtuale sceglie questo flusso, indipendentemente dalla modalità di combinazione RGB o YUB. PAR è 32:27 (16:9 / 720:480), vale a dire che l'immagine deve essere estesa orizzontalmente di questo rapporto per produrre le proporzioni dell'immagine 16:9 corrette.

Per corrispondere al par di destinazione, il mixer VMR ridimensiona il flusso 1 in base al rapporto inverso (27:32), determinando un'immagine 540 x 480. I due flussi vengono quindi compositi su una superficie. Per visualizzare correttamente l'immagine risultante, il presentatore dell'allocatore deve estendere l'immagine orizzontalmente per adattarla alle proporzioni dell'immagine 16:9.

![Esempio 1.](images/vmr-nonsquare-mixing2.png)

**Esempio 2.** Il flusso 0 è di 720 x 480 pixel con proporzioni dell'immagine di 16:9. Il flusso 1 è di 1024 x 768 pixel con proporzioni dell'immagine di 4:3.

Se VMR-9 usa la modalità di combinazione YUV, seleziona sempre il flusso 0. Di conseguenza, estende il flusso da 1 a 540 x 480 pixel, in modo che corrisponda al valore PAR del flusso 0.

Se VMR-9 usa la modalità di combinazione RGB, seleziona il flusso 1 come destinazione, perché il flusso ha le dimensioni massime dell'immagine. Estende il flusso 0 a una dimensione dell'immagine di 1024 x 576 pixel. Si noti che in questo caso, l'immagine composita ha un valore PAR di 1:1, quindi allocator-presenter non deve essere corretto per i pixel non quadrati. Potrebbe comunque essere necessario estendere il video in modo da includere il rettangolo di destinazione.

**Uso della modalità di combinazione non quadrata**

La modalità di combinazione non quadrata è consigliata se si verifica una delle condizioni seguenti:

-   L'applicazione non invia mai più di un flusso video a VMR-9.
-   L'applicazione esegue il rendering di file DVD, tv o ms-dvr. In questo caso, è consigliabile usare anche la modalità di combinazione YUV, se l'hardware grafico la supporta.

Se l'applicazione combina più flussi video che possono avere dimensioni dell'immagine o proporzioni pixel variabili, è consigliabile utilizzare la modalità di combinazione quadrata predefinita.

Per configurare la modalità di combinazione non quadrata, il grafico dei filtri deve essere arrestato e tutti i pin di input devono essere disconnessi in VMR-9. Chiamare quindi [**IVMRMixerControl9::SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) con il flag MixerPref9 \_ NonSquareMixing:


```C++
DWORD dwPrefs;
pMixControl->GetMixingPrefs(&dwPrefs);  
dwPrefs |= MixerPref9_NonSquareMixing;
pMixControl->SetMixingPrefs(dwPrefs);
```



> [!Note]  
> Se si combina il flag MixerPref9 \_ NonSquareMixing con il flag MixerPref9 \_ ARAdjustXorY, VMR-9 ignora il flag MixerPref9 \_ ARAdjustXorY.

 

Se l'applicazione usa un allocatore-presentatore personalizzato con modalità di combinazione non quadrata, tenere presente che l'immagine composita può avere un par non quadrato. Allocator-presenter deve ridimensionare l'immagine in un quadrato (1:1) PAR.

**Bitmap statiche**

Se si usa l'interfaccia [**IVMRMixerBitmap9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9) per unire una bitmap statica al video, è consigliabile considerare la bitmap come un secondo flusso video ai fini della modalità di combinazione VMR.

La macchina virtuale considera la bitmap come se la mappa di bit abbia lo stesso par della destinazione. Non ridimensiona la bitmap per adattarla alle proporzioni in pixel della destinazione. Nella configurazione predefinita della macchina virtuale, la destinazione ha un par 1:1, che corrisponde alla maggior parte delle bitmap. In modalità di combinazione non quadrata, la destinazione potrebbe avere pixel non quadrati. Per assicurarsi che la bitmap venga visualizzata correttamente, l'applicazione deve fornire un'immagine il cui PAR corrisponde al PAR di destinazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso della modalità di combinazione VMR](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



