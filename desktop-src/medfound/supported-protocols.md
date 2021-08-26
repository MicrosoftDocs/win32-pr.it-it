---
description: Protocolli supportati
ms.assetid: 3c026426-c2b7-4909-9524-9cc0bd45347e
title: Protocolli supportati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20cc5e47bddec9e00fbb62e853db5a492172da84
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468028"
---
# <a name="supported-protocols"></a>Protocolli supportati

Media Foundation supporta i protocolli seguenti:

-   RTSP (Real Time Streaming Protocol)

    RTSP viene usato principalmente per lo streaming di contenuti multimediali. Può usare UDP o TCP come protocolli di trasporto. UDP è il più efficiente per la distribuzione di contenuti perché il sovraccarico della larghezza di banda è minore rispetto ai protocolli basati su TCP. Anche se il protocollo TCP garantisce il recapito affidabile dei pacchetti, TCP non è adatto per i flussi multimediali digitali, in cui l'uso efficiente della larghezza di banda è più importante dei pacchetti occasionali persi.

-   Hypertext Transfer Protocol (HTTP)

    HTTP usa TCP e viene usato dai server Web. Lo schema "httpd://" indica che l'origine è scaricabile da un server Web. HTTP viene usato anche nel caso di firewall, in genere configurati per accettare richieste HTTP e in genere rifiutare altri protocolli di streaming.

L'applicazione può ottenere i protocolli supportati da Media Foundation tramite [**l'interfaccia IMFNetSchemeHandlerConfig.**](/windows/desktop/api/mfidl/nn-mfidl-imfnetschemehandlerconfig) A tale scopo, l'applicazione deve prima recuperare il numero di protocolli chiamando [**IMFNetSchemeHandlerConfig::GetNumberOfSupportedProtocols**](/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-getnumberofsupportedprotocols) e quindi ottenere il tipo di protocollo in base all'indice chiamando [**IMFNetSchemeHandlerConfig::GetSupportedProtocolType**](/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-getsupportedprotocoltype). Questo metodo restituisce uno dei valori definiti nell'enumerazione [**MFNETSOURCE \_ PROTOCOL \_ TYPE.**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type)

L'applicazione può anche ottenere gli schemi supportati dal sistema di risoluzione di origine chiamando la [**funzione MFGetSupportedSchemes.**](/windows/desktop/api/mfidl/nf-mfidl-mfgetsupportedschemes)

## <a name="protocol-rollover"></a>Rollover del protocollo

Quando un'applicazione specifica "mms://" come schema URL, il sistema di risoluzione di origine esegue un'operazione di *rollover del* protocollo. In questo processo, il sistema di risoluzione dell'origine determina il protocollo migliore da usare per l'origine di rete per ottenere il contenuto. In genere, per il flusso multimediale, RTSP con UDP (RTSPU) è più efficiente di HTTP. Tuttavia, se il contenuto è ospitato in un server Web, HTTP è una scelta migliore.

Il rollover del protocollo può verificarsi anche quando un tentativo di usare il protocollo specificato nello schema URL ha esito negativo. Ad esempio, un protocollo può avere esito negativo quando un firewall blocca i pacchetti UDP. In questo caso, il sistema di risoluzione di origine passa a HTTP.

Il rollover del protocollo non si applica se lo schema URL contiene un protocollo specifico, ad esempio "rtspu://". Inoltre, il rollover non viene eseguito se l'autenticazione ha esito negativo o il server ha raggiunto un limite di connessioni client. È consigliabile che le applicazioni specificano lo schema "mms://" e consentano al sistema di risoluzione di origine di selezionare il protocollo migliore per lo scenario.

La tabella seguente elenca l'ordine di rollover.




| Schemi consentiti | Ordine di rollover del protocollo | 
|-----------------|-------------------------|
| mms:// o rtsp:// | Cache veloce abilitata:<br /><ol><li>RTSP con TCP (RTSPT)<br /></li><li>RTSP con UDP (RTSPU)<br /></li><li>HTTP Streaming<br /></li><li>Download HTTP (HTTPD)<br /></li></ol>Cache veloce disabilitata:<br /><ol><li>RTSPU<br /></li><li>RTSPT<br /></li><li>HTTP Streaming<br /></li><li>HTTP Download<br /></li></ol> | 
| rtspu:// | RTSPU | 
| rtspt:// | RTSPT | 
| https:// | <ol><li>HTTP<br /></li><li>HTTPD<br /></li></ol> | 
| httpd:// | HTTPD | 




 

## <a name="retrieving-the-current-protocol"></a>Recupero del protocollo corrente

Dopo un'operazione di rollover del protocollo, l'origine di rete potrebbe usare un protocollo diverso da quello specificato dall'applicazione nello schema URL. Il risultato del rollover del protocollo è disponibile per l'applicazione dopo che l'origine di rete ha stabilito la connessione con il server multimediale.

Per ottenere il protocollo e il trasporto usati per ottenere il contenuto, l'applicazione può recuperare i valori delle proprietà per la proprietà [PROTOCOL MFNETSOURCE \_](mfnetsource-protocol-property.md) e la proprietà [TRANSPORT \_ MFNETSOURCE](mfnetsource-transport-property.md) di un oggetto **IPropertyStore** dall'origine di rete.

Il codice seguente illustra come ottenere questi valori.


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



Nel codice di esempio **precedente, IPropertyStore::GetValue** recupera il valore PROTOCOLLO MFNETSOURCE, che è un membro dell'enumerazione \_ PROTOCOL [**\_ \_ TYPE di MFNETSOURCE.**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) Per MFNETSOURCE \_ TRANSPORT, il valore è un membro dell'enumerazione [**MFNETSOURCE \_ TRANSPORT \_ TYPE.**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_transport_type)

In alternativa, l'applicazione può ottenere gli stessi valori usando il servizio MFNETSOURCE \_ STATISTICS \_ SERVICE. Per usare questo servizio, l'applicazione può chiamare la [**funzione MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) per ottenere l'archivio delle proprietà dall'origine di rete. Questo archivio delle proprietà contiene statistiche di rete nella [proprietà MFNETSOURCE \_ STATISTICS.](mfnetsource-statistics-property.md) I valori di protocollo e trasporto possono essere recuperati specificando L'ID PROTOCOLLO MFNETSOURCE e L'ID TRASPORTO \_ \_ MFNETSOURCE, definiti \_ \_ nell'enumerazione [**MFNETSOURCE \_ STATISTICS \_ IDS.**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) Il codice seguente illustra come ottenere i valori di protocollo e trasporto usando il servizio MFNETSOURCE \_ STATISTICS \_ SERVICE.


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



## <a name="enabling-and-disabling-protocols"></a>Abilitazione e disabilitazione dei protocolli

L'applicazione può configurare l'origine di rete in modo che determinati protocolli siano ignorati durante il processo di rollover. A tale scopo, le proprietà dell'origine di rete vengono usate per disabilitare protocolli specifici. La tabella seguente illustra le proprietà e i protocolli che controllano.



| Proprietà                                                                    | Descrizione                                 |
|-----------------------------------------------------------------------------|---------------------------------------------|
| [MFNETSOURCE \_ ENABLE \_ HTTP](mfnetsource-enable-http-property.md)           | Abilita o disabilita HTTP e HTTPD.         |
| [MFNETSOURCE \_ ENABLE \_ RTSP](mfnetsource-enable-rtsp-property.md)           | Abilita o disabilita RTSPU e RTSPT.        |
| [MFNETSOURCE \_ ABILITA \_ TCP](mfnetsource-enable-tcp-property.md)             | Abilita o disabilita RTSPT.                  |
| [MFNETSOURCE \_ ABILITA \_ UDP](mfnetsource-enable-udp-property.md)             | Abilita o disabilita RTSPU.                  |
| [MFNETSOURCE \_ ABILITA \_ DOWNLOAD](mfnetsource-enable-download-property.md)   | Abilita o disabilita HTTPD.                  |
| [MFNETSOURCE \_ ABILITA \_ LO STREAMING](mfnetsource-enable-streaming-property.md) | Abilita o disabilita RTSPU, RTSPT e HTTP. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Rete in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




