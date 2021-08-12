---
description: Informazioni DirectShow filtri
ms.assetid: 57b7d32e-2073-46a2-91ec-a34072134489
title: Informazioni DirectShow filtri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cef947fdcec8cc1c01d23d09bce1b46d5b4d7d2268fe1d7cd6df6a57b54d42ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118664467"
---
# <a name="about-directshow-filters"></a>Informazioni DirectShow filtri

DirectShow un'architettura modulare, in cui ogni fase di elaborazione viene eseguita da un oggetto COM denominato filtro. DirectShow un set di filtri standard da usare per le applicazioni e gli sviluppatori possono scrivere filtri personalizzati che estendono le funzionalità di DirectShow. Per illustrare, ecco i passaggi necessari per riprodurre un file video AVI, insieme ai filtri che eseguono ogni passaggio:

-   Leggere i dati non elaborati dal file come flusso di byte (filtro Origine file).
-   Esaminare le intestazioni AVI e analizzare il flusso di byte in fotogrammi video ed esempi audio separati (filtro AVI Splitter).
-   Decodificare i fotogrammi video (vari filtri del decodificatore, a seconda del formato di compressione).
-   Disegnare i fotogrammi video (filtro Renderer video).
-   Inviare gli esempi audio alla scheda audio (filtro dispositivo DirectSound predefinito).

Questi filtri sono illustrati nel diagramma seguente.

![Grafico dei filtri per la riproduzione di un file avi con video compresso](images/avi-filter-graph.png)

Come illustrato nel diagramma, ogni filtro è connesso a uno o più altri filtri. I punti di connessione sono anche oggetti COM, denominati *pin*. I filtri usano i segnaposto per spostare i dati da un filtro al successivo. Le frecce nel diagramma mostrano la direzione in cui viaggiano i dati. In DirectShow, un set di filtri è denominato *grafico di filtro*.

I filtri hanno tre stati possibili: in esecuzione, arrestato e sospeso. Quando un filtro è in esecuzione, elabora i dati multimediali. Quando viene arrestato, interrompe l'elaborazione dei dati. Lo stato sospeso viene usato per segnalere i dati prima dell'esecuzione. La sezione [Flow dati nel filtro Graph](data-flow-in-the-filter-graph.md) questo concetto viene descritto in modo più dettagliato. Con eccezioni molto rare, le modifiche dello stato vengono coordinate nell'intero grafico dei filtri. tutti i filtri nel grafico scambiano gli stati all'unisono. Di conseguenza, l'intero grafo dei filtri viene anche detto in esecuzione, arrestato o sospeso.

I filtri possono essere raggruppati in diverse categorie generali:

-   Un *filtro* di origine introduce i dati nel grafico. I dati possono derivare da un file, una rete, una fotocamera o altrove. Ogni filtro di origine gestisce un tipo diverso di origine dati.
-   Un *filtro di* trasformazione accetta un flusso di input, elabora i dati e crea un flusso di output. Codificatori e decodificatori sono esempi di filtri di trasformazione.
-   *I filtri renderer* siedono alla fine della catena. Ricevono i dati e li presentano all'utente. Ad esempio, un renderer video disegna fotogrammi video sullo schermo; un renderer audio invia dati audio alla scheda audio; e un filtro di scrittura file scrive i dati in un file.
-   Un *filtro della barra* di divisione suddivide un flusso di input in due o più output, in genere analizzando il flusso di input lungo la strada. Ad esempio, lo splitter AVI analizza un flusso di byte in flussi video e audio separati.
-   Un *filtro mux* accetta più input e li combina in un unico flusso. Ad esempio, AVI Mux esegue l'operazione inversa del separatore AVI. Accetta flussi audio e video e produce un flusso di byte in formato AVI.

Le distinzioni tra queste categorie non sono assolute. Ad esempio, il filtro lettore ASF funge sia da filtro di origine che da filtro con separatore.

Tutti DirectShow filtri espongono [**l'interfaccia IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) e tutti i pin espongono [**l'interfaccia IPin.**](/windows/desktop/api/Strmif/nn-strmif-ipin) DirectShow definisce anche molte altre interfacce che supportano funzionalità più specifiche.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su Filter Graph Manager](about-the-filter-graph-manager.md)
</dt> <dt>

[Dati Flow nel filtro Graph](data-flow-in-the-filter-graph.md)
</dt> <dt>

[DirectShow Filtri](directshow-filters.md)
</dt> </dl>

 

 



