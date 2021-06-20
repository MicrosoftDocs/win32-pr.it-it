---
description: Informazioni sulla registrazione client per Microsoft Media Foundation. La registrazione consente al server multimediale di tenere traccia dell'attività dei client che si connettono a esso.
ms.assetid: f91b48ae-3989-4c1d-929c-8ab28d7c8177
title: Registrazione client (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d994531ff16466054ca0645a35082a4845e4aa4
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409934"
---
# <a name="client-logging-microsoft-media-foundation"></a><span data-ttu-id="459c1-104">Registrazione client (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="459c1-104">Client Logging (Microsoft Media Foundation)</span></span>

<span data-ttu-id="459c1-105">L'origine di rete supporta la registrazione client, che consente al server multimediale di tenere traccia dell'attività dei client che si connettono a esso.</span><span class="sxs-lookup"><span data-stu-id="459c1-105">The network source supports client logging, which provides a way for the media server to track the activity of the clients that connect to it.</span></span> <span data-ttu-id="459c1-106">I log client consentono a un server di registrare le statistiche di connessione, rendering e streaming.</span><span class="sxs-lookup"><span data-stu-id="459c1-106">Client logs enable a server to record connection, rendering, and streaming statistics.</span></span> <span data-ttu-id="459c1-107">Questi log possono essere usati dai provider di contenuti in diversi scenari, ad esempio per tracciare l'utilizzo del server multimediale e generare la fatturazione o per distribuire contenuti di qualità appropriata a seconda della velocità della rete del client.</span><span class="sxs-lookup"><span data-stu-id="459c1-107">These logs can be used by content providers in various scenarios, such as, to trace media server usage and generate billing, or to deliver suitable-quality content depending on the speed of the client's network.</span></span>

<span data-ttu-id="459c1-108">Un file di log contiene diverse voci di eventi client.</span><span class="sxs-lookup"><span data-stu-id="459c1-108">A log file contains several client event entries.</span></span> <span data-ttu-id="459c1-109">Ogni voce di log contiene un numero di campi delimitati da spazi.</span><span class="sxs-lookup"><span data-stu-id="459c1-109">Each log entry contains a number of space-delimited fields.</span></span> <span data-ttu-id="459c1-110">Esistono due tipi di log client: *rendering* (riproduzione) *e streaming* (ricezione).</span><span class="sxs-lookup"><span data-stu-id="459c1-110">There are two types of client logs: *rendering* (playing) and *streaming* (receiving).</span></span> <span data-ttu-id="459c1-111">Poiché il contenuto può essere riprodotto e trasmesso contemporaneamente, il client può inviare una combinazione di entrambi i tipi di dati di log.</span><span class="sxs-lookup"><span data-stu-id="459c1-111">Because content can be played and streamed simultaneously, the client can send a combination of both types of log data.</span></span> <span data-ttu-id="459c1-112">In alcuni casi, possono esistere due voci di log per la stessa sessione.</span><span class="sxs-lookup"><span data-stu-id="459c1-112">In certain cases, two log entries can exist for the same session.</span></span> <span data-ttu-id="459c1-113">Ad esempio, quando La cache veloce è abilitata, il client può terminare la ricezione del contenuto trasmesso prima di completare il rendering.</span><span class="sxs-lookup"><span data-stu-id="459c1-113">For example, when Fast Cache is enabled, the client can finish receiving the streamed content before it finishes rendering it.</span></span> <span data-ttu-id="459c1-114">In tal caso, i dati del log di streaming vengono inviati prima dei dati del log di rendering.</span><span class="sxs-lookup"><span data-stu-id="459c1-114">In that case, the streaming log data would be sent before the rendering log data.</span></span>

<span data-ttu-id="459c1-115">Il client invia i dati del log di rendering al server quando il client cambia da qualsiasi stato di riproduzione (riproduzione, avanzamento rapido o riavvolgimento) a uno stato di non riproduzione (arresto, sospensione, fine del flusso e inizio del flusso).</span><span class="sxs-lookup"><span data-stu-id="459c1-115">The client sends rendering log data to the server when the client changes from any playing state (play, fast-forward, or rewind) to a non-playing state (stop, pause, end of stream, and beginning of stream).</span></span> <span data-ttu-id="459c1-116">Quando vengono inviati dati per un log di rendering, viene stabilita una connessione direttamente al server multimediale o a un server proxy configurato.</span><span class="sxs-lookup"><span data-stu-id="459c1-116">When data for a rendering log is submitted, a connection is made directly to the media server or a configured proxy server.</span></span>

<span data-ttu-id="459c1-117">Se il contenuto viene archiviato in un file di cache locale temporaneo nel computer che esegue il client, il client può leggere un file dalla cache locale e inviare i dati del log di rendering per indicare che ha riprodotto il contenuto.</span><span class="sxs-lookup"><span data-stu-id="459c1-117">If the content is stored in a temporary local cache file on the computer that is running the client, the client can read a file from its local cache and submit the rendering log data to indicate that it has played the content.</span></span> <span data-ttu-id="459c1-118">In questo caso, il client legge un file dalla cache locale, la voce del log di rendering non contiene statistiche di rete e il protocollo è impostato su Cache.</span><span class="sxs-lookup"><span data-stu-id="459c1-118">In this case, the client reads a file from its local cache, the rendering log entry does not contain any network statistics, and the protocol is set to Cache.</span></span>

<span data-ttu-id="459c1-119">Il client invia i dati del log di streaming al server per indicare come il client ha ricevuto il contenuto, ma non come è stato eseguito il rendering.</span><span class="sxs-lookup"><span data-stu-id="459c1-119">The client sends streaming log data to the server to indicate how the client received the content, but not how it was rendered.</span></span> <span data-ttu-id="459c1-120">Il client può inviare il log di streaming molto prima che il client finisca di eseguire il rendering del contenuto.</span><span class="sxs-lookup"><span data-stu-id="459c1-120">The client can send the streaming log long before the client finishes rendering the content.</span></span>

<span data-ttu-id="459c1-121">In questo argomento non vengono fornite informazioni su tutti i campi del log.</span><span class="sxs-lookup"><span data-stu-id="459c1-121">This topic does not provide information about all the log fields.</span></span> <span data-ttu-id="459c1-122">Per informazioni di riferimento complete, vedere [Struttura dei dati dei log di Windows Media.](/openspecs/windows_protocols/ms-wmlog/42c620eb-0d77-4350-b070-bcd1e182fe84)</span><span class="sxs-lookup"><span data-stu-id="459c1-122">For a complete reference, see [Windows Media Log Data Structure](/openspecs/windows_protocols/ms-wmlog/42c620eb-0d77-4350-b070-bcd1e182fe84).</span></span>

## <a name="configuring-log-fields"></a><span data-ttu-id="459c1-123">Configurazione dei campi di log</span><span class="sxs-lookup"><span data-stu-id="459c1-123">Configuring Log Fields</span></span>

<span data-ttu-id="459c1-124">Media Foundation consente al client di configurare l'origine di rete usando le proprietà .</span><span class="sxs-lookup"><span data-stu-id="459c1-124">Media Foundation enables the client to configure the network source by using properties.</span></span> <span data-ttu-id="459c1-125">L'applicazione deve impostare le proprietà appropriate in un archivio delle proprietà e passarlo a uno dei metodi del sistema di risoluzione di origine.</span><span class="sxs-lookup"><span data-stu-id="459c1-125">The application must set the appropriate properties in a property store and pass it to one of the source resolver methods.</span></span> <span data-ttu-id="459c1-126">Il sistema di risoluzione di origine crea l'origine di rete come richiesto e apre una connessione con il server.</span><span class="sxs-lookup"><span data-stu-id="459c1-126">The source resolver creates the network source as requested and opens a connection with the server.</span></span> <span data-ttu-id="459c1-127">Se la connessione ha esito positivo, il client invia informazioni su se stesso.</span><span class="sxs-lookup"><span data-stu-id="459c1-127">If the connection is successful, the client sends information about itself.</span></span>

<span data-ttu-id="459c1-128">Nella tabella seguente vengono descritti i campi del log e le proprietà corrispondenti che un'applicazione può impostare tramite il sistema di risoluzione dell'origine.</span><span class="sxs-lookup"><span data-stu-id="459c1-128">The following table describes the log fields and the corresponding properties that an application can set through the source resolver.</span></span> <span data-ttu-id="459c1-129">Queste informazioni non cambiano durante la sessione.</span><span class="sxs-lookup"><span data-stu-id="459c1-129">This information does not change during the session.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="459c1-130">Campo Registrazione</span><span class="sxs-lookup"><span data-stu-id="459c1-130">Logging field</span></span></th>
<th><span data-ttu-id="459c1-131">Descrizione</span><span class="sxs-lookup"><span data-stu-id="459c1-131">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="459c1-132">c-playerid</span><span class="sxs-lookup"><span data-stu-id="459c1-132">c-playerid</span></span></td>
<td><span data-ttu-id="459c1-133">Identificazione univoca del giocatore.</span><span class="sxs-lookup"><span data-stu-id="459c1-133">Unique identification of the player.</span></span> <span data-ttu-id="459c1-134">Queste informazioni vengono inviate all'inizio della connessione.</span><span class="sxs-lookup"><span data-stu-id="459c1-134">This information is sent at the beginning of the connection.</span></span> <span data-ttu-id="459c1-135">In genere, si tratta di un GUID del client.</span><span class="sxs-lookup"><span data-stu-id="459c1-135">Typically, this is a GUID of the client.</span></span> <span data-ttu-id="459c1-136">Il client può inviare queste informazioni al server nella <a href="mfnetsource-playerid-property.md"><strong>MFNETSOURCE_PLAYERID</strong></a> proprietà .</span><span class="sxs-lookup"><span data-stu-id="459c1-136">The client can send this information to the server in the <a href="mfnetsource-playerid-property.md"><strong>MFNETSOURCE_PLAYERID</strong></a> property.</span></span><br/> <span data-ttu-id="459c1-137">Il client invia queste informazioni al server all'inizio della connessione.</span><span class="sxs-lookup"><span data-stu-id="459c1-137">The client sends this information to the server at the beginning of the connection.</span></span><br/> <span data-ttu-id="459c1-138">Valore di esempio: &quot; {c579d042-cecc-11d1-bb31-00a0c9603954}&quot;</span><span class="sxs-lookup"><span data-stu-id="459c1-138">Sample value: &quot;{c579d042-cecc-11d1-bb31-00a0c9603954}&quot;</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="459c1-139">c-playerversion</span><span class="sxs-lookup"><span data-stu-id="459c1-139">c-playerversion</span></span></td>
<td><span data-ttu-id="459c1-140">Numero di versione del lettore inviato all'inizio della connessione.</span><span class="sxs-lookup"><span data-stu-id="459c1-140">The version number of the player that is sent at the beginning of the connection.</span></span> <span data-ttu-id="459c1-141">Il client può inviare queste informazioni al server nella <a href="mfnetsource-playerversion-property.md"><strong>MFNETSOURCE_PLAYERVERSION</strong></a> proprietà .</span><span class="sxs-lookup"><span data-stu-id="459c1-141">The client can send this information to the server in the <a href="mfnetsource-playerversion-property.md"><strong>MFNETSOURCE_PLAYERVERSION</strong></a> property.</span></span><br/> <span data-ttu-id="459c1-142">Il client invia queste informazioni al server all'inizio della connessione.</span><span class="sxs-lookup"><span data-stu-id="459c1-142">The client sends this information to the server at the beginning of the connection.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="459c1-143">cs(User-Agent)</span><span class="sxs-lookup"><span data-stu-id="459c1-143">cs(User-Agent)</span></span></td>
<td><span data-ttu-id="459c1-144">Tipo di browser usato se il lettore è stato incorporato in un browser.</span><span class="sxs-lookup"><span data-stu-id="459c1-144">Browser type used if the player was embedded in a browser.</span></span> <span data-ttu-id="459c1-145">Questo valore può essere impostato dal client nella <a href="mfnetsource-browseruseragent-property.md"><strong>proprietà</strong></a> MFNETSOURCE_BROWSERUSERAGENT.</span><span class="sxs-lookup"><span data-stu-id="459c1-145">This value can be set by the client in the <a href="mfnetsource-browseruseragent-property.md"><strong>MFNETSOURCE_BROWSERUSERAGENT</strong></a> property.</span></span><br/> <span data-ttu-id="459c1-146">Se il lettore non è stato incorporato, questo campo fa riferimento all'agente utente del client che ha generato il log.</span><span class="sxs-lookup"><span data-stu-id="459c1-146">If the player was not embedded, this field refers to the user agent of the client that generated the log.</span></span> <span data-ttu-id="459c1-147">In questo caso, il client deve impostare la <a href="mfnetsource-playeruseragent-property.md"><strong>MFNETSOURCE_PLAYERUSERAGENT</strong></a> proprietà .</span><span class="sxs-lookup"><span data-stu-id="459c1-147">In this case, the client must set the <a href="mfnetsource-playeruseragent-property.md"><strong>MFNETSOURCE_PLAYERUSERAGENT</strong></a> property.</span></span><br/> <span data-ttu-id="459c1-148">Il client invia queste informazioni al server all'inizio della connessione.</span><span class="sxs-lookup"><span data-stu-id="459c1-148">The client sends this information to the server at the beginning of the connection.</span></span><br/> <span data-ttu-id="459c1-149">Valore di esempio: &quot; Mozilla/4.0_(compatible;_MSIE_4.01;_Windows_98)&quot;</span><span class="sxs-lookup"><span data-stu-id="459c1-149">Sample value: &quot;Mozilla/4.0_(compatible;_MSIE_4.01;_Windows_98)&quot;</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="459c1-150">cs(Referer)</span><span class="sxs-lookup"><span data-stu-id="459c1-150">cs(Referer)</span></span></td>
<td><span data-ttu-id="459c1-151">URL della pagina Web in cui è stato incorporato il lettore (se è stato incorporato).</span><span class="sxs-lookup"><span data-stu-id="459c1-151">URL of the webpage in which the player was embedded (if it was embedded).</span></span> <span data-ttu-id="459c1-152">Il client può inviare queste informazioni al server nella <a href="mfnetsource-browserwebpage-property.md"><strong>proprietà MFNETSOURCE_BROWSERWEBPAGE.</strong></a></span><span class="sxs-lookup"><span data-stu-id="459c1-152">The client can send this information to the server in the <a href="mfnetsource-browserwebpage-property.md"><strong>MFNETSOURCE_BROWSERWEBPAGE</strong></a> property.</span></span><br/> <span data-ttu-id="459c1-153">Il client invia queste informazioni al server al termine della connessione.</span><span class="sxs-lookup"><span data-stu-id="459c1-153">The client sends this information to the server at the end of the connection.</span></span><br/> <span data-ttu-id="459c1-154">Valore di esempio: &quot; https://www.example.microsoft.com&quot ;</span><span class="sxs-lookup"><span data-stu-id="459c1-154">Sample value: &quot;https://www.example.microsoft.com&quot;</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="459c1-155">c-hostexe</span><span class="sxs-lookup"><span data-stu-id="459c1-155">c-hostexe</span></span></td>
<td><span data-ttu-id="459c1-156">Per le voci di log del lettore, il programma host (.exe) che è stato eseguito.</span><span class="sxs-lookup"><span data-stu-id="459c1-156">For player log entries, the host program (.exe) that was run.</span></span> <span data-ttu-id="459c1-157">Ad esempio, una pagina Web in un browser, un'applet di Microsoft Visual Basic o un lettore autonomo.</span><span class="sxs-lookup"><span data-stu-id="459c1-157">For example, a webpage in a browser, a Microsoft Visual Basic applet, or a stand-alone player.</span></span> <span data-ttu-id="459c1-158">Il client può inviare queste informazioni al server nella <a href="mfnetsource-hostexe-property.md"><strong>MFNETSOURCE_HOSTEXE</strong></a> proprietà .</span><span class="sxs-lookup"><span data-stu-id="459c1-158">The client can send this information to the server in the <a href="mfnetsource-hostexe-property.md"><strong>MFNETSOURCE_HOSTEXE</strong></a> property.</span></span><br/> <span data-ttu-id="459c1-159">Il client invia queste informazioni al server al termine della connessione.</span><span class="sxs-lookup"><span data-stu-id="459c1-159">The client sends this information to the server at the end of the connection.</span></span><br/> <span data-ttu-id="459c1-160">Valori di esempio:</span><span class="sxs-lookup"><span data-stu-id="459c1-160">Sample values:</span></span><br/>
<ul>
<li><span data-ttu-id="459c1-161">&quot;iexplore.exe&quot;</span><span class="sxs-lookup"><span data-stu-id="459c1-161">&quot;iexplore.exe&quot;</span></span></li>
<li><span data-ttu-id="459c1-162">&quot;myplayer.exe&quot;</span><span class="sxs-lookup"><span data-stu-id="459c1-162">&quot;myplayer.exe&quot;</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="459c1-163">c-hostexever</span><span class="sxs-lookup"><span data-stu-id="459c1-163">c-hostexever</span></span></td>
<td><span data-ttu-id="459c1-164">Numero di versione del programma host (.exe).</span><span class="sxs-lookup"><span data-stu-id="459c1-164">Host program (.exe) version number.</span></span> <span data-ttu-id="459c1-165">Il client può inviare queste informazioni al server nella <a href="mfnetsource-hostversion-property.md"><strong>MFNETSOURCE_HOSTVERSION</strong></a> proprietà .</span><span class="sxs-lookup"><span data-stu-id="459c1-165">The client can send this information to the server in the <a href="mfnetsource-hostversion-property.md"><strong>MFNETSOURCE_HOSTVERSION</strong></a> property.</span></span><br/> <span data-ttu-id="459c1-166">Il client invia queste informazioni al server al termine della connessione.</span><span class="sxs-lookup"><span data-stu-id="459c1-166">The client sends this information to the server at the end of the connection.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="459c1-167">Nell'esempio di codice seguente viene illustrato come un'applicazione client configura l'origine di rete.</span><span class="sxs-lookup"><span data-stu-id="459c1-167">The following code example shows how a client application configures the network source.</span></span> <span data-ttu-id="459c1-168">In questo esempio viene impostato il campo di log "c-hostexe".</span><span class="sxs-lookup"><span data-stu-id="459c1-168">This example sets the "c-hostexe" log field.</span></span>


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



## <a name="retrieving-network-statistics"></a><span data-ttu-id="459c1-169">Recupero delle statistiche di rete</span><span class="sxs-lookup"><span data-stu-id="459c1-169">Retrieving Network Statistics</span></span>

<span data-ttu-id="459c1-170">Quando l'applicazione chiama uno dei metodi del resolver di origine, crea l'origine di rete, imposta le proprietà specificate nell'archivio delle proprietà e apre una sessione con il server multimediale.</span><span class="sxs-lookup"><span data-stu-id="459c1-170">When the application calls one of the source resolver methods, it creates the network source, sets the properties specified in the property store, and opens a session with the media server.</span></span> <span data-ttu-id="459c1-171">Oltre alle informazioni configurabili descritte nella sezione precedente, i dati aggiuntivi vengono trasferiti tra il server e il client all'inizio della sessione, durante lo streaming e quando la sessione viene chiusa.</span><span class="sxs-lookup"><span data-stu-id="459c1-171">In addition to the configurable information described in the previous section, additional data is transferred between the server and the client at the beginning of the session, during streaming, and when the session is closed.</span></span>

<span data-ttu-id="459c1-172">L'applicazione può recuperare le statistiche di rete usando l'identificatore del servizio **MFNETSOURCE \_ STATISTICS \_ SERVICE.**</span><span class="sxs-lookup"><span data-stu-id="459c1-172">The application can retrieve network statistics by using the **MFNETSOURCE\_STATISTICS\_SERVICE** service identifier.</span></span> <span data-ttu-id="459c1-173">Per usare questo servizio, l'applicazione può chiamare la funzione [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) per ottenere l'archivio delle proprietà che contiene statistiche di rete nella [**proprietà MFNETSOURCE \_ STATISTICS.**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids)</span><span class="sxs-lookup"><span data-stu-id="459c1-173">To use this service, the application can call the [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) function to get the property store that contains network statistics in the [**MFNETSOURCE\_STATISTICS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids) property.</span></span> <span data-ttu-id="459c1-174">È possibile recuperare valori specifici fornendo l'identificatore corrispondente definito **nell'enumerazione MFNETSOURCE \_ STATISTICS \_ IDS.**</span><span class="sxs-lookup"><span data-stu-id="459c1-174">Specific values can be retrieved by providing the corresponding identifier defined in the **MFNETSOURCE\_STATISTICS\_IDS** enumeration.</span></span>

<span data-ttu-id="459c1-175">Nell'esempio di codice seguente viene illustrato come usare il servizio per ottenere il numero di pacchetti ricevuti dal client.</span><span class="sxs-lookup"><span data-stu-id="459c1-175">The following code example shows how to use the service to get the number of packets received by the client.</span></span>


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



<span data-ttu-id="459c1-176">L'elenco seguente descrive alcuni degli identificatori delle statistiche di rete definiti in [**MFNETSOURCE \_ STATISTICS \_ IDS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids).</span><span class="sxs-lookup"><span data-stu-id="459c1-176">The following list describes some of the network statistics identifiers defined in [**MFNETSOURCE\_STATISTICS\_IDS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids).</span></span>



| <span data-ttu-id="459c1-177">Identificatore delle statistiche di rete</span><span class="sxs-lookup"><span data-stu-id="459c1-177">Network statistics identifier</span></span>              | <span data-ttu-id="459c1-178">Descrizione</span><span class="sxs-lookup"><span data-stu-id="459c1-178">Description</span></span>                                                                                                                                                                                                                |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="459c1-179">**MFNETSOURCE \_ AVGBANDWIDTHBPS \_ ID**</span><span class="sxs-lookup"><span data-stu-id="459c1-179">**MFNETSOURCE\_AVGBANDWIDTHBPS\_ID**</span></span>       | <span data-ttu-id="459c1-180">Larghezza di banda media (in bit al secondo) alla quale il client era connesso al server.</span><span class="sxs-lookup"><span data-stu-id="459c1-180">Average bandwidth (in bits per second) at which the client was connected to the server.</span></span> <span data-ttu-id="459c1-181">Il valore viene calcolato per l'intera durata della connessione.</span><span class="sxs-lookup"><span data-stu-id="459c1-181">The value is calculated across the entire duration of the connection.</span></span>                                                              |
| <span data-ttu-id="459c1-182">**MFNETSOURCE \_ BUFFERINGCOUNT \_ ID**</span><span class="sxs-lookup"><span data-stu-id="459c1-182">**MFNETSOURCE\_BUFFERINGCOUNT\_ID**</span></span>        | <span data-ttu-id="459c1-183">Numero di volte in cui il client ha memorizzato nel buffer durante la riproduzione del flusso.</span><span class="sxs-lookup"><span data-stu-id="459c1-183">Number of times the client buffered while playing the stream.</span></span>                                                                                                                                                              |
| <span data-ttu-id="459c1-184">**MFNETSOURCE \_ BYTESRECEIVED \_ ID**</span><span class="sxs-lookup"><span data-stu-id="459c1-184">**MFNETSOURCE\_BYTESRECEIVED\_ID**</span></span>         | <span data-ttu-id="459c1-185">Numero di byte ricevuti dal client dal server.</span><span class="sxs-lookup"><span data-stu-id="459c1-185">Number of bytes received by the client from the server.</span></span> <span data-ttu-id="459c1-186">Il valore non include alcun sovraccarico aggiunto dallo stack di rete.</span><span class="sxs-lookup"><span data-stu-id="459c1-186">The value does not include any overhead that is added by the network stack.</span></span> <span data-ttu-id="459c1-187">Lo stesso contenuto trasmesso tramite protocolli diversi può comportare valori diversi.</span><span class="sxs-lookup"><span data-stu-id="459c1-187">The same content streamed by using different protocols can result in different values.</span></span> |
| <span data-ttu-id="459c1-188">**MFNETSOURCE \_ LINKBANDWIDTH \_ ID**</span><span class="sxs-lookup"><span data-stu-id="459c1-188">**MFNETSOURCE\_LINKBANDWIDTH\_ID**</span></span>         | <span data-ttu-id="459c1-189">Larghezza di banda massima disponibile del client in bit al secondo.</span><span class="sxs-lookup"><span data-stu-id="459c1-189">Maximum available bandwidth of the client in bits per second.</span></span>                                                                                                                                                              |
| <span data-ttu-id="459c1-190">**MFNETSOURCE \_ LOSTPACKETS \_ ID**</span><span class="sxs-lookup"><span data-stu-id="459c1-190">**MFNETSOURCE\_LOSTPACKETS\_ID**</span></span>           | <span data-ttu-id="459c1-191">Numero di pacchetti inviati dal server ma persi durante la trasmissione e mai riprodotti dal client.</span><span class="sxs-lookup"><span data-stu-id="459c1-191">Number of packets sent by the server but lost during transmission, and never played by the client.</span></span> <span data-ttu-id="459c1-192">Il valore non include pacchetti TCP o UDP.</span><span class="sxs-lookup"><span data-stu-id="459c1-192">The value does not include TCP or UDP packets.</span></span>                                                                          |
| <span data-ttu-id="459c1-193">**MFNETSOURCE \_ RECVPACKETS \_ ID**</span><span class="sxs-lookup"><span data-stu-id="459c1-193">**MFNETSOURCE\_RECVPACKETS\_ID**</span></span>           | <span data-ttu-id="459c1-194">Numero di pacchetti ricevuti dal server Il valore non include pacchetti TCP o UDP.</span><span class="sxs-lookup"><span data-stu-id="459c1-194">Number of packets received from the server The value does not include TCP or UDP packets.</span></span>                                                                                                                                  |
| <span data-ttu-id="459c1-195">**MFNETSOURCE \_ RECOVEREDBYECCPACKETS \_ ID**</span><span class="sxs-lookup"><span data-stu-id="459c1-195">**MFNETSOURCE\_RECOVEREDBYECCPACKETS\_ID**</span></span> | <span data-ttu-id="459c1-196">Pacchetti persi nella rete che sono stati ripristinati e ripristinati a livello client.</span><span class="sxs-lookup"><span data-stu-id="459c1-196">Packets lost in the network that were repaired and recovered at the client layer.</span></span> <span data-ttu-id="459c1-197">Questo valore non include pacchetti TCP o UDP.</span><span class="sxs-lookup"><span data-stu-id="459c1-197">This value does not include TCP or UDP packets.</span></span>                                                                                          |
| <span data-ttu-id="459c1-198">**MFNETSOURCE \_ RESENDSREQUESTED \_ ID**</span><span class="sxs-lookup"><span data-stu-id="459c1-198">**MFNETSOURCE\_RESENDSREQUESTED\_ID**</span></span>      | <span data-ttu-id="459c1-199">Numero di richieste effettuate dal client per ricevere nuovi pacchetti.</span><span class="sxs-lookup"><span data-stu-id="459c1-199">The number of requests made by the client to receive new packets.</span></span> <span data-ttu-id="459c1-200">Questo valore non include pacchetti TCP o UDP.</span><span class="sxs-lookup"><span data-stu-id="459c1-200">This value does not include TCP or UDP packets.</span></span>                                                                                                          |
| <span data-ttu-id="459c1-201">**MFNETSOURCE \_ RECOVEREDPACKETS \_ ID**</span><span class="sxs-lookup"><span data-stu-id="459c1-201">**MFNETSOURCE\_RECOVEREDPACKETS\_ID**</span></span>      | <span data-ttu-id="459c1-202">Numero di pacchetti ripristinati perché sono stati reinviati tramite UDP.</span><span class="sxs-lookup"><span data-stu-id="459c1-202">Number of packets recovered because they were resent through UDP.</span></span> <span data-ttu-id="459c1-203">Questo valore non include pacchetti TCP o UDP.</span><span class="sxs-lookup"><span data-stu-id="459c1-203">This value does not include TCP or UDP packets.</span></span> <span data-ttu-id="459c1-204">Questo campo contiene uno zero a meno che il client non utilizzi il reinvio UDP.</span><span class="sxs-lookup"><span data-stu-id="459c1-204">This field contains a zero unless the client is using UDP resend.</span></span>                                        |
| <span data-ttu-id="459c1-205">**MFNETSOURCE \_ BUFFERPROGRESS \_ ID**</span><span class="sxs-lookup"><span data-stu-id="459c1-205">**MFNETSOURCE\_BUFFERPROGRESS\_ID**</span></span>        | <span data-ttu-id="459c1-206">Percentuale del buffer di playout riempito durante la memorizzazione nel buffer.</span><span class="sxs-lookup"><span data-stu-id="459c1-206">The percentage of the playout buffer filled during buffering.</span></span>                                                                                                                                                              |
| <span data-ttu-id="459c1-207">**ID PROTOCOLLO MFNETSOURCE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="459c1-207">**MFNETSOURCE\_PROTOCOL\_ID**</span></span>              | <span data-ttu-id="459c1-208">Protocollo utilizzato per accedere al flusso.</span><span class="sxs-lookup"><span data-stu-id="459c1-208">Protocol used to access the stream.</span></span> <span data-ttu-id="459c1-209">Questo comportamento può differire dal protocollo richiesto dal client.</span><span class="sxs-lookup"><span data-stu-id="459c1-209">This may differ from the protocol requested by the client.</span></span>                                                                                                                             |
| <span data-ttu-id="459c1-210">**ID TRASPORTO MFNETSOURCE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="459c1-210">**MFNETSOURCE\_TRANSPORT\_ID**</span></span>             | <span data-ttu-id="459c1-211">Protocollo di trasporto usato per recapitare il flusso.</span><span class="sxs-lookup"><span data-stu-id="459c1-211">Transport protocol used to deliver the stream.</span></span> <span data-ttu-id="459c1-212">Deve essere UDP o TCP.</span><span class="sxs-lookup"><span data-stu-id="459c1-212">This must be either UDP or TCP.</span></span>                                                                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="459c1-213">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="459c1-213">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="459c1-214">Funzionalità dell'origine di rete</span><span class="sxs-lookup"><span data-stu-id="459c1-214">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="459c1-215">Rete in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="459c1-215">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

