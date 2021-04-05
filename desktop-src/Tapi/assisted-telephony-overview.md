---
description: Una funzionalità importante della telefonia è la piccola serie di funzioni denominate telefonia assistita.
ms.assetid: 1c41f52b-f8bf-410e-a966-9323a690a4d5
title: Panoramica della telefonia assistita
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b6a8826fd0c273936204d9250fb91504333d807
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967861"
---
# <a name="assisted-telephony-overview"></a>Panoramica della telefonia assistita

Una funzionalità importante della telefonia è la piccola serie di funzioni denominate telefonia assistita. La telefonia assistita è progettata per facilitare la creazione di chiamate vocali e di chiamate multimediali disponibili per qualsiasi applicazione, non solo per quelle dedicate alla funzionalità di telefonia. In altre parole, la telefonia assistita consente alle applicazioni di effettuare chiamate telefoniche senza che sia necessario conoscere i dettagli dei servizi dell'API di telefonia completa. Consente di estendere la telefonia a applicazioni di elaborazione di testo, fogli di calcolo, database, Personal Information Manager e altre applicazioni non di telefonia.

Per un elenco delle funzioni di telefonia assistita di TAPI 2. x della telefonia di base, vedere la Guida di riferimento alle funzioni [rapide TAPI](./tapi-quick-function-reference.md). TAPI 3. x supporta la telefonia assistita tramite l'interfaccia [**ITRequest**](/windows/desktop/api/tapi3if/nn-tapi3if-itrequest) .

L'utilità della telefonia assistita può essere illustrata nell'esempio seguente. Un'applicazione per fogli di calcolo può incorporare funzioni che compongono un numero di telefono per una chiamata vocale. Fino a quando l'applicazione non necessita di alcun controllo di chiamata dettagliato fornito dall'API di telefonia completa, la telefonia assistita è il modo più semplice ed efficiente per fornire funzionalità di telefonia it.

![telefonia assistita con un'applicazione foglio di calcolo](images/assist4.png)

La telefonia assistita e l'API di telefonia completa vengono utilizzate e implementate in modi diversi, pertanto non è consigliabile combinare chiamate di funzione di telefonia assistita e chiamate di funzioni API di telefonia all'interno di una singola applicazione.

## <a name="using-assisted-telephony"></a>Uso della telefonia assistita

Le applicazioni che utilizzano servizi di telefonia assistita avviano solo richieste di chiamata temporaneamente accodate da TAPI. L'applicazione Richiedi destinatario recupera queste richieste e le esegue per conto dell'applicazione di telefonia assistita. La funzione [**tapiRequestMakeCall**](/windows/win32/api/tapi/nf-tapi-tapirequestmakecall) richiede la creazione di una chiamata vocale. L'applicazione richiedente non controlla la chiamata.

TAPI consente all'utente di definire applicazioni destinatarie diverse o identiche per ognuno di questi servizi. Un'applicazione diventa un destinatario della richiesta mediante la registrazione con [**lineRegisterRequestRecipient**](/windows/win32/api/tapi/nf-tapi-lineregisterrequestrecipient), in cui **true** viene specificato come valore per il parametro *bEnable*. (Se si specifica **false** , l'applicazione viene annullata come destinatario della richiesta, operazione che deve essere eseguita quando è stato determinato che i compiti del destinatario passano per la sessione corrente). L'applicazione seleziona i servizi che desidera gestire nel parametro *dwRequestMode* di **lineRegisterRequestRecipient**. Un possibile valore per una richiesta è LINEREQUESTMODE \_ MAKECALL, per indicare che l'applicazione gestirà le richieste [**tapiRequestMakeCall**](/windows/win32/api/tapi/nf-tapi-tapirequestmakecall) . Se più applicazioni si registrano per gli stessi servizi, viene utilizzato uno schema di priorità per consentire all'utente di selezionare quale applicazione è preferibile per la gestione delle richieste. Questo schema di priorità è identico a quello usato per la consegna delle chiamate e il routing delle chiamate in ingresso in base a un elenco di nomi di file in **HandoffPriorities** nel registro di sistema.

## <a name="call-requests"></a>Richieste di chiamata

La telefonia assistita offre applicazioni abilitate per la telefonia con un meccanismo di facile utilizzo per effettuare chiamate telefoniche senza richiedere che lo sviluppatore diventi completamente alfabetizzato nella telefonia.

La funzione [**tapiRequestMakeCall**](/windows/win32/api/tapi/nf-tapi-tapirequestmakecall) richiede una chiamata vocale tra l'utente e una parte remota specificata dal numero di telefono. La richiesta viene effettuata a TAPI, che la passa a un'applicazione registrata come destinatario di tali richieste. Questo destinatario è un'applicazione Call Manager.

Dopo che l'applicazione ha effettuato la richiesta, la chiamata viene controllata interamente dall'applicazione Call Manager perché le applicazioni di telefonia assistita non possono gestire le chiamate. Poiché gli aspetti più complessi della telefonia e tutte le operazioni dell'interfaccia utente vengono gestiti dall'applicazione Call Manager, le applicazioni abilitate per la telefonia non devono essere modificate in alcun modo sostanziale. Infatti, le applicazioni che consentono di richiamare questa operazione dal linguaggio di script predefinito potrebbero non essere necessariamente modificate.

La funzione [**tapiGetLocationInfo**](/windows/win32/api/tapi/nf-tapi-tapigetlocationinfo) restituisce all'applicazione il codice del paese o dell'area geografica e il codice della città (area) che l'utente ha impostato nei parametri del percorso corrente nel pannello di controllo della telefonia. L'applicazione può utilizzare queste informazioni per aiutare l'utente a formare numeri di telefono canonico appropriati, ad esempio offrendo questi valori come predefiniti quando vengono immessi nuovi numeri in una voce della rubrica telefonica o in un record di database.

## <a name="request-recipients"></a>Destinatari richieste

Per eseguire la telefonia assistita sono necessari due tipi di applicazioni. I *client* di telefonia assistita sono applicazioni che utilizzano la telefonia assistita chiamando le funzioni con prefisso "TAPI". Un esempio di tale applicazione client può essere un foglio di calcolo a cui viene aggiunto un comando di menu di **selezione** o un pulsante della barra degli strumenti.

I *Server* di telefonia assistita sono applicazioni in grado di eseguire funzioni API di telefonia derivanti da una chiamata di un'altra applicazione a una funzione con prefisso "TAPI". Per rendersi noto come server di telefonia assistito, un'applicazione di questo tipo viene registrata come un server utilizzando la funzione [**lineRegisterRequestRecipient**](/windows/win32/api/tapi/nf-tapi-lineregisterrequestrecipient) .

Le funzioni della telefonia assistita, che iniziano con il prefisso "TAPI", sono note come *funzioni di richiesta*. Le applicazioni di telefonia assistita che elaborano queste richieste, ovvero i server di telefonia assistita, vengono chiamate *destinatari della richiesta*.

## <a name="processing-assisted-telephony-requests"></a>Elaborazione di richieste di telefonia assistita

Il processo con cui vengono recapitate e gestite le richieste è il seguente:

1.  Quando TAPI riceve una richiesta di telefonia assistita, verifica la presenza di un destinatario della richiesta, ovvero un'applicazione attualmente registrata per elaborare quel tipo di richiesta. Se è presente un destinatario della richiesta, la richiesta viene accodata e l'applicazione con la priorità più alta registrata per il servizio della richiesta riceve un messaggio [**di \_ richiesta di riga**](./line-request.md) . Il messaggio notifica al destinatario della richiesta che è arrivata una nuova richiesta e contiene un'indicazione della modalità della richiesta.
2.  Se TAPI non riesce a trovare un'applicazione attualmente in esecuzione per elaborare una richiesta di questo tipo, tenta di avviare un'applicazione registrata come in grado di eseguire questa operazione. Le informazioni di registrazione vengono registrate in **HandoffPriorities** nel registro di sistema. TAPI tenta di avviare le applicazioni nell'ordine in cui sono elencate nella sezione **HandoffPriorities** . (Vedere il passaggio successivo).

    Se non è attualmente registrata alcuna applicazione, TAPI esamina l'elenco di applicazioni di elaborazione richieste sulla voce associata in **HandoffPriorities**. Se la riga associata non è presente nel file, se non vi sono applicazioni elencate o se non è possibile avviare nessuna delle applicazioni nell'elenco, la richiesta viene rifiutata con l'errore TAPIERR \_ NOREQUESTRECIPIENT.

    Quando viene avviato un destinatario della richiesta (indipendentemente dal fatto che sia stato avviato da TAPI), è doveroso chiamare [**lineRegisterRequestRecipient**](/windows/win32/api/tapi/nf-tapi-lineregisterrequestrecipient) durante il processo di avvio e registrarsi come destinatario della richiesta.

3.  Se nella voce sono elencate una o più applicazioni, TAPI inizia con la prima applicazione elencata (priorità più alta) e tenta di avviarla utilizzando la funzione [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) . Se il tentativo di avviare l'applicazione ha esito negativo, TAPI tenta di avviare l'applicazione successiva nell'elenco. Quando un'applicazione viene avviata correttamente, TAPI Accoda semplicemente la richiesta e restituisce un'indicazione di esito positivo all'applicazione anche se la richiesta non è stata ancora segnalata al destinatario della richiesta.

    Una volta avviata, l'applicazione del destinatario della richiesta chiama [**lineRegisterRequestRecipient**](/windows/win32/api/tapi/nf-tapi-lineregisterrequestrecipient), che causa l'invio di un messaggio di [**\_ richiesta di riga**](./line-request.md) , segnalando che la richiesta è stata accodata. Se per qualche motivo l'applicazione avviata non viene mai registrata, la richiesta rimane in coda e rimane nella coda per un periodo illimitato fino a quando un'applicazione non si registra per quel tipo di richiesta.

4.  Se TAPI trova una tale applicazione registrata già in esecuzione o ne avvia una correttamente, Accoda la richiesta, invia un \_ messaggio di richiesta di riga all'applicazione server e restituisce un'indicazione di esito positivo per la chiamata di funzione all'applicazione di telefonia assistita. Questo messaggio di esito positivo indica solo che la richiesta è stata accettata e accodata e non è stata eseguita correttamente.

Quando l'applicazione server è pronta per l'elaborazione di una richiesta, chiama la funzione [**lineGetRequest**](/windows/win32/api/tapi/nf-tapi-linegetrequest) . Ciò consente di ricevere tutte le informazioni necessarie, ad esempio un indirizzo da comporre. Elabora quindi la richiesta, usando le funzioni TAPI, ad esempio [**lineMakeCall**](/windows/win32/api/tapi/nf-tapi-linemakecall) e [**lineDrop**](/windows/win32/api/tapi/nf-tapi-linedrop), che altrimenti verrebbero usate per inserire la chiamata. Richiamando **lineGetRequest** viene rimossa la richiesta da TAPI e i parametri della richiesta vengono copiati in un buffer di richiesta allocato dall'applicazione. Le dimensioni e l'interpretazione del contenuto del buffer dipendono dalla modalità di richiesta.

Il server deve assicurarsi che usi i parametri corretti durante l'esecuzione delle richieste. Quando si esegue questa operazione, vengono seguiti i passaggi seguenti:

1.  Il destinatario della richiesta riceve prima di tutto un messaggio di [**\_ richiesta di riga**](./line-request.md) che informa che è possibile che esistano richieste nella coda di richieste. In questo modo, l'applicazione chiama [**lineGetRequest**](/windows/win32/api/tapi/nf-tapi-linegetrequest) e continua a chiamarla finché la coda non viene svuotata (se la richiesta è per effettuare una nuova chiamata) o per eliminare una chiamata esistente. Questo messaggio non contiene i parametri per la richiesta, tranne nel caso di una richiesta di eliminazione di una chiamata esistente.
2.  Se la richiesta deve effettuare una nuova chiamata, il server di telefonia assistita usa la funzione [**lineGetRequest**](/windows/win32/api/tapi/nf-tapi-linegetrequest) per recuperare la richiesta completa, che include i parametri della richiesta. Il server ha ora tutte le informazioni necessarie, ad esempio il numero da comporre o l'identificazione del creatore della richiesta. Prima di tutto, tuttavia, il server deve allocare la memoria necessaria per archiviare queste informazioni.
3.  Infine, il server esegue la richiesta richiamando la funzione o il set di funzioni TAPI appropriato.

Se TAPI non può avviare un'applicazione in grado di fungere da destinatario della richiesta, la chiamata di telefonia assistita ha esito negativo e restituisce l'errore TAPIERR \_ NOREQUESTRECIPIENT.

## <a name="notes-on-request-recipient-operations"></a>Note sulle operazioni del destinatario della richiesta

Le informazioni seguenti riguardano i sistemi in cui vengono elaborate le richieste di telefonia assistita:

-   Il registro di sistema predefinito dovrebbe elencare un'applicazione Call Manager nell'elenco di priorità per [**tapiRequestMakeCall**](/windows/win32/api/tapi/nf-tapi-tapirequestmakecall). Sarebbe utile, ma non essenziale, che l'applicazione Call Manager disponga di un'opzione di menu che consente agli utenti di impostarla sulla priorità più elevata.
-   Quando un'applicazione del destinatario della telefonia assistita viene avviata automaticamente da TAPI e se è l'unica applicazione TAPI nel sistema, questa azione Inizializza TAPI. Se l'applicazione del destinatario di telefonia assistita Inizializza e arresta il dispositivo di linea prima di eseguire la registrazione per le richieste di telefonia assistita, viene arrestato anche TAPI e la richiesta di telefonia assistita viene persa. Anche le richieste di telefonia assistita possono andare perse quando un'altra applicazione TAPI avviata esegue un inizializzazione e una chiusura.

 

 
