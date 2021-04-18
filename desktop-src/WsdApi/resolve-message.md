---
description: Messaggio WS-Discovery utilizzato da un client per la ricerca di servizi sulla rete in base al nome.
ms.assetid: b963bd2a-47cb-4f8d-8272-a586e6d6a047
title: Risolvi messaggio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3390d97aad972f001b98587c6b5e7cd7ac708b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310272"
---
# <a name="resolve-message"></a><span data-ttu-id="ff820-103">Risolvi messaggio</span><span class="sxs-lookup"><span data-stu-id="ff820-103">Resolve Message</span></span>

<span data-ttu-id="ff820-104">Un messaggio di risoluzione è un messaggio WS-Discovery usato da un client per cercare i servizi in rete in base al nome.</span><span class="sxs-lookup"><span data-stu-id="ff820-104">A Resolve message is a WS-Discovery message used by a client to search for services on the network by name.</span></span> <span data-ttu-id="ff820-105">Un client invierà un messaggio di risoluzione solo quando verrà inviato un messaggio HTTP, ad esempio una richiesta [Get](get--metadata-exchange--http-request-and-message.md) Metadata Exchange o un messaggio di servizio.</span><span class="sxs-lookup"><span data-stu-id="ff820-105">A client will only send a Resolve message when an HTTP message (such as a [Get](get--metadata-exchange--http-request-and-message.md) metadata exchange request or a service message) will be sent.</span></span> <span data-ttu-id="ff820-106">Per ulteriori informazioni sulla risoluzione dei messaggi, vedere la sezione 6,1 della [specifica WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf).</span><span class="sxs-lookup"><span data-stu-id="ff820-106">For more information about Resolve messages, see section 6.1 of the [WS-Discovery Specification](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf).</span></span>

<span data-ttu-id="ff820-107">Un messaggio di risoluzione viene inviato dal multicast UDP alla porta 3702.</span><span class="sxs-lookup"><span data-stu-id="ff820-107">A Resolve message is sent by UDP multicast to port 3702.</span></span> <span data-ttu-id="ff820-108">I messaggi di risoluzione unicast non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="ff820-108">Unicast Resolve messages are not supported.</span></span>

<span data-ttu-id="ff820-109">I client DPWS inviano messaggi di risoluzione.</span><span class="sxs-lookup"><span data-stu-id="ff820-109">DPWS clients send Resolve messages.</span></span> <span data-ttu-id="ff820-110">Nell'elenco seguente sono illustrati gli scenari in cui WSDAPI invierà un messaggio di risoluzione.</span><span class="sxs-lookup"><span data-stu-id="ff820-110">The following list shows scenarios in which WSDAPI will send a Resolve message.</span></span>

-   <span data-ttu-id="ff820-111">Un client di individuazione della funzione Invia un messaggio di risoluzione se nessun XAddrs è incluso in un messaggio [ProbeMatches](probematches-message.md) .</span><span class="sxs-lookup"><span data-stu-id="ff820-111">A Function Discovery client sends a Resolve message if no XAddrs are included in a [ProbeMatches](probematches-message.md) message.</span></span>
-   <span data-ttu-id="ff820-112">Un client che chiama i metodi [**IWSDiscoveryProvider:: SearchById**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbyid) invierà un messaggio di risoluzione.</span><span class="sxs-lookup"><span data-stu-id="ff820-112">A client calling the [**IWSDiscoveryProvider::SearchById**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbyid) methods will send a Resolve message.</span></span>
-   <span data-ttu-id="ff820-113">Un client che chiama [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) può inviare un messaggio di risoluzione se un indirizzo di dispositivo logico viene passato a *pszDeviceId*.</span><span class="sxs-lookup"><span data-stu-id="ff820-113">A client calling [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) may send a Resolve message if a logical device address is passed to *pszDeviceId*.</span></span>
-   <span data-ttu-id="ff820-114">Un client che chiama [**WSDCreateDeviceProxyAdvanced**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxyadvanced) invierà un messaggio di risoluzione se la funzione viene chiamata con il parametro pDeviceAddress impostato su **null**.</span><span class="sxs-lookup"><span data-stu-id="ff820-114">A client calling [**WSDCreateDeviceProxyAdvanced**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxyadvanced) will send a Resolve message if the function is called with the pDeviceAddress parameter set to **NULL**.</span></span>

> [!Note]  
> <span data-ttu-id="ff820-115">Questo argomento illustra un messaggio DPWS di esempio generato da client e host di WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="ff820-115">This topic shows a sample DPWS message generated by WSDAPI clients and hosts.</span></span> <span data-ttu-id="ff820-116">WSDAPI analizzerà e accetterà altri messaggi conformi a DPWS che non sono conformi a questo esempio.</span><span class="sxs-lookup"><span data-stu-id="ff820-116">WSDAPI will parse and accept other DPWS-compliant messages that do not conform to this sample.</span></span> <span data-ttu-id="ff820-117">Non utilizzare questo esempio per verificare l'interoperabilità DPWS; usare invece lo [strumento di interoperabilità di base di WSDAPI (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx) .</span><span class="sxs-lookup"><span data-stu-id="ff820-117">Do not use this sample to verify DPWS interoperability; use the [WSDAPI Basic Interoperability Tool (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx) instead.</span></span>

 

<span data-ttu-id="ff820-118">Il messaggio SOAP seguente mostra un messaggio di risoluzione di esempio.</span><span class="sxs-lookup"><span data-stu-id="ff820-118">The following SOAP message shows a sample Resolve message.</span></span>

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope
    xmlns:soap="https://www.w3.org/2003/05/soap-envelope"
    xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing"
    xmlns:wsd="https://schemas.xmlsoap.org/ws/2005/04/discovery">
<soap:Header>
    <wsa:To>
urn:schemas-xmlsoap-org:ws:2005:04:discovery
</wsa:To>
    <wsa:Action>
        https://schemas.xmlsoap.org/ws/2005/04/discovery/Resolve
    </wsa:Action>
    <wsa:MessageID>
        urn:uuid:38d1c3d9-8d73-4424-8861-6b7ee2af24d3
    </wsa:MessageID>
</soap:Header>
<soap:Body>
    <wsd:Resolve>
        <wsa:EndpointReference>
            <wsa:Address>
                urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
            </wsa:Address>
        </wsa:EndpointReference>
    </wsd:Resolve>
</soap:Body>
</soap:Envelope>
```

<span data-ttu-id="ff820-119">Un messaggio di risoluzione presenta i punti di interesse seguenti.</span><span class="sxs-lookup"><span data-stu-id="ff820-119">A Resolve message has the following focus points.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ff820-120">Punto di interesse</span><span class="sxs-lookup"><span data-stu-id="ff820-120">Focus point</span></span></th>
<th><span data-ttu-id="ff820-121">XML</span><span class="sxs-lookup"><span data-stu-id="ff820-121">XML</span></span></th>
<th><span data-ttu-id="ff820-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ff820-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ff820-123">Risolvi</span><span class="sxs-lookup"><span data-stu-id="ff820-123">Resolve</span></span></td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Action>
    https://schemas.xmlsoap.org/ws/2005/04/discovery/Resolve
</wsa:Action></code></pre></td>
<td><span data-ttu-id="ff820-124">L'azione Risolvi SOAP identifica il messaggio come un messaggio di risoluzione.</span><span class="sxs-lookup"><span data-stu-id="ff820-124">The Resolve SOAP action identifies the message as a Resolve message.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ff820-125">MessageID</span><span class="sxs-lookup"><span data-stu-id="ff820-125">MessageID</span></span></td>
<td><pre class="syntax" data-space="preserve"><code><wsa:MessageID>
    urn:uuid:38d1c3d9-8d73-4424-8861-6b7ee2af24d3
</wsa:MessageID></code></pre></td>
<td><span data-ttu-id="ff820-126">Contiene l'identificatore del messaggio a cui viene fatto riferimento in un messaggio <a href="resolvematches-message.md">ResolveMatches</a> .</span><span class="sxs-lookup"><span data-stu-id="ff820-126">Contains the message identifier, which is referenced in a <a href="resolvematches-message.md">ResolveMatches</a> message.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ff820-127">Indirizzo</span><span class="sxs-lookup"><span data-stu-id="ff820-127">Address</span></span></td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Address>
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsa:Address></code></pre></td>
<td><span data-ttu-id="ff820-128">Contiene l'indirizzo dell'endpoint che si sta risolvendo.</span><span class="sxs-lookup"><span data-stu-id="ff820-128">Contains the address of the endpoint being resolved.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="ff820-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ff820-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff820-130">Messaggi di individuazione e scambio di metadati</span><span class="sxs-lookup"><span data-stu-id="ff820-130">Discovery and Metadata Exchange Messages</span></span>](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[<span data-ttu-id="ff820-131">Messaggio ResolveMatches</span><span class="sxs-lookup"><span data-stu-id="ff820-131">ResolveMatches Message</span></span>](resolvematches-message.md)
</dt> </dl>

 

 



