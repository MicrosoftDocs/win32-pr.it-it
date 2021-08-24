---
title: Transizioni di immagini video
description: Transizioni di immagini video
ms.assetid: 201ddbfb-567b-4893-b754-569f1e7d8466
keywords:
- Windows Media Format SDK, transizioni di immagini video
- Advanced Systems Format (ASF), transizioni di immagini video
- ASF (Advanced Systems Format), transizioni di immagini video
- transizioni di immagini video
- Windows Codec Media Video 9 Image v2
- codec, codec Windows Codec Media Video 9 Image v2
- flussi video, codec Windows Media Video 9 Image v2
- flussi video, transizioni di immagini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b0a915f34ac9a2dcc00f8bcec739d48051361c1744e8e455166d56238529d9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119771241"
---
# <a name="video-image-transitions"></a>Transizioni di immagini video

Il codec Windows Media Video 9 Image v2 anima una serie di immagini, determinando un flusso video. Il codec può modificare due immagini contemporaneamente, combinandole insieme e creando una transizione da una all'altra in base alla configurazione offerta. Questa sezione descrive le transizioni supportate e i parametri necessari.

Le transizioni sono elencate nella tabella seguente in base ai relativi identificatori globali.



| Identificatore della transizione                                                                           | Descrizione                                                                                                                                  |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [**WMT \_ VIDEOIMAGE \_ TRANSITION \_ BOW \_ TIE**](wmt-videoimage-transition-bow-tie.md)              | La nuova immagine viene rivelata in un set di triangoli sui lati opposti del frame.                                                                  |
| [**WMT \_ VIDEOIMAGE \_ TRANSITION \_ CIRCLE**](wmt-videoimage-transition-circle.md)                 | La nuova immagine viene rivelata in un cerchio.                                                                                                           |
| [**DISSOLVENZA \_ INCROCIATA \_ TRANSIZIONE VIDEOIMAGE \_ WMT \_**](wmt-videoimage-transition-cross-fade.md)        | Nessuna transizione speciale, i coefficienti di fusione delle due immagini determinano la dissolvenza incrociata (dissolvenza).                                         |
| [**WMT \_ VIDEOIMAGE \_ TRANSITION \_ DIAGONAL**](wmt-videoimage-transition-diagonal.md)             | La nuova immagine viene rivelata lungo una linea diagonale che ha origine in un angolo del frame.                                                          |
| [**WMT \_ VIDEOIMAGE \_ TRANSITION \_ DIAMOND**](wmt-videoimage-transition-diamond.md)               | La nuova immagine viene rivelata in un diamante.                                                                                                          |
| [**DISSOLVENZA \_ DELLA TRANSIZIONE DI WMT VIDEOIMAGE AL \_ \_ \_ \_ COLORE**](wmt-videoimage-transition-fade-to-color.md) | Si dissolve dall'immagine a una cornice di colore a tinta unita.                                                                                          |
| [**WMT \_ VIDEOIMAGE \_ TRANSITION \_ FILLED \_ V**](wmt-videoimage-transition-filled-v.md)            | La nuova immagine viene rivelata in un triangolo proveniente da un lato del frame.                                                                  |
| [**CAPOVOLGIMENTO \_ TRANSIZIONE \_ WMT VIDEOIMAGE \_**](wmt-videoimage-transition-flip.md)                     | L'immagine precedente viene ruotata su un asse y attraverso il centro del frame. La nuova immagine viene rivelata come la parte posteriore dell'immagine precedente.                    |
| [**WMT \_ VIDEOIMAGE \_ TRANSITION \_ INSET**](wmt-videoimage-transition-inset.md)                   | La nuova immagine viene rivelata da un rettangolo proveniente da un angolo del frame.                                                               |
| [**WMT \_ VIDEOIMAGE \_ TRANSITION \_ IRIS**](wmt-videoimage-transition-iris.md)                     | La nuova immagine viene rivelata lungo un asse x e un asse y.                                                                                          |
| [**ROLL DELLA PAGINA \_ DI TRANSIZIONE DI WMT VIDEOIMAGE \_ \_ \_**](wmt-videoimage-transition-page-roll.md)          | L'immagine precedente viene trasformata in un effetto di capovolgimento della pagina, rivelando la nuova immagine sottostante.                                                      |
| [**RETTANGOLO DI TRANSIZIONE VIDEOIMAGE WMT \_ \_ \_**](wmt-videoimage-transition-rectangle.md)           | La nuova immagine viene rivelata da un rettangolo all'interno del frame.                                                                                       |
| [**WMT \_ VIDEOIMAGE \_ TRANSITION \_ REVEAL**](wmt-videoimage-transition-reveal.md)                 | La nuova immagine viene rivelata lungo una linea retta proveniente da un lato del frame.                                                          |
| [**DIAPOSITIVA DI TRANSIZIONE VIDEOIMAGE WMT \_ \_ \_**](wmt-videoimage-transition-slide.md)                   | L'immagine precedente esce dal frame, rivelando la nuova immagine sottostante.                                                                       |
| [**WMT \_ VIDEOIMAGE \_ TRANSITION \_ SPLIT**](wmt-videoimage-transition-split.md)                   | La nuova immagine viene rivelata da una divisione orizzontale o verticale nell'immagine precedente. La divisione viene visualizzata lungo una linea retta che inizia all'interno del frame. |
| [**WMT \_ VIDEOIMAGE \_ TRANSITION \_ STAR**](wmt-videoimage-transition-star.md)                     | La nuova immagine viene rivelata da una stella a cinque punte all'interno del frame.                                                                               |
| [**ROTELLINA DI \_ TRANSIZIONE DI WMT \_ \_ VIDEOIMAGE**](wmt-videoimage-transition-wheel.md)                   | La nuova immagine viene rivelata da quattro spoke rotanti con un punto pivot comune.                                                                     |



 

Ogni transizione è descritta in modo completo nel proprio argomento.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida di riferimento alla programmazione**](programming-reference.md)
</dt> <dt>

[**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2)
</dt> </dl>

 

 




