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
# <a name="supported-protocols"></a><span data-ttu-id="5aa48-103">Protocolli supportati</span><span class="sxs-lookup"><span data-stu-id="5aa48-103">Supported Protocols</span></span>

<span data-ttu-id="5aa48-104">Media Foundation supporta i protocolli seguenti:</span><span class="sxs-lookup"><span data-stu-id="5aa48-104">Media Foundation supports the following protocols:</span></span>

-   <span data-ttu-id="5aa48-105">Protocollo RTSP (Real Time Streaming Protocol)</span><span class="sxs-lookup"><span data-stu-id="5aa48-105">Real Time Streaming Protocol (RTSP)</span></span>

    <span data-ttu-id="5aa48-106">RTSP viene usato principalmente per lo streaming di contenuti multimediali.</span><span class="sxs-lookup"><span data-stu-id="5aa48-106">RTSP is mainly used for streaming media content.</span></span> <span data-ttu-id="5aa48-107">Può utilizzare UDP o TCP come protocolli di trasporto.</span><span class="sxs-lookup"><span data-stu-id="5aa48-107">It can use UDP or TCP as transport protocols.</span></span> <span data-ttu-id="5aa48-108">UDP è la più efficiente per la distribuzione di contenuti perché l'overhead della larghezza di banda è inferiore rispetto ai protocolli basati su TCP.</span><span class="sxs-lookup"><span data-stu-id="5aa48-108">UDP is the most efficient for content delivery because the bandwidth overhead is less than with TCP-based protocols.</span></span> <span data-ttu-id="5aa48-109">Sebbene il protocollo TCP garantisca un recapito affidabile dei pacchetti, TCP non è particolarmente adatto per i flussi multimediali digitali, in cui l'uso efficiente della larghezza di banda è più importante rispetto ai pacchetti persi occasionali.</span><span class="sxs-lookup"><span data-stu-id="5aa48-109">Even though the TCP protocol ensures reliable packet delivery, TCP is not well suited for digital media streams, where efficient use of bandwidth is more important than occasional lost packets.</span></span>

-   <span data-ttu-id="5aa48-110">Hypertext Transfer Protocol (HTTP)</span><span class="sxs-lookup"><span data-stu-id="5aa48-110">Hypertext Transfer Protocol (HTTP)</span></span>

    <span data-ttu-id="5aa48-111">HTTP usa TCP e viene usato dai server Web.</span><span class="sxs-lookup"><span data-stu-id="5aa48-111">HTTP uses TCP and is used by web servers.</span></span> <span data-ttu-id="5aa48-112">Lo schema "httpd://" indica che l'origine è scaricabile da un server Web.</span><span class="sxs-lookup"><span data-stu-id="5aa48-112">The "httpd://" scheme indicates that the source is downloadable from a web server.</span></span> <span data-ttu-id="5aa48-113">Il protocollo HTTP viene usato anche in caso di firewall, che in genere sono configurati per accettare richieste HTTP e in genere rifiutano altri protocolli di streaming.</span><span class="sxs-lookup"><span data-stu-id="5aa48-113">HTTP is also used in case of firewalls, which are usually configured to accept HTTP requests and typically reject other streaming protocols.</span></span>

<span data-ttu-id="5aa48-114">L'applicazione può ottenere i protocolli supportati da Media Foundation usando l'interfaccia [**IMFNetSchemeHandlerConfig**](/windows/desktop/api/mfidl/nn-mfidl-imfnetschemehandlerconfig) .</span><span class="sxs-lookup"><span data-stu-id="5aa48-114">The application can get the protocols supported by Media Foundation by using the [**IMFNetSchemeHandlerConfig**](/windows/desktop/api/mfidl/nn-mfidl-imfnetschemehandlerconfig) interface.</span></span> <span data-ttu-id="5aa48-115">A tale scopo, l'applicazione deve prima recuperare il numero di protocolli chiamando [**IMFNetSchemeHandlerConfig:: GetNumberOfSupportedProtocols**](/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-getnumberofsupportedprotocols) e quindi ottenere il tipo di protocollo basato sull'indice chiamando [**IMFNetSchemeHandlerConfig:: GetSupportedProtocolType**](/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-getsupportedprotocoltype).</span><span class="sxs-lookup"><span data-stu-id="5aa48-115">To do this, the application must first retrieve the number of protocols, by calling [**IMFNetSchemeHandlerConfig::GetNumberOfSupportedProtocols**](/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-getnumberofsupportedprotocols) and then get the protocol type based on the index by calling [**IMFNetSchemeHandlerConfig::GetSupportedProtocolType**](/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-getsupportedprotocoltype).</span></span> <span data-ttu-id="5aa48-116">Questo metodo restituisce uno dei valori definiti nell'enumerazione del [**\_ \_ tipo di protocollo MFNETSOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) .</span><span class="sxs-lookup"><span data-stu-id="5aa48-116">This method returns one of the values defined in the [**MFNETSOURCE\_PROTOCOL\_TYPE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) enumeration.</span></span>

<span data-ttu-id="5aa48-117">L'applicazione può inoltre ottenere gli schemi supportati dal resolver di origine chiamando la funzione [**MFGetSupportedSchemes**](/windows/desktop/api/mfidl/nf-mfidl-mfgetsupportedschemes) .</span><span class="sxs-lookup"><span data-stu-id="5aa48-117">The application can also get the schemes supported by the source resolver by calling the [**MFGetSupportedSchemes**](/windows/desktop/api/mfidl/nf-mfidl-mfgetsupportedschemes) function.</span></span>

## <a name="protocol-rollover"></a><span data-ttu-id="5aa48-118">Rollover del protocollo</span><span class="sxs-lookup"><span data-stu-id="5aa48-118">Protocol Rollover</span></span>

<span data-ttu-id="5aa48-119">Quando un'applicazione specifica "mms://" come schema URL, il resolver di origine esegue un'operazione di *rollover del protocollo* .</span><span class="sxs-lookup"><span data-stu-id="5aa48-119">When an application specifies "mms://" as the URL scheme, the source resolver performs a *protocol rollover* operation.</span></span> <span data-ttu-id="5aa48-120">In questo processo, il resolver di origine determina il protocollo migliore per l'origine di rete da usare per ottenere il contenuto.</span><span class="sxs-lookup"><span data-stu-id="5aa48-120">In this process, the source resolver determines the best protocol for the network source to use for getting the content.</span></span> <span data-ttu-id="5aa48-121">In genere, per lo streaming di contenuti multimediali, RTSP con UDP (RTSP) è più efficiente di HTTP.</span><span class="sxs-lookup"><span data-stu-id="5aa48-121">Typically, for media steaming, RTSP with UDP (RTSPU) is more efficient than HTTP.</span></span> <span data-ttu-id="5aa48-122">Tuttavia, se il contenuto è ospitato in un server Web, HTTP è la scelta migliore.</span><span class="sxs-lookup"><span data-stu-id="5aa48-122">However, if the content is hosted on a web server, HTTP is a better choice.</span></span>

<span data-ttu-id="5aa48-123">Il rollover del protocollo può verificarsi anche quando un tentativo di usare il protocollo specificato nello schema URL ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="5aa48-123">Protocol rollover can also occur when an attempt to use the protocol specified in the URL scheme fails.</span></span> <span data-ttu-id="5aa48-124">Un protocollo, ad esempio, può avere esito negativo quando un firewall blocca i pacchetti UDP.</span><span class="sxs-lookup"><span data-stu-id="5aa48-124">For example, a protocol can fail when a firewall blocks UDP packets.</span></span> <span data-ttu-id="5aa48-125">In questo caso, il resolver di origine passa a HTTP.</span><span class="sxs-lookup"><span data-stu-id="5aa48-125">In this case, the source resolver switches to HTTP.</span></span>

<span data-ttu-id="5aa48-126">Il rollover del protocollo non si applica se lo schema URL contiene un protocollo specifico, ad esempio "rtspu://".</span><span class="sxs-lookup"><span data-stu-id="5aa48-126">Protocol rollover does not apply if the URL scheme contains a specific protocol, such as "rtspu://".</span></span> <span data-ttu-id="5aa48-127">Inoltre, il rollover non viene eseguito se l'autenticazione ha esito negativo o se il server ha raggiunto un limite di connessioni client.</span><span class="sxs-lookup"><span data-stu-id="5aa48-127">Also, rollover is not performed if authentication fails or the server has reached a limit of client connections.</span></span> <span data-ttu-id="5aa48-128">È consigliabile che le applicazioni specifichino lo schema "mms://" e consentono al resolver di origine di selezionare il protocollo migliore per lo scenario.</span><span class="sxs-lookup"><span data-stu-id="5aa48-128">It is recommended that applications specify the "mms://" scheme and allow the source resolver to select the best protocol for the scenario.</span></span>

<span data-ttu-id="5aa48-129">La tabella seguente elenca l'ordine di rollover.</span><span class="sxs-lookup"><span data-stu-id="5aa48-129">The following table lists the rollover order.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5aa48-130">Schemi consentiti</span><span class="sxs-lookup"><span data-stu-id="5aa48-130">Schemes allowed</span></span></th>
<th><span data-ttu-id="5aa48-131">Ordine di rollover del protocollo</span><span class="sxs-lookup"><span data-stu-id="5aa48-131">Protocol rollover order</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5aa48-132">mms://o rtsp://</span><span class="sxs-lookup"><span data-stu-id="5aa48-132">mms:// or rtsp://</span></span></td>
<td><span data-ttu-id="5aa48-133">Cache veloce abilitata:</span><span class="sxs-lookup"><span data-stu-id="5aa48-133">Fast Cache enabled:</span></span><br/>
<ol>
<li><span data-ttu-id="5aa48-134">RTSP con TCP (RTSPt)</span><span class="sxs-lookup"><span data-stu-id="5aa48-134">RTSP with TCP (RTSPT)</span></span><br/></li>
<li><span data-ttu-id="5aa48-135">RTSP con UDP (RTSPr)</span><span class="sxs-lookup"><span data-stu-id="5aa48-135">RTSP with UDP (RTSPU)</span></span><br/></li>
<li><span data-ttu-id="5aa48-136">Flusso HTTP</span><span class="sxs-lookup"><span data-stu-id="5aa48-136">HTTP Streaming</span></span><br/></li>
<li><span data-ttu-id="5aa48-137">Download HTTP (HTTPD)</span><span class="sxs-lookup"><span data-stu-id="5aa48-137">HTTP download (HTTPD)</span></span><br/></li>
</ol>
<span data-ttu-id="5aa48-138">Cache veloce disabilitata:</span><span class="sxs-lookup"><span data-stu-id="5aa48-138">Fast Cache disabled:</span></span><br/>
<ol>
<li><span data-ttu-id="5aa48-139">RTSPU</span><span class="sxs-lookup"><span data-stu-id="5aa48-139">RTSPU</span></span><br/></li>
<li><span data-ttu-id="5aa48-140">RTSPT</span><span class="sxs-lookup"><span data-stu-id="5aa48-140">RTSPT</span></span><br/></li>
<li><span data-ttu-id="5aa48-141">Flusso HTTP</span><span class="sxs-lookup"><span data-stu-id="5aa48-141">HTTP Streaming</span></span><br/></li>
<li><span data-ttu-id="5aa48-142">Download HTTP</span><span class="sxs-lookup"><span data-stu-id="5aa48-142">HTTP Download</span></span><br/></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5aa48-143">rtspu://</span><span class="sxs-lookup"><span data-stu-id="5aa48-143">rtspu://</span></span></td>
<td><span data-ttu-id="5aa48-144">RTSPU</span><span class="sxs-lookup"><span data-stu-id="5aa48-144">RTSPU</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5aa48-145">rtspt://</span><span class="sxs-lookup"><span data-stu-id="5aa48-145">rtspt://</span></span></td>
<td><span data-ttu-id="5aa48-146">RTSPT</span><span class="sxs-lookup"><span data-stu-id="5aa48-146">RTSPT</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5aa48-147"> https://</span><span class="sxs-lookup"><span data-stu-id="5aa48-147">https://</span></span></td>
<td><ol>
<li><span data-ttu-id="5aa48-148">HTTP</span><span class="sxs-lookup"><span data-stu-id="5aa48-148">HTTP</span></span><br/></li>
<li><span data-ttu-id="5aa48-149">HTTPD</span><span class="sxs-lookup"><span data-stu-id="5aa48-149">HTTPD</span></span><br/></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5aa48-150">httpd://</span><span class="sxs-lookup"><span data-stu-id="5aa48-150">httpd://</span></span></td>
<td><span data-ttu-id="5aa48-151">HTTPD</span><span class="sxs-lookup"><span data-stu-id="5aa48-151">HTTPD</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="retrieving-the-current-protocol"></a><span data-ttu-id="5aa48-152">Recupero del protocollo corrente</span><span class="sxs-lookup"><span data-stu-id="5aa48-152">Retrieving the Current Protocol</span></span>

<span data-ttu-id="5aa48-153">Dopo un'operazione di rollover del protocollo, l'origine di rete potrebbe usare un protocollo diverso da quello specificato dall'applicazione nello schema URL.</span><span class="sxs-lookup"><span data-stu-id="5aa48-153">After a protocol rollover operation, the network source might use a protocol other than the one specified by the application in the URL scheme.</span></span> <span data-ttu-id="5aa48-154">Il risultato del rollover del protocollo è disponibile per l'applicazione dopo che l'origine di rete stabilisce la connessione con il server multimediale.</span><span class="sxs-lookup"><span data-stu-id="5aa48-154">The protocol rollover result is available to the application after the network source establishes the connection with the media server.</span></span>

<span data-ttu-id="5aa48-155">Per ottenere il protocollo e il trasporto usati per ottenere il contenuto, l'applicazione può recuperare i valori delle proprietà per la proprietà del [ \_ protocollo MFNETSOURCE](mfnetsource-protocol-property.md) e la proprietà del [ \_ trasporto MFNETSOURCE](mfnetsource-transport-property.md) di un oggetto **IPropertyStore** dall'origine di rete.</span><span class="sxs-lookup"><span data-stu-id="5aa48-155">To get the protocol and transport that are used for getting the content, the application can retrieve the property values for the [MFNETSOURCE\_PROTOCOL](mfnetsource-protocol-property.md) property and the [MFNETSOURCE\_TRANSPORT](mfnetsource-transport-property.md) property of an **IPropertyStore** object from the network source.</span></span>

<span data-ttu-id="5aa48-156">Nel codice seguente viene illustrato come ottenere questi valori.</span><span class="sxs-lookup"><span data-stu-id="5aa48-156">The following code shows how to get these values.</span></span>


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



<span data-ttu-id="5aa48-157">Nel codice di esempio precedente, **IPropertyStore:: GetValue** Recupera il \_ valore del protocollo MFNETSOURCE, che è un membro dell'enumerazione del [**\_ \_ tipo di protocollo MFNETSOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) .</span><span class="sxs-lookup"><span data-stu-id="5aa48-157">In the preceding example code, **IPropertyStore::GetValue** retrieves the MFNETSOURCE\_PROTOCOL value, which is a member of the [**MFNETSOURCE\_PROTOCOL\_TYPE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_protocol_type) enumeration.</span></span> <span data-ttu-id="5aa48-158">Per il \_ trasporto MFNETSOURCE, il valore è un membro dell'enumerazione del [**\_ \_ tipo di trasporto MFNETSOURCE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_transport_type) .</span><span class="sxs-lookup"><span data-stu-id="5aa48-158">For MFNETSOURCE\_TRANSPORT, the value is a member of the [**MFNETSOURCE\_TRANSPORT\_TYPE**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_transport_type) enumeration.</span></span>

<span data-ttu-id="5aa48-159">In alternativa, l'applicazione può ottenere gli stessi valori usando il servizio MFNETSOURCE \_ Statistics \_ Service.</span><span class="sxs-lookup"><span data-stu-id="5aa48-159">Alternately, the application can get the same values by using the MFNETSOURCE\_STATISTICS\_SERVICE service.</span></span> <span data-ttu-id="5aa48-160">Per usare questo servizio, l'applicazione può chiamare la funzione [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) per ottenere l'archivio delle proprietà dall'origine di rete.</span><span class="sxs-lookup"><span data-stu-id="5aa48-160">To use this service, the application can call the [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) function to get the property store from the network source.</span></span> <span data-ttu-id="5aa48-161">Questo archivio di proprietà contiene le statistiche di rete nella proprietà [MFNETSOURCE \_ Statistics](mfnetsource-statistics-property.md) .</span><span class="sxs-lookup"><span data-stu-id="5aa48-161">This property store contains network statistics in the [MFNETSOURCE\_STATISTICS](mfnetsource-statistics-property.md) property.</span></span> <span data-ttu-id="5aa48-162">È possibile recuperare i valori di protocollo e di trasporto specificando \_ \_ l'ID del protocollo MFNETSOURCE e \_ \_ l'ID trasporto MFNETSOURCE, definiti nell'enumerazione [**MFNETSOURCE \_ Statistics \_ IDS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) .</span><span class="sxs-lookup"><span data-stu-id="5aa48-162">Protocol and transport values can be retrieved by specifying MFNETSOURCE\_PROTOCOL\_ID and MFNETSOURCE\_TRANSPORT\_ID—defined in the [**MFNETSOURCE\_STATISTICS\_IDS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) enumeration.</span></span> <span data-ttu-id="5aa48-163">Il codice seguente illustra come ottenere i valori di protocollo e trasporto usando il servizio MFNETSOURCE \_ Statistics \_ Service.</span><span class="sxs-lookup"><span data-stu-id="5aa48-163">The following code shows how to get the protocol and transport values by using the MFNETSOURCE\_STATISTICS\_SERVICE service.</span></span>


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



## <a name="enabling-and-disabling-protocols"></a><span data-ttu-id="5aa48-164">Abilitazione e disabilitazione di protocolli</span><span class="sxs-lookup"><span data-stu-id="5aa48-164">Enabling and Disabling Protocols</span></span>

<span data-ttu-id="5aa48-165">L'applicazione può configurare l'origine di rete in modo che alcuni protocolli vengano ignorati durante il processo di rollover.</span><span class="sxs-lookup"><span data-stu-id="5aa48-165">The application can configure the network source so that certain protocols are skipped during the rollover process.</span></span> <span data-ttu-id="5aa48-166">A tale scopo, vengono utilizzate le proprietà dell'origine di rete per disabilitare protocolli specifici.</span><span class="sxs-lookup"><span data-stu-id="5aa48-166">To do this, network source properties are used to disable specific protocols.</span></span> <span data-ttu-id="5aa48-167">Nella tabella seguente vengono illustrate le proprietà e i protocolli che controllano.</span><span class="sxs-lookup"><span data-stu-id="5aa48-167">The following table shows the properties and the protocols they control.</span></span>



| <span data-ttu-id="5aa48-168">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5aa48-168">Property</span></span>                                                                    | <span data-ttu-id="5aa48-169">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5aa48-169">Description</span></span>                                 |
|-----------------------------------------------------------------------------|---------------------------------------------|
| [<span data-ttu-id="5aa48-170">MFNETSOURCE \_ Abilita \_ http</span><span class="sxs-lookup"><span data-stu-id="5aa48-170">MFNETSOURCE\_ENABLE\_HTTP</span></span>](mfnetsource-enable-http-property.md)           | <span data-ttu-id="5aa48-171">Abilita o Disabilita HTTP e HTTPD.</span><span class="sxs-lookup"><span data-stu-id="5aa48-171">Enables or disables HTTP and HTTPD.</span></span>         |
| [<span data-ttu-id="5aa48-172">MFNETSOURCE \_ Abilita \_ RTSP</span><span class="sxs-lookup"><span data-stu-id="5aa48-172">MFNETSOURCE\_ENABLE\_RTSP</span></span>](mfnetsource-enable-rtsp-property.md)           | <span data-ttu-id="5aa48-173">Abilita o Disabilita RTSPr e RTSPt.</span><span class="sxs-lookup"><span data-stu-id="5aa48-173">Enables or disables RTSPU and RTSPT.</span></span>        |
| [<span data-ttu-id="5aa48-174">MFNETSOURCE \_ abilitare \_ TCP</span><span class="sxs-lookup"><span data-stu-id="5aa48-174">MFNETSOURCE\_ENABLE\_TCP</span></span>](mfnetsource-enable-tcp-property.md)             | <span data-ttu-id="5aa48-175">Abilita o Disabilita RTSPt.</span><span class="sxs-lookup"><span data-stu-id="5aa48-175">Enables or disables RTSPT.</span></span>                  |
| [<span data-ttu-id="5aa48-176">MFNETSOURCE \_ Abilita \_ UDP</span><span class="sxs-lookup"><span data-stu-id="5aa48-176">MFNETSOURCE\_ENABLE\_UDP</span></span>](mfnetsource-enable-udp-property.md)             | <span data-ttu-id="5aa48-177">Abilita o Disabilita RTSPr.</span><span class="sxs-lookup"><span data-stu-id="5aa48-177">Enables or disables RTSPU.</span></span>                  |
| [<span data-ttu-id="5aa48-178">MFNETSOURCE \_ abilitare il \_ download</span><span class="sxs-lookup"><span data-stu-id="5aa48-178">MFNETSOURCE\_ENABLE\_DOWNLOAD</span></span>](mfnetsource-enable-download-property.md)   | <span data-ttu-id="5aa48-179">Abilita o Disabilita HTTPD.</span><span class="sxs-lookup"><span data-stu-id="5aa48-179">Enables or disables HTTPD.</span></span>                  |
| [<span data-ttu-id="5aa48-180">MFNETSOURCE \_ Abilita \_ flusso</span><span class="sxs-lookup"><span data-stu-id="5aa48-180">MFNETSOURCE\_ENABLE\_STREAMING</span></span>](mfnetsource-enable-streaming-property.md) | <span data-ttu-id="5aa48-181">Abilita o Disabilita RTSPr, RTSPt e HTTP.</span><span class="sxs-lookup"><span data-stu-id="5aa48-181">Enables or disables RTSPU, RTSPT, and HTTP.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="5aa48-182">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5aa48-182">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5aa48-183">Rete in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5aa48-183">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




