---
description: Messaggio WS-Discovery inviato da un servizio in risposta a un messaggio probe del client.
ms.assetid: 58d3d016-ae29-4090-9b88-e1125db59c95
title: Messaggio ProbeMatches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 813549091edc6cbb1202d746c7a7f62ecf3e03b5
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882002"
---
# <a name="probematches-message"></a>Messaggio ProbeMatches

Un messaggio ProbeMatches è un WS-Discovery inviato da un servizio in risposta al messaggio Probe di [un](probe-message.md) client. Per altre informazioni sui messaggi ProbeMatches, vedere la sezione 5.3 della [specifica WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf).

Un messaggio ProbeMatches viene inviato dall'unicast UDP alla porta da cui è stato inviato il messaggio [Probe](probe-message.md) del client. ProbeMatches deve essere inviato entro 4 secondi dal messaggio probe. in caso contrario, Windows firewall potrebbe eliminare il pacchetto.

Se non sono inclusi XAddr nel messaggio ProbeMatches, il client può inviare un messaggio [Resolve](resolve-message.md) tramite multicast UDP alla porta 3702. Il client invierà un messaggio Resolve solo quando verrà inviato un messaggio HTTP, ad esempio una richiesta [get](get--metadata-exchange--http-request-and-message.md) metadata exchange o un messaggio del servizio.

Qualsiasi applicazione DPWS che invia messaggi [Probe](probe-message.md) riceverà messaggi ProbeMatches.

> [!Note]  
> Questo argomento illustra un messaggio DPWS di esempio generato da client e host WSDAPI. WSDAPI analizza e accetta altri messaggi conformi a DPWS non conformi a questo esempio. Non usare questo esempio per verificare l'interoperabilità di DPWS. utilizzare [WSDAPI Basic Interoperability Tool (WSDBIT).](https://msdn.microsoft.com/library/cc264250.aspx)

 

Il messaggio SOAP seguente mostra un messaggio ProbeMatches di esempio.

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope
    xmlns:soap="https://www.w3.org/2003/05/soap-envelope"
    xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing"
    xmlns:wsd="https://schemas.xmlsoap.org/ws/2005/04/discovery"
    xmlns:wsdp="https://schemas.xmlsoap.org/ws/2006/02/devprof">
<soap:Header>
    <wsa:To>
        https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
    </wsa:To>
    <wsa:Action>
        https://schemas.xmlsoap.org/ws/2005/04/discovery/ProbeMatches
    </wsa:Action>
    <wsa:MessageID>
        urn:uuid:967d0036-fe69-40ad-8191-dd1fc8ef64ab
    </wsa:MessageID>
    <wsa:RelatesTo>
        urn:uuid:29cf10da-5c41-4d55-b184-5ee15e38ce23
    </wsa:RelatesTo>
    <wsd:AppSequence InstanceId="1"
        SequenceId="urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772"
        MessageNumber="9">
    </wsd:AppSequence>
</soap:Header>
<soap:Body>
    <wsd:ProbeMatches>
        <wsd:ProbeMatch>
            <wsa:EndpointReference>
                <wsa:Address>
                    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
                </wsa:Address>
            </wsa:EndpointReference>
            <wsd:Types>wsdp:Device</wsd:Types>
            <wsd:XAddrs>
                https://192.168.0.2:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
            </wsd:XAddrs>
            <wsd:MetadataVersion>2</wsd:MetadataVersion>
        </wsd:ProbeMatch>
    </wsd:ProbeMatches>
</soap:Body>
</soap:Envelope>
```

Un messaggio ProbeMatches ha i punti di interesse seguenti.



<table>
<colgroup>
<col  />
<col  />
<col  />
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
<td>ProbeMatches</td>
<td><pre class="syntax" data-space="preserve"><code>&lt;wsa:Action&gt;
    https://schemas.xmlsoap.org/ws/2005/04/discovery/ProbeMatches
&lt;/wsa:Action&gt;</code></pre></td>
<td>L'azione SOAP ProbeMatches identifica il messaggio come messaggio ProbeMatches.</td>
</tr>
<tr class="even">
<td>RelatesTo</td>
<td><pre class="syntax" data-space="preserve"><code>&lt;wsa:RelatesTo&gt;
    urn:uuid:29cf10da-5c41-4d55-b184-5ee15e38ce23
&lt;/wsa:RelatesTo&gt;</code></pre></td>
<td>Identificatore del messaggio a cui risponde il servizio. Questa intestazione corrisponde a MessageId nel messaggio <a href="probe-message.md">probe.</a></td>
</tr>
<tr class="odd">
<td>AppSequence</td>
<td><pre class="syntax" data-space="preserve"><code><wsd:AppSequence InstanceId=&quot;1&quot;
    SequenceId=&quot;urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772&quot;
    MessageNumber=&quot;9&quot;>
&lt;/wsd:AppSequence&gt;</code></pre></td>
<td>Contiene informazioni di sequenziazione dell'applicazione, che consentono di mantenere la sequenza dei messaggi anche se vengono ricevuti non in ordine. AppSequence viene convalidato come descritto in <a href="appsequence-validation-rules.md">Regole di convalida di AppSequence.</a></td>
</tr>
<tr class="even">
<td>Indirizzo</td>
<td><pre class="syntax" data-space="preserve"><code>&lt;wsa:Address&gt;
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
&lt;/wsa:Address&gt;</code></pre></td>
<td>Contiene l'indirizzo dell'endpoint. È possibile fare riferimento a questo indirizzo in un <a href="resolve-message.md">messaggio di</a> risoluzione.</td>
</tr>
<tr class="odd">
<td>XAddrs</td>
<td><pre class="syntax" data-space="preserve"><code>&lt;wsd:XAddrs&gt;
    https://192.168.0.2:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
&lt;/wsd:XAddrs&gt;</code></pre></td>
<td>XAddrs sono indirizzi di trasporto che possono essere usati per la comunicazione tra client e servizio. Gli addr vengono convalidati come descritto in <a href="xaddr-validation-rules.md">XAddr Validation Rules</a>.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Messaggi di individuazione e Exchange metadati](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[Messaggio probe](probe-message.md)
</dt> </dl>

 

 



