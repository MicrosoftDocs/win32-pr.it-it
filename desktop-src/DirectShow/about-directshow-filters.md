---
description: Informazioni sui filtri DirectShow
ms.assetid: 57b7d32e-2073-46a2-91ec-a34072134489
title: Informazioni sui filtri DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11ddfb5dda550bee88c42ef70347c95ba7a2b003
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104555842"
---
# <a name="about-directshow-filters"></a>Informazioni sui filtri DirectShow

DirectShow usa un'architettura modulare, in cui ogni fase di elaborazione viene eseguita da un oggetto COM denominato filtro. DirectShow fornisce un set di filtri standard per le applicazioni da usare e gli sviluppatori possono scrivere filtri personalizzati che estendono la funzionalità di DirectShow. Per illustrare, di seguito sono riportati i passaggi necessari per riprodurre un file video AVI, insieme ai filtri che eseguono ogni passaggio:

-   Leggere i dati non elaborati dal file come flusso di byte (filtro origine file).
-   Esaminare le intestazioni AVI e analizzare il flusso di byte in diversi fotogrammi video ed esempi audio (filtro Splitter AVI).
-   Decodificare i fotogrammi video (vari filtri del decodificatore, a seconda del formato di compressione).
-   Creare i fotogrammi video (filtro renderer video).
-   Inviare gli esempi audio alla scheda audio (filtro di dispositivo DirectSound predefinito).

Questi filtri sono illustrati nel diagramma seguente.

![filtro del grafico per la riproduzione di un file AVI con video compresso](images/avi-filter-graph.png)

Come illustrato nel diagramma, ogni filtro è connesso a uno o più filtri. I punti di connessione sono anche oggetti COM, detti *pin*. I filtri usano pin per spostare i dati da un filtro a quello successivo. Le frecce nel diagramma mostrano la direzione in cui i dati vengono trasmessi. In DirectShow un set di filtri viene definito grafico a *filtro*.

I filtri possono avere tre stati: in esecuzione, arrestati e sospesi. Quando un filtro è in esecuzione, elabora i dati multimediali. Quando viene arrestato, interrompe l'elaborazione dei dati. Lo stato Paused viene usato per indicare i dati prima dell'esecuzione; il flusso di dati della sezione [nel grafico di filtro](data-flow-in-the-filter-graph.md) descrive questo concetto in modo più dettagliato. Con eccezioni molto rare, le modifiche di stato vengono coordinate nell'intero grafico di filtro; tutti i filtri presenti nel grafico comunicano gli stati in Unison. Quindi, l'intero grafico di filtro viene detto anche in esecuzione, arrestato o sospeso.

I filtri possono essere raggruppati in diverse categorie generali:

-   Un filtro di *origine* introduce i dati nel grafico. I dati possono provenire da un file, da una rete, da una fotocamera o da qualsiasi altra posizione. Ogni filtro di origine gestisce un tipo di origine dati diverso.
-   Un filtro di *trasformazione* accetta un flusso di input, elabora i dati e crea un flusso di output. Codificatori e decodificatori sono esempi di filtri di trasformazione.
-   I filtri *renderer* si trovano alla fine della catena. Ricevono i dati e li presentano all'utente. Un renderer video, ad esempio, disegna i fotogrammi video sullo schermo; un renderer audio invia dati audio alla scheda audio; un filtro di file writer scrive i dati in un file.
-   Un filtro *splitter* suddivide un flusso di input in due o più output, in genere analizzando il flusso di input lungo il percorso. Ad esempio, il separatore AVI analizza un flusso di byte in flussi video e audio distinti.
-   Un filtro *Mux* accetta più input e li combina in un singolo flusso. Ad esempio, il mux di AVI esegue l'operazione inversa del separatore AVI. Accetta flussi audio e video e produce un flusso di byte in formato AVI.

Le differenze tra queste categorie non sono assolute. Il filtro di lettura ASF, ad esempio, funge sia da filtro di origine che da filtro di barra di divisione.

Tutti i filtri DirectShow espongono l'interfaccia [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) e tutti i pin espongono l'interfaccia [**Ipin**](/windows/desktop/api/Strmif/nn-strmif-ipin) . DirectShow definisce anche molte altre interfacce che supportano funzionalità più specifiche.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su Filter Graph Manager](about-the-filter-graph-manager.md)
</dt> <dt>

[Flusso di dati nel grafico del filtro](data-flow-in-the-filter-graph.md)
</dt> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> </dl>

 

 



