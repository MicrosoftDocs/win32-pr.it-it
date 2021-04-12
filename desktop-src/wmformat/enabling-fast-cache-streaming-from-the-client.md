---
title: Abilitazione del flusso fast cache dal client
description: Abilitazione del flusso fast cache dal client
ms.assetid: 2a850d6f-8e1d-4aeb-9791-c51c3debf118
keywords:
- Windows Media Format SDK, abilitazione del flusso fast cache
- Windows Media Format SDK, fast cache streaming
- Advanced Systems Format (ASF), abilitazione del flusso fast cache
- ASF (Advanced Systems Format), abilitazione del flusso fast cache
- Advanced Systems Format (ASF), streaming fast cache
- ASF (formato avanzato dei sistemi), streaming fast cache
- flussi, abilitazione del flusso fast cache
- Streaming fast cache, abilitazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3f8423a6f71b86ea91a05ed74b931eaa28a64be
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104398569"
---
# <a name="enabling-fast-cache-streaming-from-the-client"></a><span data-ttu-id="383ea-111">Abilitazione del flusso fast cache dal client</span><span class="sxs-lookup"><span data-stu-id="383ea-111">Enabling Fast Cache Streaming from the Client</span></span>

<span data-ttu-id="383ea-112">Fast cache è una tecnologia di streaming in cui il server opportunisticamente trasmette contenuto a una velocità in bit superiore rispetto a quella necessaria per la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="383ea-112">Fast Cache is a streaming technology in which the server opportunistically streams content at a higher bit rate than what is needed for playback.</span></span>

<span data-ttu-id="383ea-113">Se la larghezza di banda disponibile è superiore alla velocità in bit del contenuto, i flussi della cache veloce hanno una velocità superiore e il contenuto viene memorizzato nel buffer.</span><span class="sxs-lookup"><span data-stu-id="383ea-113">If the available bandwidth is higher than the bit rate of the content, Fast Cache streams at the higher rate and buffers the content.</span></span> <span data-ttu-id="383ea-114">Questo consente di ridurre le interruzioni in un secondo momento se la rete viene congestionata.</span><span class="sxs-lookup"><span data-stu-id="383ea-114">This helps to reduce interruptions later if the network becomes congested.</span></span> <span data-ttu-id="383ea-115">Se la larghezza di banda di rete è inferiore alla velocità in bit del contenuto, la cache veloce memorizza nel buffer una parte dei dati prima che venga avviata la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="383ea-115">If network bandwidth is lower than the bit rate of the content, Fast Cache buffers a portion of the data before playback starts.</span></span> <span data-ttu-id="383ea-116">La cache veloce è consigliata per le reti non affidabili, ad esempio reti wireless o reti che riscontrano fluttuazioni di grandi dimensioni nel traffico di rete, ad esempio modem via cavo.</span><span class="sxs-lookup"><span data-stu-id="383ea-116">Fast Cache is recommended for unreliable networks, such as wireless networks, or networks that experience large fluctuations in network traffic, such as cable modems.</span></span> <span data-ttu-id="383ea-117">È inoltre consigliato per il contenuto della velocità in bit variabile (VBR).</span><span class="sxs-lookup"><span data-stu-id="383ea-117">It is also recommended for variable bit rate (VBR) content.</span></span> <span data-ttu-id="383ea-118">I requisiti di larghezza di banda per il contenuto VBR non sono costanti e la cache veloce consente al lettore di memorizzare nel buffer il flusso durante le porzioni a bassa velocità in bit.</span><span class="sxs-lookup"><span data-stu-id="383ea-118">The bandwidth requirements for VBR content are not constant, and Fast Cache enables the reader to buffer the stream during the lower-bit-rate portions.</span></span>

<span data-ttu-id="383ea-119">Il flusso fast cache è supportato solo per contenuti su richiesta.</span><span class="sxs-lookup"><span data-stu-id="383ea-119">Fast Cache streaming is supported only for on-demand content.</span></span> <span data-ttu-id="383ea-120">Inoltre, il server deve essere configurato in modo da usare lo streaming veloce della cache.</span><span class="sxs-lookup"><span data-stu-id="383ea-120">In addition, the server must be configured to use Fast Cache streaming.</span></span>

<span data-ttu-id="383ea-121">Per abilitare la cache veloce nell'oggetto Reader, chiamare i metodi [**IWMReaderNetworkConfig2:: SetEnableContentCaching**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-setenablecontentcaching) e [**IWMReaderNetworkConfig2:: SetEnableFastCache**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-setenablefastcache) con il valore **true**.</span><span class="sxs-lookup"><span data-stu-id="383ea-121">To enable Fast Cache in the reader object, call the [**IWMReaderNetworkConfig2::SetEnableContentCaching**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-setenablecontentcaching) and [**IWMReaderNetworkConfig2::SetEnableFastCache**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig2-setenablefastcache) methods with the value **TRUE**.</span></span> <span data-ttu-id="383ea-122">Il primo metodo consente al Reader di memorizzare nella cache il contenuto trasmesso.</span><span class="sxs-lookup"><span data-stu-id="383ea-122">The first method enables the reader to cache streamed content.</span></span> <span data-ttu-id="383ea-123">Il secondo consente di usare la cache veloce in particolare.</span><span class="sxs-lookup"><span data-stu-id="383ea-123">The second enables the use of Fast Cache in particular.</span></span>

<span data-ttu-id="383ea-124">Con queste impostazioni, il lettore attiverà fast cache per impostazione predefinita se la larghezza di banda di rete è significativamente superiore o inferiore alla velocità in bit del contenuto e se il server lo supporta.</span><span class="sxs-lookup"><span data-stu-id="383ea-124">With these settings, the reader will activate Fast Cache by default if the network bandwidth is significantly higher or lower than the bit rate of the content, and if the server supports it.</span></span> <span data-ttu-id="383ea-125">L'utente può inoltre controllare se l'oggetto Reader utilizza la cache veloce aggiungendo uno o più dei modificatori seguenti all'URL.</span><span class="sxs-lookup"><span data-stu-id="383ea-125">The user can also control whether the reader object uses Fast Cache by adding one or more of the following modifiers to the URL.</span></span>



| <span data-ttu-id="383ea-126">Modificatore</span><span class="sxs-lookup"><span data-stu-id="383ea-126">Modifier</span></span>         | <span data-ttu-id="383ea-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="383ea-127">Description</span></span>                                                                                                                                                                                                                                                                                                                                      |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="383ea-128">WMCache</span><span class="sxs-lookup"><span data-stu-id="383ea-128">WMCache</span></span>          | <span data-ttu-id="383ea-129">Se questo modificatore è presente, il valore ' 0' Disabilita in modo esplicito la cache veloce, mentre il valore ' 1' lo Abilita in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="383ea-129">If this modifier is present, the value '0' explicitly disables Fast Cache, while the value '1' explicitly enables it.</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="383ea-130">WMBitrate</span><span class="sxs-lookup"><span data-stu-id="383ea-130">WMBitrate</span></span>        | <span data-ttu-id="383ea-131">Questo modificatore specifica la velocità in bit massima del server.</span><span class="sxs-lookup"><span data-stu-id="383ea-131">This modifier specifies the maximum bit rate from the server.</span></span> <span data-ttu-id="383ea-132">Questo modificatore può essere usato per limitare la cache veloce a un determinato limite di larghezza di banda.</span><span class="sxs-lookup"><span data-stu-id="383ea-132">This modifier can be used to restrict Fast Cache to a certain bandwidth limit.</span></span> <span data-ttu-id="383ea-133">Questo modificatore viene ignorato se una larghezza di banda di connessione esplicita è già impostata con una chiamata a [**IWMReaderNetworkConfig:: SetConnectionBandwidth**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setconnectionbandwidth).</span><span class="sxs-lookup"><span data-stu-id="383ea-133">This modifier is ignored if an explicit connection bandwidth is already set with a call to [**IWMReaderNetworkConfig::SetConnectionBandwidth**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-setconnectionbandwidth).</span></span> |
| <span data-ttu-id="383ea-134">WMContentBitrate</span><span class="sxs-lookup"><span data-stu-id="383ea-134">WMContentBitrate</span></span> | <span data-ttu-id="383ea-135">Questo modificatore specifica la velocità in bit per il contenuto.</span><span class="sxs-lookup"><span data-stu-id="383ea-135">This modifier specifies the bit rate for the content.</span></span> <span data-ttu-id="383ea-136">Il lettore utilizza questo modificatore, se presente, quando seleziona i flussi da un file con velocità in bit multipla (MBR).</span><span class="sxs-lookup"><span data-stu-id="383ea-136">The reader uses this modifier, if present, when it selects streams from a multiple bit rate (MBR) file.</span></span> <span data-ttu-id="383ea-137">In questo modo, il lettore può ricevere contenuto a bitrate elevato su una connessione lenta, con tempi e ritardi di buffer molto lunghi.</span><span class="sxs-lookup"><span data-stu-id="383ea-137">This can cause the reader to receive high bit rate content over a slow connection, which results in very long buffering times and delays.</span></span>                                          |



 

<span data-ttu-id="383ea-138">Il modificatore WMCache = 1 impone al lettore di usare lo streaming veloce della cache, indipendentemente dalla larghezza di banda di rete o dalla velocità in bit del contenuto e indipendentemente dalle chiamate precedenti a **SetEnableFastCache**.</span><span class="sxs-lookup"><span data-stu-id="383ea-138">The modifier WMCache=1 forces the reader to use Fast Cache streaming, regardless of the network bandwith or the bit rate of the content and regardless of any previous calls to **SetEnableFastCache**.</span></span> <span data-ttu-id="383ea-139">Tuttavia, non esegue l'override dell'impostazione **SetEnableContentCaching** nel lettore; né sostituisce la configurazione del server.</span><span class="sxs-lookup"><span data-stu-id="383ea-139">However, it does not override the **SetEnableContentCaching** setting on the reader; nor does it override the server configuration.</span></span>

<span data-ttu-id="383ea-140">I modificatori di URL hanno il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="383ea-140">URL modifiers have the following form:</span></span>

<span data-ttu-id="383ea-141">*URL*? *modificatore* = *valore* di</span><span class="sxs-lookup"><span data-stu-id="383ea-141">*url*?*modifier*=*value*</span></span>

<span data-ttu-id="383ea-142">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="383ea-142">For example:</span></span>

<span data-ttu-id="383ea-143">mms://MyServer/MyVideo.wmv? WMCache = 1</span><span class="sxs-lookup"><span data-stu-id="383ea-143">mms://MyServer/MyVideo.wmv?WMCache=1</span></span>

<span data-ttu-id="383ea-144">È possibile specificare più di un modificatore; usare una e commerciale (&) per separarli:</span><span class="sxs-lookup"><span data-stu-id="383ea-144">More than one modifier can specified; use an ampersand (&) to separate them:</span></span>

<span data-ttu-id="383ea-145">mms://MyServer/MyVideo.wmv? WMCache = 1&WMContentBitrate = 56000</span><span class="sxs-lookup"><span data-stu-id="383ea-145">mms://MyServer/MyVideo.wmv?WMCache=1&WMContentBitrate=56000</span></span>

 

 




