---
description: Messaggio WS-Discovery utilizzato da un client per la ricerca di servizi nella rete in base al tipo di servizio.
ms.assetid: a0ede1d9-2e13-4d5e-8ccd-9e0c0217cac7
title: Messaggio Probe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 913c163be8d82297a642b1a97a7d28e0c403ca08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131135"
---
# <a name="probe-message"></a>Messaggio Probe

Un messaggio Probe è un messaggio WS-Discovery usato da un client per cercare i servizi nella rete in base al tipo di servizio. Per ulteriori informazioni sui messaggi Probe, vedere la sezione 5,2 della [specifica WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf).

Un messaggio Probe viene inviato dal multicast UDP alla porta 3702. I messaggi Probe unicast non sono supportati.

I client DPWS inviano messaggi Probe. Nell'elenco seguente sono illustrati gli scenari in cui WSDAPI invierà un messaggio Probe.

-   I client di individuazione funzione inviano messaggi Probe.
-   I client WSDAPI che chiamano [**IWSDiscoveryProvider:: SearchByAddress**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbyaddress) inviano messaggi di probe.
-   I client WSDAPI che chiamano [**IWSDiscoveryProvider:: SearchByType**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbytype) inviano messaggi di probe.
-   Le applicazioni che usano l'individuazione diretta inviano messaggi Probe tramite HTTP o HTTPS.

> [!Note]  
> Questo argomento illustra un messaggio DPWS di esempio generato da client e host di WSDAPI. WSDAPI analizzerà e accetterà altri messaggi conformi a DPWS che non sono conformi a questo esempio. Non utilizzare questo esempio per verificare l'interoperabilità DPWS; usare invece lo [strumento di interoperabilità di base di WSDAPI (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx) .

 

Il messaggio SOAP seguente mostra un messaggio Probe di esempio.

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

Un messaggio Probe presenta i punti di interesse seguenti.



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
<td>L'azione SOAP Probe identifica il messaggio come messaggio Probe.</td>
</tr>
<tr class="even">
<td>MessageID</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:MessageID>
    urn:uuid:29cf10da-5c41-4d55-b184-5ee15e38ce23
</wsa:MessageID></code></pre></td>
<td>Contiene l'identificatore del messaggio, a cui fa riferimento l'elemento latest in un messaggio <a href="probematches-message.md">ProbeMatches</a> .</td>
</tr>
<tr class="odd">
<td>Tipi</td>
<td><pre class="syntax" data-space="preserve"><code><wsd:Types>wsdp:Device</wsd:Types></code></pre></td>
<td>Contiene i tipi di WS-Discovery per i quali il client esegue la ricerca. Questo elemento non deve essere vuoto.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Messaggi di individuazione e scambio di metadati](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[Messaggio ProbeMatches](probematches-message.md)
</dt> </dl>

 

 



