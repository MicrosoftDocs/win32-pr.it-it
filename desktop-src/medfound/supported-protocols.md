---
description: Protocolli supportati
ms.assetid: 3c026426-c2b7-4909-9524-9cc0bd45347e
title: Protocolli supportati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e618f47a1ffc4a81c36e48407b93da54d7d532f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753839"
---
# <a name="supported-protocols"></a>Protocolli supportati

Media Foundation supporta i protocolli seguenti:

-   Protocollo RTSP (Real Time Streaming Protocol)

    RTSP viene usato principalmente per lo streaming di contenuti multimediali. Può utilizzare UDP o TCP come protocolli di trasporto. UDP è la più efficiente per la distribuzione di contenuti perché l'overhead della larghezza di banda è inferiore rispetto ai protocolli basati su TCP. Sebbene il protocollo TCP garantisca un recapito affidabile dei pacchetti, TCP non è particolarmente adatto per i flussi multimediali digitali, in cui l'uso efficiente della larghezza di banda è più importante rispetto ai pacchetti persi occasionali.

-   Hypertext Transfer Protocol (HTTP)

    HTTP usa TCP e viene usato dai server Web. Lo schema "httpd://" indica che l'origine è scaricabile da un server Web. Il protocollo HTTP viene usato anche in caso di firewall, che in genere sono configurati per accettare richieste HTTP e in genere rifiutano altri protocolli di streaming.

L'applicazione può ottenere i protocolli supportati da Media Foundation usando l'interfaccia [**IMFNetSchemeHandlerConfig**](/windows/desktop/api/mfidl/nn-mfidl-imfnetschemehandlerconfig) . A tale scopo, l'applicazione deve prima recuperare il numero di protocolli chiamando [**IMFNetSchemeHandlerConfig:: GetNumberOfSupportedProtocols**](/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-getnumberofsupportedprotocols) e quindi ottenere il tipo di protocollo basato sull'indice chiamando [**IMFNetSchemeHandlerConfig:: GetSupportedProtocolType**](/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-getsupportedprotocoltype). Questo metodo restituisce uno dei valori definiti nell'enumerazione del [**\_ \_ tipo di protocollo MFNETSOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) .

L'applicazione può inoltre ottenere gli schemi supportati dal resolver di origine chiamando la funzione [**MFGetSupportedSchemes**](/windows/desktop/api/mfidl/nf-mfidl-mfgetsupportedschemes) .

## <a name="protocol-rollover"></a>Rollover del protocollo

Quando un'applicazione specifica "mms://" come schema URL, il resolver di origine esegue un'operazione di *rollover del protocollo* . In questo processo, il resolver di origine determina il protocollo migliore per l'origine di rete da usare per ottenere il contenuto. In genere, per lo streaming di contenuti multimediali, RTSP con UDP (RTSP) è più efficiente di HTTP. Tuttavia, se il contenuto è ospitato in un server Web, HTTP è la scelta migliore.

Il rollover del protocollo può verificarsi anche quando un tentativo di usare il protocollo specificato nello schema URL ha esito negativo. Un protocollo, ad esempio, può avere esito negativo quando un firewall blocca i pacchetti UDP. In questo caso, il resolver di origine passa a HTTP.

Il rollover del protocollo non si applica se lo schema URL contiene un protocollo specifico, ad esempio "rtspu://". Inoltre, il rollover non viene eseguito se l'autenticazione ha esito negativo o se il server ha raggiunto un limite di connessioni client. È consigliabile che le applicazioni specifichino lo schema "mms://" e consentono al resolver di origine di selezionare il protocollo migliore per lo scenario.

La tabella seguente elenca l'ordine di rollover.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Schemi consentiti</th>
<th>Ordine di rollover del protocollo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>mms://o rtsp://</td>
<td>Cache veloce abilitata:<br/>
<ol>
<li>RTSP con TCP (RTSPt)<br/></li>
<li>RTSP con UDP (RTSPr)<br/></li>
<li>Flusso HTTP<br/></li>
<li>Download HTTP (HTTPD)<br/></li>
</ol>
Cache veloce disabilitata:<br/>
<ol>
<li>RTSPU<br/></li>
<li>RTSPT<br/></li>
<li>Flusso HTTP<br/></li>
<li>Download HTTP<br/></li>
</ol></td>
</tr>
<tr class="even">
<td>rtspu://</td>
<td>RTSPU</td>
</tr>
<tr class="odd">
<td>rtspt://</td>
<td>RTSPT</td>
</tr>
<tr class="even">
<td>https://</td>
<td><ol>
<li>HTTP<br/></li>
<li>HTTPD<br/></li>
</ol></td>
</tr>
<tr class="odd">
<td>httpd://</td>
<td>HTTPD</td>
</tr>
</tbody>
</table>



 

## <a name="retrieving-the-current-protocol"></a>Recupero del protocollo corrente

Dopo un'operazione di rollover del protocollo, l'origine di rete potrebbe usare un protocollo diverso da quello specificato dall'applicazione nello schema URL. Il risultato del rollover del protocollo è disponibile per l'applicazione dopo che l'origine di rete stabilisce la connessione con il server multimediale.

Per ottenere il protocollo e il trasporto usati per ottenere il contenuto, l'applicazione può recuperare i valori delle proprietà per la proprietà del [ \_ protocollo MFNETSOURCE](mfnetsource-protocol-property.md) e la proprietà del [ \_ trasporto MFNETSOURCE](mfnetsource-transport-property.md) di un oggetto **IPropertyStore** dall'origine di rete.

Nel codice seguente viene illustrato come ottenere questi valori.


```C++
// Create an IPropertyStore object.
    IPropertyStore *pProp = NULL;
    hr = CreatePropertyStore(&pProp);

    PROPVARIANT var;
    PropVariantInit(&var);

// Get the property store from the network source.
// The network source is created by the source resolver. Not shown.
    if (SUCCEEDED(hr))
    {
        hr = pNetworkSource->QueryInterface 
                (__uuidof(IPropertyStore), 
                (void**)&pProp);
    }
    if (SUCCEEDED(hr))
    {
        // Create a property key.
        PROPERTYKEY key;
        // Get the MFNETSOURCE_PROTOCOL property value.
        key.fmtid = MFNETSOURCE_PROTOCOL;
        hr = pProp->GetValue (key, &var);

        // Get the MFNETSOURCE_TRANSPORT property value.
        key.fmtid = MFNETSOURCE_TRANSPORT;
        key.pid = 0;
        hr = pProp->GetValue (key, &var);

    }
```



Nel codice di esempio precedente, **IPropertyStore:: GetValue** Recupera il \_ valore del protocollo MFNETSOURCE, che è un membro dell'enumerazione del [**\_ \_ tipo di protocollo MFNETSOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) . Per il \_ trasporto MFNETSOURCE, il valore è un membro dell'enumerazione del [**\_ \_ tipo di trasporto MFNETSOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_transport_type) .

In alternativa, l'applicazione può ottenere gli stessi valori usando il servizio MFNETSOURCE \_ Statistics \_ Service. Per usare questo servizio, l'applicazione può chiamare la funzione [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) per ottenere l'archivio delle proprietà dall'origine di rete. Questo archivio di proprietà contiene le statistiche di rete nella proprietà [MFNETSOURCE \_ Statistics](mfnetsource-statistics-property.md) . È possibile recuperare i valori di protocollo e di trasporto specificando \_ \_ l'ID del protocollo MFNETSOURCE e \_ \_ l'ID trasporto MFNETSOURCE, definiti nell'enumerazione [**MFNETSOURCE \_ Statistics \_ IDS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) . Il codice seguente illustra come ottenere i valori di protocollo e trasporto usando il servizio MFNETSOURCE \_ Statistics \_ Service.


```C++
// Create an IPropertyStore object.
    IPropertyStore *pProp = NULL;
    hr = CreatePropertyStore(&pProp);

    HRESULT hr = S_OK;

    hr = MFGetService(
        pMediaSource, 
        MFNETSOURCE_STATISTICS_SERVICE, 
        IID_IPropertyStore, 
        (void**) & pProp); 

    if (SUCCEEDED(hr))
    {
        // Create a property key.
        PROPERTYKEY key;
        // Get the property value.
        key.fmtid = MFNETSOURCE_STATISTICS;
        key.pid = MFNETSOURCE_PROTOCOL_ID;
        hr = pProp->GetValue (key, &var);

        // Get the transport value.
        key.fmtid = MFNETSOURCE_STATISTICS;
        key.pid = MFNETSOURCE_TRANSPORT_ID;
        hr = pProp->GetValue (key, &var);

    }
```



## <a name="enabling-and-disabling-protocols"></a>Abilitazione e disabilitazione di protocolli

L'applicazione può configurare l'origine di rete in modo che alcuni protocolli vengano ignorati durante il processo di rollover. A tale scopo, vengono utilizzate le proprietà dell'origine di rete per disabilitare protocolli specifici. Nella tabella seguente vengono illustrate le proprietà e i protocolli che controllano.



| Proprietà                                                                    | Descrizione                                 |
|-----------------------------------------------------------------------------|---------------------------------------------|
| [MFNETSOURCE \_ Abilita \_ http](mfnetsource-enable-http-property.md)           | Abilita o Disabilita HTTP e HTTPD.         |
| [MFNETSOURCE \_ Abilita \_ RTSP](mfnetsource-enable-rtsp-property.md)           | Abilita o Disabilita RTSPr e RTSPt.        |
| [MFNETSOURCE \_ abilitare \_ TCP](mfnetsource-enable-tcp-property.md)             | Abilita o Disabilita RTSPt.                  |
| [MFNETSOURCE \_ Abilita \_ UDP](mfnetsource-enable-udp-property.md)             | Abilita o Disabilita RTSPr.                  |
| [MFNETSOURCE \_ abilitare il \_ download](mfnetsource-enable-download-property.md)   | Abilita o Disabilita HTTPD.                  |
| [MFNETSOURCE \_ Abilita \_ flusso](mfnetsource-enable-streaming-property.md) | Abilita o Disabilita RTSPr, RTSPt e HTTP. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Rete in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




