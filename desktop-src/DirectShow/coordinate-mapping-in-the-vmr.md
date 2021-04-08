---
description: Mapping delle coordinate in VMR
ms.assetid: f0821b90-51d1-4e77-8aed-04337a3dd623
title: Mapping delle coordinate in VMR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c18b38249471e6e68e36f1b9051f51e920f62b31
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876237"
---
# <a name="coordinate-mapping-in-the-vmr"></a>Mapping delle coordinate in VMR

In questa sezione vengono descritte le cinque trasformazioni applicate a un'immagine di origine prima che venga eseguito il mapping di VMR nell'immagine di output finale.

1.  La trasformazione *T (src)* esegue il mapping del rettangolo di origine al rettangolo di destinazione. Questi vengono specificati dai membri **rcSource** e **RcTarget** della struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) o [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) nel tipo di supporto. Questo mapping pre-elabora l'immagine di origine mentre passa a VMR.
2.  La trasformazione *T (flag)* esegue tutte le modifiche alle immagini specificate dai flag nell'esempio multimediale. Incluse le trasformazioni, ad esempio la traslazione verticale e la scalabilità, per contenere i flag interlacci Bob. La trasformazione interlacciata raddoppia l'altezza dell'immagine e possibilmente converte l'immagine dalla metà di una linea video se si trova nel campo dispari.
3.  La trasformazione *T (AR)* regola l'immagine in pixel quadrati, in base alle proporzioni dell'immagine. Per i tipi di supporto **VIDEOINFOHEADER** , le proporzioni sono determinate dalle dimensioni dell'immagine. Per i tipi **VIDEOINFOHEADER2** , le proporzioni sono determinate dai campi **dwPictAspectRatioX** e **dwPictAspectRatioY** , a meno che non \_ \_ siano impostati i flag AMCONTROL su \_ 16x9 o AMCONTROL \_ Pad \_ per 4x3 \_ . Questa trasformazione presuppone che l'impostazione di visualizzazione del monitoraggio corrisponda alle proporzioni fisiche del monitoraggio. Se, ad esempio, l'utente dispone di un monitoraggio con proporzioni di 4 x 3, ma imposta la visualizzazione su 1280 x 768 pixel (5 x 3), l'immagine non avrà le proporzioni corrette.
4.  La trasformazione *T (Mix)* trasforma l'immagine all'interno dell'immagine di destinazione usando i rettangoli normalizzati specificati nei metodi [**IVMRMixerControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol) . I rettangoli normalizzati consentono all'applicazione di organizzare il modo in cui i flussi di origine sono posizionati e ridimensionati in relazione l'uno con l'altro. VMR calcola l'immagine di destinazione calcolando le dimensioni massime di tutte le immagini di origine e centrando ciascuna di esse all'interno di un rettangolo di delimitazione globale. Agli angoli del rettangolo di delimitazione viene assegnato l'intervallo (0, 0) a (1,1). Il rettangolo di delimitazione viene corretto prima dell'esecuzione del grafico e rimane costante anche se i flussi vengono aggiunti o eliminati. I rettangoli di destinazione per ogni flusso possono trovarsi all'esterno dell'intervallo (0, 0) a (1,1) e comunque essere validi.
5.  Infine, una parte dell'immagine mista può essere trasformata dal mapping *T (DST)*, specificato dai rettangoli di origine e di destinazione nell'interfaccia [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) in VMR. Se il Allocator-Presenter viene sostituito e l'interfaccia **IBasicVideo** non viene usata, l'applicazione deve implementare l'interfaccia [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) ed eseguire il mapping delle coordinate in uno spazio lineare 2D. Anche le coordinate del mouse restituite al navigatore DVD devono trovarsi in questo spazio. Se, ad esempio, un'applicazione esegue il rendering di video su un cubo rotante, restituirà l'intero schermo per il controllo senza finestra e restituirà le coordinate del mouse relative alla visualizzazione.

La trasformazione complessiva dell'immagine dai dati di origine al renderer finale è la seguente:

T = T (src) \* t (flag) t (AR) t (Mix) \* t (DST)\*

dove \* indica che l'immagine può essere ritagliata nell'immagine di destinazione in quella fase. Si noti che si tratta di tutte le trasformazioni affini, quindi il VMR può combinarle in un'unica trasformazione.

L'inverso della trasformazione è:

![trasformazione inversa](images/vmrmapping-t-1.png)

Il fattore T (src) T (flag) T (AR) è relativo alla risoluzione dell'origine. In Factor T (Mix) il rettangolo di origine normalizzato è relativo all'immagine con correzione dell'aspetto. Il rettangolo di destinazione normalizzato è relativo alla risoluzione dell'output. Nel diagramma seguente vengono illustrate queste relazioni.

![passaggi di trasformazione immagine](images/vmrmapping-transform-steps.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di VMR per gli sviluppatori di filtri DirectShow](using-the-vmr-for-directshow-filter-developers.md)
</dt> </dl>

 

 



