---
description: Configurazione del filtro DVD Graph
ms.assetid: 0c68c456-2240-4090-b45c-bd098cfea645
title: Configurazione del filtro DVD Graph
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ece69f77ac4a4e6674bbcd12404a10b7f765a514e18cb31963d2ed7f981799e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118653089"
---
# <a name="dvd-filter-graph-configuration"></a>Configurazione del filtro DVD Graph

In questa sezione vengono descritte le varie configurazioni dei grafi dei filtri per la riproduzione di DVD in DirectShow. Questi diagrammi vengono forniti principalmente come riferimento. Lo strumento di navigazione DVD compila il grafo, quindi in generale non è necessario comprendere i dettagli della configurazione del grafo. Per altre informazioni, vedere [Building the DVD Filter Graph](building-the-dvd-filter-graph.md).

La figura seguente mostra un grafo di filtro DVD con un decodificatore software.

![Grafico dei filtri dvd per Windows xp](images/dvd-graph-xp.png)

Quando è presente un decodificatore hardware, viene in genere connesso direttamente alla scheda video da una porta video. In questo modo i bit video decodificati possono essere inviati direttamente al buffer dei fotogrammi nella scheda grafica senza passare alla memoria host. Per gestire questa connessione diretta nelle versioni precedenti di Windows, DirectShow supporta DirectDraw Video Port Extensions (VPE) tramite un'interfaccia in [Overlay Mixer Filter](overlay-mixer-filter.md).

> [!Note]  
> Il Mixer overlay è ora deprecato.

 

In Windows XP e versioni successive, un decodificatore hardware può connettersi al filtro [di Gestione porte](video-port-manager.md) video.

![Grafico dvd per Windows xp con decodificatore hardware](images/dvd-hwgraph-xp.png)

In tutti questi grafici lo strumento di navigazione DVD è il filtro di origine. esegue diverse attività:

-   Legge i dati di navigazione e video dal disco.
-   Demultiplexa i dati di video, audio e immagini secondarie in flussi separati.
-   Pompa i flussi nel grafo per un'ulteriore elaborazione e il rendering finale.
-   Informa l'applicazione di eventi correlati a DVD.

Nel flusso audio, lo strumento di navigazione DVD si connette a valle a un decodificatore audio, che si connette al filtro [renderer DirectSound,](directsound-renderer-filter.md)il renderer audio predefinito. Nei flussi di video e immagini secondarie, i filtri [downstream](overlay-mixer-filter.md)sono il decodificatore video di terze parti e il renderer di combinazione di video (o overlay Mixer e il [renderer video](video-renderer-filter.md) nelle applicazioni di livello inferiore). Se l'applicazione gestirà i dati con sottotitoli codificati alla riga 21, è necessario aggiungere il filtro DirectShow Line 21 Decoder 2 al grafico. Ciò comporta una singola chiamata al metodo. il filtro verrà connesso automaticamente.

L'applicazione comunica con lo strumento di spostamento DVD e controlla lo strumento di spostamento DVD tramite le interfacce personalizzate esponge: [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2), ovvero i metodi "set" e [**IDvdInfo2,**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2)ovvero i metodi "get". Deve anche comunicare con il gestore del grafo del filtro (tramite [**IMediaControl)**](/windows/desktop/api/Control/nn-control-imediacontrol)per arrestare, avviare e controllare in caso contrario il grafo. Potrebbe anche essere necessario controllare altri singoli filtri, ad esempio il filtro Sovrimpressione Mixer per passare dalla visualizzazione a finestra a schermo intero. Per altre informazioni, vedere [**IMixerPinConfig2.**](/windows/desktop/api/Mpconfig/nn-mpconfig-imixerpinconfig2) La configurazione esatta del grafo varia a seconda del tipo di decodificatore MPEG-2 installato, se è necessario gestire i dati con sottotitoli codificati alla riga 21 e altri fattori.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Applicazioni DVD](dvd-applications.md)
</dt> </dl>

 

 



