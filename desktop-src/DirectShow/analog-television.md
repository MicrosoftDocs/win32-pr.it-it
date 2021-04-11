---
description: Televisione analoga
ms.assetid: 9f2c18ec-3684-42a8-a3df-5f8827b27642
title: Televisione analoga
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33af8ba94831afed59d783598dbf6bc0eaee0ec6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124251"
---
# <a name="analog-television"></a>Televisione analoga

La televisione analogica differisce da altri scenari di acquisizione video in diversi modi:

-   La scheda Tuner viene sintonizzata su un segnale analogico, che viene quindi digitato.
-   L'audio viene portato nel segnale analogico. Il modo in cui l'audio raggiunge la scheda audio varia a seconda dell'hardware.
-   Il segnale può contenere dati aggiuntivi nell'intervallo di spaziatura verticale (VBI), ad esempio sottotitoli (CC), World Standard Teletext (WST) e Extended Data Services (XDS).

Il diagramma seguente illustra un tipico grafico di filtro per l'anteprima della televisione.

![grafico analogico TV](images/vidcap06.png)

-   Il filtro del [sintonizzatore TV](tv-tuner-filter.md) controlla l'ottimizzazione.
-   Il filtro [audio TV](tv-audio-filter.md) controlla la decodifica audio.
-   Se la scheda Tuner contiene più di un input fisico, il filtro per la barra del [video analogo](analog-video-crossbar-filter.md) consente all'applicazione di selezionare l'input da decodificare e di cui eseguire il rendering.
-   Il filtro di [acquisizione video WDM](wdm-video-capture-filter.md) recapita il flusso video digitato.

Il generatore di grafici di acquisizione inserisce automaticamente tutti i filtri necessari a Monte dal filtro di acquisizione.

Questa sezione contiene i seguenti argomenti:

-   [Ottimizzazione della televisione analoga](analog-television-tuning.md)
-   [Audio TV analogico](analog-television-audio.md)
-   [Didascalie e televideo chiusi](closed-captions-and-teletext.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Acquisizione video](video-capture.md)
</dt> </dl>

 

 



