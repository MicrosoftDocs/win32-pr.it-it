---
description: Messaggio di WS-Discovery inviato da un servizio in risposta a un messaggio Probe dei client.
ms.assetid: 58d3d016-ae29-4090-9b88-e1125db59c95
title: Messaggio ProbeMatches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfd856cda51d558073585f41f3db23c75fea7f17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312673"
---
# <a name="probematches-message"></a>Messaggio ProbeMatches

Un messaggio ProbeMatches è un messaggio WS-Discovery inviato da un servizio in risposta al messaggio [Probe](probe-message.md) del client. Per ulteriori informazioni sui messaggi ProbeMatches, vedere la sezione 5,3 della [specifica WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf).

Un messaggio ProbeMatches viene inviato dall'unicast UDP alla porta da cui è stato inviato il messaggio [Probe](probe-message.md) del client. ProbeMatches deve essere inviato entro 4 secondi dal messaggio Probe; in caso contrario, Windows Firewall possibile eliminare il pacchetto.

Se nel messaggio ProbeMatches non è incluso alcun XAddrs, il client può inviare un messaggio di [risoluzione](resolve-message.md) tramite multicast UDP alla porta 3702. Il client invierà un messaggio di risoluzione solo quando verrà inviato un messaggio HTTP, ad esempio una richiesta [Get](get--metadata-exchange--http-request-and-message.md) Metadata Exchange o un messaggio di servizio.

Tutte le applicazioni DPWS che inviano messaggi [Probe](probe-message.md) riceveranno messaggi ProbeMatches.

> [!Note]  
> Questo argomento illustra un messaggio DPWS di esempio generato da client e host di WSDAPI. WSDAPI analizzerà e accetterà altri messaggi conformi a DPWS che non sono conformi a questo esempio. Non utilizzare questo esempio per verificare l'interoperabilità DPWS; usare invece lo [strumento di interoperabilità di base di WSDAPI (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx) .

 

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

Un messaggio ProbeMatches presenta i punti di interesse seguenti.



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
<td>ProbeMatches</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Action>
    https://schemas.xmlsoap.org/ws/2005/04/discovery/ProbeMatches
</wsa:Action></code></pre></td>
<td>L'azione SOAP ProbeMatches identifica il messaggio come un messaggio ProbeMatches.</td>
</tr>
<tr class="even">
<td>RelatesTo</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:RelatesTo>
    urn:uuid:29cf10da-5c41-4d55-b184-5ee15e38ce23
</wsa:RelatesTo></code></pre></td>
<td>Identificatore del messaggio a cui il servizio risponde. Questa intestazione corrisponde al MessageId nel messaggio del <a href="probe-message.md">Probe</a> .</td>
</tr>
<tr class="odd">
<td>AppSequence</td>
<td><pre class="syntax" data-space="preserve"><code><wsd:AppSequence InstanceId=&quot;1&quot;
    SequenceId=&quot;urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772&quot;
    MessageNumber=&quot;9&quot;>
</wsd:AppSequence></code></pre></td>
<td>Contiene informazioni di sequenziazione dell'applicazione, che consentono di mantenere la sequenza di messaggi anche se non vengono ricevuti in ordine. AppSequence viene convalidato come descritto in <a href="appsequence-validation-rules.md">regole di convalida AppSequence</a>.</td>
</tr>
<tr class="even">
<td>Indirizzo</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Address>
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsa:Address></code></pre></td>
<td>Contiene l'indirizzo dell'endpoint. È possibile fare riferimento a questo indirizzo in un messaggio di <a href="resolve-message.md">risoluzione</a> .</td>
</tr>
<tr class="odd">
<td>XAddrs</td>
<td><pre class="syntax" data-space="preserve"><code><wsd:XAddrs>
    https://192.168.0.2:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsd:XAddrs></code></pre></td>
<td>XAddrs sono indirizzi di trasporto che possono essere usati per la comunicazione tra client e servizio. Gli indirizzi vengono convalidati come descritto in <a href="xaddr-validation-rules.md">regole di convalida XAddr</a>.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Messaggi di individuazione e scambio di metadati](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[Messaggio Probe](probe-message.md)
</dt> </dl>

 

 



