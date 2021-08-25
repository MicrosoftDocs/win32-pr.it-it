---
description: Introduzione alla programmazione DirectShow'applicazione
ms.assetid: 21a72efa-95df-4754-8304-ad56965a914d
title: Introduzione alla programmazione DirectShow'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a448d49939e69b7c8a3b244b27a91a93eaf941eebf1960b7b2a53e4ad9137341
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823516"
---
# <a name="introduction-to-directshow-application-programming"></a>Introduzione alla programmazione DirectShow'applicazione

Questo articolo presenta la terminologia e i concetti di base usati in DirectShow. Dopo aver letto questa sezione, si sarà pronti per scrivere la prima DirectShow applicazione.

**Filtri e grafici di filtro**

Il blocco predefinito di DirectShow è un componente software denominato *filtro*. Un filtro è un componente software che esegue un'operazione su un flusso multimediale. Ad esempio, DirectShow filtri

-   lettura di file
-   ottenere video da un dispositivo di acquisizione video
-   decodificare vari formati di flusso, ad esempio video MPEG-1
-   passare dati alla scheda grafica o audio

I filtri ricevono l'input e producono l'output. Ad esempio, se un filtro decodifica video MPEG-1, l'input è il flusso con codifica MPEG e l'output è una serie di fotogrammi video non compressi.

In DirectShow un'applicazione esegue qualsiasi attività connettendo catene di filtri, in modo che l'output di un filtro diventi l'input per un altro. Un set di filtri connessi è denominato grafico *di filtro*. Ad esempio, il diagramma seguente mostra un grafico di filtro per la riproduzione di un file AVI.

![filtrare il grafico per riprodurre un file avi](images/avi-filter-graph.png)

Il filtro Origine file legge il file AVI dal disco rigido. Il filtro AVI Splitter analizza il file in due flussi, un flusso video compresso e un flusso audio. Il filtro decompressore AVI decodifica i fotogrammi video. Il filtro Renderer video disegna i fotogrammi sulla visualizzazione usando DirectDraw o GDI. Il filtro Dispositivo DirectSound predefinito riproduce il flusso audio usando DirectSound.

L'applicazione non deve gestire tutto questo flusso di dati. I filtri sono invece controllati da un componente di alto livello denominato Filter Graph Manager. L'applicazione esegue chiamate API di alto livello, ad esempio "Esegui" (per spostare i dati nel grafo) o "Stop" (per arrestare il flusso di dati). Se è necessario un maggiore controllo sulle operazioni del flusso, è possibile accedere ai filtri direttamente tramite le interfacce COM. Filter Graph Manager passa anche le notifiche degli eventi all'applicazione.

Filter Graph Manager ha anche un altro scopo: fornisce metodi che consentono all'applicazione di compilare il grafico dei filtri, connettendo i filtri. (DirectShow fornisce anche vari oggetti helper che semplificano questo processo. Queste informazioni sono descritte in modo approfondito nella documentazione.

**Scrittura di un DirectShow appalto**

In termini generali, è necessario eseguire tre attività DirectShow'applicazione. Questi elementi sono illustrati nel diagramma seguente.

![tipica applicazione directshow](images/fgm.png)

1.  L'applicazione crea un'istanza di Filter Graph Manager.
2.  L'applicazione usa Filter Graph Manager per creare un grafo di filtro. Il set esatto di filtri nel grafico dipenderà dall'applicazione.
3.  L'applicazione usa Filter Graph Manager per controllare il grafico dei filtri e trasmettere i dati tramite i filtri. Durante questo processo, l'applicazione risponderà anche agli eventi di Filter Graph Manager.

Al termine dell'elaborazione, l'applicazione rilascia filter Graph Manager e tutti i filtri.

DirectShow è basato su COM; i filtri Graph Manager e i filtri sono tutti oggetti COM. È necessario avere una conoscenza generale della programmazione client COM prima di iniziare a DirectShow. Sono disponibili molti libri sulla programmazione COM.

Per iniziare a usare DirectShow, leggere l'articolo How To Play a File (Come riprodurre un [file),](how-to-play-a-file.md)che presenta una semplice applicazione console per riprodurre un file video. La sezione About DirectShow (Informazioni su [DirectShow)](about-directshow.md) illustra l'architettura DirectShow in modo più dettagliato, mentre la sezione Using DirectShow (Uso di [DirectShow)](using-directshow.md) esamina gli scenari principali supportati da DirectShow, ad esempio acquisizione, modifica video, riproduzione di DVD e tv.

 

 



