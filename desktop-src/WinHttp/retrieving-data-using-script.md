---
description: Questo argomento include un esempio di come scrivere uno script che ottiene i dati tramite i servizi HTTP di Microsoft Windows (WinHTTP) in modo sincrono o asincrono.
ms.assetid: 84b847f8-4d9e-4fea-9e87-df4c65b54a02
title: Recupero di dati tramite script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 734516cf75f92cc43ab4cb15f22bd97aa803ec33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966421"
---
# <a name="retrieving-data-using-script"></a>Recupero di dati tramite script

Questo argomento include un esempio di come scrivere uno script che ottiene i dati tramite i servizi HTTP di Microsoft Windows (WinHTTP) in modo sincrono o asincrono. I concetti illustrati in questo esempio rappresentano la base per la scrittura di applicazioni server client o di livello intermedio che richiedono l'accesso ai dati tramite il protocollo HTTP.

-   [Prerequisiti e requisiti](#prerequisites-and-requirements)
-   [Recupero dei dati in modo sincrono](#retrieving-data-synchronously)
-   [Recupero dei dati in modo asincrono](#retrieving-data-asynchronously)
-   [Argomenti correlati](#related-topics)

## <a name="prerequisites-and-requirements"></a>Prerequisiti e requisiti

Oltre a una conoscenza approfondita di Microsoft JScript, questo esempio richiede quanto segue:

-   Versione corrente del Software Development Kit (SDK) di Microsoft Windows.
-   Lo strumento di configurazione proxy per stabilire le impostazioni proxy per i servizi HTTP di Microsoft Windows (WinHTTP), se la connessione a Internet avviene tramite un server proxy. Per ulteriori informazioni, vedere [ProxyCfg.exe, uno strumento di configurazione proxy](proxycfg-exe--a-proxy-configuration-tool.md).
-   Una certa familiarità con i concetti e la [terminologia di rete](network-terminology.md) .

## <a name="retrieving-data-synchronously"></a>Recupero dei dati in modo sincrono

**Per creare uno script che ottenga il testo da una pagina Web in modo sincrono, eseguire le operazioni seguenti:**

1.  Aprire un editor di testo.
2.  Copiare il codice seguente nell'editor di testo.

    ```JScript
    function getText(strURL)
    {
        var strResult;
        
        try
        {
            // Create the WinHTTPRequest ActiveX Object.
            var WinHttpReq = new ActiveXObject(
                                      "WinHttp.WinHttpRequest.5.1");
            
            //  Create an HTTP request.
            var temp = WinHttpReq.Open("GET", strURL, false);

            //  Send the HTTP request.
            WinHttpReq.Send();
            
            //  Retrieve the response text.
            strResult = WinHttpReq.ResponseText;
        }
        catch (objError)
        {
            strResult = objError + "\n"
            strResult += "WinHTTP returned error: " + 
                (objError.number & 0xFFFF).toString() + "\n\n";
            strResult += objError.description;
        }
        
        //  Return the response text.
        return strResult;
    }

    WScript.Echo(getText("https://www.microsoft.com/default.htm"));
    ```

    

3.  Salvare il file con il nome "Retrieve.js".
4.  Al prompt dei comandi digitare "cscript Retrieve.js" e premere INVIO.

A questo punto si dispone di uno script che usa un oggetto [**WinHttpRequest**](winhttprequest.md) per ottenere il codice sorgente HTML per la pagina Web in https://www.microsoft.com . Potrebbe essere necessario attendere alcuni secondi prima che il codice venga visualizzato.

L'applicazione contiene una sola funzione, "gettext". La prima riga dello script crea l'oggetto [**WinHttpRequest**](winhttprequest.md) .


```JScript
    // Create the WinHTTPRequest ActiveX Object.
    var WinHttpReq = new ActiveXObject("WinHttp.WinHttpRequest.5.1");
```



Quando il motore JScript rileva questa riga, crea un'istanza di questo oggetto. Se viene visualizzato il messaggio di errore "componente ActiveX non è in grado di creare l'oggetto", in questa riga, probabilmente il WinHttp.dll non è stato registrato correttamente o non è presente nel sistema.

La riga successiva dello script chiama il metodo [**Open**](iwinhttprequest-open.md) .


```JScript
    //  Create an HTTP request.
    WinHttpReq.Open("GET", "https://www.microsoft.com", false);
```



Tre parametri specificano il [*verbo http*](glossary.md) da usare, il nome della risorsa e se usare WinHTTP in modo sincrono o asincrono. In questo esempio, il metodo usa il *verbo http*"Get" per ottenere i dati da https://www.microsoft.com . Se si specifica **false** per l'ultimo parametro, viene determinato che la transazione viene eseguita in modo sincrono. Il metodo [**Open**](iwinhttprequest-open.md) non stabilisce una connessione alla risorsa come potrebbe implicare il nome. Ma Inizializza le strutture di dati interne che conservano le informazioni sulla sessione, sulla connessione e sulla richiesta.

Il metodo [**Send**](iwinhttprequest-send.md) assembla le intestazioni della richiesta e Invia la richiesta. Quando viene chiamato in modalità sincrona, il metodo [**Send**](iwinhttprequest-send.md) attende anche una risposta prima di consentire all'applicazione di continuare.


```JScript
    // Send the HTTP request.
    WinHttpReq.Send();
```



Dopo l'invio della richiesta, lo script restituisce il valore della proprietà [**ResponseText**](iwinhttprequest-responsetext.md) dell'oggetto [**WinHttpRequest**](winhttprequest.md) . Questa proprietà contiene il corpo dell'entità della risposta, in questo caso, l'origine di un documento.


```JScript
    // Get the response text.
    return WinHttpReq.ResponseText;
```



L'esecuzione dello script viene sospesa mentre viene recuperato l'intero testo della risorsa. Il testo della risorsa viene restituito dalla funzione e visualizzato.

L'oggetto [**WinHttpRequest**](winhttprequest.md) garantisce che tutte le risorse interne allocate per la transazione HTTP vengano rilasciate.

## <a name="retrieving-data-asynchronously"></a>Recupero dei dati in modo asincrono

Il recupero dei dati in modo asincrono tramite WinHTTP è molto simile al recupero sincrono dei dati. Modificare lo script della sezione precedente facendo due piccole modifiche.

1.  Impostare il terzo parametro del metodo [**Open**](iwinhttprequest-open.md) su "true" invece di "false" per specificare che i metodi WinHTTP devono essere eseguiti in modo asincrono.
    ```JScript
       //  Create a HTTP request.
        var temp = WinHttpReq.Open("GET", strURL, true);
    ```

    

2.  Richiamare il metodo [**waitForResponse**](iwinhttprequest-waitforresponse.md) prima di accedere alla proprietà [**ResponseText**](iwinhttprequest-responsetext.md) per assicurarsi che sia stata ricevuta l'intera risposta.
    ```JScript
        //  Send the HTTP request.
        WinHttpReq.Send();
            
        // Wait for the entire response.
        WinHttpReq.WaitForResponse();
            
        //  Retrieve the response text.
        strResult = WinHttpReq.ResponseText;
    ```

    

Il vantaggio principale dell'uso di WinHTTP in modo asincrono nello script è che il metodo [**Send**](iwinhttprequest-send.md) restituisce immediatamente un risultato. La richiesta viene preparata e inviata da un thread di lavoro. Ciò consente all'applicazione di eseguire altre operazioni mentre è in attesa della risposta. Prima di tentare di accedere alla risposta, verificare che l'intera risposta sia stata ricevuta chiamando il metodo [**waitForResponse**](iwinhttprequest-waitforresponse.md) . In caso contrario, può verificarsi un errore.

Il metodo [**waitForResponse**](iwinhttprequest-waitforresponse.md) può essere utilizzato anche per specificare un valore di timeout per la transazione. Un parametro facoltativo consente di specificare il valore di timeout in secondi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**WinHttpRequest**](winhttprequest.md)
</dt> <dt>

[Richiesta di commenti HTTP/1.1 (RFC 2616)](https://www.ietf.org/rfc/rfc2616.txt)
</dt> </dl>

 

 



