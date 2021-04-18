---
description: Configurazione del grafico del filtro DVD
ms.assetid: 0c68c456-2240-4090-b45c-bd098cfea645
title: Configurazione del grafico del filtro DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ec7bb8757e5246fc01309fbef55e654436560b2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522402"
---
# <a name="dvd-filter-graph-configuration"></a>Configurazione del grafico del filtro DVD

In questa sezione vengono descritte le varie configurazioni del grafico filtro per la riproduzione DVD in DirectShow. Questi diagrammi vengono forniti principalmente per riferimento. Il navigatore DVD compila il grafo, quindi in generale non è necessario comprendere i dettagli della configurazione del grafo. Per altre informazioni, vedere [Building the DVD Filter Graph](building-the-dvd-filter-graph.md).

Nella figura seguente viene illustrato un grafico del filtro DVD con un decodificatore software.

![grafico filtro DVD per Windows XP](images/dvd-graph-xp.png)

Quando è presente un decodificatore hardware, questo viene in genere connesso direttamente alla scheda video tramite una porta video. In questo modo, i bit video decodificati possono essere inviati direttamente al buffer frame sulla scheda grafica senza passare alla memoria host. Per gestire questa connessione diretta nelle versioni precedenti di Windows, DirectShow supporta le estensioni VPE (DirectDraw video Port Extensions) tramite un'interfaccia sul [filtro del mixer sovrapposto](overlay-mixer-filter.md).

> [!Note]  
> Il mixer overlay è ora deprecato.

 

In Windows XP e versioni successive, un decodificatore hardware può connettersi al filtro di [gestione porta video](video-port-manager.md) .

![Graph DVD per Windows XP con un decoder hardware](images/dvd-hwgraph-xp.png)

In tutti questi grafici, il navigatore DVD è il filtro di origine; esegue diverse attività:

-   Legge i dati di navigazione e video dal disco.
-   Esegue il demultiplexing dei dati video, audio e subpicture in flussi distinti.
-   Pompa i flussi nel grafico per un'ulteriore elaborazione e un eventuale rendering.
-   Informa l'applicazione di eventi correlati a DVD.

Nel flusso audio, il navigatore DVD si connette a valle a un decoder audio, che si connette al [filtro renderer DirectSound](directsound-renderer-filter.md), il renderer audio predefinito. Nei flussi video e subpicture, i filtri downstream sono il decodificatore video di terze parti e il renderer di mixaggio video (o il [mixer overlay](overlay-mixer-filter.md)e il [renderer video](video-renderer-filter.md) nelle applicazioni di livello inferiore). Se l'applicazione gestirà i dati della riga 21 con didascalia chiusa, è necessario aggiungere il filtro del decodificatore 2 della riga 21 al grafico. Si tratta di una singola chiamata al metodo. il filtro verrà connesso automaticamente.

L'applicazione comunica con e controlla il navigatore DVD tramite le interfacce personalizzate esposte da DVD Navigator: [**IDVDControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2), ovvero i metodi "set" e [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2), ovvero i metodi "Get". Deve inoltre comunicare con Filter Graph Manager (tramite [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)) per arrestare, avviare e controllare altrimenti il grafo. Potrebbe anche essere necessario controllare altri filtri singoli, ad esempio il filtro del mixer sovrapposto per passare da un schermo a schermo intero a un altro. Per ulteriori informazioni, vedere [**IMixerPinConfig2**](/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2). La configurazione esatta del grafo varia a seconda del tipo di decodificatore MPEG-2 installato, se è necessario gestire la riga 21 dati con didascalia chiusa e altri fattori.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Applicazioni DVD](dvd-applications.md)
</dt> </dl>

 

 



