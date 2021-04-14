---
description: Connessione intelligente
ms.assetid: 938ba1b0-822e-4871-8786-b7eeee243867
title: Connessione intelligente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12aead305867ccec1f1f1f0cbd76c652ba3ec412
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482301"
---
# <a name="intelligent-connect"></a>Connessione intelligente

La connessione intelligente è il meccanismo utilizzato dal gestore del grafo del filtro per compilare i grafici dei filtri. È costituito da diversi algoritmi correlati che selezionano i filtri e li aggiungono al grafico dei filtri.

Leggere questo argomento se si verificano problemi durante la creazione di un grafico di filtro specifico e si desidera risolvere il problema o se si sta scrivendo un filtro personalizzato e si desidera renderlo disponibile per la compilazione automatica dei grafici.

La connessione intelligente prevede i seguenti metodi di [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) :

-   [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter)
-   [**IGraphBuilder:: Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render)
-   [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile)
-   [**IGraphBuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect)

### <a name="igraphbuilderaddsourcefilter"></a>IGraphBuilder::AddSourceFilter

Il metodo [**IGraphBuilder:: AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) aggiunge un filtro di origine in grado di eseguire il rendering di un file specificato. In primo luogo, Cerca nel registro di sistema e trova la corrispondenza con il protocollo (ad esempio `https://` ), l'estensione del nome del file o un set di *byte di controllo* predeterminati, che sono byte con offset specifici nel file che corrispondono a determinati modelli. Per informazioni dettagliate, vedere la pagina relativa alla [registrazione di un tipo di file personalizzato](registering-a-custom-file-type.md). Supponendo che il metodo trovi un filtro di origine appropriato, crea un'istanza di tale filtro, la aggiunge al grafo e chiama il metodo [**IFileSourceFilter:: Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) del filtro con il nome del file.

### <a name="igraphbuilderrender"></a>IGraphBuilder:: Render

Il metodo [**IGraphBuilder:: Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) compila una sottosezione di un grafico. Inizia da un pin di output non connesso e funziona a valle, aggiungendo nuovi filtri in base alle esigenze. Il filtro iniziale deve essere già presente nel grafico. A ogni passaggio, il metodo **Render** Cerca un filtro in grado di connettersi al filtro precedente. Il flusso può creare un ramo se un filtro di connessione ha più pin di output. La ricerca si interrompe quando ogni flusso dispone di un renderer. Se il metodo di **rendering** si blocca, è possibile eseguire il backup e riprovare usando un set di filtri diverso.

Per connettere ogni pin di output, il metodo [**Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) esegue le operazioni seguenti:

1.  Se il pin supporta l'interfaccia [**IStreamBuilder**](/windows/desktop/api/Strmif/nn-strmif-istreambuilder) , il gestore del grafo del filtro delega l'intero processo al metodo [**IStreamBuilder:: Render**](/windows/desktop/api/Strmif/nf-strmif-istreambuilder-render) del PIN. Esponendo questa interfaccia, il pin si assume la responsabilità di creare il resto del grafo fino al renderer. Tuttavia, pochissimi pin supportano questa interfaccia.
2.  Il gestore del grafico del filtro tenta di utilizzare i filtri memorizzati nella cache, se presenti. Durante il processo di connessione intelligente, il gestore del grafico dei filtri può memorizzare nella cache i filtri dei passaggi precedenti del processo. (Vedere anche [creazione di grafici dinamici](dynamic-graph-building.md)).
3.  Se il grafico del filtro contiene filtri con pin di input non connessi, il gestore del grafico del filtro li tenterà di nuovo. È possibile forzare il metodo [**Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) a provare un filtro particolare aggiungendo tale filtro al grafo prima di chiamare **il rendering**.
4.  A partire da Windows 7, DirectShow include un elenco di filtri preferiti per determinati sottotipi di supporti. Se è presente un filtro preferito per il tipo di supporto di cui è in corso il rendering, il gestore del grafico del filtro tenterà di filtrare il filtro. Un'applicazione può modificare l'elenco dei filtri preferiti usando l'interfaccia [**IAMPluginControl**](/windows/desktop/api/Strmif/nn-strmif-iamplugincontrol) . Le modifiche apportate all'elenco influiscono sul processo corrente dell'applicazione e vengono eliminate al termine del processo.
5.  Infine, se non è stato trovato alcun filtro appropriato, il gestore del grafico dei filtri Cerca nel registro di sistema, usando il metodo [**IFilterMapper2:: EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) . Tenta di far corrispondere i tipi di supporti preferiti del PIN di output ai tipi di supporti elencati nel registro di sistema.

    Ogni filtro viene registrato con un valore di *Merit*, un valore numerico che indica il modo in cui il filtro è preferibile rispetto ad altri filtri. Il metodo [**EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) restituisce i filtri in ordine di merito, con un valore minimo di Merit, che **\_ \_ non \_ USA** + 1. Ignora i filtri con un valore Merit of **Merit \_ che \_ non \_ USA** o meno. Anche i filtri vengono raggruppati in categorie, definiti da GUID. Le categorie stesse hanno il merito e il metodo **EnumMatchingFilters** ignora qualsiasi categoria con un valore Merit of **Merit che \_ \_ non \_ USA** o meno, anche se i filtri in tale categoria hanno valori Merit più elevati.

    A partire da Windows 7, DirectShow include un elenco di filtri bloccati per determinati sottotipi di supporti. Filter Graph Manager ignora i filtri in questo elenco. Un'applicazione può modificare l'elenco dei filtri bloccati usando l'interfaccia [**IAMPluginControl**](/windows/desktop/api/Strmif/nn-strmif-iamplugincontrol) . Le modifiche apportate a questo elenco influiscono sul processo corrente dell'applicazione e vengono eliminate al termine del processo.

Per riepilogare, il metodo [**Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) tenta i filtri nell'ordine seguente:

1.  Usare [**IStreamBuilder**](/windows/desktop/api/Strmif/nn-strmif-istreambuilder).
2.  Provare i filtri memorizzati nella cache.
3.  Provare i filtri nel grafico.
4.  Windows 7 o versioni successive: provare il filtro preferito per il tipo di supporto, se disponibile.
5.  Cercare i filtri nel registro di sistema.

### <a name="igraphbuilderrenderfile"></a>IGraphBuilder:: RenderFile

Il metodo [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) compila un grafico di riproduzione predefinito da un nome file. Internamente, questo metodo usa [**AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) per individuare il filtro di origine corretto e il [**rendering**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) per compilare il resto del grafo.

### <a name="igraphbuilderconnect"></a>IGraphBuilder:: Connect

Il metodo [**IGraphBuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) connette un pin di output a un pin di input. Se necessario, questo metodo aggiunge filtri intermedi, usando una variante dell'algoritmo descritto per il metodo [**Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) :

1.  Provare una connessione diretta tra i filtri, senza filtri intermedi.
2.  Provare i filtri memorizzati nella cache.
3.  Provare i filtri nel grafico.
4.  Windows 7 o versioni successive: provare il filtro preferito per il tipo di supporto, se disponibile.
5.  Cercare i filtri nel registro di sistema.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtra categorie](filter-categories.md)
</dt> <dt>

[Merito](merit.md)
</dt> <dt>

[Simulazione della creazione di grafici con GraphEdit](simulating-graph-building-with-graphedit.md)
</dt> <dt>

[Creazione del grafico di filtro](building-the-filter-graph.md)
</dt> </dl>

 

 



