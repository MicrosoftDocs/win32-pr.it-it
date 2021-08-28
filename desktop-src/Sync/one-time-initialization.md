---
description: I componenti sono spesso progettati per eseguire attività di inizializzazione quando vengono chiamati per la prima volta, anziché quando vengono caricati.
ms.assetid: 404c083c-7bee-44c2-b8e7-da1901b6ab2f
title: One-Time inizializzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51e513c18be3fcce85c8d2cde16bbe11edcf6a1597bb06c37279ecaa8add6598
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073081"
---
# <a name="one-time-initialization"></a>One-Time inizializzazione

I componenti sono spesso progettati per eseguire attività di inizializzazione quando vengono chiamati per la prima volta, anziché quando vengono caricati. Le funzioni di inizializzazione una sola volta assicurano che l'inizializzazione venga eseguita una sola volta, anche quando più thread possono tentare l'inizializzazione.

**Windows Server 2003 e Windows XP:** Le applicazioni devono fornire la propria sincronizzazione per l'inizializzazione una sola volta usando le [funzioni interlocked](interlocked-variable-access.md) o un altro meccanismo di sincronizzazione. Le funzioni di inizializzazione una sola volta sono disponibili a partire da Windows Vista e Windows Server 2008.

Le funzioni di inizializzazione una sola volta offrono vantaggi significativi per garantire che l'inizializzazione sia eseguita da un solo thread:

-   Sono ottimizzati per la velocità.
-   Creano le barriere appropriate sulle architetture del processore che le richiedono.
-   Supportano sia l'inizializzazione bloccata che l'inizializzazione parallela.
-   Evitano il blocco interno in modo che il codice possa funzionare in modo asincrono o sincrono.

Il sistema gestisce il processo di inizializzazione tramite una struttura **INIT \_ ONCE** opaca che contiene dati e informazioni sullo stato. Il chiamante alloca questa struttura e la inizializza chiamando [**InitOnceInitialize**](/windows/win32/api/synchapi/nf-synchapi-initonceinitialize) (per inizializzare la struttura in modo dinamico) o assegnando la costante **INIT \_ ONCE STATIC \_ \_ INIT** alla variabile di struttura (per inizializzare la struttura in modo statico). Inizialmente, i dati archiviati nella struttura di inizializzazione una sola volta sono NULL e il relativo stato non è inizializzato.

Le strutture di inizializzazione una sola volta non possono essere condivise tra processi.

Il thread che esegue l'inizializzazione può facoltativamente impostare un contesto disponibile per il chiamante al termine dell'inizializzazione. Il contesto può essere un oggetto di sincronizzazione o un valore o una struttura di dati. Se il contesto è un valore, il valore **INIT \_ ONCE \_ CTX \_ RESERVED \_ BITS** di basso livello deve essere zero. Se il contesto è una struttura di dati, la struttura dei dati deve essere **allineata con DWORD.** Il contesto viene restituito al chiamante nel parametro di output *lpContext* della [**funzione InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) o [**InitOnceExecuteOnce.**](/windows/win32/api/synchapi/nf-synchapi-initonceexecuteonce)

L'inizializzazione una sola volta può essere eseguita in modo sincrono o asincrono. È possibile usare una funzione di callback facoltativa per l'inizializzazione una sola volta sincrona.

## <a name="synchronous-one-time-initialization"></a>Inizializzazione una sola volta sincrona

La procedura seguente descrive l'inizializzazione una sola volta sincrona che non usa una funzione di callback.

1.  Il primo thread che chiama correttamente la [**funzione InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) determina l'avvio dell'inizializzazione una sola volta. Per l'inizializzazione una sola volta sincrona, **InitOnceBeginInitialize** deve essere chiamato senza il flag **\_ \_ ASYNC INIT ONCE.**
2.  I thread successivi che tentano l'inizializzazione vengono bloccati fino a quando il primo thread non completa l'inizializzazione o non ha esito negativo. Se il primo thread ha esito negativo, il thread successivo può tentare l'inizializzazione e così via.
3.  Al termine dell'inizializzazione, il thread chiama la [**funzione InitOnceComplete.**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) Il thread può facoltativamente creare un oggetto di sincronizzazione (o altri dati di contesto) e specificarlo nel *parametro lpContext* della **funzione InitOnceComplete.**
4.  Se l'inizializzazione ha esito positivo, lo stato della struttura di inizializzazione una sola volta viene modificato in inizializzato e l'handle *lpContext* (se presente) viene archiviato nella struttura di inizializzazione. I successivi tentativi di inizializzazione restituiscono questi dati di contesto. Se l'inizializzazione non riesce, i dati sono **NULL.**

La procedura seguente descrive l'inizializzazione una sola volta sincrona che usa una funzione di callback.

1.  Il primo thread che chiama correttamente la [**funzione InitOnceExecuteOnce**](/windows/win32/api/synchapi/nf-synchapi-initonceexecuteonce) passa un puntatore a una funzione di callback [*InitOnceCallback*](/windows/win32/api/synchapi/nc-synchapi-pinit_once_fn) definita dall'applicazione e a tutti i dati richiesti dalla funzione di callback. Se la chiamata ha esito positivo, viene eseguita la funzione di callback *InitOnceCallback.*
2.  I thread successivi che tentano l'inizializzazione vengono bloccati fino a quando il primo thread non completa l'inizializzazione o non ha esito negativo. Se il primo thread ha esito negativo, il thread successivo può tentare l'inizializzazione e così via.
3.  Al termine dell'inizializzazione, la funzione di callback restituisce . La funzione di callback può facoltativamente creare un oggetto di sincronizzazione (o altri dati di contesto) e specificarlo nel parametro di output *Context.*
4.  Se l'inizializzazione ha esito positivo, lo stato della struttura di inizializzazione una sola volta viene modificato in inizializzato e l'handle *di* contesto (se presente) viene archiviato nella struttura di inizializzazione. I successivi tentativi di inizializzazione restituiscono questi dati di contesto. Se l'inizializzazione non riesce, i dati sono **NULL.**

## <a name="asynchronous-one-time-initialization"></a>Inizializzazione una sola volta asincrona

La procedura seguente descrive l'inizializzazione una sola volta asincrona.

1.  Se più thread tentano contemporaneamente di avviare l'inizializzazione chiamando [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) con **INIT \_ ONCE \_ ASYNC,** la funzione ha esito positivo per tutti i thread con il parametro *fPending* impostato su **TRUE.** Solo un thread avrà effettivamente esito positivo durante l'inizializzazione. altri tentativi simultanei non modificano lo stato di inizializzazione.
2.  Quando [**viene restituito InitOnceBeginInitialize,**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) il *parametro fPending* indica lo stato di inizializzazione:
    -   Se *fPending* è **FALSE,** un thread ha avuto esito positivo in fase di inizializzazione. Altri thread devono pulire tutti i dati di contesto creati e usare i dati di contesto nel parametro di output *lpContext* [**di InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize).
    -   Se *fPending è* **TRUE,** l'inizializzazione non è ancora stata completata e gli altri thread devono continuare.
3.  Ogni thread chiama la [**funzione InitOnceComplete.**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) Il thread può facoltativamente creare un oggetto di sincronizzazione (o altri dati di contesto) e specificarlo nel *parametro lpContext* di **InitOnceComplete.**
4.  Quando [**viene restituito InitOnceComplete,**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) il relativo valore restituito indica se il thread chiamante ha avuto esito positivo durante l'inizializzazione.
    -   Se [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) ha esito positivo, il thread chiamante ha avuto esito positivo durante l'inizializzazione. Lo stato della struttura di inizializzazione una sola volta viene modificato in inizializzato e l'handle *lpContext* (se presente) viene archiviato nella struttura di inizializzazione.
    -   Se [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) ha esito negativo, un altro thread ha avuto esito positivo durante l'inizializzazione. Il thread chiamante deve pulire tutti i dati di contesto creati e chiamare [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) con **INIT \_ ONCE CHECK \_ \_ SOLO** per recuperare i dati di contesto archiviati nella struttura di inizializzazione una sola volta.

## <a name="calling-one-time-initialization-from-multiple-sites"></a>Chiamata One-Time inizializzazione da più siti

L'inizializzazione una sola volta sorvegliata da una singola struttura **INIT \_ ONCE** può essere eseguita da siti mutiple. È possibile passare un callback diverso da ogni sito e la sincronizzazione con e senza callback può essere mista. L'inizializzazione è ancora garantita per eseguire correttamente una sola volta.

Tuttavia, l'inizializzazione asincrona e sincrona non può essere mista: una volta tentata l'inizializzazione asincrona, i tentativi di avviare l'inizializzazione sincrona hanno esito negativo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso dellOne-Time inizializzazione](using-one-time-initialization.md)
</dt> </dl>

 

 
