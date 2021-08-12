---
description: Uso della sovrimpressione Mixer nell'acquisizione video
ms.assetid: 43468fa2-6dea-439d-9e24-f47a053ad561
title: Uso della sovrimpressione Mixer nell'acquisizione video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 134ada11ca55009b3ad67ba80c82575ab2d9bdf5a7329a88157ed4e003eca74c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118651195"
---
# <a name="using-the-overlay-mixer-in-video-capture"></a>Uso della sovrimpressione Mixer nell'acquisizione video

Esistono alcuni tipi di video che il filtro [renderer video](video-renderer-filter.md) non può visualizzare da solo. In queste situazioni, il renderer video deve funzionare con il filtro di Mixer [sovrimpressione.](overlay-mixer-filter.md) L'Mixer sovrimpressione gestisce il rendering, mentre il renderer video gestisce la finestra video. La sovrimpressione Mixer è necessaria nelle situazioni seguenti:

-   Pin di porta video (VP). Se il dispositivo di acquisizione usa una porta video, la sovrimpressione Mixer gestisce la sovrimpressione hardware.
-   Video interlacciato. Per i video interlacciati, il decodificatore richiede un formato [**VIDEOINFOHEADER2,**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) che non è supportato dal renderer video.
-   Sottotitoli. Il rendering del testo della didascalia viene eseguito come bitmap a 8 bit per pixel, che l'oggetto Overlay Mixer sovrappone al video.

Il metodo **RenderStream** di Capture Graph Builder inserisce la sovrimpressione Mixer quando necessario. Se si compila il grafo senza usare Capture Graph Builder, tuttavia, è necessario verificare ognuna di queste situazioni e inserire la sovrimpressione Mixer se stessi.

-   \[! Importante\]  
    > Se il dispositivo ha un pin VP, è necessario connettere il Mixer overlay anche se non è necessaria la funzionalità di anteprima nell'applicazione. Con una porta video, il dispositivo di acquisizione invia sempre i dati video alla sovrimpressione hardware, quindi la sovrimpressione Mixer è sempre necessaria.

     

I filtri del renderer di combinazione video (VMR-7 e VMR-9) supportano entrambi video interlacciati e sono in grado di combinare bitmap di sottotitoli codificati nel video principale. Se si usa la macchina virtuale per questi scenari, non è necessario usare la funzionalità Di sovrimpressione Mixer. VMR-9 non supporta le connessioni pin VP. VMR-7 supporta le connessioni pin VP tramite il filtro Video Port Manager. È tuttavia possibile che alcuni driver non funzionino correttamente con Gestione porte video. Per questo motivo, è comunque consigliabile Mixer sovrimpressione per i pin VP.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Argomenti avanzati sull'acquisizione](advanced-capture-topics.md)
</dt> <dt>

[Pin della porta video](video-port-pins.md)
</dt> <dt>

[Tipo di formato VideoInfo2](videoinfo2-format-type.md)
</dt> </dl>

 

 



