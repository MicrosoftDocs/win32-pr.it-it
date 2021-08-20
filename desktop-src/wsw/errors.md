---
title: Errors
description: In questa sezione vengono descritti gli errori che possono verificarsi Windows funzioni dei servizi Web in seguito a un errore di esecuzione del comando.
ms.assetid: 2e5b853f-589c-4f89-9d7e-cd02263a2247
keywords:
- Errori dei servizi Web per Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a08a6371dcc5265239c6a25ce0c01075cff3ae12533862ed8a1cbbbe7aba705
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026529"
---
# <a name="errors"></a>Errors

In questa sezione vengono descritti gli errori che possono verificarsi Windows funzioni dei servizi Web in seguito a un errore di esecuzione del comando.

-   [Parametri Out](#out-parameters)
-   [Codici errore](#error-codes)
-   [Errori di tipo Rtf](#rich-errors)
-   [Errori ed errori](#faults-and-errors)
-   [Informazioni sugli errori sensibili alla lingua](#language-sensitive-error-information)
-   [Codici di errore canonici](#canonical-error-codes)
-   [Utilizzo API non valido](#invalid-api-usage)
-   [Sicurezza](#security)

## <a name="out-parameters"></a>Parametri Out

Come regola generale, il valore dei parametri out non viene modificato se una funzione ha esito negativo.

Esistono alcune istanze in cui i parametri out vengono modificati se la funzione ha esito negativo. Questi casi vengono definiti in modo esplicito nella documentazione per ogni parametro. Se la documentazione non cita alcuna modifica dei parametri out in caso di errore, è possibile presupporre che la funzione non li modificherà.

## <a name="error-codes"></a>Codici errore

Tutti i codici restituiti di errore sono HRESULT. Questa API definisce un set di HRESULT nell'intervallo FACILITY WEBSERVICES, ma restituisce anche gli errori definiti altrove \_ nell'API Windows.

Per informazioni sui codici di errore restituiti, vedere la documentazione per api specifiche. L'elenco non deve essere esaustivo per ogni API, ma piuttosto un elenco di codici di errore per i quali esistono scenari comuni per la gestione esplicita. Un chiamante deve sempre presupporre che altri codici di errore siano possibili da qualsiasi API.

Questa API definisce un numero relativamente ridotto di codici di errore, che corrispondono agli scenari in cui un programma dovrà intervenire in base all'errore. I codici di errore da soli potrebbero non essere sufficienti per determinare cosa è andato storto o per fornire una buona descrizione del problema all'utente. La migliore comprensione del problema deriva dall'uso di errori rtf, come descritto di seguito.

## <a name="rich-errors"></a>Errori di tipo Rtf

Oltre a restituire un codice di errore, un chiamante può facoltativamente richiedere informazioni dettagliate sull'errore per qualsiasi chiamata API passando un oggetto [WS \_ ERROR](ws-error.md) non **NULL.** Per creare un oggetto errore, usare [**WsCreateError**](/windows/desktop/api/WebServices/nf-webservices-wscreateerror). Se si verifica un errore, l'API che ha causato l'errore riempirà l'oggetto errore con un contesto aggiuntivo sulla situazione dell'errore. Se non si verifica alcun errore, l'oggetto errore non viene modificato. Il passaggio **di un** oggetto errore NULL indica che il chiamante non è interessato a informazioni dettagliate sugli errori. I chiamato (inclusi i callback) devono essere preparati per gestire gli **oggetti errore NULL.**

Si noti che lo stesso oggetto errore può essere usato per più chiamate API, ma può essere usato solo per una chiamata API alla volta (perché è a thread singolo). Ogni volta che si verifica un errore, le informazioni sull'errore vengono aggiunte all'oggetto errore. Durante la rimozione di una catena di chiamate, più funzioni possono aggiungere informazioni all'oggetto errore per fornire un contesto aggiuntivo sull'errore. Per cancellare il contenuto dell'oggetto errore prima di riutilizzarlo (dopo che si verifica un errore), usare [**WsResetError**](/windows/desktop/api/WebServices/nf-webservices-wsreseterror). Se non si verifica alcun errore, non è necessario reimpostare l'oggetto errore prima di riutilizzarlo.

Le informazioni dettagliate sugli errori sono costituite dalle seguenti:

-   Set di valori di proprietà, che forniscono informazioni aggiuntive sull'errore, se presente. Vedere [**PROPRIETÀ \_ ERROR \_ DI WS**](/windows/desktop/api/WebServices/ns-webservices-ws_error_property).
-   Zero o più stringhe di errore. Le stringhe vengono aggiunte [**tramite WsAddErrorString**](/windows/desktop/api/WebServices/nf-webservices-wsadderrorstring)e possono essere sottoposti a query usando [**WsGetErrorString**](/windows/desktop/api/WebServices/nf-webservices-wsgeterrorstring). È possibile eseguire query sul numero di stringhe usando [**WS \_ ERROR PROPERTY STRING \_ \_ \_ COUNT**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id).

## <a name="faults-and-errors"></a>Errori ed errori

Per [informazioni sulla relazione](faults.md) tra errori e errori, vedere Errori.

## <a name="language-sensitive-error-information"></a>Informazioni sugli errori sensibili alla lingua

Quando si crea un oggetto errore, viene specificato il LANGID della traduzione della lingua desiderata per le informazioni sull'errore. Viene usato quando si aggiungono informazioni sull'errore all'oggetto errore.

Questo valore di lingua può essere recuperato o impostato usando [**WS \_ ERROR PROPERTY \_ \_ LANGID**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id).

## <a name="canonical-error-codes"></a>Codici di errore canonici

Questa API fornisce un set canonico di codici di errore (WS E) che consentono di usare tecnologie di comunicazione diverse senza dover dipendere dai codici di errore specifici \_ \_ \* dell'implementazione sottostante specifica. Per un elenco completo di questi codici di errore, vedere Windows [valori restituiti dei servizi Web](windows-web-services-return-values.md).

Ciò consente, ad esempio, a un programma di controllare il codice di errore **WS \_ E ENDPOINT NOT \_ \_ \_ FOUND** se si usa TCP, UDP o HTTP e di intraprendere un'azione, ad esempio il tentativo di usare un endpoint diverso.

Quando un codice di errore specifico dell'implementazione viene mappato a un errore canonico, il codice di errore originale viene salvato nell'oggetto errore ed è comunque possibile accedervi a scopo diagnostico. Per altre informazioni, vedere CODICE ERRORE ORIGINALE [**\_ PROPRIETÀ \_ \_ \_ \_ ERRORE WS.**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id)

## <a name="invalid-api-usage"></a>Utilizzo API non valido

I codici di errore seguenti sono riservati per l'utilizzo non valido dell'API e non verranno restituiti in altre circostanze. Se viene restituito uno di questi errori, potrebbe essere un'indicazione di un bug dell'applicazione.

-   **OPERAZIONE WS \_ E \_ NON \_ VALIDA**
-   **E \_ INVALIDARG**

Le enumerazioni seguenti fanno parte della traccia:

-   [**ID PROPRIETÀ ERRORE WS \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id)
-   [**CODICE DI \_ ECCEZIONE WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_exception_code)

I codici di errore seguenti fanno parte della traccia:

-   **CERT \_ E \_ CN \_ NO \_ MATCH**
-   **CERT \_ E \_ SCADUTO**
-   **CERT \_ E \_ UNTRUSTEDROOT**
-   **CERT \_ E \_ UTILIZZO \_ ERRATO**
-   **REVOCA \_ DI CRYPT E \_ \_ OFFLINE**
-   **E \_ INVALIDARG**
-   **E \_ OUTOFMEMORY**
-   **INDIRIZZO \_ WS E \_ \_ IN \_ USO**
-   **INDIRIZZO \_ WS E \_ \_ NON \_ DISPONIBILE**
-   **ACCESSO \_ ALL'ENDPOINT WS E \_ \_ \_ NEGATO**
-   **AZIONE \_ ENDPOINT WS E \_ \_ NON \_ \_ SUPPORTATA**
-   **ENDPOINT \_ WS E \_ \_ DISCONNESSO**
-   **ERRORE \_ DELL'ENDPOINT WS E \_ \_**
-   **ERRORE \_ DELL'ENDPOINT WS E \_ \_ \_ RICEVUTO**
-   **ENDPOINT \_ WS E \_ \_ NON \_ DISPONIBILE**
-   **ENDPOINT \_ WS E \_ \_ NON \_ TROVATO**
-   **ENDPOINT \_ WS E \_ \_ TROPPO \_ OCCUPATO**
-   **ENDPOINT \_ WS E \_ \_ NON RAGGIUNGIBILE**
-   **URL \_ DELL'ENDPOINT WS E \_ \_ NON \_ VALIDO**
-   **FORMATO WS \_ E \_ NON \_ VALIDO**
-   **OPERAZIONE WS \_ E \_ NON \_ VALIDA**
-   **WS \_ E \_ NON \_ SUPPORTATO**
-   **WS \_ E NESSUNA TRADUZIONE \_ \_ \_ DISPONIBILE**
-   **OVERFLOW \_ NUMERICO WS E \_ \_**
-   **ERRORE \_ DELL'OGGETTO WS E \_ \_**
-   **OPERAZIONE \_ WS E \_ \_ ABBANDONATA**
-   **OPERAZIONE \_ WS E \_ \_ INTERROTTA**
-   **TIMEOUT \_ DELL'OPERAZIONE WS E \_ \_ \_**
-   **WS \_ E \_ ALTRO**
-   **ACCESSO PROXY WS \_ E \_ \_ \_ NEGATO**
-   **ERRORE DEL PROXY WS \_ E \_ \_**
-   **IL PROXY WS \_ E \_ RICHIEDE \_ \_ \_ L'AUTENTICAZIONE DI BASE**
-   **IL PROXY WS \_ E \_ RICHIEDE \_ \_ \_ L'AUTENTICAZIONE DIGEST**
-   **IL PROXY WS \_ E \_ RICHIEDE \_ \_ \_ L'AUTENTICAZIONE NEGOZIATA**
-   **IL \_ PROXY WS E \_ \_ RICHIEDE \_ L'AUTENTICAZIONE \_ NTLM**
-   **QUOTA \_ WS E \_ \_ SUPERATA**
-   **ERRORE DEL \_ SISTEMA DI SICUREZZA WS E \_ \_ \_**
-   **TOKEN DI \_ SICUREZZA WS E \_ \_ \_ SCADUTO**
-   **ERRORE DI \_ VERIFICA DELLA SICUREZZA WS \_ \_ \_ E**
-   **IL SERVER WS \_ E \_ RICHIEDE \_ \_ \_ L'AUTENTICAZIONE DI BASE**
-   **IL SERVER WS \_ E \_ RICHIEDE \_ \_ \_ L'AUTENTICAZIONE DIGEST**
-   **IL SERVER WS \_ E \_ RICHIEDE \_ \_ \_ L'AUTENTICAZIONE NEGOZIATA**
-   **IL SERVER WS \_ E \_ RICHIEDE \_ \_ L'AUTENTICAZIONE \_ NTLM**
-   **WS \_ S \_ ASYNC**
-   **WS \_ S \_ END**

Le funzioni seguenti fanno parte della traccia:

-   [**ID PROPRIETÀ ERRORE WS \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_error_property_id)
-   [**CODICE DI \_ ECCEZIONE WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_exception_code)

L'handle seguente fa parte della traccia:

-   [ERRORE \_ WS](ws-error.md)

La struttura seguente fa parte della traccia:

-   [**PROPRIETÀ ERROR DI WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_error_property)

## <a name="security"></a>Sicurezza

Esistono alcune considerazioni sulla sicurezza di cui l'utente dell'oggetto errore deve essere a conoscenza:

-   L'oggetto errore può contenere dati non attendibili. Esempi di questo tipo sono: WS FAULT e le stringhe di errore, entrambe archiviate nell'oggetto errore in base alle informazioni ricevute su \_ un canale non attendibile. L'utente dell'oggetto errore deve prestare attenzione quando esamina le informazioni nell'oggetto errore e prendere decisioni in base ai relativi valori.
-   Un utente dell'oggetto errore deve [**chiamare WsResetError**](/windows/desktop/api/WebServices/nf-webservices-wsreseterror) dopo aver esaminato le informazioni sull'errore. La mancata riuscita di questa operazione può causare l'accumulo di memoria.
-   Un utente dell'oggetto errore deve prestare particolare attenzione quando usa il valore WS FULL FAULT DISCLOSURE dell'enumerazione \_ \_ \_ [**WS \_ FAULT \_ DISCLOSURE,**](/windows/desktop/api/WebServices/ne-webservices-ws_fault_disclosure) perché l'errore generato potrebbe contenere informazioni private accumulate nell'ambito del processo di registrazione degli errori.

 

 




