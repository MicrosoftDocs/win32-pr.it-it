---
description: Panoramica della Graph compilazione
ms.assetid: 5753f06c-ecfd-48d7-a8e9-768b798e9279
title: Panoramica della Graph compilazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c16b943714e2e559286b805a8489152805d9b0e037a77603bacd00f8b0135cc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118152947"
---
# <a name="overview-of-graph-building"></a>Panoramica della Graph compilazione

Per creare un grafo di filtro, iniziare creando un'istanza di Filter Graph Manager:


```C++
IGraphBuilder* pIGB;
HRESULT hr = CoCreateInstance(CLSID_FilterGraph,
    NULL, CLSCTX_INPROC_SERVER, IID_IGraphBuilder,
    (void **)&pIGB);
```



Filter Graph Manager supporta i metodi di creazione di grafi seguenti:

-   [**IFilterGraph::ConnectDirect**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-connectdirect) tenta di stabilire una connessione diretta tra due pin. Se i pin non possono connettersi, il metodo ha esito negativo.
-   [**IGraphBuilder::Connessione**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) connette due pin. Se possibile, crea una connessione diretta. In caso contrario, usa filtri intermedi per completare la connessione.
-   [**IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) inizia da un segnaposto di output e compila il resto del grafico. Questo metodo aggiunge filtri in base alle esigenze, lavorando a valle, fino a raggiungere un filtro renderer.
-   [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) compila un grafo di riproduzione di file completo.
-   [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) aggiunge un filtro al grafico. Non connette il filtro. È necessario creare il filtro prima di chiamare questo metodo, chiamando **CoCreateInstance** o usando Filter Mapper o System Device Enumerator.

Questi metodi forniscono tre approcci di base per la compilazione del grafo:

1.  Il filtro Graph Manager compila l'intero grafico.
2.  Il filtro Graph Manager compila parte del grafico.
3.  L'applicazione compila l'intero grafo.

**Gestione filtri Graph compila l'intera Graph**

Se si vuole semplicemente riprodurre un file creato in un formato riconosciuto, ad esempio AVI, MPEG, WAV o MP3, usare il **metodo RenderFile.** L'articolo How To Play a File (Come riprodurre un [file)](how-to-play-a-file.md) illustra come eseguire questa operazione.

Il **metodo RenderFile** inizia cercando nel Registro di sistema un filtro di origine in grado di analizzare il file. Usa il protocollo (ad esempio " " nell'URL), l'estensione di file o modelli di byte predefiniti nel file per `https://` determinare il filtro di origine. Per informazioni dettagliate, [vedere Registrazione di un tipo di file personalizzato](registering-a-custom-file-type.md).

Per compilare il resto del grafico, Filter Graph Manager usa un processo iterativo in cui accetta i tipi di supporti supportati da un filtro sui relativi pin di output e cerca nel Registro di sistema i filtri che accetteranno tale tipo di supporto come input. Usa diversi criteri per restringere la ricerca e assegnare priorità ai filtri:

-   La *categoria di filtro* identifica la funzionalità generale del filtro.
-   Il tipo di supporto descrive il tipo di dati che il filtro può accettare come input o recapitare come output.
-   Il *merito* determina l'ordine in cui vengono tentati i filtri. Se due filtri nella stessa categoria di filtri supportano entrambi gli stessi tipi di input, Filter Graph Manager seleziona quello con il valore di merito più alto. Ad alcuni filtri viene assegnato un valore di merito basso perché sono progettati per scopi specifici e devono essere aggiunti al grafo solo dall'applicazione.

Filter Graph Manager usa [l'oggetto Filter Mapper](filter-mapper.md) per eseguire ricerche nel Registro di sistema.

Quando ogni filtro viene aggiunto, l'Graph Manager cerca di connetterlo al pin di output del filtro precedente. I filtri negoziano per determinare se possono connettersi e, in tal caso, il tipo di supporto da usare per la connessione. Se il nuovo filtro non è in grado di connettersi, Graph Gestione filtri lo rimuove e tenta un altro filtro. Questo processo continua fino a quando non viene eseguito il rendering di ogni flusso.

**Il filtro Graph Manager compila parte del Graph**

Per eseguire un'operazione oltre alla semplice riproduzione di un file, l'applicazione deve eseguire almeno una parte del lavoro di creazione del grafo. Ad esempio, un'applicazione di acquisizione video deve selezionare un filtro di origine di acquisizione e aggiungerlo al grafo. Se si scrivono dati in un file AVI, è necessario aggiungere i filtri AVI Mux e File Writer al grafo. Tuttavia, spesso è possibile consentire a Filter Graph Manager di completare il grafico. Ad esempio, è possibile eseguire il rendering di un segnaposto per l'anteprima chiamando il **metodo Render.**

**L'applicazione compila l'intero Graph**

In alcuni scenari, l'applicazione potrebbe dover compilare il grafico aggiungendo e connettendo ogni filtro. In questo caso, probabilmente si conoscono in modo specifico i filtri da aggiungere al grafico. Con questo approccio, l'applicazione aggiunge ogni filtro chiamando **AddFilter**, enumera i pin sui filtri e li connette chiamando **Connessione** **o ConnectDirect**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di grafici con Capture Graph Builder](building-graphs-with-the-capture-graph-builder.md)
</dt> <dt>

[Enumerazione di dispositivi e filtri](enumerating-devices-and-filters.md)
</dt> <dt>

[Enumerazione di oggetti in un filtro Graph](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[Tecniche Graph-Building generale](general-graph-building-techniques.md)
</dt> <dt>

[Compilazione del filtro Graph](building-the-filter-graph.md)
</dt> </dl>

 

 



