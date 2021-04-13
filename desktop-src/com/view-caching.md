---
title: Visualizza Caching
description: Visualizza Caching
ms.assetid: d19c111c-1367-43a2-97a9-35dc0ff5dcc8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 592c5bc2555e907cdc4e600465b807387c3a5548
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104399756"
---
# <a name="view-caching"></a>Visualizza Caching

Un'applicazione contenitore deve essere in grado di ottenere una presentazione di un oggetto allo scopo di visualizzarlo o stamparlo per gli utenti quando il documento è aperto, ma l'applicazione server dell'oggetto non è in esecuzione o non è installata nel computer dell'utente. Per presupporre, tuttavia, che i server di tutti gli oggetti che potrebbero essere presenti in un documento siano installati nel computer di ogni utente e che possa sempre essere eseguito su richiesta non è realistico. Il gestore di oggetti predefinito, disponibile in qualsiasi momento, risolve questo dilemma memorizzando nella cache le presentazioni degli oggetti nell'archivio del documento e modificando queste presentazioni su qualsiasi piattaforma indipendentemente dalla disponibilità del server oggetti in una particolare installazione del contenitore.

I contenitori possono mantenere le presentazioni di disegno per uno o più dispositivi di destinazione specifici, oltre a quello necessario per gestire l'oggetto sullo schermo. Inoltre, se si trasferisce l'oggetto da una piattaforma a un'altra, OLE converte automaticamente i formati di dati dell'oggetto in quelli supportati nella nuova piattaforma. Se, ad esempio, si sposta un oggetto da Windows a Macintosh, OLE convertirà le presentazioni metafile in formati PICT.

Per presentare all'utente una rappresentazione accurata di un oggetto incorporato, l'applicazione contenitore dell'oggetto avvia una finestra di dialogo con il gestore dell'oggetto, richiedendo i dati e le istruzioni di disegno. Per essere in grado di soddisfare le richieste del contenitore, il gestore deve implementare le interfacce [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject), [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2)e [**IOleCache**](/windows/desktop/api/OleIdl/nn-oleidl-iolecache) .

[**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) consente a un'applicazione contenitore OLE di recuperare e inviare dati ai relativi oggetti incorporati o collegati. Quando i dati vengono modificati in un oggetto, questa interfaccia fornisce un modo per rendere disponibili i nuovi dati al contenitore da parte dell'oggetto e fornisce al contenitore un modo per aggiornare i dati nella relativa copia dell'oggetto. Per informazioni generali sul trasferimento dei dati, vedere il capitolo 4 Trasferimento dati.

L'interfaccia [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2) è molto simile all'interfaccia [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) con la differenza che richiede a un oggetto di disegnarsi in un contesto di dispositivo, ad esempio una schermata, una stampante o un metafile, anziché spostare o copiare i dati in memoria o in un altro supporto di trasferimento. Lo scopo dell'interfaccia è quello di consentire a un contenitore OLE di ottenere rappresentazioni pittoriche alternative degli oggetti incorporati, i cui dati sono già presenti, evitando così il sovraccarico dovuto alla necessità di trasferire le istanze completamente nuove degli stessi oggetti dati semplicemente per ottenere nuove istruzioni di disegno. Al contrario, l'interfaccia **IViewObject2** consente al contenitore di richiedere a un oggetto di fornire una rappresentazione pittorica di se stesso disegnando in un contesto di dispositivo specificato dal contenitore.

Quando si chiama l'interfaccia [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2) , un'applicazione contenitore può anche specificare che l'oggetto si disegna in un dispositivo di destinazione diverso da quello in cui verrà effettivamente eseguito il rendering. In questo modo il contenitore, se necessario, consente di generare rendering diversi da un singolo oggetto. Ad esempio, il chiamante potrebbe chiedere all'oggetto di comporre se stesso per una stampante anche se il disegno risultante verrà visualizzato sullo schermo. Il risultato, ovviamente, sarebbe un'anteprima di stampa dell'oggetto.

L'interfaccia [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2)fornisce anche metodi che consentono ai contenitori di registrarsi per le notifiche di modifica della visualizzazione. Come per i dati e gli avvisi OLE, una connessione di avviso di visualizzazione consente a un contenitore di aggiornare i rendering di un oggetto in base alla propria convenienza piuttosto che in risposta a una chiamata dall'oggetto. Se, ad esempio, una nuova versione dell'applicazione server di un oggetto è stata in grado di offrire visualizzazioni aggiuntive degli stessi dati, il gestore predefinito dell'oggetto chiamerebbe l'implementazione di [**IAdviseSink:: OnViewChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onviewchange) di ogni contenitore per indicare che le nuove presentazioni erano disponibili. Il contenitore recupera queste informazioni dal sink di notifica solo quando necessario.

Poiché i contesti di dispositivo Windows hanno un significato solo all'interno di un singolo processo, non è possibile passare i puntatori [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2) tra i limiti dei processi. Di conseguenza, i server OLE locali e remoti non necessitano di alcun tipo di implementazione dell'interfaccia, che non funzionerebbe correttamente anche in caso affermativo. Solo i gestori di oggetti e i server in-process implementano l'interfaccia **IViewObject2**. OLE fornisce un'implementazione predefinita, che è possibile utilizzare nei propri server OLE in-process e gestori di oggetti semplicemente aggregando il gestore predefinito OLE. In alternativa, è possibile scrivere un'implementazione personalizzata di **IViewObject2**.

Un oggetto implementa l'interfaccia [**IOleCache**](/windows/desktop/api/OleIdl/nn-oleidl-iolecache) per consentire al gestore di conoscere le funzionalità che deve memorizzare nella cache. Il gestore dell'oggetto possiede inoltre la cache e ne garantisce l'aggiornamento. Quando l'oggetto incorporato entra nello stato in esecuzione, il gestore imposta le connessioni consultive appropriate sull'oggetto server, che funge da sink. Le implementazioni dell'interfaccia [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) e [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2)operano all'esterno dei dati memorizzati nella cache sul lato client. L'implementazione del gestore di **IViewObject2** è responsabile della determinazione dei formati di dati da memorizzare nella cache per soddisfare le richieste di creazione del client. L'implementazione del gestore di **IDataObject** è responsabile del recupero dei dati in vari formati e così via tra la memoria e l'istanza [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) sottostante dell'oggetto incorporato. I gestori personalizzati possono usare queste implementazioni aggregando il gestore predefinito.

> [!Note]  
> L'interfaccia [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2) è un'estensione funzionale semplice di [**IViewObject**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject) e deve essere implementata al posto della seconda interfaccia, che ora è obsoleta. Oltre a fornire i metodi **IViewObject** , l'interfaccia **IViewObject2** fornisce un singolo membro aggiuntivo, [**GetExtent**](/windows/desktop/api/OleIdl/nf-oleidl-iviewobject2-getextent), che consente a un'applicazione contenitore di ottenere le dimensioni della presentazione di un oggetto dalla cache senza dover prima spostare l'oggetto nello stato in esecuzione con una chiamata a [**IOleObject:: GetExtent**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getextent).

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Documenti composti](compound-documents.md)
</dt> </dl>

 

 