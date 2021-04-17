---
description: Introduzione alla programmazione di applicazioni DirectShow
ms.assetid: 21a72efa-95df-4754-8304-ad56965a914d
title: Introduzione alla programmazione di applicazioni DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6218a346a7eb9711259c025aef09133ef2e58f6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401177"
---
# <a name="introduction-to-directshow-application-programming"></a>Introduzione alla programmazione di applicazioni DirectShow

Questo articolo presenta i concetti e la terminologia di base usati in DirectShow. Dopo aver letto questa sezione, si sarà pronti per scrivere la prima applicazione DirectShow.

**Filtra e filtra i grafici**

Il blocco predefinito di DirectShow è un componente software denominato *filtro*. Un filtro è un componente software che esegue un'operazione su un flusso multimediale. Ad esempio, i filtri DirectShow possono

-   Leggi file
-   ottenere video da un dispositivo di acquisizione video
-   decodificare diversi formati di flusso, ad esempio MPEG-1 video
-   passare i dati alla scheda grafica o audio

I filtri ricevono l'input e producono l'output. Se, ad esempio, un filtro decodifica il video MPEG-1, l'input è il flusso codificato MPEG e l'output è costituito da una serie di fotogrammi video non compressi.

In DirectShow, un'applicazione esegue qualsiasi attività connettendo catene di filtri, in modo che l'output di un filtro diventi l'input per un altro. Un set di filtri connessi è denominato *grafico a filtro*. Il diagramma seguente, ad esempio, Mostra un grafico di filtro per la riproduzione di un file AVI.

![filtrare il grafico per riprodurre un file AVI](images/avi-filter-graph.png)

Il filtro di origine file legge il file AVI dal disco rigido. Il filtro Splitter AVI analizza il file in due flussi, un flusso video compresso e un flusso audio. Il filtro Decompressore AVI decodifica i fotogrammi video. Il filtro renderer video disegna i frame sullo schermo, usando DirectDraw o GDI. Il filtro di dispositivo DirectSound predefinito riproduce il flusso audio usando DirectSound.

Non è necessario che l'applicazione gestisca tutti i flussi di dati. I filtri sono invece controllati da un componente di livello elevato denominato Filter Graph Manager. L'applicazione effettua chiamate API di alto livello, ad esempio "Run" (per spostare i dati attraverso il grafo) o "Stop" (per arrestare il flusso di dati). Se è necessario un maggiore controllo sulle operazioni di flusso, è possibile accedere ai filtri direttamente tramite le interfacce COM. Filter Graph Manager passa anche le notifiche degli eventi all'applicazione.

Il gestore del grafo del filtro rappresenta anche un altro scopo: fornisce metodi che consentono all'applicazione di creare il grafico del filtro connettendo i filtri. DirectShow fornisce anche vari oggetti helper che semplificano questo processo. Questi sono descritti accuratamente nella documentazione di.

**Scrittura di un'applicazione DirectShow**

In termini generali, esistono tre attività che devono essere eseguite da qualsiasi applicazione DirectShow. Sono illustrati nel diagramma seguente.

![applicazione DirectShow tipica](images/fgm.png)

1.  L'applicazione crea un'istanza di Filter Graph Manager.
2.  Nell'applicazione viene utilizzato Filter Graph Manager per creare un grafico di filtro. Il set esatto di filtri nel grafico dipende dall'applicazione.
3.  L'applicazione utilizza Filter Graph Manager per controllare il grafico del filtro e trasmettere i dati tramite i filtri. Durante questo processo, l'applicazione risponderà anche agli eventi del gestore del grafico dei filtri.

Al termine dell'elaborazione, l'applicazione rilascia la gestione del grafo dei filtri e tutti i filtri.

DirectShow si basa su COM; Filter Graph Manager e i filtri sono tutti oggetti COM. Prima di iniziare a programmare DirectShow, è necessario avere una conoscenza generale della programmazione dei client COM. Sono disponibili molti libri sulla programmazione COM.

Per iniziare a usare DirectShow, vedere l'articolo [come riprodurre un file](how-to-play-a-file.md), che presenta una semplice applicazione console per riprodurre un file video. La sezione [relativa a DirectShow](about-directshow.md) illustra in modo più dettagliato l'architettura DirectShow, mentre la sezione relativa all' [uso di DirectShow](using-directshow.md) esamina gli scenari principali supportati da DirectShow, ad esempio acquisizione, modifica video, riproduzione DVD e televisione.

 

 



