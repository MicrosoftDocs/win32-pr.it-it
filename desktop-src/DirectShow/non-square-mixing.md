---
description: Combinazione non quadrata
ms.assetid: 8d27a921-5638-43ac-807d-e3bd7b9b2de8
title: Combinazione non quadrata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79d23f423f0dbe19f1ff0ba35c44f8fd2f8732bc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522050"
---
# <a name="non-square-mixing"></a>Combinazione non quadrata

Questo argomento si applica a Windows XP Service Pack 2 o versioni successive.

Quando VMR-9 combina due o più flussi, è possibile che si verifichi il ridimensionamento in due punti: quando il mixer composi i flussi di input e quando Allocator-Presenter esegue il rendering dell'immagine composita.

![operazioni di combinazione VMR](images/vmr-nonsquare-mixing.png)

Le versioni precedenti di VMR-9 compostano sempre i flussi di input usando una percentuale quadrata (1:1) di proporzioni in pixel, anche in presenza di un unico flusso video. Se il flusso di input presenta pixel non quadrati, questo ha causato un'operazione di ridimensionamento non necessaria. Il ridimensionamento deve essere evitato quanto più possibile, ovviamente perché peggiora la qualità dell'immagine finale.

A partire da Windows XP Service Pack 2, VMR-9 supporta due modi diversi per evitare il problema del doppio ridimensionamento:

-   Implementare un allocatore-Presenter personalizzato e supportare l'interfaccia [**IVMRSurfaceAllocatorEx9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatorex9) .
-   Usare la modalità di combinazione non quadrata.

In questa sezione viene descritta la modalità di combinazione non quadrata. Le applicazioni possono combinare entrambe le tecniche.

**Funzionamento della combinazione non quadrata**

In modalità di combinazione non quadrata, VMR-9 Seleziona un flusso di input come dimensione di destinazione e PAR. Il mixer di VMR non ridimensiona il video da tale flusso o da altri flussi con le stesse dimensioni dell'immagine e PAR. I flussi con dimensioni o proporzioni diverse vengono ridimensionati in modo da corrispondere alla parità di destinazione e alla cassettatura per adattarsi alle dimensioni dell'immagine di output finale.

La scelta dei flussi dipende dalla modalità di combinazione corrente:

-   La modalità di combinazione YUV è limitata a un flusso video sul pin 0. (Gli altri pin possono avere flussi di didascalie o sottotitoli). Pertanto, VMR-9 seleziona sempre il pin 0 per la dimensione dell'immagine di destinazione e la PAR.
-   In modalità di combinazione RGB, VMR seleziona il flusso con le dimensioni massime dell'immagine. Se è presente più di un oggetto, viene selezionato quello con l'ordine z più elevato; Se è ancora presente una cravatta, viene selezionato il flusso con il numero di pin più basso.

**Esempi di operazione**

**Esempio 1.** Il flusso 0 è 720 x 480 pixel con proporzioni dell'immagine 16:9. Il flusso 1 è un 640 x 480 pixel con proporzioni dell'immagine 4:3.

In questo esempio, il flusso 0 ha le dimensioni massime dell'immagine, quindi VMR sceglie questo flusso, indipendentemente dalla modalità di combinazione RGB o dalla modalità di combinazione YUB. Il valore PAR è 32:27 (16:9/720:480), che indica che l'immagine deve essere allungata orizzontalmente in base a questo rapporto per produrre le proporzioni dell'immagine 16:9 corrette.

Per corrispondere alla parità di destinazione, il mixer VMR ridimensiona il flusso 1 in base al rapporto inverso (27:32), ottenendo un'immagine 540 x 480. I due flussi vengono quindi composti in una superficie. Per visualizzare correttamente l'immagine risultante, il relatore allocatore deve allungare l'immagine orizzontalmente per adattarsi alle proporzioni dell'immagine 16:9.

![esempio 1.](images/vmr-nonsquare-mixing2.png)

**Esempio 2.** Il flusso 0 è 720 x 480 pixel con proporzioni dell'immagine 16:9. Il flusso 1 è un 1024 x 768 pixel con proporzioni dell'immagine 4:3.

Se VMR-9 USA la modalità di combinazione YUV, seleziona sempre il flusso 0. Estende quindi il flusso da 1 a 540 x 480 pixel, in modo da corrispondere alla PAR del flusso 0.

Se VMR-9 USA la modalità di combinazione RGB, seleziona il flusso 1 come destinazione, perché tale flusso ha le dimensioni massime dell'immagine. Estende il flusso 0 alla dimensione di un'immagine di 1024 x 576 pixel. Si noti che in questo caso l'immagine composita ha un valore pari a 1:1, pertanto non è necessario che l'allocatore-Presenter venga corretto per i pixel non quadrati. Potrebbe comunque essere necessario estendere il video per tenere conto del rettangolo di destinazione.

**Uso della modalità di combinazione non quadrata**

La modalità di combinazione non quadrata è consigliata se si verifica una delle condizioni seguenti:

-   L'applicazione non invia mai più di un flusso video a VMR-9.
-   L'applicazione esegue il rendering dei file DVD, TV o MS-DVR. In questo caso, è consigliabile usare anche la modalità di combinazione YUV se l'hardware grafico lo supporta.

Se l'applicazione combina più flussi video che possono avere dimensioni diverse per le immagini o proporzioni di pixel, è consigliabile usare la modalità di combinazione quadrata predefinita.

Per configurare la modalità di combinazione non quadrata, è necessario arrestare il grafico del filtro e tutti i pin di input disconnessi in VMR-9. Chiamare quindi [**IVMRMixerControl9:: SetMixingPrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrmixercontrol9-setmixingprefs) con il \_ flag NonSquareMixing di MixerPref9:


```C++
DWORD dwPrefs;
pMixControl->GetMixingPrefs(&dwPrefs);  
dwPrefs |= MixerPref9_NonSquareMixing;
pMixControl->SetMixingPrefs(dwPrefs);
```



> [!Note]  
> Se si combina il \_ flag MixerPref9 NonSquareMixing con il \_ flag MixerPref9 ARADJUSTXORY, VMR-9 ignora il flag MixerPref9 ARAdjustXorY \_ .

 

Se l'applicazione usa un presentatore-Presenter personalizzato con modalità di combinazione non quadrata, tenere presente che l'immagine composita potrebbe avere una PAR non quadrata. Allocator-Presenter deve ridimensionare l'immagine in una PAR quadrata (1:1).

**Bitmap statiche**

Se si usa l'interfaccia [**IVMRMixerBitmap9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixerbitmap9) per combinare una bitmap statica nel video, è consigliabile considerare la bitmap come un secondo flusso video per la modalità di combinazione VMR.

Il VMR considera la bitmap come avente la stessa parità della destinazione. Non ridimensiona la bitmap per adattarla alle proporzioni in pixel della destinazione. Nella configurazione predefinita di VMR, la destinazione ha una PAR 1:1, che corrisponde alla maggior parte delle bitmap. In modalità di combinazione non quadrata, la destinazione potrebbe avere pixel non quadrati. Per assicurarsi che la bitmap venga visualizzata correttamente, l'applicazione deve fornire un'immagine il cui PAR corrisponda alla parità di destinazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso della modalità di combinazione VMR](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



