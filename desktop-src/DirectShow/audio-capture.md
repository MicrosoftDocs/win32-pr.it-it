---
description: Acquisizione audio
ms.assetid: 2b7fbdcb-7b59-407e-8e82-e66bd5606507
title: Acquisizione audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e91c9063d96a5e56d078651c338b0ffd80f5aa79
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104342016"
---
# <a name="audio-capture"></a>Acquisizione audio

Un'applicazione può usare DirectShow per acquisire dati audio da microfoni, lettori di nastri e altri dispositivi, tramite gli input nella scheda audio. Gli scenari tipici includono:

-   Registrazione di una narrazione VoiceOver per il duplicato successivo su un flusso video.
-   Conversione del contenuto audio analogico legacy in formato digitale.
-   Acquisizione di voce o musica per la trasmissione in rete.

Gli utenti finali hanno diverse opzioni per l'acquisizione di audio dalla scheda audio al disco rigido. La maggior parte delle schede fornisce applicazioni per la combinazione e la registrazione dagli input audio. Windows fornisce un registratore audio, una semplice applicazione di utilità per la registrazione da un microfono. Il codificatore Windows Media può essere incorporato in un'applicazione DirectShow come [oggetto DMO (DirectX Media Object](directx-media-objects.md) ). Questa sezione descrive come integrare la funzionalità di acquisizione audio all'interno dell'applicazione usando DirectShow.

Questa sezione contiene i seguenti argomenti:

-   [Informazioni sul filtro di acquisizione audio](about-the-audio-capture-filter.md)
-   [Selezione di un dispositivo di acquisizione](selecting-a-capture-device.md)
-   [Creazione di un grafico di acquisizione audio](creating-an-audio-capture-graph.md)
-   [Creazione di un grafico di acquisizione audio con anteprima](creating-an-audio-capture-graph-with-preview.md)
-   [Impostazione delle proprietà di acquisizione audio](setting-audio-capture-properties.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di DirectShow](using-directshow.md)
</dt> </dl>

 

 



