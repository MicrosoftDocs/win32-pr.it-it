---
description: Uso del mixer overlay in acquisizione video
ms.assetid: 43468fa2-6dea-439d-9e24-f47a053ad561
title: Uso del mixer overlay in acquisizione video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72bff115d566654732e80c0bcb0f554c4ad96e65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057831"
---
# <a name="using-the-overlay-mixer-in-video-capture"></a>Uso del mixer overlay in acquisizione video

Sono disponibili alcuni tipi di video in cui il filtro [renderer video](video-renderer-filter.md) non può essere visualizzato da solo. In queste situazioni, il renderer video deve funzionare con il filtro [Overlay Mixer](overlay-mixer-filter.md) . Il mixer overlay gestisce il rendering, mentre il renderer video gestisce la finestra video. Il mixer overlay è necessario nelle situazioni seguenti:

-   PIN della porta video (VP). Se il dispositivo di acquisizione usa una porta video, il mixer della sovrimpressione gestisce la sovrimpressione hardware.
-   Video interlacciato. Per i video interlacciati, il decodificatore richiede un formato [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) , che non è supportato dal renderer video.
-   Didascalie chiuse. Il testo della didascalia viene sottoposto a rendering come bitmap a 8 bit per pixel, sovrapposte al video dal mixer sovrapposto.

Il metodo **RenderStream** del generatore di grafici di acquisizione inserisce il mixer della sovrimpressione ogni volta che è necessario. Se si compila il grafo senza usare il generatore di grafici di acquisizione, tuttavia, è necessario verificare la presenza di queste situazioni e inserire il mixer sovrapposto.

-   \[! Importante\]  
    > Se il dispositivo ha un pin VP, è necessario connettere il mixer overlay anche se non è necessaria la funzionalità di anteprima nell'applicazione. Con una porta video, il dispositivo di acquisizione Invia sempre i dati video alla sovrapposizione hardware, quindi il mixer overlay è sempre necessario.

     

I filtri renderer video mixing (VMR-7 e VMR-9) supportano entrambi i video interlacciati e possono combinare bitmap didascalie chiuse nel video principale. Se si usa VMR per questi scenari, non è necessario usare il mixer overlay. VMR-9 non supporta le connessioni pin VP. VMR-7 supporta le connessioni pin VP tramite il filtro gestione porta video. Tuttavia, è possibile che alcuni driver non funzionino correttamente con il gestore della porta video. Per questo motivo, il mixer overlay è ancora consigliato per i pin VP.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Argomenti sull'acquisizione avanzata](advanced-capture-topics.md)
</dt> <dt>

[PIN della porta video](video-port-pins.md)
</dt> <dt>

[Tipo di formato VideoInfo2](videoinfo2-format-type.md)
</dt> </dl>

 

 



