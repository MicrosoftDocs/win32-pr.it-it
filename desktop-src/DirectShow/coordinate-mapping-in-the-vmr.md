---
description: Mapping delle coordinate nella macchina virtuale
ms.assetid: f0821b90-51d1-4e77-8aed-04337a3dd623
title: Mapping delle coordinate nella macchina virtuale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad128e4d4e40fe3141f0b23edde1e06df8c5044e0a9877e2d9a2fcc3f293a9fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073797"
---
# <a name="coordinate-mapping-in-the-vmr"></a>Mapping delle coordinate nella macchina virtuale

In questa sezione vengono descritte le cinque trasformazioni applicate a un'immagine di origine prima di essere mappate dal VMR all'immagine di output finale.

1.  La trasformazione *T(Src) esegue* il mapping del rettangolo di origine al rettangolo di destinazione. Sono specificati dai membri **rcSource** e **rcTarget** della struttura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) o [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) nel tipo di supporto. Questo mapping pre-elabora l'immagine di origine durante il passaggio al vmr.
2.  La trasformazione *T(Flag)* esegue qualsiasi manipolazione di immagine specificata dai flag nell'esempio multimediale. Sono incluse trasformazioni come la traslazione verticale e la scalabilità per contenere i flag di interlacciamento bob. La trasformazione interlacciato raddoppia l'altezza dell'immagine ed eventualmente converte l'immagine di metà di una linea video se si trova nel campo dispari.
3.  La trasformazione *T(AR)* regola l'immagine in pixel quadrati, in base alle proporzioni dell'immagine. Per i tipi di supporti **VIDEOINFOHEADER,** le proporzioni sono determinate dalle dimensioni dell'immagine. Per i tipi **VIDEOINFOHEADER2,** le proporzioni sono determinate dai campi **dwPictAspectRatioX** e **dwPictAspectRatioY,** a meno che non siano impostati i flag \_ AMCONTROL PAD \_ TO \_ 16x9 o AMCONTROL \_ PAD TO \_ \_ 4x3. Questa trasformazione presuppone che l'impostazione di visualizzazione del monitoraggio corrisponda alle proporzioni fisiche del monitoraggio. Ad esempio, se l'utente ha un monitor con proporzioni 4 x 3, ma imposta la visualizzazione su 1280 x 768 pixel (5 x 3), l'immagine non avrà le proporzioni corrette.
4.  La trasformazione *T(Mix)* trasforma l'immagine all'interno dell'immagine di destinazione usando i rettangoli normalizzati specificati nei metodi [**IVMRMixerControl.**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol) I rettangoli normalizzati consentono all'applicazione di organizzare il modo in cui i flussi di origine vengono posizionati e ridimensionati l'uno rispetto all'altro. La macchina virtuale calcola l'immagine di destinazione calcolando le dimensioni massime di tutte le immagini di origine e centrando ognuna all'interno di un rettangolo di delimitazione complessivo. Agli angoli del rettangolo di delimitazione viene assegnato l'intervallo (0,0) a (1,1). Il rettangolo di delimitazione viene corretto prima dell'esecuzione del grafo e rimane costante anche se i flussi vengono aggiunti o eliminati. I rettangoli di destinazione per ogni flusso possono trovarsi al di fuori dell'intervallo compreso tra (0,0) e (1,1) e essere comunque validi.
5.  Infine, una parte dell'immagine mista può essere trasformata dal mapping *T(Dst),* specificato dai rettangoli di origine e di destinazione [**nell'interfaccia IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) nella macchina virtuale. Se il Allocator-Presenter viene sostituito e **l'interfaccia IBasicVideo** non viene usata, l'applicazione deve implementare l'interfaccia [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) ed eseguire il mapping delle coordinate in uno spazio lineare 2D. Anche le coordinate del mouse restituite allo strumento di spostamento DVD devono essere in questo spazio. Ad esempio, se un'applicazione esegue il rendering del video su un cubo rotante, restituisce l'intera visualizzazione per il controllo senza finestra e restituisce le coordinate del mouse relative alla visualizzazione.

La trasformazione complessiva dell'immagine dai dati di origine al renderer finale è:

T = T(Src) \* T(Flag)T(Ar)T(Mix) \* T(Dst)\*

dove \* indica che l'immagine può essere ritagliata nell'immagine di destinazione in tale fase. Si noti che si tratta di tutte trasformazioni affine, quindi la macchina virtuale può combinarle in un'unica trasformazione.

L'inverso della trasformazione è:

![trasformazione inversa](images/vmrmapping-t-1.png)

Il fattore T(Src) T(Flag) T(Ar) è relativo alla risoluzione di origine. Nel fattore T(Mix), il rettangolo di origine normalizzato è relativo all'immagine con correzione degli aspetti. Il rettangolo di destinazione normalizzato è relativo alla risoluzione di output. Il diagramma seguente illustra queste relazioni.

![Passaggi di trasformazione delle immagini](images/vmrmapping-transform-steps.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso della macchina virtuale per gli sviluppatori DirectShow filtri](using-the-vmr-for-directshow-filter-developers.md)
</dt> </dl>

 

 



