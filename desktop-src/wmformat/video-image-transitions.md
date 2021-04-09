---
title: Transizioni di immagini video
description: Transizioni di immagini video
ms.assetid: 201ddbfb-567b-4893-b754-569f1e7d8466
keywords:
- Windows Media Format SDK, transizioni di immagini video
- ASF (Advanced Systems Format), transizioni di immagini video
- ASF (Advanced Systems Format), transizioni di immagini video
- transizioni di immagini video
- Codec Windows Media Video 9 image V2
- codecs, Windows Media Video 9 image V2 codec
- flussi video, codec Windows Media Video 9 image V2
- flussi video, transizioni di immagini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbfd02628a78196a73750c2c0ff6b9e9c3d6729c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044522"
---
# <a name="video-image-transitions"></a>Transizioni di immagini video

Il codec Windows Media Video 9 image V2 aggiunge un'animazione a una serie di immagini, ottenendo così un flusso video. Il codec può manipolare due immagini contemporaneamente, fondendole insieme e creando una transizione da una all'altra in base alla configurazione fornita. Questa sezione descrive le transizioni supportate e i parametri necessari.

Le transizioni sono elencate nella tabella seguente in base agli identificatori globali.



| Identificatore di transizione                                                                           | Descrizione                                                                                                                                  |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [**WMT \_ VIDEOIMAGE \_ Transition \_ Papillon \_**](wmt-videoimage-transition-bow-tie.md)              | La nuova immagine viene rivelata in un set di triangoli sui lati opposti del frame.                                                                  |
| [**\_cerchio di \_ transizione \_ VIDEOIMAGE di WMT**](wmt-videoimage-transition-circle.md)                 | La nuova immagine viene rivelata in un cerchio.                                                                                                           |
| [**\_ \_ \_ dissolvenza incrociata transizione VIDEOIMAGE WMT \_**](wmt-videoimage-transition-cross-fade.md)        | Nessuna transizione speciale, i coefficienti di Blend delle due immagini determinano la dissolvenza incrociata (dissolvenza).                                         |
| [**\_ \_ diagonale transizione VIDEOIMAGE WMT \_**](wmt-videoimage-transition-diagonal.md)             | Viene rilevata una nuova immagine lungo una linea diagonale che ha origine in un angolo del frame.                                                          |
| [**WMT \_ VIDEOIMAGE \_ Transition \_ Diamond**](wmt-videoimage-transition-diamond.md)               | La nuova immagine viene rivelata in un rombo.                                                                                                          |
| [**\_ \_ dissolvenza WMT VIDEOIMAGE transizione \_ \_ a \_ colore**](wmt-videoimage-transition-fade-to-color.md) | Viene risolto dall'immagine in un frame di colore a tinta unita.                                                                                          |
| [**WMT \_ VIDEOIMAGE \_ - \_ riempimento della transizione \_**](wmt-videoimage-transition-filled-v.md)            | La nuova immagine viene rivelata in un triangolo originato da un lato del frame.                                                                  |
| [**WMT \_ VIDEOIMAGE \_ transizione \_ Flip**](wmt-videoimage-transition-flip.md)                     | L'immagine precedente viene ruotata su un asse y attraverso il centro del frame. La nuova immagine viene rivelata come parte posteriore dell'immagine precedente.                    |
| [**\_Insert WMT VIDEOIMAGE \_ Transition \_**](wmt-videoimage-transition-inset.md)                   | La nuova immagine viene rivelata da un rettangolo originato da un angolo del frame.                                                               |
| [**\_ \_ Iris transizione VIDEOIMAGE \_ WMT**](wmt-videoimage-transition-iris.md)                     | Viene rilevata una nuova immagine lungo un asse x e un asse y.                                                                                          |
| [**\_ \_ \_ Roll pagina transizione VIDEOIMAGE \_ di WMT**](wmt-videoimage-transition-page-roll.md)          | L'immagine precedente viene trasformata in un effetto di capovolgimento della pagina, mostrando la nuova immagine sotto.                                                      |
| [**\_rettangolo di \_ transizione \_ VIDEOIMAGE di WMT**](wmt-videoimage-transition-rectangle.md)           | La nuova immagine viene rivelata da un rettangolo all'interno del frame.                                                                                       |
| [**WMT \_ VIDEOIMAGE \_ transizione \_**](wmt-videoimage-transition-reveal.md)                 | La nuova immagine viene rivelata lungo una linea retta originata da un lato del frame.                                                          |
| [**\_diapositiva di \_ transizione \_ VIDEOIMAGE di WMT**](wmt-videoimage-transition-slide.md)                   | L'immagine precedente viene spostata all'esterno del frame, mostrando la nuova immagine sotto.                                                                       |
| [**\_ \_ divisione transizione VIDEOIMAGE di WMT \_**](wmt-videoimage-transition-split.md)                   | La nuova immagine viene rivelata da una suddivisione orizzontale o verticale nell'immagine precedente. La divisione viene visualizzata lungo una linea retta che inizia all'interno del frame. |
| [**\_stella della \_ transizione \_ VIDEOIMAGE di WMT**](wmt-videoimage-transition-star.md)                     | La nuova immagine viene rivelata da una stella a cinque punte all'interno del frame.                                                                               |
| [**\_ \_ rotellina di transizione VIDEOIMAGE di WMT \_**](wmt-videoimage-transition-wheel.md)                   | La nuova immagine viene rivelata da quattro spoke rotanti con un punto di perno comune.                                                                     |



 

Ogni transizione è descritta in modo completo in un argomento.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida di riferimento alla programmazione**](programming-reference.md)
</dt> <dt>

[**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2)
</dt> </dl>

 

 




