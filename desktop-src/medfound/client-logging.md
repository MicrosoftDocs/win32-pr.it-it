---
description: Registrazione client
ms.assetid: f91b48ae-3989-4c1d-929c-8ab28d7c8177
title: Registrazione client (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb3cb03c8026e91acd567358e7004211b7fdde4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225832"
---
# <a name="client-logging-microsoft-media-foundation"></a><span data-ttu-id="72aa3-103">Registrazione client (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="72aa3-103">Client Logging (Microsoft Media Foundation)</span></span>

<span data-ttu-id="72aa3-104">L'origine di rete supporta la registrazione client, che consente al server multimediale di tenere traccia dell'attività dei client che si connettono.</span><span class="sxs-lookup"><span data-stu-id="72aa3-104">The network source supports client logging, which provides a way for the media server to track the activity of the clients that connect to it.</span></span> <span data-ttu-id="72aa3-105">I registri client consentono a un server di registrare le statistiche di connessione, rendering e flusso.</span><span class="sxs-lookup"><span data-stu-id="72aa3-105">Client logs enable a server to record connection, rendering, and streaming statistics.</span></span> <span data-ttu-id="72aa3-106">Questi log possono essere usati dai provider di contenuti in diversi scenari, ad esempio, per tracciare l'utilizzo del server multimediale e generare la fatturazione o per fornire contenuti di qualità adeguata a seconda della velocità della rete del client.</span><span class="sxs-lookup"><span data-stu-id="72aa3-106">These logs can be used by content providers in various scenarios, such as, to trace media server usage and generate billing, or to deliver suitable-quality content depending on the speed of the client's network.</span></span>

<span data-ttu-id="72aa3-107">Un file di log contiene diverse voci dell'evento client.</span><span class="sxs-lookup"><span data-stu-id="72aa3-107">A log file contains several client event entries.</span></span> <span data-ttu-id="72aa3-108">Ogni voce di log contiene un numero di campi delimitati da spazi.</span><span class="sxs-lookup"><span data-stu-id="72aa3-108">Each log entry contains a number of space-delimited fields.</span></span> <span data-ttu-id="72aa3-109">Esistono due tipi di log client: *rendering* (riproduzione) e *streaming* (ricezione).</span><span class="sxs-lookup"><span data-stu-id="72aa3-109">There are two types of client logs: *rendering* (playing) and *streaming* (receiving).</span></span> <span data-ttu-id="72aa3-110">Poiché il contenuto può essere riprodotto e trasmesso simultaneamente, il client può inviare una combinazione di entrambi i tipi di dati di log.</span><span class="sxs-lookup"><span data-stu-id="72aa3-110">Because content can be played and streamed simultaneously, the client can send a combination of both types of log data.</span></span> <span data-ttu-id="72aa3-111">In alcuni casi, per la stessa sessione possono esistere due voci di log.</span><span class="sxs-lookup"><span data-stu-id="72aa3-111">In certain cases, two log entries can exist for the same session.</span></span> <span data-ttu-id="72aa3-112">Ad esempio, quando la cache veloce è abilitata, il client può completare la ricezione del contenuto trasmesso prima di completarne il rendering.</span><span class="sxs-lookup"><span data-stu-id="72aa3-112">For example, when Fast Cache is enabled, the client can finish receiving the streamed content before it finishes rendering it.</span></span> <span data-ttu-id="72aa3-113">In tal caso, i dati del log di streaming verrebbero inviati prima dei dati del log di rendering.</span><span class="sxs-lookup"><span data-stu-id="72aa3-113">In that case, the streaming log data would be sent before the rendering log data.</span></span>

<span data-ttu-id="72aa3-114">Il client invia i dati di log di rendering al server quando il client passa da qualsiasi stato di riproduzione (riproduzione, avanzamento rapido o riavvolgimento) a uno stato non di riproduzione (arresto, pausa, fine del flusso e inizio del flusso).</span><span class="sxs-lookup"><span data-stu-id="72aa3-114">The client sends rendering log data to the server when the client changes from any playing state (play, fast-forward, or rewind) to a non-playing state (stop, pause, end of stream, and beginning of stream).</span></span> <span data-ttu-id="72aa3-115">Quando vengono inviati i dati di un log di rendering, viene effettuata una connessione direttamente al server multimediale o a un server proxy configurato.</span><span class="sxs-lookup"><span data-stu-id="72aa3-115">When data for a rendering log is submitted, a connection is made directly to the media server or a configured proxy server.</span></span>

<span data-ttu-id="72aa3-116">Se il contenuto viene archiviato in un file di cache locale temporaneo nel computer in cui è in esecuzione il client di, il client può leggere un file dalla cache locale e inviare i dati del log di rendering per indicare che ha eseguito il contenuto.</span><span class="sxs-lookup"><span data-stu-id="72aa3-116">If the content is stored in a temporary local cache file on the computer that is running the client, the client can read a file from its local cache and submit the rendering log data to indicate that it has played the content.</span></span> <span data-ttu-id="72aa3-117">In questo caso, il client legge un file dalla cache locale, la voce del log di rendering non contiene statistiche di rete e il protocollo è impostato su cache.</span><span class="sxs-lookup"><span data-stu-id="72aa3-117">In this case, the client reads a file from its local cache, the rendering log entry does not contain any network statistics, and the protocol is set to Cache.</span></span>

<span data-ttu-id="72aa3-118">Il client invia i dati di log di streaming al server per indicare il modo in cui il client ha ricevuto il contenuto, ma non come è stato eseguito il rendering.</span><span class="sxs-lookup"><span data-stu-id="72aa3-118">The client sends streaming log data to the server to indicate how the client received the content, but not how it was rendered.</span></span> <span data-ttu-id="72aa3-119">Il client può inviare il log di streaming Long prima che il client completi il rendering del contenuto.</span><span class="sxs-lookup"><span data-stu-id="72aa3-119">The client can send the streaming log long before the client finishes rendering the content.</span></span>

<span data-ttu-id="72aa3-120">In questo argomento non vengono fornite informazioni su tutti i campi del log.</span><span class="sxs-lookup"><span data-stu-id="72aa3-120">This topic does not provide information about all the log fields.</span></span> <span data-ttu-id="72aa3-121">Per un riferimento completo, vedere [struttura dei dati del log di Windows Media](/openspecs/windows_protocols/ms-wmlog/42c620eb-0d77-4350-b070-bcd1e182fe84).</span><span class="sxs-lookup"><span data-stu-id="72aa3-121">For a complete reference, see [Windows Media Log Data Structure](/openspecs/windows_protocols/ms-wmlog/42c620eb-0d77-4350-b070-bcd1e182fe84).</span></span>

## <a name="configuring-log-fields"></a><span data-ttu-id="72aa3-122">Configurazione di campi di log</span><span class="sxs-lookup"><span data-stu-id="72aa3-122">Configuring Log Fields</span></span>

<span data-ttu-id="72aa3-123">Media Foundation consente al client di configurare l'origine di rete usando le proprietà.</span><span class="sxs-lookup"><span data-stu-id="72aa3-123">Media Foundation enables the client to configure the network source by using properties.</span></span> <span data-ttu-id="72aa3-124">L'applicazione deve impostare le proprietà appropriate in un archivio di proprietà e passarla a uno dei metodi del resolver di origine.</span><span class="sxs-lookup"><span data-stu-id="72aa3-124">The application must set the appropriate properties in a property store and pass it to one of the source resolver methods.</span></span> <span data-ttu-id="72aa3-125">Il resolver di origine crea l'origine di rete come richiesto e apre una connessione con il server.</span><span class="sxs-lookup"><span data-stu-id="72aa3-125">The source resolver creates the network source as requested and opens a connection with the server.</span></span> <span data-ttu-id="72aa3-126">Se la connessione ha esito positivo, il client invia informazioni su se stesso.</span><span class="sxs-lookup"><span data-stu-id="72aa3-126">If the connection is successful, the client sends information about itself.</span></span>

<span data-ttu-id="72aa3-127">Nella tabella seguente vengono descritti i campi di log e le proprietà corrispondenti che un'applicazione può impostare tramite il resolver di origine.</span><span class="sxs-lookup"><span data-stu-id="72aa3-127">The following table describes the log fields and the corresponding properties that an application can set through the source resolver.</span></span> <span data-ttu-id="72aa3-128">Queste informazioni non cambiano durante la sessione.</span><span class="sxs-lookup"><span data-stu-id="72aa3-128">This information does not change during the session.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="72aa3-129">Campo di registrazione</span><span class="sxs-lookup"><span data-stu-id="72aa3-129">Logging field</span></span></th>
<th><span data-ttu-id="72aa3-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="72aa3-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="72aa3-131">c-playerid</span><span class="sxs-lookup"><span data-stu-id="72aa3-131">c-playerid</span></span></td>
<td><span data-ttu-id="72aa3-132">Identificazione univoca del lettore.</span><span class="sxs-lookup"><span data-stu-id="72aa3-132">Unique identification of the player.</span></span> <span data-ttu-id="72aa3-133">Queste informazioni vengono inviate all'inizio della connessione.</span><span class="sxs-lookup"><span data-stu-id="72aa3-133">This information is sent at the beginning of the connection.</span></span> <span data-ttu-id="72aa3-134">Si tratta in genere di un GUID del client.</span><span class="sxs-lookup"><span data-stu-id="72aa3-134">Typically, this is a GUID of the client.</span></span> <span data-ttu-id="72aa3-135">Il client può inviare queste informazioni al server nella proprietà <a href="mfnetsource-playerid-property.md"><strong>MFNETSOURCE_PLAYERID</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="72aa3-135">The client can send this information to the server in the <a href="mfnetsource-playerid-property.md"><strong>MFNETSOURCE_PLAYERID</strong></a> property.</span></span><br/> <span data-ttu-id="72aa3-136">Il client invia queste informazioni al server all'inizio della connessione.</span><span class="sxs-lookup"><span data-stu-id="72aa3-136">The client sends this information to the server at the beginning of the connection.</span></span><br/> <span data-ttu-id="72aa3-137">Valore di esempio: &quot; {c579d042-CECC-11D1-BB31-00a0c9603954}&quot;</span><span class="sxs-lookup"><span data-stu-id="72aa3-137">Sample value: &quot;{c579d042-cecc-11d1-bb31-00a0c9603954}&quot;</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="72aa3-138">c-playerversion</span><span class="sxs-lookup"><span data-stu-id="72aa3-138">c-playerversion</span></span></td>
<td><span data-ttu-id="72aa3-139">Numero di versione del lettore inviato all'inizio della connessione.</span><span class="sxs-lookup"><span data-stu-id="72aa3-139">The version number of the player that is sent at the beginning of the connection.</span></span> <span data-ttu-id="72aa3-140">Il client può inviare queste informazioni al server nella proprietà <a href="mfnetsource-playerversion-property.md"><strong>MFNETSOURCE_PLAYERVERSION</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="72aa3-140">The client can send this information to the server in the <a href="mfnetsource-playerversion-property.md"><strong>MFNETSOURCE_PLAYERVERSION</strong></a> property.</span></span><br/> <span data-ttu-id="72aa3-141">Il client invia queste informazioni al server all'inizio della connessione.</span><span class="sxs-lookup"><span data-stu-id="72aa3-141">The client sends this information to the server at the beginning of the connection.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="72aa3-142">CS (User-Agent)</span><span class="sxs-lookup"><span data-stu-id="72aa3-142">cs(User-Agent)</span></span></td>
<td><span data-ttu-id="72aa3-143">Tipo di browser utilizzato se il lettore è incorporato in un browser.</span><span class="sxs-lookup"><span data-stu-id="72aa3-143">Browser type used if the player was embedded in a browser.</span></span> <span data-ttu-id="72aa3-144">Questo valore può essere impostato dal client nella proprietà <a href="mfnetsource-browseruseragent-property.md"><strong>MFNETSOURCE_BROWSERUSERAGENT</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="72aa3-144">This value can be set by the client in the <a href="mfnetsource-browseruseragent-property.md"><strong>MFNETSOURCE_BROWSERUSERAGENT</strong></a> property.</span></span><br/> <span data-ttu-id="72aa3-145">Se il lettore non è incorporato, questo campo fa riferimento all'agente utente del client che ha generato il log.</span><span class="sxs-lookup"><span data-stu-id="72aa3-145">If the player was not embedded, this field refers to the user agent of the client that generated the log.</span></span> <span data-ttu-id="72aa3-146">In questo caso, il client deve impostare la proprietà <a href="mfnetsource-playeruseragent-property.md"><strong>MFNETSOURCE_PLAYERUSERAGENT</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="72aa3-146">In this case, the client must set the <a href="mfnetsource-playeruseragent-property.md"><strong>MFNETSOURCE_PLAYERUSERAGENT</strong></a> property.</span></span><br/> <span data-ttu-id="72aa3-147">Il client invia queste informazioni al server all'inizio della connessione.</span><span class="sxs-lookup"><span data-stu-id="72aa3-147">The client sends this information to the server at the beginning of the connection.</span></span><br/> <span data-ttu-id="72aa3-148">Valore di esempio: &quot; Mozilla/4.0 _ (compatibile; _MSIE_4.01; _Windows_98)&quot;</span><span class="sxs-lookup"><span data-stu-id="72aa3-148">Sample value: &quot;Mozilla/4.0_(compatible;_MSIE_4.01;_Windows_98)&quot;</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="72aa3-149">CS (Referer)</span><span class="sxs-lookup"><span data-stu-id="72aa3-149">cs(Referer)</span></span></td>
<td><span data-ttu-id="72aa3-150">URL della pagina Web in cui il lettore è stato incorporato (se era incorporato).</span><span class="sxs-lookup"><span data-stu-id="72aa3-150">URL of the webpage in which the player was embedded (if it was embedded).</span></span> <span data-ttu-id="72aa3-151">Il client può inviare queste informazioni al server nella proprietà <a href="mfnetsource-browserwebpage-property.md"><strong>MFNETSOURCE_BROWSERWEBPAGE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="72aa3-151">The client can send this information to the server in the <a href="mfnetsource-browserwebpage-property.md"><strong>MFNETSOURCE_BROWSERWEBPAGE</strong></a> property.</span></span><br/> <span data-ttu-id="72aa3-152">Il client invia queste informazioni al server alla fine della connessione.</span><span class="sxs-lookup"><span data-stu-id="72aa3-152">The client sends this information to the server at the end of the connection.</span></span><br/> <span data-ttu-id="72aa3-153">Valore di esempio: &quot; https://www.example.microsoft.com&quot ;</span><span class="sxs-lookup"><span data-stu-id="72aa3-153">Sample value: &quot;https://www.example.microsoft.com&quot;</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="72aa3-154">c-hostexe</span><span class="sxs-lookup"><span data-stu-id="72aa3-154">c-hostexe</span></span></td>
<td><span data-ttu-id="72aa3-155">Per le voci di log del lettore, il programma host (exe) eseguito.</span><span class="sxs-lookup"><span data-stu-id="72aa3-155">For player log entries, the host program (.exe) that was run.</span></span> <span data-ttu-id="72aa3-156">Ad esempio, una pagina Web in un browser, un'applet Microsoft Visual Basic o un lettore autonomo.</span><span class="sxs-lookup"><span data-stu-id="72aa3-156">For example, a webpage in a browser, a Microsoft Visual Basic applet, or a stand-alone player.</span></span> <span data-ttu-id="72aa3-157">Il client può inviare queste informazioni al server nella proprietà <a href="mfnetsource-hostexe-property.md"><strong>MFNETSOURCE_HOSTEXE</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="72aa3-157">The client can send this information to the server in the <a href="mfnetsource-hostexe-property.md"><strong>MFNETSOURCE_HOSTEXE</strong></a> property.</span></span><br/> <span data-ttu-id="72aa3-158">Il client invia queste informazioni al server alla fine della connessione.</span><span class="sxs-lookup"><span data-stu-id="72aa3-158">The client sends this information to the server at the end of the connection.</span></span><br/> <span data-ttu-id="72aa3-159">Valori di esempio:</span><span class="sxs-lookup"><span data-stu-id="72aa3-159">Sample values:</span></span><br/>
<ul>
<li><span data-ttu-id="72aa3-160">&quot;iexplore.exe&quot;</span><span class="sxs-lookup"><span data-stu-id="72aa3-160">&quot;iexplore.exe&quot;</span></span></li>
<li><span data-ttu-id="72aa3-161">&quot;myplayer.exe&quot;</span><span class="sxs-lookup"><span data-stu-id="72aa3-161">&quot;myplayer.exe&quot;</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="72aa3-162">c-hostexever</span><span class="sxs-lookup"><span data-stu-id="72aa3-162">c-hostexever</span></span></td>
<td><span data-ttu-id="72aa3-163">Numero di versione del programma host (exe).</span><span class="sxs-lookup"><span data-stu-id="72aa3-163">Host program (.exe) version number.</span></span> <span data-ttu-id="72aa3-164">Il client può inviare queste informazioni al server nella proprietà <a href="mfnetsource-hostversion-property.md"><strong>MFNETSOURCE_HOSTVERSION</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="72aa3-164">The client can send this information to the server in the <a href="mfnetsource-hostversion-property.md"><strong>MFNETSOURCE_HOSTVERSION</strong></a> property.</span></span><br/> <span data-ttu-id="72aa3-165">Il client invia queste informazioni al server alla fine della connessione.</span><span class="sxs-lookup"><span data-stu-id="72aa3-165">The client sends this information to the server at the end of the connection.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="72aa3-166">Nell'esempio di codice seguente viene illustrata la configurazione dell'origine di rete da parte di un'applicazione client.</span><span class="sxs-lookup"><span data-stu-id="72aa3-166">The following code example shows how a client application configures the network source.</span></span> <span data-ttu-id="72aa3-167">Questo esempio Mostra come impostare il campo del log "c-hostexe".</span><span class="sxs-lookup"><span data-stu-id="72aa3-167">This example sets the "c-hostexe" log field.</span></span>


```C++
// Creates a media source from a URL.
//
// This example demonstrates how to set the MFNETSOURCE_HOSTEXE
// configuration property on the network source.

HRESULT CreateMediaSourceWithLogParams(
    PCWSTR pszURL, 
    IMFMediaSource **ppSource
    )
{
    IPropertyStore *pConfig = NULL;

    // Configure the property store.
    HRESULT hr = PSCreateMemoryPropertyStore(IID_PPV_ARGS(&pConfig));

    if (SUCCEEDED(hr))
    {
        PROPERTYKEY key;
        key.fmtid =  MFNETSOURCE_HOSTEXE;
        key.pid = 0;

        PROPVARIANT var;
        var.vt = VT_LPWSTR;
        var.pwszVal = L"MyPlayer.exe";

        hr = pConfig->SetValue(key, var);
    }

    // Create the source media source.
    if (SUCCEEDED(hr))
    {
        hr = CreateMediaSource(pszURL, pConfig, ppSource);
    }

    SafeRelease(&pConfig);
    return hr;
}
```



## <a name="retrieving-network-statistics"></a><span data-ttu-id="72aa3-168">Recupero delle statistiche di rete</span><span class="sxs-lookup"><span data-stu-id="72aa3-168">Retrieving Network Statistics</span></span>

<span data-ttu-id="72aa3-169">Quando l'applicazione chiama uno dei metodi del resolver di origine, crea l'origine di rete, imposta le proprietà specificate nell'archivio delle proprietà e apre una sessione con il server multimediale.</span><span class="sxs-lookup"><span data-stu-id="72aa3-169">When the application calls one of the source resolver methods, it creates the network source, sets the properties specified in the property store, and opens a session with the media server.</span></span> <span data-ttu-id="72aa3-170">Oltre alle informazioni configurabili descritte nella sezione precedente, i dati aggiuntivi vengono trasferiti tra il server e il client all'inizio della sessione, durante il flusso e quando la sessione viene chiusa.</span><span class="sxs-lookup"><span data-stu-id="72aa3-170">In addition to the configurable information described in the previous section, additional data is transferred between the server and the client at the beginning of the session, during streaming, and when the session is closed.</span></span>

<span data-ttu-id="72aa3-171">L'applicazione può recuperare le statistiche di rete usando l'identificatore del servizio **MFNETSOURCE \_ Statistics \_** .</span><span class="sxs-lookup"><span data-stu-id="72aa3-171">The application can retrieve network statistics by using the **MFNETSOURCE\_STATISTICS\_SERVICE** service identifier.</span></span> <span data-ttu-id="72aa3-172">Per usare questo servizio, l'applicazione può chiamare la funzione [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) per ottenere l'archivio delle proprietà contenente le statistiche di rete nella proprietà [**MFNETSOURCE \_ Statistics**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) .</span><span class="sxs-lookup"><span data-stu-id="72aa3-172">To use this service, the application can call the [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) function to get the property store that contains network statistics in the [**MFNETSOURCE\_STATISTICS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) property.</span></span> <span data-ttu-id="72aa3-173">È possibile recuperare valori specifici fornendo l'identificatore corrispondente definito nell'enumerazione **MFNETSOURCE \_ Statistics \_ IDS** .</span><span class="sxs-lookup"><span data-stu-id="72aa3-173">Specific values can be retrieved by providing the corresponding identifier defined in the **MFNETSOURCE\_STATISTICS\_IDS** enumeration.</span></span>

<span data-ttu-id="72aa3-174">Nell'esempio di codice seguente viene illustrato come utilizzare il servizio per ottenere il numero di pacchetti ricevuti dal client.</span><span class="sxs-lookup"><span data-stu-id="72aa3-174">The following code example shows how to use the service to get the number of packets received by the client.</span></span>


```C++
HRESULT GetPacketsReceived(IMFMediaSession *pSession, DWORD *pcPackets)
{
    IPropertyStore *pProp = NULL;
    PROPVARIANT var;

    // Get the property store from the media session.
    HRESULT hr = MFGetService(
        pSession, 
        MFNETSOURCE_STATISTICS_SERVICE, 
        IID_PPV_ARGS(&pProp)
        );

    // Get the number of packets received by the client.

    if (SUCCEEDED(hr))
    {
        PROPERTYKEY key;
        key.fmtid = MFNETSOURCE_STATISTICS;
        key.pid = MFNETSOURCE_RECVPACKETS_ID;

        hr = pProp->GetValue(key, &var);
    }

    if (SUCCEEDED(hr))
    {
        *pcPackets = var.lVal;
    }

    PropVariantClear(&var);
    SafeRelease(&pProp);
    return hr;
}
```



<span data-ttu-id="72aa3-175">Nell'elenco seguente vengono descritti alcuni degli identificatori delle statistiche di rete definiti in [**MFNETSOURCE \_ Statistics \_ IDS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids).</span><span class="sxs-lookup"><span data-stu-id="72aa3-175">The following list describes some of the network statistics identifiers defined in [**MFNETSOURCE\_STATISTICS\_IDS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids).</span></span>



| <span data-ttu-id="72aa3-176">Identificatore statistiche di rete</span><span class="sxs-lookup"><span data-stu-id="72aa3-176">Network statistics identifier</span></span>              | <span data-ttu-id="72aa3-177">Descrizione</span><span class="sxs-lookup"><span data-stu-id="72aa3-177">Description</span></span>                                                                                                                                                                                                                |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72aa3-178">**\_ID AVGBANDWIDTHBPS \_ MFNETSOURCE**</span><span class="sxs-lookup"><span data-stu-id="72aa3-178">**MFNETSOURCE\_AVGBANDWIDTHBPS\_ID**</span></span>       | <span data-ttu-id="72aa3-179">Larghezza di banda media (in bit al secondo) a cui il client è connesso al server.</span><span class="sxs-lookup"><span data-stu-id="72aa3-179">Average bandwidth (in bits per second) at which the client was connected to the server.</span></span> <span data-ttu-id="72aa3-180">Il valore viene calcolato nell'intera durata della connessione.</span><span class="sxs-lookup"><span data-stu-id="72aa3-180">The value is calculated across the entire duration of the connection.</span></span>                                                              |
| <span data-ttu-id="72aa3-181">**\_ID BUFFERINGCOUNT \_ MFNETSOURCE**</span><span class="sxs-lookup"><span data-stu-id="72aa3-181">**MFNETSOURCE\_BUFFERINGCOUNT\_ID**</span></span>        | <span data-ttu-id="72aa3-182">Numero di volte in cui il client è memorizzato nel buffer durante la riproduzione del flusso.</span><span class="sxs-lookup"><span data-stu-id="72aa3-182">Number of times the client buffered while playing the stream.</span></span>                                                                                                                                                              |
| <span data-ttu-id="72aa3-183">**\_ID BYTESRECEIVED \_ MFNETSOURCE**</span><span class="sxs-lookup"><span data-stu-id="72aa3-183">**MFNETSOURCE\_BYTESRECEIVED\_ID**</span></span>         | <span data-ttu-id="72aa3-184">Numero di byte ricevuti dal client dal server.</span><span class="sxs-lookup"><span data-stu-id="72aa3-184">Number of bytes received by the client from the server.</span></span> <span data-ttu-id="72aa3-185">Il valore non include alcun overhead aggiunto dallo stack di rete.</span><span class="sxs-lookup"><span data-stu-id="72aa3-185">The value does not include any overhead that is added by the network stack.</span></span> <span data-ttu-id="72aa3-186">Lo stesso contenuto trasmesso tramite protocolli diversi può produrre valori diversi.</span><span class="sxs-lookup"><span data-stu-id="72aa3-186">The same content streamed by using different protocols can result in different values.</span></span> |
| <span data-ttu-id="72aa3-187">**\_ID LINKBANDWIDTH \_ MFNETSOURCE**</span><span class="sxs-lookup"><span data-stu-id="72aa3-187">**MFNETSOURCE\_LINKBANDWIDTH\_ID**</span></span>         | <span data-ttu-id="72aa3-188">Larghezza di banda massima disponibile del client in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="72aa3-188">Maximum available bandwidth of the client in bits per second.</span></span>                                                                                                                                                              |
| <span data-ttu-id="72aa3-189">**\_ID LOSTPACKETS \_ MFNETSOURCE**</span><span class="sxs-lookup"><span data-stu-id="72aa3-189">**MFNETSOURCE\_LOSTPACKETS\_ID**</span></span>           | <span data-ttu-id="72aa3-190">Numero di pacchetti inviati dal server ma persi durante la trasmissione e mai riprodotti dal client.</span><span class="sxs-lookup"><span data-stu-id="72aa3-190">Number of packets sent by the server but lost during transmission, and never played by the client.</span></span> <span data-ttu-id="72aa3-191">Il valore non include i pacchetti TCP o UDP.</span><span class="sxs-lookup"><span data-stu-id="72aa3-191">The value does not include TCP or UDP packets.</span></span>                                                                          |
| <span data-ttu-id="72aa3-192">**\_ID RECVPACKETS \_ MFNETSOURCE**</span><span class="sxs-lookup"><span data-stu-id="72aa3-192">**MFNETSOURCE\_RECVPACKETS\_ID**</span></span>           | <span data-ttu-id="72aa3-193">Numero di pacchetti ricevuti dal server. il valore non include i pacchetti TCP o UDP.</span><span class="sxs-lookup"><span data-stu-id="72aa3-193">Number of packets received from the server The value does not include TCP or UDP packets.</span></span>                                                                                                                                  |
| <span data-ttu-id="72aa3-194">**\_ID RECOVEREDBYECCPACKETS \_ MFNETSOURCE**</span><span class="sxs-lookup"><span data-stu-id="72aa3-194">**MFNETSOURCE\_RECOVEREDBYECCPACKETS\_ID**</span></span> | <span data-ttu-id="72aa3-195">Pacchetti persi nella rete ripristinati e ripristinati a livello di client.</span><span class="sxs-lookup"><span data-stu-id="72aa3-195">Packets lost in the network that were repaired and recovered at the client layer.</span></span> <span data-ttu-id="72aa3-196">Questo valore non include i pacchetti TCP o UDP.</span><span class="sxs-lookup"><span data-stu-id="72aa3-196">This value does not include TCP or UDP packets.</span></span>                                                                                          |
| <span data-ttu-id="72aa3-197">**\_ID RESENDSREQUESTED \_ MFNETSOURCE**</span><span class="sxs-lookup"><span data-stu-id="72aa3-197">**MFNETSOURCE\_RESENDSREQUESTED\_ID**</span></span>      | <span data-ttu-id="72aa3-198">Numero di richieste effettuate dal client per la ricezione di nuovi pacchetti.</span><span class="sxs-lookup"><span data-stu-id="72aa3-198">The number of requests made by the client to receive new packets.</span></span> <span data-ttu-id="72aa3-199">Questo valore non include i pacchetti TCP o UDP.</span><span class="sxs-lookup"><span data-stu-id="72aa3-199">This value does not include TCP or UDP packets.</span></span>                                                                                                          |
| <span data-ttu-id="72aa3-200">**\_ID RECOVEREDPACKETS \_ MFNETSOURCE**</span><span class="sxs-lookup"><span data-stu-id="72aa3-200">**MFNETSOURCE\_RECOVEREDPACKETS\_ID**</span></span>      | <span data-ttu-id="72aa3-201">Numero di pacchetti ripristinati perché sono stati inviati tramite UDP.</span><span class="sxs-lookup"><span data-stu-id="72aa3-201">Number of packets recovered because they were resent through UDP.</span></span> <span data-ttu-id="72aa3-202">Questo valore non include i pacchetti TCP o UDP.</span><span class="sxs-lookup"><span data-stu-id="72aa3-202">This value does not include TCP or UDP packets.</span></span> <span data-ttu-id="72aa3-203">Questo campo contiene uno zero, a meno che il client non usi il riinvio UDP.</span><span class="sxs-lookup"><span data-stu-id="72aa3-203">This field contains a zero unless the client is using UDP resend.</span></span>                                        |
| <span data-ttu-id="72aa3-204">**\_ID BUFFERPROGRESS \_ MFNETSOURCE**</span><span class="sxs-lookup"><span data-stu-id="72aa3-204">**MFNETSOURCE\_BUFFERPROGRESS\_ID**</span></span>        | <span data-ttu-id="72aa3-205">Percentuale del buffer di riproduzione riempita durante il buffering.</span><span class="sxs-lookup"><span data-stu-id="72aa3-205">The percentage of the playout buffer filled during buffering.</span></span>                                                                                                                                                              |
| <span data-ttu-id="72aa3-206">**\_ID del protocollo MFNETSOURCE \_**</span><span class="sxs-lookup"><span data-stu-id="72aa3-206">**MFNETSOURCE\_PROTOCOL\_ID**</span></span>              | <span data-ttu-id="72aa3-207">Protocollo utilizzato per accedere al flusso.</span><span class="sxs-lookup"><span data-stu-id="72aa3-207">Protocol used to access the stream.</span></span> <span data-ttu-id="72aa3-208">Questo può essere diverso dal protocollo richiesto dal client.</span><span class="sxs-lookup"><span data-stu-id="72aa3-208">This may differ from the protocol requested by the client.</span></span>                                                                                                                             |
| <span data-ttu-id="72aa3-209">**\_ID trasporto \_ MFNETSOURCE**</span><span class="sxs-lookup"><span data-stu-id="72aa3-209">**MFNETSOURCE\_TRANSPORT\_ID**</span></span>             | <span data-ttu-id="72aa3-210">Protocollo di trasporto usato per fornire il flusso.</span><span class="sxs-lookup"><span data-stu-id="72aa3-210">Transport protocol used to deliver the stream.</span></span> <span data-ttu-id="72aa3-211">Deve essere UDP o TCP.</span><span class="sxs-lookup"><span data-stu-id="72aa3-211">This must be either UDP or TCP.</span></span>                                                                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="72aa3-212">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="72aa3-212">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="72aa3-213">Funzionalità di origine della rete</span><span class="sxs-lookup"><span data-stu-id="72aa3-213">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="72aa3-214">Rete in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="72aa3-214">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

