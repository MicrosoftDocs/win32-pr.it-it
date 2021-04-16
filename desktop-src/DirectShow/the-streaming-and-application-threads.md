---
description: Il flusso e i thread dell'applicazione
ms.assetid: 954f7abd-fe06-430a-b6f7-d60852826bc9
title: Il flusso e i thread dell'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 432e613ff0322377c042e796d84ef7affdda99c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530246"
---
# <a name="the-streaming-and-application-threads"></a>Il flusso e i thread dell'applicazione

Qualsiasi applicazione DirectShow contiene almeno due thread importanti: il thread dell'applicazione e uno o più thread di streaming. Gli esempi vengono distribuiti nei thread di streaming e le modifiche di stato avvengono nel thread dell'applicazione. Il thread di streaming principale viene creato da un filtro di origine o di parser. Altri filtri possono creare thread di lavoro che forniscono esempi e sono considerati anche thread di streaming.

Alcuni metodi vengono chiamati sul thread dell'applicazione, mentre altri vengono chiamati su un thread di streaming. Ad esempio:

-   Thread di streaming: [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive), [**IMemInputPin:: ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple), [**Ipin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream), [**IMemAllocator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer).
-   Thread applicazione: [**IMediaFilter::P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause), [**IMediaFilter:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run), [**IMediaFilter:: Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop), [**IMediaSeeking:: sepositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions), [**Ipin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush), [**Ipin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush).
-   Eseguire una delle operazioni seguenti: [**Ipin:: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment).

Avere un thread di streaming separato consente ai dati di passare attraverso il grafo mentre il thread dell'applicazione è in attesa dell'input dell'utente. Il pericolo di più thread, tuttavia, è che un filtro può creare risorse durante la sospensione (sul thread dell'applicazione), usarle all'interno di un metodo di flusso ed eliminarle quando si arresta (anche sul thread dell'applicazione). Se non si presta attenzione, il thread di streaming potrebbe provare a usare le risorse dopo che sono state eliminate definitivamente. La soluzione consiste nel proteggere le risorse usando sezioni critiche e sincronizzare i metodi di streaming con le modifiche di stato.

Per proteggere lo stato del filtro, un filtro necessita di una sezione critica. La classe [**CBaseFilter**](cbasefilter.md) ha una variabile membro per questa sezione critica, [**CBaseFilter:: m \_ pLock**](cbasefilter-m-plock.md). Questa sezione critica è denominata blocco del filtro. Ogni pin di input necessita inoltre di una sezione critica per proteggere le risorse usate dal thread di streaming. Queste sezioni critiche sono denominate blocchi di streaming. è necessario dichiararli nella classe del pin derivato. È più semplice usare la classe [**CCritSec**](ccritsec.md) , che esegue il wrapping di un **oggetto \_ sezione critica** di Windows e può essere bloccata usando la classe [**CAutoLock**](cautolock.md) . La classe **CCritSec** fornisce anche alcune utili funzioni di debug. Per ulteriori informazioni, vedere la [sezione critica funzioni di debug](critical-section-debugging-functions.md).

Quando un filtro viene arrestato o scaricato, deve sincronizzare il thread dell'applicazione con il thread di streaming. Per evitare il deadlock, è necessario prima sbloccare il thread di streaming, che potrebbe essere bloccato per diversi motivi:

-   È in attesa di ottenere un esempio all'interno del metodo [**IMemAllocator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) , perché sono in uso tutti gli esempi dell'allocatore.
-   È in attesa della restituzione di un altro filtro da un metodo di streaming, ad esempio **Receive**.
-   È in attesa all'interno di uno dei propri metodi di streaming, per rendere disponibile una risorsa.
-   Si tratta di un filtro renderer in attesa dell'ora di presentazione dell'esempio successivo
-   Si tratta di un filtro renderer in attesa all'interno del metodo **Receive** mentre è in pausa.

Pertanto, quando il filtro viene arrestato o scaricato, deve eseguire le operazioni seguenti:

-   Rilasciare qualsiasi esempio che contiene per qualsiasi motivo. Questa operazione sblocca il metodo **GetBuffer** .
-   Tornare da qualsiasi metodo di streaming il più rapidamente possibile. Se un metodo di streaming è in attesa di una risorsa, è necessario arrestare immediatamente l'attesa.
-   Avviare il rifiuto degli esempi nella **ricezione**, in modo che il thread di streaming non acceda ad altre risorse. La classe [**CBaseInputPin**](cbaseinputpin.md) gestisce automaticamente questa operazione.
-   Il metodo **Stop** deve eseguire il commit di tutti gli allocatori del filtro. La classe **CBaseInputPin** gestisce automaticamente questa operazione.

Lo scaricamento e l'arresto di entrambi si verificano nel thread dell'applicazione. Un filtro si interrompe in risposta al metodo [**IMediaControl:: Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) . Filter Graph Manager rilascia il comando stop nell'ordine upstream, a partire dai renderer e procedendo a ritroso con i filtri di origine. Il comando Stop si verifica completamente all'interno del metodo **CBaseFilter:: Stop** del filtro. Quando il metodo viene restituito, il filtro deve trovarsi nello stato interrotto.

Lo scaricamento in genere si verifica a causa di un comando seek. Un comando di scaricamento viene avviato dal filtro di origine o del parser e viaggia a valle. Lo svuotamento avviene in due fasi: il metodo [**Ipin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) informa un filtro per eliminare tutti i dati in sospeso e in arrivo. il metodo [**Ipin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) segnala al filtro di accettare nuovamente i dati. Lo svuotamento richiede due fasi perché la chiamata **BeginFlush** si trova nel thread dell'applicazione, durante il quale il thread di streaming continua a recapitare i dati. Alcuni esempi possono pertanto arrivare dopo la chiamata a **BeginFlush** . Il filtro deve rimuovere questi. Tutti gli esempi che arrivano dopo la chiamata a **EndFlush** sono sicuramente nuovi e devono essere recapitati.

Le sezioni seguenti contengono esempi di codice che illustrano come implementare i metodi di filtro più importanti, ad esempio **pause**, **Receive** e così via, in modo da evitare deadlock e race condition. Ogni filtro prevede tuttavia requisiti diversi, pertanto sarà necessario adattare questi esempi al filtro specifico.

> [!Note]  
> Le classi base [**CTransformFilter**](ctransformfilter.md) e [**CTransInPlaceFilter**](ctransinplacefilter.md) gestiscono molti dei problemi descritti in questo articolo. Se si sta scrivendo un filtro di trasformazione e il filtro non è in attesa di eventi all'interno di un metodo di flusso o se si tiene conto di campioni al di fuori della **ricezione**, queste classi di base dovrebbero essere sufficienti.

 

 

 



