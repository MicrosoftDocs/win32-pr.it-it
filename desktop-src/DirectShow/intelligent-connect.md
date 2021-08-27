---
description: Gestione Connessione
ms.assetid: 938ba1b0-822e-4871-8786-b7eeee243867
title: Gestione Connessione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2248dc936076dfcad1b2ad934da4ef6a8b1e28a260ff75ebca3a63ec6356bf6b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107701"
---
# <a name="intelligent-connect"></a>Gestione Connessione

Intelligent Connessione è il meccanismo utilizzato da Filter Graph Manager per creare grafici filtro. È costituito da diversi algoritmi correlati che selezionano i filtri e li aggiungono al grafo dei filtri.

Leggere questo argomento se si verificano problemi durante la creazione di un determinato grafo di filtro e si vuole risolvere il problema oppure se si sta scrivendo un filtro personalizzato e si vuole renderlo disponibile per la compilazione automatica del grafico.

Il Connessione intelligente prevede i metodi [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) seguenti:

-   [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter)
-   [**IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render)
-   [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile)
-   [**IGraphBuilder::Connessione**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect)

### <a name="igraphbuilderaddsourcefilter"></a>IGraphBuilder::AddSourceFilter

Il [**metodo IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) aggiunge un filtro di origine in grado di eseguire il rendering di un file specificato. Cerca prima di tutto nel Registro di sistema e trova le corrispondenze con il protocollo (ad esempio ), l'estensione del nome file o un set di byte di controllo predeterminati, ovvero byte in corrispondenza di offset specifici nel file che corrispondono a determinati `https://` modelli.  Per informazioni dettagliate, [vedere Registrazione di un tipo di file personalizzato](registering-a-custom-file-type.md). Supponendo che il metodo individua un filtro di origine appropriato, crea quindi un'istanza di tale filtro, la aggiunge al grafo e chiama il metodo [**IFileSourceFilter::Load**](/windows/desktop/api/Strmif/nf-strmif-ifilesourcefilter-load) del filtro con il nome file.

### <a name="igraphbuilderrender"></a>IGraphBuilder::Render

Il [**metodo IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) compila una sottosezione di un grafo. Inizia da un pin di output non interconnesso e funziona a valle, aggiungendo nuovi filtri in base alle esigenze. Il filtro iniziale deve essere già presente nel grafico. A ogni passaggio, il **metodo Render** cerca un filtro in grado di connettersi al filtro precedente. Il flusso può creare un ramo se un filtro di connessione ha più pin di output. La ricerca viene arrestata quando ogni flusso ha un renderer. Se il **metodo Render** si blocca, potrebbe eseguire il backup e riprovare, usando un set diverso di filtri.

Per connettere ogni pin di output, [**il metodo Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) esegue le operazioni seguenti:

1.  Se il pin supporta [**l'interfaccia IStreamBuilder,**](/windows/desktop/api/Strmif/nn-strmif-istreambuilder) Filter Graph Manager delega l'intero processo al metodo [**IStreamBuilder::Render del**](/windows/desktop/api/Strmif/nf-strmif-istreambuilder-render) pin. Esponendo questa interfaccia, il segnaposto si assume la responsabilità di compilare il resto del grafico, fino al renderer. Tuttavia, pochissimi pin supportano questa interfaccia.
2.  Gestione filtri Graph tenta di usare filtri memorizzati nella cache, se presenti. Durante il processo di Connessione intelligente, Gestione filtri Graph possibile memorizzare nella cache i filtri dei passaggi precedenti del processo. Vedere anche [Dynamic Graph Building](dynamic-graph-building.md).
3.  Se il grafico dei filtri contiene filtri con pin di input non collegati, l'Graph di filtro prova a eseguire i tentativi successivi. È possibile forzare il [**metodo Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) a provare un filtro specifico aggiungendo tale filtro al grafico prima di chiamare **Render**.
4.  A partire Windows 7, DirectShow un elenco di filtri preferiti per determinati sottotipi di supporti. Se è presente un filtro preferito per il tipo di supporto di cui viene eseguito il rendering, l'Graph Di gestione filtri prova a eseguire il filtro successivo. Un'applicazione può modificare l'elenco dei filtri preferiti usando [**l'interfaccia IAMPluginControl.**](/windows/desktop/api/Strmif/nn-strmif-iamplugincontrol) Le modifiche apportate all'elenco influiscono sul processo corrente dell'applicazione e vengono eliminate al termine del processo.
5.  Infine, se non è stato trovato alcun filtro appropriato, Filter Graph Manager cerca nel Registro di sistema usando il metodo [**IFilterMapper2::EnumMatchingFilters.**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) Prova a trovare la corrispondenza tra i tipi di supporti preferiti del pin di output e i tipi di supporti elencati nel Registro di sistema.

    Ogni filtro viene registrato con *un merito,* un valore numerico che indica quanto sia preferibile il filtro rispetto ad altri filtri. Il [**metodo EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) restituisce i filtri in ordine di merito, con un merito minimo di **MERIT DO NOT \_ \_ \_ USE** + 1. Ignora i filtri con merito **NON \_ \_ USARE \_** o meno. I filtri sono anche raggruppati in categorie, definite in base al GUID. Le categorie hanno merito e il metodo **EnumMatchingFilters** ignora qualsiasi categoria con merito **MERIT DO NOT \_ \_ \_ USE** o inferiore, anche se i filtri in tale categoria hanno valori di merito più elevati.

    A partire Windows 7, DirectShow un elenco di filtri bloccati per determinati sottotipi di supporti. Gestione Graph filtri ignora i filtri in questo elenco. Un'applicazione può modificare l'elenco di filtri bloccati usando [**l'interfaccia IAMPluginControl.**](/windows/desktop/api/Strmif/nn-strmif-iamplugincontrol) Le modifiche apportate a questo elenco influiscono sul processo corrente dell'applicazione e vengono eliminate al termine del processo.

Per riepilogare, il [**metodo Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) prova i filtri nell'ordine seguente:

1.  Usare [**IStreamBuilder**](/windows/desktop/api/Strmif/nn-strmif-istreambuilder).
2.  Provare i filtri memorizzati nella cache.
3.  Provare i filtri nel grafico.
4.  Windows 7 o versione successiva: provare il filtro preferito per il tipo di supporto, se presente.
5.  Cercare i filtri nel Registro di sistema.

### <a name="igraphbuilderrenderfile"></a>IGraphBuilder::RenderFile

Il [**metodo IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) compila un grafico di riproduzione predefinito da un nome file. Internamente, questo metodo usa [**AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) per individuare il filtro di origine corretto ed [**Esegui rendering**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) per compilare il resto del grafico.

### <a name="igraphbuilderconnect"></a>IGraphBuilder::Connessione

Il [**metodo IGraphBuilder::Connessione**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) connette un pin di output a un pin di input. Questo metodo aggiunge filtri intermedi, se necessario, usando una variante dell'algoritmo descritto per il [**metodo Render:**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render)

1.  Provare a stabilire una connessione diretta tra i filtri, senza filtri intermedi.
2.  Provare i filtri memorizzati nella cache.
3.  Provare i filtri nel grafico.
4.  Windows 7 o versione successiva: provare il filtro preferito per il tipo di supporto, se presente.
5.  Cercare i filtri nel Registro di sistema.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtrare le categorie](filter-categories.md)
</dt> <dt>

[Merito](merit.md)
</dt> <dt>

[Simulazione Graph compilazione con GraphModifica](simulating-graph-building-with-graphedit.md)
</dt> <dt>

[Compilazione del filtro Graph](building-the-filter-graph.md)
</dt> </dl>

 

 



