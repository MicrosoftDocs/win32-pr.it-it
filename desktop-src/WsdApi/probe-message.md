---
description: Messaggio WS-Discovery utilizzato da un client per cercare i servizi in rete in base al tipo di servizio.
ms.assetid: a0ede1d9-2e13-4d5e-8ccd-9e0c0217cac7
title: Messaggio probe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abaf4b397abec699dd0a116fe5cddd97578543f917a7994287f5000e17079def
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130633"
---
# <a name="probe-message"></a>Messaggio probe

Un messaggio probe è un messaggio WS-Discovery usato da un client per cercare i servizi in rete in base al tipo di servizio. Per altre informazioni sui messaggi probe, vedere la sezione 5.2 della [specifica WS-Discovery.](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf)

Un messaggio probe viene inviato dal multicast UDP alla porta 3702. I messaggi probe unicast non sono supportati.

I client DPWS inviano messaggi probe. L'elenco seguente illustra gli scenari in cui WSDAPI invierà un messaggio probe.

-   I client di individuazione delle funzioni inviano messaggi probe.
-   I client WSDAPI che chiamano [**IWSDiscoveryProvider::SearchByAddress inviano**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbyaddress) messaggi Probe.
-   I client WSDAPI che chiamano [**IWSDiscoveryProvider::SearchByType**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbytype) inviano messaggi Probe.
-   Le applicazioni che usano l'individuazione diretta inviano messaggi Probe su HTTP o HTTPS.

> [!Note]  
> Questo argomento illustra un messaggio DPWS di esempio generato da client e host WSDAPI. WSDAPI analizza e accetta altri messaggi conformi a DPWS non conformi a questo esempio. Non usare questo esempio per verificare l'interoperabilità di DPWS. utilizzare [WSDAPI Basic Interoperability Tool (WSDBIT).](https://msdn.microsoft.com/library/cc264250.aspx)

 

Il messaggio SOAP seguente mostra un messaggio probe di esempio.

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope
    xmlns:soap="https://www.w3.org/2003/05/soap-envelope"
    xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing"
    xmlns:wsd="https://schemas.xmlsoap.org/ws/2005/04/discovery"
    xmlns:wsdp="https://schemas.xmlsoap.org/ws/2006/02/devprof">
<soap:Header>
    <wsa:To>
        urn:schemas-xmlsoap-org:ws:2005:04:discovery
    </wsa:To>
    <wsa:Action>
        https://schemas.xmlsoap.org/ws/2005/04/discovery/Probe
    </wsa:Action>
    <wsa:MessageID>
        urn:uuid:29cf10da-5c41-4d55-b184-5ee15e38ce23
    </wsa:MessageID>
</soap:Header>
<soap:Body>
    <wsd:Probe>
        <wsd:Types>wsdp:Device</wsd:Types>
    </wsd:Probe>
</soap:Body>
```

Un messaggio Probe ha i punti di interesse seguenti.



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
<td>Probe</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Action>
    https://schemas.xmlsoap.org/ws/2005/04/discovery/Probe
</wsa:Action></code></pre></td>
<td>L'azione SOAP Probe identifica il messaggio come messaggio probe.</td>
</tr>
<tr class="even">
<td>MessageID</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:MessageID>
    urn:uuid:29cf10da-5c41-4d55-b184-5ee15e38ce23
</wsa:MessageID></code></pre></td>
<td>Contiene l'identificatore del messaggio a cui fa riferimento l'elemento RelatesTo in <a href="probematches-message.md">un messaggio ProbeMatches.</a></td>
</tr>
<tr class="odd">
<td>Tipi</td>
<td><pre class="syntax" data-space="preserve"><code><wsd:Types>wsdp:Device</wsd:Types></code></pre></td>
<td>Contiene i WS-Discovery per cui il client esegue la ricerca. Questo elemento non deve essere vuoto.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Messaggi di individuazione e Exchange metadati](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[Messaggio ProbeMatches](probematches-message.md)
</dt> </dl>

 

 



