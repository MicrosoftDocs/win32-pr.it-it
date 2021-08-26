---
description: Se l'host generico e il client hanno esito positivo, ma l'host e il client effettivi hanno comunque esito negativo, è possibile che la richiesta di metadati non venga avviata. La registrazione WinHTTP può essere usata per verificare che i messaggi in uscita vengano generati e inviati correttamente.
ms.assetid: ab4568bd-fc05-4e2a-ac8c-f035e6583a36
title: Uso della registrazione WinHTTP per verificare il traffico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 031359dac8c8fa890568d6833cbfdf8c3d41d43bd52403a7def61a7392e8e23a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995221"
---
# <a name="using-winhttp-logging-to-verify-get-traffic"></a>Uso della registrazione WinHTTP per verificare il traffico

Se l'host generico e il client hanno esito positivo, ma l'host e il client effettivi hanno comunque esito negativo, è possibile che la richiesta di metadati non venga avviata. [La registrazione WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) può essere usata per verificare che i messaggi in uscita vengano generati e inviati correttamente.

Le applicazioni client basate su WSDAPI usano [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) per connettersi ai dispositivi. Gli host di dispositivi basati su WSDAPI non usano WinHTTP. Inoltre, alcuni proxy di terze parti non usano WinHTTP. Quando si esegue la risoluzione dei problemi di un host o di un proxy che non usa WinHTTP, ignorare questa procedura di diagnostica e continuare la risoluzione dei problemi seguendo le procedure descritte in [Inspecting Network Traces for HTTP Metadata Exchange](inspecting-network-traces-for-http-metadata-exchange.md).

[La registrazione WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) non mostra tutto il traffico a livello TCP. Passare a [Inspecting Network Traces for HTTP Metadata Exchange](inspecting-network-traces-for-http-metadata-exchange.md) se il traffico oltre al traffico HTTP è di interesse.

**Per usare la registrazione WinHTTP per verificare l'accesso al traffico**

1.  [Acquisire i log WinHTTP.](capturing-winhttp-logs.md)
2.  Avviare Blocco note o un altro editor di testo. L'editor di testo deve essere eseguito come amministratore.
3.  Aprire il file di log WinHTTP.
4.  Verificare che siano state inviate le richieste HTTP necessarie e i messaggi di metadati.

Se nei [log WinHTTP](get--metadata-exchange--http-request-and-message.md) viene trovato un messaggio Get per l'host, le richieste di metadati vengono inviate correttamente a WinHTTP. Continuare la risoluzione dei problemi seguendo le procedure descritte in [Inspecting Network Traces for HTTP Metadata Exchange](inspecting-network-traces-for-http-metadata-exchange.md).

Se non [è possibile](get--metadata-exchange--http-request-and-message.md) trovare un messaggio Get per l'host nei log WinHTTP, la richiesta di metadati non viene avviata. Ciò può verificarsi quando l'host pubblica XAddrs non validi. Verificare che XAddrs nell'host sia conforme alle regole di convalida [XAddr](xaddr-validation-rules.md).

## <a name="verifying-that-the-required-http-requests-and-metadata-messages-were-sent"></a>Verifica dell'invio delle richieste HTTP e dei messaggi di metadati necessari

Per lo scambio di metadati riuscito, è necessario che si verifichino gli eventi seguenti:

-   Il client WSDAPI genera una richiesta HTTP in uscita. Questa richiesta viene inviata all'host WSDAPI.
-   Il client invia un [messaggio Get](get--metadata-exchange--http-request-and-message.md) all'host.

Questi eventi vengono acquisiti nei log WinHTTP.

Il frammento di file di log WinHTTP seguente mostra una richiesta HTTP in uscita generata da un client WSDAPI.

``` syntax
16:51:47.893 ::*0000004* :: WinHttpSendRequest(0x36aae0, "", 0, 0x0, 0, 658, 0)
16:51:47.893 ::*0000004* :: WinHttpSendRequest() returning TRUE
16:51:47.897 ::*0000004* :: sending data:
16:51:47.897 ::*0000004* :: 226 (0xe2) bytes
16:51:47.897 ::*0000004* :: <<<<-------- HTTP stream follows below ----------------------------------------------->>>>
16:51:47.897 ::*0000004* :: POST /dbe17c74-3b21-4f52-addc-b84b444f73a0 HTTP/1.1
16:51:47.897 ::*0000004* :: Content-Type: application/soap+xml
16:51:47.897 ::*0000004* :: User-Agent: WSDAPI
16:51:47.897 ::*0000004* :: Host: 192.168.0.1:5357
16:51:47.897 ::*0000004* :: Content-Length: 658
16:51:47.897 ::*0000004* :: Connection: Keep-Alive
16:51:47.897 ::*0000004* :: Cache-Control: no-cache
16:51:47.897 ::*0000004* :: Pragma: no-cache
16:51:47.897 ::*0000004* :: 
16:51:47.897 ::*0000004* :: 
16:51:47.897 ::*0000004* :: <<<<-------- End ----------------------------------------------->>>>
```

Il frammento di file di log WinHTTP seguente mostra un [messaggio](get--metadata-exchange--http-request-and-message.md) Get. Questo messaggio deve seguire immediatamente la richiesta HTTP.

``` syntax
16:51:47.898 ::*0000004* :: WinHttpWriteData(0x36aae0, 0x11aa7c4, 658, 0x0)
16:51:47.899 ::*0000004* :: sending data:
16:51:47.899 ::*0000004* :: 658 (0x292) bytes
16:51:47.899 ::*0000004* :: <<<<-------- HTTP stream follows below ----------------------------------------------->>>>
16:51:47.899 ::*0000004* :: <?xml version="1.0" encoding="utf-8" ?>
16:51:47.899 ::*0000004* :: <soap:Envelope xmlns:soap="https://www.w3.org/2003/05/soap-envelope" xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing"><soap:Header><wsa:To>urn:uuid:dbe17c74-3b21-4f52-addc-b84b444f73a0</wsa:To><wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/Get</wsa:Action><wsa:MessageID>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:MessageID><wsa:ReplyTo><wsa:Address>https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous</wsa:Address></wsa:ReplyTo><wsa:From><wsa:Address>urn:uuid:b32467b5-e7ee-4ae3-8a8e-f5aa417c23b6</wsa:Address></wsa:From></soap:Header><soap:Body></soap:Body></soap:Envelope>
16:51:47.899 ::*0000004* :: <<<<-------- End ----------------------------------------------->>>>
16:51:47.899 ::*0000004* :: WinHttpWriteData() returning TRUE
```

**L'elemento Action** ( `<wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/Get</wsa:Action>` ) identifica il messaggio come [messaggio](get--metadata-exchange--http-request-and-message.md) Get. Verificare che il valore dell'elemento **To** (ad esempio, ) corrisponda all'ID dispositivo annunciato dall'host nei messaggi udp WS-Discovery `<wsa:To>urn:uuid:dbe17c74-3b21-4f52-addc-b84b444f73a0</wsa:To>` originali. L'ID dispositivo annunciato dall'host può essere controllato usando l'host di debug WSD. Per altre informazioni, vedere [Using a Generic Host and Client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).

Inoltre, la risposta dell'host alla richiesta di metadati è disponibile nei log WinHTTP del client. L'host genera [un messaggio GetResponse](getresponse--metadata-exchange--message.md) in risposta al messaggio [Get del](get--metadata-exchange--http-request-and-message.md) client.

Il frammento di file di log WinHTTP seguente mostra un messaggio [GetResponse](getresponse--metadata-exchange--message.md) in ingresso ricevuto da un client WSDAPI.

``` syntax
16:51:47.899 ::*0000004* :: WinHttpReceiveResponse(0x36aae0, 0x0)
16:51:47.899 ::*0000004* :: WinHttpReceiveResponse() returning TRUE
16:51:47.899 ::*Session* :: DllMain(0x73fc0000, DLL_THREAD_ATTACH, 0x0)
16:51:47.902 ::*0000004* :: received data:
16:51:47.902 ::*0000004* :: 1024 (0x400) bytes
16:51:47.902 ::*0000004* :: <<<<-------- HTTP stream follows below ----------------------------------------------->>>>
16:51:47.902 ::*0000004* :: HTTP/1.1 200 
16:51:47.902 ::*0000004* :: Content-Type: application/soap+xml
16:51:47.902 ::*0000004* :: Server: Microsoft-HTTPAPI/2.0
16:51:47.902 ::*0000004* :: Date: Fri, 15 Jun 2007 23:51:47 GMT
16:51:47.905 ::*0000004* :: Content-Length: 2228
16:51:47.905 ::*0000004* :: 
16:51:47.905 ::*0000004* :: <?xml version="1.0" encoding="utf-8" ?>
16:51:47.905 ::*0000004* :: <soap:Envelope xmlns:soap="https://www.w3.org/2003/05/soap-envelope" xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsx="https://schemas.xmlsoap.org/ws/2004/09/mex" xmlns:wsdp="https://schemas.xmlsoap.org/ws/2006/02/devprof" xmlns:un0="http://schemas.microsoft.com/windows/pnpx/2005/10" xmlns:pub="http://schemas.microsoft.com/windows/pub/2005/07"><soap:Header><wsa:To>https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous</wsa:To><wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/GetResponse</wsa:Action><wsa:MessageID>urn:uuid:2884cbcc-2848-4c35-9327-5ab5451a8729</wsa:MessageID><wsa:RelatesTo>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:RelatesTo></soap:Header><soap:Body><wsx:Metadata><wsx:MetadataSection Dialect="https://schemas.xmlsoap.org/ws/2006/02/devprof/ThisDevice"><wsdp:ThisDevice><wsd
16:51:47.905 ::*0000004* :: <<<<-------- End ----------------------------------------------->>>>
```

**L'elemento Action** ( `<wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/GetResponse</wsa:Action>` ) identifica il messaggio come messaggio [GetResponse.](getresponse--metadata-exchange--message.md) Verificare che il valore **dell'elemento RelatesTo** del messaggio GetResponse corrisponda al valore dell'elemento **MessageID** del [messaggio Get.](get--metadata-exchange--http-request-and-message.md) In questo esempio il valore dell'elemento **RelatesTo** ( ) corrisponde al valore `<wsa:RelatesTo>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:RelatesTo>` **dell'elemento MessageID** del messaggio Get ( `<wsa:MessageID>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:MessageID>` ).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[WinHTTP](/windows/desktop/WinHttp/winhttp-start-page)
</dt> <dt>

[Acquisizione di log WinHTTP](capturing-winhttp-logs.md)
</dt> <dt>

[Procedure di diagnostica WSDAPI](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Attività iniziali con la risoluzione dei problemi di WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 
