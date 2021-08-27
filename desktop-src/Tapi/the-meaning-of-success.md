---
description: Quando un'operzione restituisce SUCCESS, la funzione è stata completata correttamente fino a un punto definito dall'API in base a una funzione per funzione.
ms.assetid: e4077d77-dee1-4f1a-a6ee-20ca2f92a1ec
title: Significato di SUCCESS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ae38aa834b3c60107c0245be2c792703a9c038c6e9b96f982e720bf417af58f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126121"
---
# <a name="the-meaning-of-success"></a>Significato di SUCCESS

## <a name="tapi-2x"></a>TAPI 2.x

Quando un'operazione restituisce un'indicazione SUCCESS (in modo sincrono in caso di restituzione della funzione per le operazioni sincrone o in modo asincrono tramite un messaggio [**LINE \_ REPLY**](./line-reply.md) o [**PHONE \_ REPLY**](./phone-reply.md) per le operazioni asincrone), si presuppone che sia true quanto segue:

-   La funzione è stata completata fino a un punto definito dall'API in base a una funzione per funzione. Dopo che tale punto è stato raggiunto, l'operazione è stata completata completamente o sarà in uno stato tale che i messaggi di stato indipendenti informeranno l'applicazione sullo stato di avanzamento successivo.

    Ad esempio, l'implementazione di [**lineMakeCall**](/windows/win32/api/tapi/nf-tapi-linemakecall) di un provider di servizi deve restituire SUCCESS non oltre il momento in cui la chiamata entra nello stato di chiamata di procedura. Idealmente, il provider deve indicare SUCCESS appena possibile, ad esempio quando la chiamata entra nello stato di chiamata del segnale di chiamata (se applicabile). Una volta restituito SUCCESS all'applicazione, i messaggi LINE \_ CALLSTATE informeranno l'applicazione sullo stato di avanzamento della chiamata. I provider di servizi che ritardano la restituzione dell'indicazione **lineMakeCall** SUCCESS, ad esempio fino al completamento della composizione, devono tenere presente che in questo modo il provider si trova in uno svantaggio perché l'usabilità a livello di applicazione può essere fortemente limitata. Ad esempio, non sarebbe possibile per un utente annullare la richiesta di configurazione della chiamata in corso fino al completamento della composizione e all'invio di tutte le cifre al commutatore.

-   Le funzioni che restituiscono informazioni ( ad esempio [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo)) restituiscono SUCCESS solo quando le informazioni richieste sono disponibili per l'applicazione. Le funzioni che restituiscono handle (a righe o chiamate) possono restituire SUCCESS solo dopo che l'handle è valido. Non è necessario inviare messaggi sulla riga o sulla chiamata prima dell'indicazione SUCCESS della funzione che ne ha causato la creazione. Il provider di servizi è responsabile dell'eliminazione di tali messaggi.
-   Le funzioni che abilitano determinate condizioni permanenti ( ad esempio [**lineMonitorDigits**](/windows/win32/api/tapi/nf-tapi-linemonitordigits)) restituiscono SUCCESS solo dopo l'abilitazione della condizione, non quando la condizione viene rimossa nuovamente (ad esempio, non quando è stato completato il monitoraggio di tutte le cifre).
-   Le funzioni di controllo delle chiamate ( ad esempio [**lineHold**](/windows/win32/api/tapi/nf-tapi-linehold) o [**lineSetupTransfer**](/windows/win32/api/tapi/nf-tapi-linesetuptransfer), ma non [**lineMakeCall**](/windows/win32/api/tapi/nf-tapi-linemakecall)) restituiscono SUCCESS al termine dell'operazione. Alcune reti telefoniche non forniscono il riconoscimento (positivo o negativo) del completamento di determinate richieste effettuate dai provider di servizi. In tali situazioni, il provider di servizi deve decidere se la richiesta ha esito positivo o negativo. Pertanto, SUCCESS può indicare che il provider di servizi ha avviato azioni per soddisfare la richiesta, ma non necessariamente altro. Ad esempio, il provider potrebbe non ricevere alcun riconoscimento affermativo alla richiesta dall'opzione , anche se ha già inviato un messaggio di operazione riuscita all'applicazione.

## <a name="tapi-3x"></a>TAPI 3.x

Quando un'operazione restituisce un'indicazione SUCCESS (in modo sincrono in caso di restituzione della funzione per le operazioni sincrone o in modo asincrono con una chiamata alla procedura di callback [**ASYNC \_ COMPLETION**](/windows/win32/api/tspi/nc-tspi-async_completion) per le operazioni asincrone), si presuppone che sia true quanto segue:

-   La funzione è stata completata fino a un punto definito dal provider di servizi. Il provider di servizi definisce il punto funzione per funzione. Dopo aver raggiunto tale punto, l'operazione è stata completata completamente o si trova in uno stato tale che i successivi messaggi di stato indipendenti informeranno l'applicazione dello stato di avanzamento.
-   Le funzioni che restituiscono informazioni,ad esempio [**\_ linePark TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linepark) o [**\_ lineDevSpecific TSPI,**](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific)restituiscono SUCCESS solo quando le informazioni richieste sono disponibili per il chiamante. Le funzioni che restituiscono handle (a righe aperte, telefoni aperti o chiamate) restituiscono gli handle immediatamente al ritorno della funzione. Sia il provider di servizi che il chiamante devono considerare gli handle come "non ancora validi" fino all'eventuale indicazione SUCCESS. Il provider di servizi è responsabile di impedire qualsiasi messaggio di callback alla procedura [**LINEEVENT**](/windows/win32/api/tspi/nc-tspi-lineevent) o [**PHONEEVENT**](/windows/desktop/api/tspi/nc-tspi-phoneevent) relativa alla riga aperta, al telefono aperto o alla chiamata fino a dopo l'indicazione SUCCESS. Se il risultato finale è un errore, qualsiasi handle restituito diventa immediatamente non valido senza ulteriori azioni.
-   Le funzioni che abilitano determinate condizioni permanenti (ad [**\_ esempio, lineMonitorDigits TSPI)**](/windows/win32/api/tspi/nf-tspi-tspi_linemonitordigits)restituiscono SUCCESS solo dopo l'abilitazione della condizione, non quando la condizione viene rimossa nuovamente (ad esempio, non quando il monitoraggio delle cifre è completo).
-   Le funzioni di controllo di chiamata (ad esempio [**\_ lineHold TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linehold) e [**\_ lineSetupTransfer TSPI,**](/windows/win32/api/tspi/nf-tspi-tspi_linesetuptransfer)ma non [**\_ lineMakeCall TSPI)**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall)restituiscono SUCCESS al termine dell'operazione. Negli ambienti di telefonia che non forniscono un riconoscimento positivo di queste funzioni, il provider di servizi è obbligato a prendere una decisione con il massimo sforzo in merito all'esito positivo o negativo della funzione.
-   L'implementazione di [**\_ lineMakeCall TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall) di un provider di servizi deve restituire SUCCESS non oltre il momento in cui la chiamata entra nello *stato di* chiamata di procedura. Idealmente, il provider indica SUCCESS appena possibile, ad esempio quando la chiamata entra nello stato di chiamata *dialtone* (se applicabile). Quando viene restituito SUCCESS all'applicazione, i [**messaggi LINE \_ CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) segnalano al chiamante lo stato di avanzamento della chiamata. I provider di servizi che ritardano la restituzione dell'indicazione **\_ lineMakeCall SUCCESS di TSPI,** ad esempio fino al completamento della composizione, limitano fortemente la flessibilità a livello di applicazione. Il ritardo nella restituzione di SUCCESS in **TSPI \_ lineMakeCall** impedisce a un utente di annullare la richiesta di configurazione della chiamata in corso fino al termine della composizione e tutte le cifre vengono inviate al commutatore.

 

 
