---
description: Thread di streaming e dell'applicazione
ms.assetid: 954f7abd-fe06-430a-b6f7-d60852826bc9
title: Thread di streaming e dell'applicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a90916c14395a21aa5c53481c96b03fb6bbb2a8d4162cf996ef18ac15ce5e856
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119583121"
---
# <a name="the-streaming-and-application-threads"></a>Thread di streaming e dell'applicazione

Qualsiasi DirectShow contiene almeno due thread importanti: il thread dell'applicazione e uno o più thread di streaming. Gli esempi vengono recapitati nei thread di streaming e le modifiche di stato vengono apportate nel thread dell'applicazione. Il thread di streaming principale viene creato da un filtro di origine o parser. Altri filtri potrebbero creare thread di lavoro che forniscono esempi e questi sono considerati thread di streaming.

Alcuni metodi vengono chiamati sul thread dell'applicazione, mentre altri vengono chiamati su un thread di streaming. Esempio:

-   Thread di streaming: [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive), [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple), [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream), [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer).
-   Thread dell'applicazione: [**IMediaFilter::P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause), [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run), [**IMediaFilter::Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop), [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions), [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush), [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush).
-   In entrambi [**i caso: IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment).

La presenza di un thread di streaming separato consente il flusso dei dati attraverso il grafico mentre il thread dell'applicazione attende l'input dell'utente. Il rischio di più thread, tuttavia, è che un filtro possa creare risorse quando viene sospeso (nel thread dell'applicazione), usarle all'interno di un metodo di streaming ed eliminare le risorse quando si arresta (anche nel thread dell'applicazione). Se non si fa attenzione, il thread di streaming potrebbe provare a usare le risorse dopo che sono state distrutte. La soluzione consiste nel proteggere le risorse usando sezioni critiche e sincronizzare i metodi di streaming con le modifiche di stato.

Un filtro richiede una sezione critica per proteggere lo stato del filtro. La [**classe CBaseFilter**](cbasefilter.md) ha una variabile membro per questa sezione critica, [**CBaseFilter::m \_ pLock**](cbasefilter-m-plock.md). Questa sezione critica è denominata blocco filtro. Ogni pin di input necessita inoltre di una sezione critica per proteggere le risorse usate dal thread di streaming. Queste sezioni critiche sono denominate blocchi di streaming. è necessario dichiararli nella classe pin derivata. È più semplice usare la [**classe CCritSec,**](ccritsec.md) che esegue il wrapping di un Windows **CRITICAL \_ SECTION** e può essere bloccata usando [**la classe CAutoLock.**](cautolock.md) La **classe CCritSec** fornisce anche alcune funzioni di debug utili. Per altre informazioni, vedere [Funzioni di debug della sezione critica.](critical-section-debugging-functions.md)

Quando un filtro si arresta o scarica, deve sincronizzare il thread dell'applicazione con il thread di streaming. Per evitare il deadlock, è necessario prima sbloccare il thread di streaming, che potrebbe essere bloccato per diversi motivi:

-   È in attesa di ottenere un esempio all'interno del [**metodo IMemAllocator::GetBuffer,**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) perché tutti gli esempi dell'allocatore sono in uso.
-   È in attesa della restituzione di un altro filtro da un metodo di flusso, ad esempio **Receive.**
-   È in attesa all'interno di uno dei propri metodi di streaming, perché alcune risorse diventino disponibili.
-   Si tratta di un filtro renderer in attesa dell'ora di presentazione dell'esempio successivo
-   Si tratta di un filtro renderer in attesa all'interno **del metodo Receive** mentre è in pausa.

Pertanto, quando il filtro si arresta o scarica, deve eseguire le operazioni seguenti:

-   Rilasciare tutti gli esempi che contiene per qualsiasi motivo. In questo modo viene sbloccato **il metodo GetBuffer.**
-   Restituire da qualsiasi metodo di streaming il più rapidamente possibile. Se un metodo di streaming è in attesa di una risorsa, deve interrompere immediatamente l'attesa.
-   Avviare il rifiuto degli esempi in **Receive**, in modo che il thread di streaming non accedono ad altre risorse. La [**classe CBaseInputPin**](cbaseinputpin.md) gestisce automaticamente questa operazione.
-   Il **metodo Stop** deve eseguire il decommit di tutti gli allocatori del filtro. La **classe CBaseInputPin** gestisce automaticamente questa operazione.

Lo scaricamento e l'arresto si verificano entrambi nel thread dell'applicazione. Un filtro si arresta in risposta al [**metodo IMediaControl::Stop.**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) Gestione filtri Graph il comando stop in ordine upstream, a partire dai renderer e a ritroso fino ai filtri di origine. Il comando stop viene eseguito completamente all'interno del **metodo CBaseFilter::Stop del** filtro. Quando il metodo viene restituito, il filtro deve essere in stato arrestato.

Lo scaricamento si verifica in genere a causa di un comando seek. Un comando flush inizia dall'origine o dal filtro del parser e si sposta a valle. Lo scaricamento avviene in due fasi: il [**metodo IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) indica a un filtro di rimuovere tutti i dati in sospeso e in ingresso. Il [**metodo IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) segnala al filtro di accettare nuovamente i dati. Lo scaricamento richiede due fasi perché la **chiamata BeginFlush** si trova nel thread dell'applicazione, durante la quale il thread di streaming continua a recapitare i dati. Pertanto, alcuni esempi possono arrivare dopo la **chiamata BeginFlush.** Il filtro deve eliminare questi elementi. Tutti gli esempi che arrivano dopo **la chiamata EndFlush** sono garantiti come nuovi e devono essere recapitati.

Le sezioni seguenti contengono esempi di codice che illustrano come implementare i metodi di filtro più importanti, ad esempio **Pause,** **Receive** e così via, in modo da evitare deadlock e race conditions. Ogni filtro ha tuttavia requisiti diversi, pertanto sarà necessario adattare questi esempi al filtro specifico.

> [!Note]  
> Le classi di base [**CTransformFilter**](ctransformfilter.md) [**e CTransInPlaceFilter**](ctransinplacefilter.md) gestiscono molti dei problemi descritti in questo articolo. Se si scrive un filtro di trasformazione e il filtro non attende gli eventi all'interno di un metodo di streaming o contiene esempi all'esterno di **Receive,** queste classi di base dovrebbero essere sufficienti.

 

 

 



