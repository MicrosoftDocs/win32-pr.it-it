---
description: Se l'host e il client generici hanno esito positivo, ma l'host e il client effettivi hanno ancora esito negativo, è possibile che la richiesta di metadati non venga avviata. È possibile utilizzare la registrazione WinHTTP per verificare che i messaggi in uscita vengano generati e inviati correttamente.
ms.assetid: ab4568bd-fc05-4e2a-ac8c-f035e6583a36
title: Uso della registrazione WinHTTP per verificare il traffico Get
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 448e4a127baf90a64291cbd14477c424270b332d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231664"
---
# <a name="using-winhttp-logging-to-verify-get-traffic"></a><span data-ttu-id="aa9c3-104">Uso della registrazione WinHTTP per verificare il traffico Get</span><span class="sxs-lookup"><span data-stu-id="aa9c3-104">Using WinHTTP Logging to Verify Get Traffic</span></span>

<span data-ttu-id="aa9c3-105">Se l'host e il client generici hanno esito positivo, ma l'host e il client effettivi hanno ancora esito negativo, è possibile che la richiesta di metadati non venga avviata.</span><span class="sxs-lookup"><span data-stu-id="aa9c3-105">If the generic host and client succeed but the actual host and client still fail, it is possible that the metadata request is not being initiated.</span></span> <span data-ttu-id="aa9c3-106">È possibile utilizzare la registrazione [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) per verificare che i messaggi in uscita vengano generati e inviati correttamente.</span><span class="sxs-lookup"><span data-stu-id="aa9c3-106">[WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) logging can be used to verify that outbound messages are being generated and sent correctly.</span></span>

<span data-ttu-id="aa9c3-107">Le applicazioni client basate su WSDAPI usano [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) per connettersi ai dispositivi.</span><span class="sxs-lookup"><span data-stu-id="aa9c3-107">WSDAPI-based client applications use [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) to connect to devices.</span></span> <span data-ttu-id="aa9c3-108">Gli host di dispositivi basati su WSDAPI non utilizzano WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="aa9c3-108">WSDAPI-based device hosts do not use WinHTTP.</span></span> <span data-ttu-id="aa9c3-109">Inoltre, alcuni proxy di terze parti non utilizzano WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="aa9c3-109">Also, some third-party proxies do not use WinHTTP.</span></span> <span data-ttu-id="aa9c3-110">Quando si risolvono i problemi relativi a un host o un proxy che non usa WinHTTP, ignorare questa procedura di diagnostica e continuare la risoluzione dei problemi seguendo le procedure descritte in [controllo delle tracce di rete per lo scambio di metadati http](inspecting-network-traces-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="aa9c3-110">When troubleshooting a host or proxy that does not use WinHTTP, skip this diagnostic procedure and continue troubleshooting by following the procedures in [Inspecting Network Traces for HTTP Metadata Exchange](inspecting-network-traces-for-http-metadata-exchange.md).</span></span>

<span data-ttu-id="aa9c3-111">La registrazione [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) non Mostra tutto il traffico a livello di TCP.</span><span class="sxs-lookup"><span data-stu-id="aa9c3-111">[WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) logging does not show all TCP-level traffic.</span></span> <span data-ttu-id="aa9c3-112">Passare a [esaminare le tracce di rete per lo scambio di metadati http](inspecting-network-traces-for-http-metadata-exchange.md) se il traffico oltre il traffico HTTP è di interesse.</span><span class="sxs-lookup"><span data-stu-id="aa9c3-112">Skip to [Inspecting Network Traces for HTTP Metadata Exchange](inspecting-network-traces-for-http-metadata-exchange.md) if traffic besides the HTTP traffic is of interest.</span></span>

<span data-ttu-id="aa9c3-113">**Per usare la registrazione WinHTTP per verificare il traffico Get**</span><span class="sxs-lookup"><span data-stu-id="aa9c3-113">**To use WinHTTP logging to verify Get traffic**</span></span>

1.  [<span data-ttu-id="aa9c3-114">Acquisire i log WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="aa9c3-114">Capture the WinHTTP logs.</span></span>](capturing-winhttp-logs.md)
2.  <span data-ttu-id="aa9c3-115">Avviare Blocco note o un altro editor di testo.</span><span class="sxs-lookup"><span data-stu-id="aa9c3-115">Start Notepad or another text editor.</span></span> <span data-ttu-id="aa9c3-116">L'editor di testo deve essere eseguito come amministratore.</span><span class="sxs-lookup"><span data-stu-id="aa9c3-116">The text editor must be run as Administrator.</span></span>
3.  <span data-ttu-id="aa9c3-117">Aprire il file di log WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="aa9c3-117">Open the WinHTTP log file.</span></span>
4.  <span data-ttu-id="aa9c3-118">Verificare che le richieste HTTP e i messaggi di metadati richiesti siano stati inviati.</span><span class="sxs-lookup"><span data-stu-id="aa9c3-118">Verify that the required HTTP requests and metadata messages were sent.</span></span>

<span data-ttu-id="aa9c3-119">Se viene trovato un messaggio [Get](get--metadata-exchange--http-request-and-message.md) per l'host nei log WinHTTP, le richieste di metadati vengono inviate a WinHTTP correttamente.</span><span class="sxs-lookup"><span data-stu-id="aa9c3-119">If a [Get](get--metadata-exchange--http-request-and-message.md) message for the host is found in the WinHTTP logs, then the metadata requests are being sent to WinHTTP successfully.</span></span> <span data-ttu-id="aa9c3-120">Continuare la risoluzione dei problemi seguendo le procedure descritte in [controllo delle tracce di rete per lo scambio di metadati http](inspecting-network-traces-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="aa9c3-120">Continue troubleshooting by following the procedures in [Inspecting Network Traces for HTTP Metadata Exchange](inspecting-network-traces-for-http-metadata-exchange.md).</span></span>

<span data-ttu-id="aa9c3-121">Se non è possibile trovare un messaggio [Get](get--metadata-exchange--http-request-and-message.md) per l'host nei log WinHTTP, la richiesta di metadati non viene avviata.</span><span class="sxs-lookup"><span data-stu-id="aa9c3-121">If a [Get](get--metadata-exchange--http-request-and-message.md) message cannot be found for the host in the WinHTTP logs, then the metadata request is not being initiated.</span></span> <span data-ttu-id="aa9c3-122">Questo problema può verificarsi quando l'host pubblica XAddrs non validi.</span><span class="sxs-lookup"><span data-stu-id="aa9c3-122">This can happen when the host publishes invalid XAddrs.</span></span> <span data-ttu-id="aa9c3-123">Verificare che XAddrs nell'host siano conformi alle [regole di convalida XAddr](xaddr-validation-rules.md).</span><span class="sxs-lookup"><span data-stu-id="aa9c3-123">Verify that the XAddrs on the host conform to the [XAddr validation rules](xaddr-validation-rules.md).</span></span>

## <a name="verifying-that-the-required-http-requests-and-metadata-messages-were-sent"></a><span data-ttu-id="aa9c3-124">Verifica dell'invio delle richieste HTTP e dei messaggi di metadati necessari</span><span class="sxs-lookup"><span data-stu-id="aa9c3-124">Verifying that the required HTTP requests and metadata messages were sent</span></span>

<span data-ttu-id="aa9c3-125">Per lo scambio di metadati riuscito devono verificarsi gli eventi seguenti:</span><span class="sxs-lookup"><span data-stu-id="aa9c3-125">The following events must occur for successful metadata exchange:</span></span>

-   <span data-ttu-id="aa9c3-126">Il client WSDAPI genera una richiesta HTTP in uscita.</span><span class="sxs-lookup"><span data-stu-id="aa9c3-126">The WSDAPI client generates an outbound HTTP request.</span></span> <span data-ttu-id="aa9c3-127">Questa richiesta viene inviata all'host WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="aa9c3-127">This request is sent to the WSDAPI host.</span></span>
-   <span data-ttu-id="aa9c3-128">Il client invia un messaggio [Get](get--metadata-exchange--http-request-and-message.md) all'host.</span><span class="sxs-lookup"><span data-stu-id="aa9c3-128">The client sends a [Get](get--metadata-exchange--http-request-and-message.md) message to the host.</span></span>

<span data-ttu-id="aa9c3-129">Questi eventi vengono acquisiti nei log WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="aa9c3-129">These events are captured in the WinHTTP logs.</span></span>

<span data-ttu-id="aa9c3-130">Il frammento di file di log WinHTTP seguente mostra una richiesta HTTP in uscita generata da un client WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="aa9c3-130">The following WinHTTP log file snippet shows an outbound HTTP request generated by a WSDAPI client.</span></span>

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

<span data-ttu-id="aa9c3-131">Il frammento di file di log WinHTTP seguente mostra un messaggio [Get](get--metadata-exchange--http-request-and-message.md) .</span><span class="sxs-lookup"><span data-stu-id="aa9c3-131">The following WinHTTP log file snippet shows a [Get](get--metadata-exchange--http-request-and-message.md) message.</span></span> <span data-ttu-id="aa9c3-132">Questo messaggio deve seguire immediatamente la richiesta HTTP.</span><span class="sxs-lookup"><span data-stu-id="aa9c3-132">This message should immediately follow the HTTP request.</span></span>

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

<span data-ttu-id="aa9c3-133">L'elemento **Action** ( `<wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/Get</wsa:Action>` ) identifica il messaggio come messaggio [Get](get--metadata-exchange--http-request-and-message.md) .</span><span class="sxs-lookup"><span data-stu-id="aa9c3-133">The **Action** element (`<wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/Get</wsa:Action>`) identifies the message as a [Get](get--metadata-exchange--http-request-and-message.md) message.</span></span> <span data-ttu-id="aa9c3-134">Verificare che il valore dell'elemento **a** (ad esempio, `<wsa:To>urn:uuid:dbe17c74-3b21-4f52-addc-b84b444f73a0</wsa:To>` ) corrisponda all'ID dispositivo annunciato dall'host nei messaggi di WS-Discovery UDP originali.</span><span class="sxs-lookup"><span data-stu-id="aa9c3-134">Verify that the value of the **To** element (for example, `<wsa:To>urn:uuid:dbe17c74-3b21-4f52-addc-b84b444f73a0</wsa:To>`) matches the device ID advertised by the host in the original UDP WS-Discovery messages.</span></span> <span data-ttu-id="aa9c3-135">L'ID dispositivo annunciato dall'host può essere controllato usando l'host di debug WSD.</span><span class="sxs-lookup"><span data-stu-id="aa9c3-135">The device ID advertised by the host can be checked by using the WSD Debug Host.</span></span> <span data-ttu-id="aa9c3-136">Per ulteriori informazioni, vedere [utilizzo di un host e un client generici per UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="aa9c3-136">For more information, see [Using a Generic Host and Client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span></span>

<span data-ttu-id="aa9c3-137">Inoltre, è possibile trovare la risposta dell'host alla richiesta di metadati nei log WinHTTP del client.</span><span class="sxs-lookup"><span data-stu-id="aa9c3-137">In addition, the host's response to the metadata request can be found in the client's WinHTTP logs.</span></span> <span data-ttu-id="aa9c3-138">L'host genera un messaggio [GetResponse](getresponse--metadata-exchange--message.md) in risposta al messaggio [Get](get--metadata-exchange--http-request-and-message.md) del client.</span><span class="sxs-lookup"><span data-stu-id="aa9c3-138">The host generates a [GetResponse](getresponse--metadata-exchange--message.md) message in response to the client's [Get](get--metadata-exchange--http-request-and-message.md) message.</span></span>

<span data-ttu-id="aa9c3-139">Il frammento di file di log WinHTTP seguente mostra un messaggio [GetResponse](getresponse--metadata-exchange--message.md) in ingresso ricevuto da un client wsdapi.</span><span class="sxs-lookup"><span data-stu-id="aa9c3-139">The following WinHTTP log file snippet shows an inbound [GetResponse](getresponse--metadata-exchange--message.md) message received by a WSDAPI client.</span></span>

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

<span data-ttu-id="aa9c3-140">L'elemento **Action** ( `<wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/GetResponse</wsa:Action>` ) identifica il messaggio come messaggio [GetResponse](getresponse--metadata-exchange--message.md) .</span><span class="sxs-lookup"><span data-stu-id="aa9c3-140">The **Action** element (`<wsa:Action>https://schemas.xmlsoap.org/ws/2004/09/transfer/GetResponse</wsa:Action>`) identifies the message as a [GetResponse](getresponse--metadata-exchange--message.md) message.</span></span> <span data-ttu-id="aa9c3-141">Verificare che il valore dell'elemento **Repiù recente** del messaggio GetResponse corrisponda al valore dell'elemento **MessageID** del messaggio [Get](get--metadata-exchange--http-request-and-message.md) .</span><span class="sxs-lookup"><span data-stu-id="aa9c3-141">Verify that the value of the **RelatesTo** element of the GetResponse message matches the value of the **MessageID** element of the [Get](get--metadata-exchange--http-request-and-message.md) message.</span></span> <span data-ttu-id="aa9c3-142">In questo esempio, il valore dell'elemento **Repiù recente** ( `<wsa:RelatesTo>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:RelatesTo>` ) corrisponde al valore dell'elemento **MessageID** del messaggio Get ( `<wsa:MessageID>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:MessageID>` ).</span><span class="sxs-lookup"><span data-stu-id="aa9c3-142">In this example, the value of the **RelatesTo** element (`<wsa:RelatesTo>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:RelatesTo>`) matches the value of the **MessageID** element of the Get message (`<wsa:MessageID>urn:uuid:8506ac50-3646-4621-9680-86f484d87909</wsa:MessageID>`).</span></span>

## <a name="related-topics"></a><span data-ttu-id="aa9c3-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="aa9c3-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa9c3-144">WinHTTP</span><span class="sxs-lookup"><span data-stu-id="aa9c3-144">WinHTTP</span></span>](/windows/desktop/WinHttp/winhttp-start-page)
</dt> <dt>

[<span data-ttu-id="aa9c3-145">Acquisizione dei log WinHTTP</span><span class="sxs-lookup"><span data-stu-id="aa9c3-145">Capturing WinHTTP Logs</span></span>](capturing-winhttp-logs.md)
</dt> <dt>

[<span data-ttu-id="aa9c3-146">Procedure di diagnostica WSDAPI</span><span class="sxs-lookup"><span data-stu-id="aa9c3-146">WSDAPI Diagnostic Procedures</span></span>](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[<span data-ttu-id="aa9c3-147">Introduzione con la risoluzione dei problemi di WSDAPI</span><span class="sxs-lookup"><span data-stu-id="aa9c3-147">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 
