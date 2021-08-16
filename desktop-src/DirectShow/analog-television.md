---
description: Tv analogica
ms.assetid: 9f2c18ec-3684-42a8-a3df-5f8827b27642
title: Tv analogica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 886c2b3f93ca70fb4a533f131611431c4a15df51169f70ed49f321c0ccfc8c2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117824760"
---
# <a name="analog-television"></a>Tv analogica

La tv analoga è diversa da altri scenari di acquisizione video in diversi modi:

-   La scheda si tuner si abilita a un segnale analogico, che viene quindi digitalizzato.
-   L'audio viene trasportato nel segnale analogico. Il modo in cui l'audio raggiunge la scheda audio varia a seconda dell'hardware.
-   Il segnale può contenere dati aggiuntivi nell'intervallo di blanking verticale (VBI), ad esempio sottotitoli codificati (CC), WST (World Standard Teletext) e extended data services (XDS).

Il diagramma seguente mostra un grafico di filtro tipico per l'anteprima di programmi televisivi.

![grafico della tv analogica](images/vidcap06.png)

-   Il [filtro Siner TV controlla](tv-tuner-filter.md) l'ottimizzazione.
-   Il [filtro AUDIO TV](tv-audio-filter.md) controlla la decodifica audio.
-   Se la scheda siner ha più di un input fisico, il filtro [crossbar video](analog-video-crossbar-filter.md) analogico consente all'applicazione di selezionare l'input decodificato e sottoposto a rendering.
-   Il [filtro di acquisizione video WDM](wdm-video-capture-filter.md) recapita il flusso video digitalizzato.

Capture Graph Builder inserisce automaticamente tutti i filtri necessari a monte dal filtro di acquisizione.

Questa sezione contiene i seguenti argomenti:

-   [Ottimizzazione della tv analogica](analog-television-tuning.md)
-   [Audio televisivo analogico](analog-television-audio.md)
-   [Sottotitoli codificati e teletext](closed-captions-and-teletext.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Acquisizione video](video-capture.md)
</dt> </dl>

 

 



