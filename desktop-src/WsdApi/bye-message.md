---
description: Messaggio WS-Discovery usato per annunciare la partenza di un dispositivo o di un servizio dalla rete.
ms.assetid: 7b9abfcc-28ab-4f29-af69-6dc68e3f51b6
title: Messaggio di bye
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8276c05314b31782442bfdf6de998dd41241391de9dc94947409041c8f4aa420
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117738653"
---
# <a name="bye-message"></a>Messaggio di bye

Un messaggio Bye è un WS-Discovery usato per annunciare la partenza di un dispositivo o di un servizio dalla rete. Per altre informazioni sui messaggi Bye, vedere la sezione 4.2 della [specifica WS-Discovery.](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf)

I messaggi bye non sono richieste. I messaggi sono facoltativi.

> [!Note]  
> Questo argomento illustra un messaggio DPWS di esempio generato da client e host WSDAPI. WSDAPI anaserà e accetterà altri messaggi conformi a DPWS che non sono conformi a questo esempio. Non usare questo esempio per verificare l'interoperabilità DPWS. usare [WSDAPI Basic Interoperability Tool (WSDBIT).](https://msdn.microsoft.com/library/cc264250.aspx)

 

Il messaggio SOAP seguente mostra un messaggio Bye di esempio.

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
        https://schemas.xmlsoap.org/ws/2005/04/discovery/Bye
    </wsa:Action>
    <wsa:MessageID>
        urn:uuid:193ccfa0-347d-41a1-9285-f500b6b96a15
    </wsa:MessageID>
    <wsd:AppSequence InstanceId="2"
        SequenceId="urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772"
        MessageNumber="21">
    </wsd:AppSequence>
</soap:Header>
<soap:Body>
    <wsd:Bye>
        <wsa:EndpointReference>
            <wsa:Address>
                urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
            </wsa:Address>
        </wsa:EndpointReference>
    </wsd:Bye>
</soap:Body>
```

Un messaggio Bye ha i punti di interesse seguenti.



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
    https://schemas.xmlsoap.org/ws/2005/04/discovery/Bye
</wsa:Action></code></pre></td>
<td>L'azione SOAP Bye identifica il messaggio come messaggio Bye.</td>
</tr>
<tr class="even">
<td>AppSequence</td>
<td><pre class="syntax" data-space="preserve"><code><wsd:AppSequence InstanceId=&quot;2&quot;
    SequenceId=&quot;urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772&quot;
    MessageNumber=&quot;21&quot;>
</wsd:AppSequence></code></pre></td>
<td>Contiene informazioni di sequenziazione dell'applicazione, che consentono di mantenere la sequenza di messaggi anche se vengono ricevuti in ordine. AppSequence viene convalidato come descritto in Regole di convalida <a href="appsequence-validation-rules.md">di AppSequence</a>.</td>
</tr>
<tr class="odd">
<td>Indirizzo</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Address>
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsa:Address></code></pre></td>
<td>Contiene l'indirizzo dell'endpoint in modalità offline.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Messaggi di individuazione e Exchange metadati](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[Messaggio Hello](hello-message.md)
</dt> </dl>

 

 



