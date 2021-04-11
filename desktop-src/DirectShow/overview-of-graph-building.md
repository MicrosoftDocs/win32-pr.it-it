---
description: Panoramica della creazione di grafici
ms.assetid: 5753f06c-ecfd-48d7-a8e9-768b798e9279
title: Panoramica della creazione di grafici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f69ef9ea0f4f9e21d33372ad2a37a59b512d5dcc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124365"
---
# <a name="overview-of-graph-building"></a>Panoramica della creazione di grafici

Per creare un grafico di filtro, iniziare creando un'istanza di Filter Graph Manager:


```C++
IGraphBuilder* pIGB;
HRESULT hr = CoCreateInstance(CLSID_FilterGraph,
    NULL, CLSCTX_INPROC_SERVER, IID_IGraphBuilder,
    (void **)&pIGB);
```



Filter Graph Manager supporta i seguenti metodi di creazione di grafici:

-   [**IFilterGraph:: ConnectDirect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-connectdirect) tenta di effettuare una connessione diretta tra due pin. Se i pin non possono connettersi, il metodo ha esito negativo.
-   [**IGraphBuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) connette due pin. Se possibile, esegue una connessione diretta. In caso contrario, vengono utilizzati filtri intermedi per completare la connessione.
-   [**IGraphBuilder:: Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) inizia da un pin di output e compila il resto del grafo. Questo metodo aggiunge i filtri in base alle esigenze, lavorando a valle, fino a raggiungere un filtro renderer.
-   [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) compila un grafo completo per la riproduzione di file.
-   [**IFilterGraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) aggiunge un filtro al grafico. Il filtro non viene connesso. È necessario creare il filtro prima di chiamare questo metodo, chiamando **CoCreateInstance** o utilizzando il mapper del filtro o l'enumeratore di dispositivi di sistema.

Questi metodi forniscono tre approcci di base per la compilazione del grafo:

1.  Filter Graph Manager compila l'intero grafico.
2.  Il gestore del grafico del filtro compila parte del grafico.
3.  L'applicazione compila l'intero grafico.

**Filter Graph Manager compila l'intero grafico**

Se si vuole semplicemente riprodurre un file creato in un formato riconosciuto, ad esempio AVI, MPEG, WAV o MP3, usare il metodo **RenderFile** . Questo articolo [illustra come eseguire](how-to-play-a-file.md) questa operazione.

Il metodo **RenderFile** inizia con la ricerca nel registro di sistema di un filtro di origine in grado di analizzare il file. Usa il protocollo (ad esempio " `https://` " nell'URL), l'estensione di file o i modelli di byte predefiniti nel file per determinare il filtro di origine. Per informazioni dettagliate, vedere la pagina relativa alla [registrazione di un tipo di file personalizzato](registering-a-custom-file-type.md).

Per creare il resto del grafo, il gestore del grafico di filtro usa un processo iterativo in cui accetta i tipi di supporto supportati da un filtro sui pin di output e Cerca nel registro di sistema i filtri che accettano tale tipo di supporto come input. USA diversi criteri per limitare la ricerca e assegnare priorità ai filtri:

-   La *categoria Filter* identifica la funzionalità generale del filtro.
-   Il tipo di supporto descrive il tipo di dati che il filtro può accettare come input o recapitare come output.
-   Il *merito* determina l'ordine in cui vengono tentati i filtri. Se due filtri nella stessa categoria di filtro supportano entrambi gli stessi tipi di input, il gestore del grafico di filtro seleziona quello con il valore di Merit massimo. Ai filtri viene assegnato intenzionalmente un valore di Merit basso perché sono progettati per finalità specializzate e devono essere aggiunti al grafico solo dall'applicazione.

Filter Graph Manager usa l'oggetto [Filter Mapper](filter-mapper.md) per eseguire ricerche nel registro di sistema.

Quando ogni filtro viene aggiunto, il gestore del grafico del filtro tenta di connetterlo al pin di output del filtro precedente. I filtri negoziano per determinare se possono connettersi e, in tal caso, quale tipo di supporto utilizzare per la connessione. Se il nuovo filtro non è in grado di connettersi, il gestore del grafico del filtro lo ignora e tenta un altro filtro. Questo processo continua fino a quando non viene eseguito il rendering di ogni flusso.

**Filter Graph Manager compila parte del grafico**

Per eseguire un'operazione oltre a riprodurre semplicemente un file, l'applicazione deve eseguire almeno alcune delle operazioni di compilazione del grafo. Ad esempio, un'applicazione di acquisizione video deve selezionare un filtro origine di acquisizione e aggiungerlo al grafico. Se si scrivono dati in un file AVI, è necessario aggiungere al grafico i filtri mux e writer di file AVI. Tuttavia, spesso è possibile consentire a Filter Graph Manager di completare il grafo. È ad esempio possibile eseguire il rendering di un PIN per l'anteprima chiamando il metodo **Render** .

**L'applicazione compila l'intero grafico**

In alcuni scenari, è possibile che l'applicazione debba compilare il grafico aggiungendo e connettendo ogni filtro. In questo caso, è probabile che si conoscano in particolare i filtri da aggiungere al grafico. Con questo approccio, l'applicazione aggiunge ogni filtro chiamando **addFilter**, enumera i pin sui filtri e li connette chiamando **Connect** o **ConnectDirect**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di grafici con il generatore di grafici di acquisizione](building-graphs-with-the-capture-graph-builder.md)
</dt> <dt>

[Enumerazione dei dispositivi e dei filtri](enumerating-devices-and-filters.md)
</dt> <dt>

[Enumerazione di oggetti in un grafico di filtro](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[Tecniche di Graph-Building generali](general-graph-building-techniques.md)
</dt> <dt>

[Creazione del grafico di filtro](building-the-filter-graph.md)
</dt> </dl>

 

 



