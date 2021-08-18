---
description: Messaggio WS-Discovery usato da un client per cercare i servizi nella rete in base al nome.
ms.assetid: b963bd2a-47cb-4f8d-8272-a586e6d6a047
title: Risolvere il messaggio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54887db566ee428e6bfe9ec2de9016a637884b092611a85e607c55aaa4176abc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991611"
---
# <a name="resolve-message"></a>Risolvere il messaggio

Un messaggio di risoluzione è WS-Discovery usato da un client per cercare i servizi in rete in base al nome. Un client invierà un messaggio Resolve solo quando verrà inviato un messaggio HTTP, ad esempio una richiesta [get](get--metadata-exchange--http-request-and-message.md) metadata exchange o un messaggio di servizio. Per altre informazioni sulla risoluzione dei messaggi, vedere la sezione 6.1 della [specifica WS-Discovery.](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf)

Un messaggio di risoluzione viene inviato dal multicast UDP alla porta 3702. I messaggi Unicast Resolve non sono supportati.

I client DPWS inviano messaggi Resolve. L'elenco seguente illustra gli scenari in cui WSDAPI invierà un messaggio resolve.

-   Un client di individuazione delle funzioni invia un messaggio di risoluzione se non sono inclusi XAddrs in [un messaggio ProbeMatches.](probematches-message.md)
-   Un client che chiama [**i metodi IWSDiscoveryProvider::SearchById**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbyid) invierà un messaggio Resolve.
-   Un client che chiama [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) può inviare un messaggio Resolve se un indirizzo di dispositivo logico viene passato a *pszDeviceId*.
-   Un client che chiama [**WSDCreateDeviceProxyAdvanced**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxyadvanced) invierà un messaggio Resolve se la funzione viene chiamata con il parametro pDeviceAddress impostato su **NULL.**

> [!Note]  
> Questo argomento illustra un messaggio DPWS di esempio generato da client e host WSDAPI. WSDAPI anaserà e accetterà altri messaggi conformi a DPWS che non sono conformi a questo esempio. Non usare questo esempio per verificare l'interoperabilità DPWS. usare [WSDAPI Basic Interoperability Tool (WSDBIT).](https://msdn.microsoft.com/library/cc264250.aspx)

 

Il messaggio SOAP seguente mostra un messaggio resolve di esempio.

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

Un messaggio Risolvi presenta i punti di interesse seguenti.



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
<td>L'azione Risolvi SOAP identifica il messaggio come messaggio di risoluzione.</td>
</tr>
<tr class="even">
<td>MessageID</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:MessageID>
    urn:uuid:38d1c3d9-8d73-4424-8861-6b7ee2af24d3
</wsa:MessageID></code></pre></td>
<td>Contiene l'identificatore del messaggio a cui viene fatto riferimento in <a href="resolvematches-message.md">un messaggio ResolveMatches.</a></td>
</tr>
<tr class="odd">
<td>Indirizzo</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Address>
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsa:Address></code></pre></td>
<td>Contiene l'indirizzo dell'endpoint da risolvere.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Messaggi di individuazione e Exchange metadati](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[Messaggio ResolveMatches](resolvematches-message.md)
</dt> </dl>

 

 



