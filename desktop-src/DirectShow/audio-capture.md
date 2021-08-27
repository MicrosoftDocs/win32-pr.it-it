---
description: Acquisizione audio
ms.assetid: 2b7fbdcb-7b59-407e-8e82-e66bd5606507
title: Acquisizione audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62f76924e170c29e4488e2b7bd31bddbe8702ebe78d9ed146471bdfa21598d12
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108711"
---
# <a name="audio-capture"></a>Acquisizione audio

Un'applicazione può DirectShow per acquisire dati audio da microfoni, lettori nastro e altri dispositivi, tramite gli input nella scheda audio. Gli scenari tipici includono:

-   Registrazione di una narrazione di voiceover per il successivo doppiaggio su un flusso video.
-   Conversione del contenuto audio analogico legacy in formato digitale.
-   Acquisizione di voce o musica per la trasmissione in rete.

Gli utenti finali hanno diverse opzioni per l'acquisizione di audio dalla scheda audio al disco rigido. La maggior parte delle schede fornisce applicazioni per la combinazione e la registrazione dai rispettivi input audio. Windows fornisce Sound Recorder, una semplice applicazione di utilità per la registrazione da un microfono. Il Windows Media Encoder può essere incorporato in un'applicazione DirectShow come oggetto multimediale [DirectX](directx-media-objects.md) (DMO). Questa sezione descrive come integrare la funzionalità di acquisizione audio all'interno di un'applicazione usando DirectShow.

Questa sezione contiene i seguenti argomenti:

-   [Informazioni sul filtro di acquisizione audio](about-the-audio-capture-filter.md)
-   [Selezione di un dispositivo di acquisizione](selecting-a-capture-device.md)
-   [Creazione di un'acquisizione audio Graph](creating-an-audio-capture-graph.md)
-   [Creazione di un'acquisizione audio Graph anteprima](creating-an-audio-capture-graph-with-preview.md)
-   [Impostazione delle proprietà di acquisizione audio](setting-audio-capture-properties.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di DirectShow](using-directshow.md)
</dt> </dl>

 

 



