---
description: Messaggio WS-Transfer utilizzato per rispondere a una richiesta di metadati.
ms.assetid: aff05317-35db-4ea6-9692-1e09e4682fe7
title: Messaggio GetResponse (scambio di metadati)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b91546076698f17a25b8a87444ae3eca71d65a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231671"
---
# <a name="getresponse-metadata-exchange-message"></a>Messaggio GetResponse (scambio di metadati)

Un messaggio GetResponse è un messaggio WS-Transfer usato per rispondere a una richiesta di metadati. Per ulteriori informazioni sui messaggi GetResponse, vedere la sezione 3,1 della [specifica WS-Transfer](https://specs.xmlsoap.org/ws/2004/09/transfer/WS-Transfer.pdf).

Tutte le applicazioni DPWS che inviano messaggi [Get](get--metadata-exchange--http-request-and-message.md) riceveranno messaggi GetResponse.

> [!Note]  
> Questo argomento illustra un messaggio DPWS di esempio generato da client e host di WSDAPI. WSDAPI analizzerà e accetterà altri messaggi conformi a DPWS che non sono conformi a questo esempio. Non utilizzare questo esempio per verificare l'interoperabilità DPWS; usare invece lo [strumento di interoperabilità di base di WSDAPI (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx) .

 

Il messaggio SOAP seguente mostra un messaggio GetResponse di esempio.

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope
    xmlns:soap="https://www.w3.org/2003/05/soap-envelope"
    xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing"
    xmlns:wsx="https://schemas.xmlsoap.org/ws/2004/09/mex"
    xmlns:wsdp="https://schemas.xmlsoap.org/ws/2006/02/devprof"
    xmlns:sim="https://schemas.example.org/SimpleService"
    xmlns:att="https://schemas.example.org/AttachmentService"
    xmlns:eve="https://schemas.example.org/EventingService">
<soap:Header>
    <wsa:To>
        https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
    </wsa:To>
    <wsa:Action>
        https://schemas.xmlsoap.org/ws/2004/09/transfer/GetResponse
    </wsa:Action>
    <wsa:MessageID>
        urn:uuid:119dcdf5-fc0d-4d40-bf1f-de52dc292744
    </wsa:MessageID>
    <wsa:RelatesTo>
        urn:uuid:027bec45-c37c-466c-936c-68f648abe2bb
    </wsa:RelatesTo>
</soap:Header>
<soap:Body>
    <wsx:Metadata>
        <wsx:MetadataSection Dialect="https://schemas.xmlsoap.org/ws/2006/02/devprof/ThisDevice">
            <wsdp:ThisDevice>
                <wsdp:FriendlyName>
                    WSDAPI Basic Interop Server
                </wsdp:FriendlyName>
                <wsdp:FirmwareVersion>alpha</wsdp:FirmwareVersion>
                <wsdp:SerialNumber>1</wsdp:SerialNumber>
            </wsdp:ThisDevice>
        </wsx:MetadataSection>
        <wsx:MetadataSection Dialect="https://schemas.xmlsoap.org/ws/2006/02/devprof/ThisModel">
            <wsdp:ThisModel>
                <wsdp:Manufacturer>
                    Microsoft
                </wsdp:Manufacturer>
                <wsdp:ManufacturerUrl>
                    https://www.microsoft.com/
                </wsdp:ManufacturerUrl>
                <wsdp:ModelName>
                    WSDAPI Interop device
                </wsdp:ModelName>
                <wsdp:ModelNumber>0.1</wsdp:ModelNumber>
                <wsdp:ModelUrl>
                    https://www.microsoft.com/
                </wsdp:ModelUrl>
                <wsdp:PresentationUrl>
                    https://www.microsoft.com/
                </wsdp:PresentationUrl>
            </wsdp:ThisModel>
        </wsx:MetadataSection>
        <wsx:MetadataSection Dialect="https://schemas.xmlsoap.org/ws/2006/02/devprof/Relationship">
            <wsdp:Relationship Type="https://schemas.xmlsoap.org/ws/2006/02/devprof/host">
                <wsdp:Host>
                    <wsa:EndpointReference>
                        <wsa:Address>
                            urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
                        </wsa:Address>
                    </wsa:EndpointReference>
                    <wsdp:Types>sim:SimpleDeviceType</wsdp:Types>
                    <wsdp:ServiceId>
                        https://testdevice.interop/SimpleDevice
                    </wsdp:ServiceId>
                </wsdp:Host>
                <wsdp:Hosted>
                    <wsa:EndpointReference>
                        <wsa:Address>
                            https://192.168.0.2:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
                        </wsa:Address>
                    </wsa:EndpointReference>
                    <wsdp:Types>sim:SimpleService</wsdp:Types>
                    <wsdp:ServiceId>
                        https://testdevice.interop/SimpleService1
                    </wsdp:ServiceId>
                </wsdp:Hosted>
            </wsdp:Relationship>
        </wsx:MetadataSection>
    </wsx:Metadata>
</soap:Body>
</soap:Envelope>
```

Un messaggio GetResponse presenta i punti di interesse seguenti.



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
<td>GetResponse</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Action>
    https://schemas.xmlsoap.org/ws/2004/09/transfer/GetResponse
</wsa:Action></code></pre></td>
<td>L'azione SOAP GetResponse identifica il messaggio come messaggio GetResponse.</td>
</tr>
<tr class="even">
<td>RelatesTo</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:RelatesTo>
    urn:uuid:027bec45-c37c-466c-936c-68f648abe2bb
</wsa:RelatesTo></code></pre></td>
<td>Identificatore del messaggio a cui il dispositivo sta rispondendo. Questa intestazione corrisponde al MessageID nel messaggio <a href="get--metadata-exchange--http-request-and-message.md">Get</a> .</td>
</tr>
<tr class="odd">
<td>Indirizzo</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Address>
    https://192.168.0.2:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsa:Address></code></pre></td>
<td>Contiene l'indirizzo dell'endpoint dei servizi ospitati in questo dispositivo.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Messaggi di individuazione e scambio di metadati](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[Recupera messaggio](get--metadata-exchange--http-request-and-message.md)
</dt> </dl>

 

 



