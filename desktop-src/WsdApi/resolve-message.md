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
# <a name="resolve-message"></a>Risolvi messaggio

Un messaggio di risoluzione è un messaggio WS-Discovery usato da un client per cercare i servizi in rete in base al nome. Un client invierà un messaggio di risoluzione solo quando verrà inviato un messaggio HTTP, ad esempio una richiesta [Get](get--metadata-exchange--http-request-and-message.md) Metadata Exchange o un messaggio di servizio. Per ulteriori informazioni sulla risoluzione dei messaggi, vedere la sezione 6,1 della [specifica WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf).

Un messaggio di risoluzione viene inviato dal multicast UDP alla porta 3702. I messaggi di risoluzione unicast non sono supportati.

I client DPWS inviano messaggi di risoluzione. Nell'elenco seguente sono illustrati gli scenari in cui WSDAPI invierà un messaggio di risoluzione.

-   Un client di individuazione della funzione Invia un messaggio di risoluzione se nessun XAddrs è incluso in un messaggio [ProbeMatches](probematches-message.md) .
-   Un client che chiama i metodi [**IWSDiscoveryProvider:: SearchById**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbyid) invierà un messaggio di risoluzione.
-   Un client che chiama [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) può inviare un messaggio di risoluzione se un indirizzo di dispositivo logico viene passato a *pszDeviceId*.
-   Un client che chiama [**WSDCreateDeviceProxyAdvanced**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxyadvanced) invierà un messaggio di risoluzione se la funzione viene chiamata con il parametro pDeviceAddress impostato su **null**.

> [!Note]  
> Questo argomento illustra un messaggio DPWS di esempio generato da client e host di WSDAPI. WSDAPI analizzerà e accetterà altri messaggi conformi a DPWS che non sono conformi a questo esempio. Non utilizzare questo esempio per verificare l'interoperabilità DPWS; usare invece lo [strumento di interoperabilità di base di WSDAPI (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx) .

 

Il messaggio SOAP seguente mostra un messaggio di risoluzione di esempio.

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

Un messaggio di risoluzione presenta i punti di interesse seguenti.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Punto di interesse</th>
<th>XML</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Risolvi</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Action>
    https://schemas.xmlsoap.org/ws/2005/04/discovery/Resolve
</wsa:Action></code></pre></td>
<td>L'azione Risolvi SOAP identifica il messaggio come un messaggio di risoluzione.</td>
</tr>
<tr class="even">
<td>MessageID</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:MessageID>
    urn:uuid:38d1c3d9-8d73-4424-8861-6b7ee2af24d3
</wsa:MessageID></code></pre></td>
<td>Contiene l'identificatore del messaggio a cui viene fatto riferimento in un messaggio <a href="resolvematches-message.md">ResolveMatches</a> .</td>
</tr>
<tr class="odd">
<td>Indirizzo</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Address>
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsa:Address></code></pre></td>
<td>Contiene l'indirizzo dell'endpoint che si sta risolvendo.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Messaggi di individuazione e scambio di metadati](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[Messaggio ResolveMatches](resolvematches-message.md)
</dt> </dl>

 

 



