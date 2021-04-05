---
title: Registrazione dei dati del flusso
description: Registrazione dei dati del flusso
ms.assetid: c902a755-afdd-4dea-bc3e-036555fdff10
keywords:
- Playlist Windows Media Metafile, registrazione dei dati del flusso
- playlist, dati del flusso di registrazione
- playlist di metafile, dati del flusso di registrazione
- Playlist Windows Media Metafile, registrazione dati di flusso
- playlist, registrazione dei dati di flusso
- playlist di metafile, registrazione dei dati di flusso
- registrazione dei dati del flusso
- registrazione dati di flusso
- Media Player di Windows, registrazione dei dati del flusso
- Windows Media Player, registrazione dati di flusso
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f234851cabf071ed2308fb5c96df2b53b60b9d45
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116929"
---
# <a name="logging-stream-data"></a><span data-ttu-id="d7c97-113">Registrazione dei dati del flusso</span><span class="sxs-lookup"><span data-stu-id="d7c97-113">Logging Stream Data</span></span>

<span data-ttu-id="d7c97-114">Le informazioni registrate possono essere acquisite e usate per determinare il comportamento del visualizzatore, ad esempio la frequenza di visualizzazione di un flusso o se un utente specifico ha visualizzato un flusso e per quanto tempo la qualità.</span><span class="sxs-lookup"><span data-stu-id="d7c97-114">Logged information can be acquired and used to determine viewer behavior, for example, how often a stream is viewed, or if a specific user viewed a stream and for how long at what quality.</span></span>

<span data-ttu-id="d7c97-115">Le informazioni di registrazione vengono inviate automaticamente al server da cui ha avuto origine la playlist.</span><span class="sxs-lookup"><span data-stu-id="d7c97-115">Logging information is automatically sent to the server from which the playlist originated.</span></span> <span data-ttu-id="d7c97-116">È inoltre possibile inviare le informazioni di registrazione a server aggiuntivi, inclusi i server Web utilizzati esclusivamente per la registrazione.</span><span class="sxs-lookup"><span data-stu-id="d7c97-116">You can also send logging information to additional servers, including web servers you use exclusively for logging.</span></span> <span data-ttu-id="d7c97-117">A tale scopo, usare l'elemento **LogURL** , specificando un URL valido per l'attributo **href** .</span><span class="sxs-lookup"><span data-stu-id="d7c97-117">To do this, use the **LOGURL** element, specifying a valid URL for the **HREF** attribute.</span></span> <span data-ttu-id="d7c97-118">È possibile includere elementi **LogURL** come elementi figlio dell'elemento **ASX** e come elementi figlio dei singoli elementi di **immissione** .</span><span class="sxs-lookup"><span data-stu-id="d7c97-118">You can include **LOGURL** elements as children of the **ASX** element and as children of individual **ENTRY** elements.</span></span> <span data-ttu-id="d7c97-119">Quando la playlist viene aperta per la prima volta, le informazioni di registrazione vengono inviate al server di origine e a ogni URL specificato in **LogURL** Children dell'elemento **ASX** .</span><span class="sxs-lookup"><span data-stu-id="d7c97-119">When the playlist is first opened, logging information is sent to the origin server and to each URL specified in **LOGURL** children of the **ASX** element.</span></span> <span data-ttu-id="d7c97-120">Quindi, quando viene raggiunta ogni voce, le informazioni di registrazione specifiche di tale voce vengono inviate a ogni URL specificato in **LogURL** Children dell'elemento **entry** .</span><span class="sxs-lookup"><span data-stu-id="d7c97-120">Then, as each entry is reached, logging information specific to that entry is sent to each URL specified in **LOGURL** children of the **ENTRY** element.</span></span>

<span data-ttu-id="d7c97-121">Windows Media Format SDK supporta l'elemento **LogURL** tramite l'interfaccia **IWMSReaderNetworkConfig** e i metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="d7c97-121">The Windows Media Format SDK supports the **LOGURL** element through the **IWMSReaderNetworkConfig** interface and the following methods:</span></span>


```XML
HRESULT AddLoggingUrl(LPCWSTR pwszUrl);
HRESULT GetLoggingUrl(DWORD dwIndex, LPCWSTR pwszUrl, DWORD *pcchUrl);
HRESULT GetLoggingUrlCount(DWORD *pdwUrlCount);
HRESULT ResetLoggingUrlList();

```



<span data-ttu-id="d7c97-122">Oltre alle informazioni registrate automaticamente, una playlist di metafile può registrare informazioni personalizzate mediante l'uso dell'elemento **param** .</span><span class="sxs-lookup"><span data-stu-id="d7c97-122">In addition to the information that is automatically logged, a metafile playlist can log custom information through the use of the **PARAM** element.</span></span> <span data-ttu-id="d7c97-123">Per utilizzare l'elemento **param** in questo modo, impostare l'attributo **Name** su "log:" seguito da un nome di campo di log e da uno spazio dei nomi XML facoltativo separato dal nome del campo da altri due punti (":").</span><span class="sxs-lookup"><span data-stu-id="d7c97-123">To use the **PARAM** element in this way, set the **NAME** attribute to "log:" followed by a log field name and an optional XML namespace separated from the field name by another colon (":").</span></span> <span data-ttu-id="d7c97-124">Ogni elemento dopo i due due punti viene considerato come uno spazio dei nomi, quindi il nome del campo non deve contenere i due punti.</span><span class="sxs-lookup"><span data-stu-id="d7c97-124">Everything after the second colon is treated as a namespace, so the field name should not contain a colon.</span></span>

<span data-ttu-id="d7c97-125">Il campo di log specificato nell'attributo **Name** viene impostato sul valore dell'attributo **value** .</span><span class="sxs-lookup"><span data-stu-id="d7c97-125">The log field specified in the **NAME** attribute is set to the value of the **VALUE** attribute.</span></span> <span data-ttu-id="d7c97-126">Se il log non contiene ancora un campo con il nome specificato, verrà aggiunto.</span><span class="sxs-lookup"><span data-stu-id="d7c97-126">If the log does not already contain a field with the specified name, it will be added.</span></span>

<span data-ttu-id="d7c97-127">**Codice di esempio**</span><span class="sxs-lookup"><span data-stu-id="d7c97-127">**Example Code**</span></span>


```XML

    <ASX version="3.0">
      <LOGURL href="https://www.proseware.com/log.asp?SomeArg=SomeVal" />
      <ENTRY>
        <REF href="mms://ucast.proseware.com/Media1.wma" />
        <LOGURL href="https://www.proseware.com/cgi-bin/logging.pl?SomeArg=SomeVal" />
        <LOGURL href="https://www.proseware.com/WMLogging.dll?SomeArg=SomeVal" />
        <PARAM name="log:cs-media-role" value="Advertisement"/>
        <PARAM name="log:cs-media-name:namespace" value="Music"/>
        <REF href=rtsp://ucast.proseware.com/Media1.wma"/>
      </ENTRY>
      <ENTRY>
        <REF href="mms://ucast.proseware.com/Media2.wma"/>
      </ENTRY>
    </ASX>
    

```



## <a name="related-topics"></a><span data-ttu-id="d7c97-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d7c97-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7c97-129">**Playlist di metafile**</span><span class="sxs-lookup"><span data-stu-id="d7c97-129">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="d7c97-130">**Riferimento agli elementi metafile di Windows Media**</span><span class="sxs-lookup"><span data-stu-id="d7c97-130">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> </dl>

 

 




