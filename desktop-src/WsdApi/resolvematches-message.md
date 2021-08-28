---
description: Messaggio WS-Discovery inviato in risposta a un client Risolvere un messaggio da un servizio corrispondente.
ms.assetid: 0eaa4348-968e-4b45-9509-8b15476edaa1
title: Messaggio ResolveMatches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 140d279a5e66835b7754e3f501732263dff430f2
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883641"
---
# <a name="resolvematches-message"></a>Messaggio ResolveMatches

Un messaggio ResolveMatches è un WS-Discovery inviato in risposta al messaggio [Resolve](resolve-message.md) di un client da un servizio corrispondente. Per altre informazioni sui messaggi ResolveMatches, vedere la sezione 6.2 della [specifica WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf).

Un messaggio ResolveMatches viene inviato dall'unicast UDP alla porta 3702 (la porta da cui è stato inviato il messaggio [Resolve](resolve-message.md) del client). ResolveMatches deve essere inviato entro 4 secondi dal messaggio Resolve. in caso contrario, Windows firewall potrebbe eliminare il pacchetto.

Qualsiasi applicazione DPWS che invia [messaggi Resolve](resolve-message.md) riceverà messaggi ResolveMatches.

> [!Note]  
> Questo argomento illustra un messaggio DPWS di esempio generato da client e host WSDAPI. WSDAPI analizza e accetta altri messaggi conformi a DPWS non conformi a questo esempio. Non usare questo esempio per verificare l'interoperabilità di DPWS. utilizzare [WSDAPI Basic Interoperability Tool (WSDBIT).](https://msdn.microsoft.com/library/cc264250.aspx)

 

Il messaggio SOAP seguente mostra un messaggio ResolveMatches di esempio.

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
        https://schemas.xmlsoap.org/ws/2005/04/discovery/ResolveMatches
    </wsa:Action>
    <wsa:MessageID>
        urn:uuid:64ddd01c-b0d6-4afd-aba6-6f1f161ce9d4
    </wsa:MessageID>
    <wsa:RelatesTo>
        urn:uuid:38d1c3d9-8d73-4424-8861-6b7ee2af24d3
    </wsa:RelatesTo>
    <wsd:AppSequence InstanceId="1"
        SequenceId="urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772"
        MessageNumber="6">
    </wsd:AppSequence>
</soap:Header>
<soap:Body>
    <wsd:ResolveMatches>
        <wsd:ResolveMatch>
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
        </wsd:ResolveMatch>
    </wsd:ResolveMatches>
</soap:Body>
</soap:Envelope>
```

Un messaggio ResolveMatches ha i punti di interesse seguenti.



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
<td>ResolveMatches</td>
<td><pre class="syntax" data-space="preserve"><code>&lt;wsa:Action&gt;
    https://schemas.xmlsoap.org/ws/2005/04/discovery/ResolveMatches
&lt;/wsa:Action&gt;</code></pre></td>
<td>L'azione SOAP ResolveMatches identifica il messaggio come messaggio ResolveMatches.</td>
</tr>
<tr class="even">
<td>RelatesTo</td>
<td><pre class="syntax" data-space="preserve"><code>&lt;wsa:RelatesTo&gt;
    urn:uuid:38d1c3d9-8d73-4424-8861-6b7ee2af24d3
&lt;/wsa:RelatesTo&gt;</code></pre></td>
<td>Identificatore del messaggio a cui risponde il servizio. Questa intestazione corrisponde a MessageId nel messaggio <a href="resolve-message.md">Resolve.</a></td>
</tr>
<tr class="odd">
<td>AppSequence</td>
<td><pre class="syntax" data-space="preserve"><code><wsd:AppSequence InstanceId=&quot;1&quot;
    SequenceId=&quot;urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772&quot;
    MessageNumber=&quot;6&quot;>
&lt;/wsd:AppSequence&gt;</code></pre></td>
<td>Contiene informazioni di sequenziazione dell'applicazione, che consentono di mantenere la sequenza dei messaggi anche se vengono ricevuti non in ordine. AppSequence viene convalidato come descritto in <a href="appsequence-validation-rules.md">Regole di convalida di AppSequence.</a></td>
</tr>
<tr class="even">
<td>Indirizzo</td>
<td><pre class="syntax" data-space="preserve"><code>&lt;wsa:Address&gt;
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
&lt;/wsa:Address&gt;</code></pre></td>
<td>Contiene l'indirizzo dell'endpoint da risolvere.</td>
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

[Risolvere il messaggio](resolve-message.md)
</dt> </dl>

 

 



