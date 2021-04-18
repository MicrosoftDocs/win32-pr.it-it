---
description: Messaggio WS-Transfer usato per richiedere i metadati.
ms.assetid: 18bf27aa-6ae5-4419-ae68-6df9eda10cd4
title: Get (scambio di metadati) richiesta e messaggio HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8ad240a51fdbabf4184b8769f4e3cca6daa4244
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310305"
---
# <a name="get-metadata-exchange-http-request-and-message"></a>Get (scambio di metadati) richiesta e messaggio HTTP

Un messaggio Get è un messaggio WS-Transfer usato per richiedere i metadati. Per ulteriori informazioni su come ottenere i messaggi, vedere la sezione 3,1 della [specifica WS-Transfer](https://specs.xmlsoap.org/ws/2004/09/transfer/WS-Transfer.pdf). Poiché lo scambio di metadati viene eseguito tramite HTTP, un messaggio Get è il payload di una richiesta HTTP.

I client DPWS inviano messaggi Get. I client di individuazione funzioni, i client WSDAPI che chiamano [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy)e i client WSDAPI che chiamano [**WSDCreateDeviceProxyAdvanced**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxyadvanced) inviano questo messaggio.

> [!Note]  
> Questo argomento illustra un messaggio DPWS di esempio generato da client e host di WSDAPI. WSDAPI analizzerà e accetterà altri messaggi conformi a DPWS che non sono conformi a questo esempio. Non utilizzare questo esempio per verificare l'interoperabilità DPWS; usare invece lo [strumento di interoperabilità di base di WSDAPI (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx) .

 

Nell'esempio seguente viene illustrata una richiesta HTTP Get di esempio.

``` syntax
POST /37f86d35-e6ac-4241-964f-1d9ae46fb366
HTTP/1.1
Content-Type: application/soap+xml
User-Agent: WSDAPI
Host: 192.168.0.2:5357
Content-Length: 658
Connection: Keep-Alive
Cache-Control: no-cache
Pragma: no-cache
```

Una richiesta GET HTTP presenta i punti di interesse seguenti.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Punto di interesse</th>
<th>Riga di intestazione</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>percorso URL</td>
<td><pre class="syntax" data-space="preserve"><code>POST /37f86d35-e6ac-4241-964f-1d9ae46fb366</code></pre></td>
<td>Percorso URL in cui è stata inviata la richiesta HTTP Get.</td>
</tr>
<tr class="even">
<td>Host e porta</td>
<td><pre class="syntax" data-space="preserve"><code>Host: 192.168.0.2:5357</code></pre></td>
<td>Host e porta a cui è stata indirizzata la richiesta GET HTTP.</td>
</tr>
</tbody>
</table>



 

Il messaggio SOAP seguente mostra un messaggio di esempio Get.

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope
    xmlns:soap="https://www.w3.org/2003/05/soap-envelope"
    xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing">
<soap:Header>
    <wsa:To>
        urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
    </wsa:To>
    <wsa:Action>
        https://schemas.xmlsoap.org/ws/2004/09/transfer/Get
    </wsa:Action>
    <wsa:MessageID>
        urn:uuid:027bec45-c37c-466c-936c-68f648abe2bb
    </wsa:MessageID>
    <wsa:ReplyTo>
        <wsa:Address>
            https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
        </wsa:Address>
    </wsa:ReplyTo>
    <wsa:From>
        <wsa:Address>
            urn:uuid:49e131df-351a-4ece-9a6f-6a862d31cffa
        </wsa:Address>
    </wsa:From>
</soap:Header>
<soap:Body>
</soap:Body>
```

Un messaggio Get presenta i punti di interesse seguenti.



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
<td>A</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:To>
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsa:To></code></pre></td>
<td>Identificatore del dispositivo a cui vengono richiesti i metadati.</td>
</tr>
<tr class="even">
<td>Recupero</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Action>
    https://schemas.xmlsoap.org/ws/2004/09/transfer/Get
</wsa:Action</code></pre></td>
<td>L'azione Get SOAP identifica il messaggio come messaggio Get.</td>
</tr>
<tr class="odd">
<td>MessageID</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:MessageID>
    urn:uuid:027bec45-c37c-466c-936c-68f648abe2bb
</wsa:MessageID></code></pre></td>
<td>Contiene l'identificatore del messaggio a cui viene fatto riferimento in un messaggio <a href="getresponse--metadata-exchange--message.md">GetResponse</a> .</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Messaggi di individuazione e scambio di metadati](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[Messaggio GetResponse](getresponse--metadata-exchange--message.md)
</dt> </dl>

 

 



