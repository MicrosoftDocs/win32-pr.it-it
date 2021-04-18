---
description: I componenti sono spesso progettati per eseguire attività di inizializzazione quando vengono chiamati per la prima volta, anziché quando vengono caricati.
ms.assetid: 404c083c-7bee-44c2-b8e7-da1901b6ab2f
title: Inizializzazione One-Time
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16f451e3c51716b4ff6f33b55d8d8602b5d5c28f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318610"
---
# <a name="one-time-initialization"></a>Inizializzazione One-Time

I componenti sono spesso progettati per eseguire attività di inizializzazione quando vengono chiamati per la prima volta, anziché quando vengono caricati. Le funzioni di inizializzazione monouso assicurano che l'inizializzazione venga eseguita una sola volta, anche quando più thread possono tentare l'inizializzazione.

**Windows Server 2003 e Windows XP:** Le applicazioni devono fornire una sincronizzazione personalizzata per l'inizializzazione singola usando le [funzioni Interlocked](interlocked-variable-access.md) o un altro meccanismo di sincronizzazione. Le funzioni di inizializzazione una volta sono disponibili a partire da Windows Vista e Windows Server 2008.

Le funzioni di inizializzazione monouso offrono vantaggi significativi per garantire che solo un thread esegua l'inizializzazione:

-   Sono ottimizzate per la velocità.
-   Creano le barriere appropriate nelle architetture del processore che le richiedono.
-   Supportano sia l'inizializzazione bloccata che quella parallela.
-   Evitano il blocco interno, in modo che il codice possa funzionare in modo asincrono o sincrono.

Il sistema gestisce il processo di inizializzazione tramite una struttura opaca **init \_ once** che contiene dati e informazioni sullo stato. Il chiamante alloca questa struttura e la inizializza chiamando [**InitOnceInitialize**](/windows/win32/api/synchapi/nf-synchapi-initonceinitialize) (per inizializzare la struttura in modo dinamico) o assegnando la costante **init \_ una volta \_ statico \_ init** alla variabile di struttura (per inizializzare la struttura in modo statico). Inizialmente, i dati archiviati nella struttura di inizializzazione singola sono NULL e il suo stato non è inizializzato.

Le strutture di inizializzazione monouso non possono essere condivise tra processi.

Il thread che esegue l'inizializzazione può facoltativamente impostare un contesto disponibile al chiamante al termine dell'inizializzazione. Il contesto può essere un oggetto di sincronizzazione o può essere un valore o una struttura di dati. Se il contesto è un valore, il relativo init di basso livello, **\_ una volta che i \_ \_ \_ bit riservati di CTX** , devono essere pari a zero. Se il contesto è una struttura di dati, è necessario che la struttura dei dati sia allineata a **DWORD**. Il contesto viene restituito al chiamante nel parametro di output *lpContext* della funzione [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) o [**InitOnceExecuteOnce**](/windows/win32/api/synchapi/nf-synchapi-initonceexecuteonce) .

L'inizializzazione unica può essere eseguita in modo sincrono o asincrono. Una funzione di callback facoltativa può essere utilizzata per l'inizializzazione unica sincrona.

## <a name="synchronous-one-time-initialization"></a>Inizializzazione unica sincrona

Nei passaggi seguenti viene descritta l'inizializzazione unica sincrona che non utilizza una funzione di callback.

1.  Il primo thread per chiamare la funzione [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) fa sì che l'inizializzazione venga avviata una sola volta. Per l'inizializzazione unica sincrona, è necessario chiamare **InitOnceBeginInitialize** senza il flag **init \_ once \_ asincrono** .
2.  I thread successivi che tentano l'inizializzazione vengono bloccati fino a quando il primo thread non completa l'inizializzazione o non riesce. Se il primo thread ha esito negativo, il thread successivo può tentare l'inizializzazione e così via.
3.  Al termine dell'inizializzazione, il thread chiama la funzione [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) . Il thread può facoltativamente creare un oggetto di sincronizzazione (o altri dati di contesto) e specificarlo nel parametro *lpContext* della funzione **InitOnceComplete** .
4.  Se l'inizializzazione ha esito positivo, lo stato della struttura di inizializzazione singola viene modificato in Initialized e l'handle *lpContext* (se presente) viene archiviato nella struttura di inizializzazione. I tentativi di inizializzazione successivi restituiscono i dati di contesto. Se l'inizializzazione ha esito negativo, i dati sono **null**.

Nei passaggi seguenti viene descritta l'inizializzazione unica sincrona che utilizza una funzione di callback.

1.  Il primo thread per chiamare correttamente la funzione [**InitOnceExecuteOnce**](/windows/win32/api/synchapi/nf-synchapi-initonceexecuteonce) passa un puntatore a una funzione di callback [*InitOnceCallback*](/windows/win32/api/synchapi/nc-synchapi-pinit_once_fn) definita dall'applicazione e ai dati richiesti dalla funzione di callback. Se la chiamata ha esito positivo, viene eseguita la funzione di callback *InitOnceCallback* .
2.  I thread successivi che tentano l'inizializzazione vengono bloccati fino a quando il primo thread non completa l'inizializzazione o non riesce. Se il primo thread ha esito negativo, il thread successivo può tentare l'inizializzazione e così via.
3.  Al termine dell'inizializzazione, la funzione di callback restituisce. La funzione di callback può creare facoltativamente un oggetto di sincronizzazione (o altri dati di contesto) e specificarlo nel parametro di output del *contesto* .
4.  Se l'inizializzazione ha esito positivo, lo stato della struttura di inizializzazione monouso viene modificato in Initialized e l'handle del *contesto* , se presente, viene archiviato nella struttura di inizializzazione. I tentativi di inizializzazione successivi restituiscono i dati di contesto. Se l'inizializzazione ha esito negativo, i dati sono **null**.

## <a name="asynchronous-one-time-initialization"></a>Inizializzazione unica asincrona

Nei passaggi seguenti viene descritta l'inizializzazione unica asincrona.

1.  Se più thread tentano simultaneamente di iniziare l'inizializzazione chiamando [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) con **init \_ una volta \_ Async**, la funzione ha esito positivo per tutti i thread il cui parametro *fPending* è impostato su **true**. Solo un thread avrà effettivamente esito positivo in fase di inizializzazione. altri tentativi simultanei non modificano lo stato di inizializzazione.
2.  Quando [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) restituisce, il parametro *fPending* indica lo stato di inizializzazione:
    -   Se *fPending* è **false**, un thread ha avuto esito positivo in fase di inizializzazione. Altri thread devono pulire tutti i dati di contesto creati e usare i dati di contesto nel parametro di output *lpContext* di [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize).
    -   Se *fPending* è **true**, l'inizializzazione non è ancora stata completata e gli altri thread continuano.
3.  Ogni thread chiama la funzione [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) . Il thread può facoltativamente creare un oggetto di sincronizzazione (o altri dati di contesto) e specificarlo nel parametro *lpContext* di **InitOnceComplete**.
4.  Quando [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) restituisce, il relativo valore restituito indica se il thread chiamante ha avuto esito positivo in fase di inizializzazione.
    -   Se [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) ha esito positivo, il thread chiamante ha avuto esito positivo in fase di inizializzazione. Lo stato della struttura di inizializzazione monouso viene modificato in Initialized e l'handle *lpContext* (se presente) viene archiviato nella struttura di inizializzazione.
    -   Se [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) ha esito negativo, un altro thread ha completato l'inizializzazione. Il thread chiamante deve pulire tutti i dati di contesto creati e chiamare [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) con **init \_ una sola volta \_ Check \_ solo** per recuperare i dati di contesto archiviati nella struttura di inizializzazione unica.

## <a name="calling-one-time-initialization-from-multiple-sites"></a>Chiamata dell'inizializzazione di One-Time da più siti

L'inizializzazione unica sorvegliata da una singola struttura **init \_ once** può essere eseguita da siti multipli. è possibile che vengano passati callback diversi da ogni sito e che la sincronizzazione con e senza callback possa essere mista. L'inizializzazione è ancora garantita per eseguire sucesfully una sola volta.

L'inizializzazione asincrona e sincrona, tuttavia, non può essere mista: una volta eseguito un tentativo di inizializzazione asincrona, i tentativi di avviare l'inizializzazione sincrona

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Utilizzo dell'inizializzazione One-Time](using-one-time-initialization.md)
</dt> </dl>

 

 
