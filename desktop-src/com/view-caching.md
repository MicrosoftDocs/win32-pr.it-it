---
title: Visualizzare Caching
description: Visualizzare Caching
ms.assetid: d19c111c-1367-43a2-97a9-35dc0ff5dcc8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b155c0a9d3229db85a52b0589c4854bdee9a2e8e4171e231480036c512af737
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047679"
---
# <a name="view-caching"></a>Visualizzare Caching

Un'applicazione contenitore deve essere in grado di ottenere una presentazione di un oggetto allo scopo di visualizzarlo o stamparlo per gli utenti quando il documento è aperto ma l'applicazione server dell'oggetto non è in esecuzione o non è installata nel computer dell'utente. Presupporre, tuttavia, che i server per tutti gli oggetti che si potrebbero trovare in un documento siano installati nel computer di ogni utente e possano essere sempre eseguiti su richiesta non sono realistici. Il gestore di oggetti predefinito, disponibile in qualsiasi momento, risolve questo problema memorizzando nella cache le presentazioni di oggetti nell'archivio del documento e modificando queste presentazioni in qualsiasi piattaforma, indipendentemente dalla disponibilità del server oggetti in una particolare installazione del contenitore.

I contenitori possono gestire presentazioni di disegno per uno o più dispositivi di destinazione specifici oltre a quello necessario per mantenere l'oggetto sullo schermo. Inoltre, se si converte l'oggetto da una piattaforma a un'altra, OLE converte automaticamente i formati di dati dell'oggetto in quelli supportati nella nuova piattaforma. Ad esempio, se si sposta un oggetto da Windows a Macintosh, OLE convertirà le presentazioni dei metafile in formati PICT.

Per presentare all'utente una rappresentazione accurata di un oggetto incorporato, l'applicazione contenitore dell'oggetto avvia una finestra di dialogo con il gestore dell'oggetto, richiedendo dati e istruzioni di disegno. Per poter soddisfare le richieste del contenitore, il gestore deve implementare le interfacce [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject), [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2)e [**IOleCache.**](/windows/desktop/api/OleIdl/nn-oleidl-iolecache)

[**IDataObject consente**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) a un'applicazione contenitore OLE di ottenere e inviare dati ai relativi oggetti incorporati o collegati. Quando i dati cambiano in un oggetto, questa interfaccia consente all'oggetto di rendere disponibili i nuovi dati al relativo contenitore e fornisce al contenitore un modo per aggiornare i dati nella copia dell'oggetto. Per una descrizione generale del trasferimento dei dati, vedere il capitolo 4, Trasferimento dei dati.

L'interfaccia [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2) è molto simile all'interfaccia [**IDataObject,**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) ad eccezione del fatto che richiede a un oggetto di disegnare se stesso in un contesto di dispositivo, ad esempio uno schermo, una stampante o un metafile, anziché spostare o copiare i dati in memoria o in un altro supporto di trasferimento. Lo scopo dell'interfaccia è consentire a un contenitore OLE di ottenere rappresentazioni grafici alternative dei relativi oggetti incorporati, i cui dati sono già disponibili, evitando così il sovraccarico di dover trasferire istanze completamente nuove degli stessi oggetti dati semplicemente per ottenere nuove istruzioni di disegno. Al contrario, **l'interfaccia IViewObject2** consente al contenitore di chiedere a un oggetto di fornire una rappresentazione grafica di se stesso disegnando su un contesto di dispositivo specificato dal contenitore.

Quando si chiama [**l'interfaccia IViewObject2,**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2) un'applicazione contenitore può anche specificare che l'oggetto deve disegnare se stesso in un dispositivo di destinazione diverso da quello in cui verrà effettivamente eseguito il rendering. In questo modo il contenitore, se necessario, può generare rendering diversi da un singolo oggetto. Ad esempio, il chiamante potrebbe chiedere all'oggetto di comporre se stesso per una stampante anche se il rendering del disegno risultante verrà eseguito sullo schermo. Il risultato, naturalmente, sarebbe un'anteprima di stampa dell'oggetto .

[**L'interfaccia IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2)fornisce anche metodi che consentono ai contenitori di registrarsi per le notifiche di modifica della visualizzazione. Come con i dati e gli avvisi OLE, una connessione di avviso di visualizzazione consente a un contenitore di aggiornare i rendering di un oggetto in base alle proprie esigenze anziché in risposta a una chiamata dall'oggetto . Ad esempio, se una nuova versione dell'applicazione server di un oggetto offrisse visualizzazioni aggiuntive degli stessi dati, il gestore predefinito dell'oggetto chiamerebbe l'implementazione di [**IAdviseSink::OnViewChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onviewchange) di ogni contenitore per invii che le nuove presentazioni erano disponibili. Il contenitore recupererà queste informazioni dal sink di notifica solo quando necessario.

Poiché Windows di dispositivo hanno un significato solo all'interno di un singolo processo, non è possibile passare puntatori [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2) attraverso i limiti del processo. Di conseguenza, i server locali e remoti OLE non hanno alcuna necessità di implementare l'interfaccia , che non funzionerebbe correttamente anche se lo facevano. Solo i gestori di oggetti e i server in-process implementano **l'interfaccia IViewObject2.** OLE fornisce un'implementazione predefinita, che è possibile usare nei server in-process OLE e nei gestori di oggetti semplicemente aggregando il gestore predefinito OLE. Oppure è possibile scrivere un'implementazione personalizzata di **IViewObject2.**

Un oggetto implementa [**l'interfaccia IOleCache**](/windows/desktop/api/OleIdl/nn-oleidl-iolecache) per consentire al gestore di conoscere le funzionalità da memorizzare nella cache. Il gestore dell'oggetto possiede anche la cache e garantisce che sia aggiornata. Quando l'oggetto incorporato entra nello stato di esecuzione, il gestore configura le connessioni di consulenza appropriate sull'oggetto server, con se stesso che funge da sink. Le [**implementazioni dell'interfaccia IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) e [**IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2)operano fuori dei dati memorizzati nella cache sul lato client. L'implementazione del gestore **di IViewObject2** è responsabile della determinazione dei formati di dati da memorizzare nella cache per soddisfare le richieste di disegno del client. L'implementazione del gestore **di IDataObject** è responsabile del recupero dei dati in vari formati e così via tra la memoria e l'istanza [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) sottostante dell'oggetto incorporato. I gestori personalizzati possono usare queste implementazioni aggregando sul gestore predefinito.

> [!Note]  
> [**L'interfaccia IViewObject2**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject2) è una semplice estensione funzionale di [**IViewObject**](/windows/desktop/api/OleIdl/nn-oleidl-iviewobject) e deve essere implementata al posto dell'ultima interfaccia, che è ora obsoleta. Oltre a fornire i metodi **IViewObject,** l'interfaccia **IViewObject2** fornisce un singolo membro aggiuntivo, [**GetExtent,**](/windows/desktop/api/OleIdl/nf-oleidl-iviewobject2-getextent)che consente a un'applicazione contenitore di ottenere le dimensioni della presentazione di un oggetto dalla cache senza prima dover spostare l'oggetto nello stato di esecuzione con una chiamata a [**IOleObject::GetExtent.**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getextent)

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Documenti composti](compound-documents.md)
</dt> </dl>

 

 