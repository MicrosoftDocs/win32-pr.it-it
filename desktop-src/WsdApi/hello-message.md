---
description: Messaggio WS-Discovery usato per annunciare la presenza di un dispositivo o di un servizio sulla rete.
ms.assetid: a7402e02-9bdc-49ec-ba93-8a32f55b9dd8
title: Messaggio Hello
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6504f25d360de055d7c0715266472e212540a14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312687"
---
# <a name="hello-message"></a>Messaggio Hello

Un messaggio Hello è un messaggio WS-Discovery usato per annunciare la presenza di un dispositivo o di un servizio sulla rete. I messaggi Hello vengono inviati anche in altri scenari. Per ulteriori informazioni sui messaggi Hello, vedere la sezione 4,1 della [specifica WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf).

Un messaggio Hello viene inviato dal multicast UDP alla porta 3702. Questo messaggio non è richiesto.

> [!Note]  
> Questo argomento illustra un messaggio DPWS di esempio generato da client e host di WSDAPI. WSDAPI analizzerà e accetterà altri messaggi conformi a DPWS che non sono conformi a questo esempio. Non utilizzare questo esempio per verificare l'interoperabilità DPWS; usare invece lo [strumento di interoperabilità di base di WSDAPI (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx) .

 

Il messaggio SOAP seguente mostra un esempio di messaggio Hello.

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
        https://schemas.xmlsoap.org/ws/2005/04/discovery/Hello
    </wsa:Action>
    <wsa:MessageID>
        urn:uuid:0f5d604c-81ac-4abc-8010-51dbffad55f2
    </wsa:MessageID>
    <wsd:AppSequence InstanceId="2"
        SequenceId="urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772"
        MessageNumber="14">
    </wsd:AppSequence>
</soap:Header>
<soap:Body>
    <wsd:Hello>
        <wsa:EndpointReference>
            <wsa:Address>
                urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
            </wsa:Address>
        </wsa:EndpointReference>
        <wsd:Types>wsdp:Device</wsd:Types>
        <wsd:MetadataVersion>2</wsd:MetadataVersion>
    </wsd:Hello>
</soap:Body>
```

Un messaggio Hello presenta i punti di interesse seguenti.



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
<td>Ciao</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Action>
    https://schemas.xmlsoap.org/ws/2005/04/discovery/Hello
</wsa:Action></code></pre></td>
<td>L'azione SOAP Hello identifica il messaggio come messaggio Hello.</td>
</tr>
<tr class="even">
<td>AppSequence</td>
<td><pre class="syntax" data-space="preserve"><code><wsd:AppSequence InstanceId=&quot;2&quot;
    SequenceId=&quot;urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772&quot;
    MessageNumber=&quot;14&quot;>
</wsd:AppSequence></code></pre></td>
<td>Contiene informazioni di sequenziazione dell'applicazione, che consentono di mantenere la sequenza di messaggi anche se non vengono ricevuti in ordine. AppSequence viene convalidato come descritto in <a href="appsequence-validation-rules.md">regole di convalida AppSequence</a>.</td>
</tr>
<tr class="odd">
<td>Indirizzo</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Address>
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsa:Address></code></pre></td>
<td>Contiene l'indirizzo dell'endpoint. È possibile fare riferimento a questo indirizzo in un messaggio di <a href="resolve-message.md">risoluzione</a> .</td>
</tr>
<tr class="even">
<td>Tipi</td>
<td><pre class="syntax" data-space="preserve"><code><wsd:Types>wsdp:Device</wsd:Types></code></pre></td>
<td>Contiene i tipi di WS-Discovery annunciati dall'host.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Messaggi di individuazione e scambio di metadati](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[Bye-messaggio](bye-message.md)
</dt> </dl>

 

 



