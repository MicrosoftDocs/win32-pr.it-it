---
title: Errors
description: In questa sezione vengono illustrati gli errori che possono essere causati dalle funzioni dei servizi Web Windows in seguito a un errore di esecuzione del comando.
ms.assetid: 2e5b853f-589c-4f89-9d7e-cd02263a2247
keywords:
- Errori dei servizi Web per Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e70f10d673bf8f37664d792d8cf969f0329dc363
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855698"
---
# <a name="errors"></a>Errors

In questa sezione vengono illustrati gli errori che possono essere causati dalle funzioni dei servizi Web Windows in seguito a un errore di esecuzione del comando.

-   [Parametri out](#out-parameters)
-   [Codici errore](#error-codes)
-   [Errori avanzati](#rich-errors)
-   [Errori ed errori](#faults-and-errors)
-   [Informazioni sull'errore sensibile alla lingua](#language-sensitive-error-information)
-   [Codici di errore canonici](#canonical-error-codes)
-   [Utilizzo API non valido](#invalid-api-usage)
-   [Sicurezza](#security)

## <a name="out-parameters"></a>Parametri out

Come regola generale, il valore dei parametri out non viene modificato se una funzione ha esito negativo.

Se la funzione ha esito negativo, esistono alcune istanze in cui i parametri out vengono modificati. Questi casi vengono indicati in modo esplicito nella documentazione per ogni parametro. Se la documentazione non menziona alcuna modifica dei parametri in caso di errore, è possibile presupporre che la funzione non le modificherà.

## <a name="error-codes"></a>Codici errore

Tutti i codici di errore restituiti sono HRESULT. Questa API definisce un set di HRESULT nell' \_ intervallo Servizi WEBservices, ma restituisce anche gli errori definiti altrove nell'API Windows.

Per informazioni sui codici di errore restituiti, vedere la documentazione per le API specifiche. L'elenco non deve essere esaustivo per ogni API, bensì un elenco di codici di errore per i quali sono disponibili scenari comuni per la gestione esplicita. Un chiamante deve sempre presupporre che siano possibili altri codici di errore da qualsiasi API.

Questa API definisce un numero relativamente ridotto di codici di errore, che corrispondono a scenari in cui un programma desidera eseguire un'azione in base all'errore. Solo i codici di errore potrebbero non essere sufficienti per determinare la causa dell'errore o per fornire una descrizione corretta del problema all'utente. La migliore comprensione del problema deriva dall'utilizzo di errori avanzati, come descritto di seguito.

## <a name="rich-errors"></a>Errori avanzati

In aggiunta alla restituzione di un codice di errore, un chiamante può facoltativamente richiedere informazioni dettagliate sugli errori per qualsiasi chiamata API passando un oggetto [ \_ errore WS](ws-error.md) non **null**. Per creare un oggetto Error, usare [**WsCreateError**](/windows/desktop/api/WebServices/nf-webservices-wscreateerror). Se si verifica un errore, l'API che ha causato l'errore compilerà l'oggetto errore con contesto aggiuntivo sulla situazione di errore. Se non è presente alcun errore, l'oggetto errore non viene modificato. Il passaggio di un oggetto Error **null** indica che il chiamante non è interessato a informazioni dettagliate sugli errori. È necessario preparare i chiamanti (compresi i callback) per gestire gli oggetti di errore **null** .

Si noti che lo stesso oggetto Error può essere usato per più chiamate API, ma può essere usato solo per una chiamata API alla volta (in quanto è a thread singolo). Ogni volta che si verifica un errore, le informazioni sull'errore vengono accodate all'oggetto Error. Quando una catena di chiamate viene ricaricata, più funzioni possono aggiungere informazioni all'oggetto errore per fornire un contesto aggiuntivo sull'errore. Per cancellare il contenuto dell'oggetto Error prima di riutilizzarlo (dopo che si è verificato un errore), utilizzare [**WsResetError**](/windows/desktop/api/WebServices/nf-webservices-wsreseterror). Se non si verificano errori, non è necessario reimpostare l'oggetto errore prima di riutilizzarlo.

Le informazioni dettagliate sugli errori sono costituite dai seguenti elementi:

-   Set di valori di proprietà che fornisce informazioni aggiuntive sull'errore, se presente. Vedere [**\_ \_ Proprietà WS Error**](/windows/desktop/api/WebServices/ns-webservices-ws_error_property).
-   Zero o più stringhe di errore. Le stringhe vengono aggiunte utilizzando [**WsAddErrorString**](/windows/desktop/api/WebServices/nf-webservices-wsadderrorstring)e possono essere sottoposte a query utilizzando [**WsGetErrorString**](/windows/desktop/api/WebServices/nf-webservices-wsgeterrorstring). Il numero di stringhe può essere sottoposto a query utilizzando il [**\_ conteggio delle stringhe di \_ proprietà \_ \_ WS Error**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id).

## <a name="faults-and-errors"></a>Errori ed errori

Vedere [errori](faults.md) per informazioni sul modo in cui sono correlati gli errori e gli errori.

## <a name="language-sensitive-error-information"></a>Informazioni sull'errore sensibile alla lingua

Quando si crea un oggetto Error, viene specificato il LANGID della traduzione della lingua desiderata per le informazioni sull'errore. Viene utilizzato quando si aggiungono informazioni sugli errori all'oggetto Error.

Questo valore di lingua può essere recuperato o impostato utilizzando la [**\_ Proprietà WS Error \_ \_ LangID**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id).

## <a name="canonical-error-codes"></a>Codici di errore canonici

Questa API fornisce un set di codici di errore (WS \_ E \_ \* ) canonico che consente di utilizzare diverse tecnologie di comunicazione senza dover dipendere dai codici di errore specifici dell'implementazione sottostante specifica. Per un elenco completo di questi codici di errore, vedere [valori restituiti di servizi Web Windows](windows-web-services-return-values.md).

Questo consente, ad esempio, a un programma di verificare se il codice di errore **WS \_ e \_ endpoint \_ non \_** è stato trovato se si utilizza TCP, UDP o http ed eseguire un'azione, ad esempio il tentativo di utilizzare un endpoint diverso.

Quando viene eseguito il mapping di un codice di errore specifico dell'implementazione a un errore canonico, il codice di errore originale viene salvato nell'oggetto Error ed è ancora possibile accedervi per scopi diagnostici. Per ulteriori informazioni, vedere il [**\_ \_ \_ \_ \_ codice di errore originale della proprietà WS Error**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id) .

## <a name="invalid-api-usage"></a>Utilizzo API non valido

I codici di errore seguenti sono riservati per l'utilizzo dell'API non valido e non verranno restituiti in altre circostanze. Se viene restituito uno di questi errori, può essere un'indicazione di un bug dell'applicazione.

-   **\_operazione WS E \_ non valida \_**
-   **E \_ INVALIDARG**

Le enumerazioni seguenti fanno parte della traccia:

-   [**\_ \_ ID proprietà errore \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id)
-   [**\_codice eccezione \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_exception_code)

I codici di errore seguenti fanno parte della traccia:

-   **CERT \_ E \_ CN \_ Nessuna \_ corrispondenza**
-   **CERTIFICATO \_ E \_ scaduto**
-   **CERTIFICATO \_ E \_ UNTRUSTEDROOT**
-   **uso di CERT \_ E \_ errato \_**
-   **REVOCA della crittografia \_ E in \_ \_ modalità offline**
-   **E \_ INVALIDARG**
-   **E \_ OutOfMemory**
-   **\_Indirizzo WS \_ E \_ in \_ uso**
-   **\_Indirizzo WS \_ E \_ non \_ disponibile**
-   **\_ \_ accesso all'endpoint WS E \_ \_ negato**
-   **\_ \_ azione endpoint WS \_ E \_ non \_ supportata**
-   **WS \_ E \_ endpoint \_ disconnesso**
-   **\_ \_ errore endpoint WS \_ E**
-   **\_ \_ errore endpoint WS \_ E \_ ricevuto**
-   **\_endpoint WS \_ E \_ non \_ disponibile**
-   **\_endpoint WS \_ E \_ non \_ trovato**
-   **WS \_ E \_ endpoint \_ troppo \_ occupato**
-   **\_endpoint WS E non \_ \_ raggiungibile**
-   **\_URL endpoint WS E \_ non valido \_ \_**
-   **\_formato WS E \_ non valido \_**
-   **\_operazione WS E \_ non valida \_**
-   **WS \_ E \_ non \_ supportato**
-   **WS \_ E \_ Nessuna \_ conversione \_ disponibile**
-   **\_ \_ overflow numerico WS \_ E**
-   **errore di WS \_ E \_ Object \_**
-   **\_operazione WS \_ E \_ abbandonata**
-   **\_operazione WS \_ E \_ interrotta**
-   **\_timeout dell' \_ operazione WS E \_ \_**
-   **WS \_ E \_ altro**
-   **\_ \_ accesso proxy WS \_ E \_ negato**
-   **\_ \_ errore proxy WS \_ E**
-   **WS \_ E \_ proxy \_ richiede \_ l' \_ autenticazione di base**
-   **WS \_ E \_ proxy \_ richiede \_ l' \_ autenticazione digest**
-   **WS \_ E \_ proxy \_ richiede \_ l' \_ autenticazione Negotiate**
-   **WS \_ E \_ proxy \_ richiede \_ l' \_ autenticazione NTLM**
-   **\_quota WS \_ E \_ superata**
-   **\_errore del \_ sistema di protezione WS E \_ \_**
-   **\_token di \_ sicurezza WS E \_ \_ scaduto**
-   **\_errore di \_ Verifica di sicurezza WS E \_ \_**
-   **WS \_ E \_ server \_ richiede \_ l' \_ autenticazione di base**
-   **WS \_ E \_ server \_ richiede \_ l' \_ autenticazione digest**
-   **WS \_ E \_ server \_ richiede \_ l' \_ autenticazione Negotiate**
-   **WS \_ E \_ server \_ richiede \_ l' \_ autenticazione NTLM**
-   **WS \_ S \_ asincrono**
-   **\_fine WS \_**

Le funzioni seguenti fanno parte della traccia:

-   [**\_ \_ ID proprietà errore \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id)
-   [**\_codice eccezione \_ WS**](/windows/desktop/api/WebServices/ne-webservices-ws_exception_code)

Il seguente handle fa parte della traccia:

-   [\_errore WS](ws-error.md)

La struttura seguente fa parte della traccia:

-   [**\_Proprietà WS Error \_**](/windows/desktop/api/WebServices/ns-webservices-ws_error_property)

## <a name="security"></a>Sicurezza

È necessario tenere presenti alcune considerazioni di sicurezza che l'utente dell'oggetto Error deve tenere presente:

-   L'oggetto Error può contenere dati non attendibili. Gli esempi sono: l'errore WS \_ e le stringhe di errore, che possono essere memorizzate nell'oggetto errore in base alle informazioni ricevute su un canale non attendibile. Per esaminare le informazioni nell'oggetto errore e prendere decisioni in base ai relativi valori, è necessario prestare attenzione all'utente dell'oggetto Error.
-   Un utente dell'oggetto Error deve chiamare [**WsResetError**](/windows/desktop/api/WebServices/nf-webservices-wsreseterror) dopo aver esaminato le informazioni sull'errore. In caso contrario, può causare un accumulo di memoria.
-   Un utente dell'oggetto Error deve prestare particolare attenzione quando si usa il \_ \_ \_ valore di divulgazione di errore completo WS dell'enumerazione di [**\_ \_ divulgazione degli errori WS**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_disclosure) , perché l'errore generato potrebbe contenere informazioni private accumulate come parte del processo di registrazione degli errori.

 

 




