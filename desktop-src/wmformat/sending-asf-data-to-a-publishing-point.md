---
title: Invio di dati ASF a un punto di pubblicazione
description: Invio di dati ASF a un punto di pubblicazione
ms.assetid: 8f01beae-4270-4cf5-afff-3f7014cae90f
keywords:
- Windows Media Format SDK, invio di dati ASF
- Windows Media Format SDK, punti di pubblicazione
- Formato di sistemi avanzati (ASF), invio di dati
- ASF (Advanced Systems Format), invio di dati
- Formato di sistemi avanzati (ASF), punti di pubblicazione
- ASF (formato avanzato dei sistemi), punti di pubblicazione
- punti di pubblicazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a0f38f4d24a458681c4b0dc4ee6d1a73563bdd2
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "103724125"
---
# <a name="sending-asf-data-to-a-publishing-point"></a><span data-ttu-id="c9b2b-110">Invio di dati ASF a un punto di pubblicazione</span><span class="sxs-lookup"><span data-stu-id="c9b2b-110">Sending ASF Data to a Publishing Point</span></span>

<span data-ttu-id="c9b2b-111">È possibile utilizzare Windows Media Format SDK per eseguire il push dei dati ASF a un punto di pubblicazione in un server Windows Media.</span><span class="sxs-lookup"><span data-stu-id="c9b2b-111">You can use the Windows Media Format SDK to push ASF data to a publishing point on a Windows Media server.</span></span> <span data-ttu-id="c9b2b-112">Il server trasmette quindi i dati dal punto di pubblicazione.</span><span class="sxs-lookup"><span data-stu-id="c9b2b-112">The server then broadcasts the data from that publishing point.</span></span> <span data-ttu-id="c9b2b-113">Questo scenario è utile se si intende acquisire o ricodificare il contenuto in un computer e si desidera distribuire il contenuto da un altro computer (o più computer).</span><span class="sxs-lookup"><span data-stu-id="c9b2b-113">This scenario is useful if you are capturing or re-encoding content on one computer, and wish to distribute the content from another computer (or several computers).</span></span> <span data-ttu-id="c9b2b-114">È utile anche se è necessario spostare il contenuto da un computer all'interno di un firewall a un server Windows Media all'esterno del firewall, perché la distribuzione push usa il protocollo HTTP.</span><span class="sxs-lookup"><span data-stu-id="c9b2b-114">It is also useful if you need to move content from a computer inside a firewall to a Windows Media server outside the firewall, because push distribution uses the HTTP protocol.</span></span>

> [!Note]  
> <span data-ttu-id="c9b2b-115">Un *punto di pubblicazione* funziona essenzialmente come un redirector.</span><span class="sxs-lookup"><span data-stu-id="c9b2b-115">A *publishing point* acts essentially like a redirector.</span></span> <span data-ttu-id="c9b2b-116">Il client specifica il punto di pubblicazione nell'URL (ad esempio, mms://MyServer/MyPublishingPoint) e il server lo converte in una richiesta di contenuto.</span><span class="sxs-lookup"><span data-stu-id="c9b2b-116">The client specifies the publishing point in the URL (for example, mms://MyServer/MyPublishingPoint) and the server translates this into a request for content.</span></span>

 

<span data-ttu-id="c9b2b-117">Per eseguire il push dei dati nel punto di pubblicazione, alleghi l'oggetto sink push all'oggetto writer.</span><span class="sxs-lookup"><span data-stu-id="c9b2b-117">To push data to the publishing point, attach the push sink object to the writer object.</span></span> <span data-ttu-id="c9b2b-118">Il sink di push viene utilizzato per aprire la connessione al server e gestire la sessione di push.</span><span class="sxs-lookup"><span data-stu-id="c9b2b-118">The push sink is used to open the connection to the server and manage the push session.</span></span> <span data-ttu-id="c9b2b-119">L'oggetto writer gestisce tutti gli altri aspetti della creazione del file.</span><span class="sxs-lookup"><span data-stu-id="c9b2b-119">The writer object handles all the other aspects of creating the file.</span></span>

<span data-ttu-id="c9b2b-120">Eseguire la procedura seguente:</span><span class="sxs-lookup"><span data-stu-id="c9b2b-120">Perform the following steps:</span></span>

1.  <span data-ttu-id="c9b2b-121">Creare l'oggetto writer chiamando la funzione [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) , che restituisce un puntatore [**IWMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter) .</span><span class="sxs-lookup"><span data-stu-id="c9b2b-121">Create the writer object by calling the [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) function, which returns an [**IWMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter) pointer.</span></span>
2.  <span data-ttu-id="c9b2b-122">Creare l'oggetto sink di push chiamando la funzione [**WMCreateWriterPushSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink) , che restituisce un puntatore [**IWMWriterPushSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpushsink) .</span><span class="sxs-lookup"><span data-stu-id="c9b2b-122">Create the push sink object by calling the [**WMCreateWriterPushSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriterpushsink) function, which returns an [**IWMWriterPushSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpushsink) pointer.</span></span>
3.  <span data-ttu-id="c9b2b-123">Collegare il sink di rete al writer chiamando [**IWMWriterAdvanced:: AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) sul writer, con un puntatore all'interfaccia **IWMWriterPushSink** del sink di rete.</span><span class="sxs-lookup"><span data-stu-id="c9b2b-123">Attach the network sink to the writer by calling [**IWMWriterAdvanced::AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) on the writer, with a pointer to the network sink's **IWMWriterPushSink** interface.</span></span>
4.  <span data-ttu-id="c9b2b-124">Connettersi al server chiamando [**IWMWriterPushSink:: Connect**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpushsink-connect).</span><span class="sxs-lookup"><span data-stu-id="c9b2b-124">Connect to the server by calling [**IWMWriterPushSink::Connect**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpushsink-connect).</span></span>
5.  <span data-ttu-id="c9b2b-125">Scrivere il flusso.</span><span class="sxs-lookup"><span data-stu-id="c9b2b-125">Write the stream.</span></span> <span data-ttu-id="c9b2b-126">Questo passaggio prevede l'impostazione del profilo nell'oggetto writer, l'invio di esempi al writer e possibilmente altre attività.</span><span class="sxs-lookup"><span data-stu-id="c9b2b-126">This step involves setting the profile on the writer object, sending samples to the writer, and possibly other tasks.</span></span> <span data-ttu-id="c9b2b-127">Per ulteriori informazioni, vedere la pagina relativa alla [scrittura di file ASF](writing-asf-files.md).</span><span class="sxs-lookup"><span data-stu-id="c9b2b-127">For more information, see [Writing ASF Files](writing-asf-files.md).</span></span> <span data-ttu-id="c9b2b-128">Altre attività possono includere l'impostazione degli attributi dei metadati (come descritto in [uso dei metadati](working-with-metadata.md)) o l'impostazione di DRM Live nel flusso (come descritto in [Abilitazione del supporto DRM](enabling-drm-support.md)).</span><span class="sxs-lookup"><span data-stu-id="c9b2b-128">Additional tasks might include setting metadata attributes (as described in [Working with Metadata](working-with-metadata.md)) or setting live-DRM on the stream (as described in [Enabling DRM Support](enabling-drm-support.md)).</span></span> <span data-ttu-id="c9b2b-129">Queste attività vengono eseguite esattamente come per la scrittura di file ASF.</span><span class="sxs-lookup"><span data-stu-id="c9b2b-129">These tasks are performed exactly as they are for ASF file writing.</span></span>
6.  <span data-ttu-id="c9b2b-130">Al termine della scrittura, chiamare [**IWMWriterAdvanced:: RemoveSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink) sul writer per scollegare l'oggetto sink di push.</span><span class="sxs-lookup"><span data-stu-id="c9b2b-130">After you are done writing, call [**IWMWriterAdvanced::RemoveSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink) on the writer to detach the push sink object.</span></span>
7.  <span data-ttu-id="c9b2b-131">Chiamare [**IWMWriterPushSink:: EndSession**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpushsink-endsession) sul sink di push per terminare la sessione con il server.</span><span class="sxs-lookup"><span data-stu-id="c9b2b-131">Call [**IWMWriterPushSink::EndSession**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpushsink-endsession) on the push sink to end the session with the server.</span></span>

<span data-ttu-id="c9b2b-132">Questi passaggi sono illustrati nell'applicazione di esempio WMVNetWrite.</span><span class="sxs-lookup"><span data-stu-id="c9b2b-132">These steps are illustrated in the WMVNetWrite sample application.</span></span>

> [!Note]  
> <span data-ttu-id="c9b2b-133">Se si invia un file di solo video con velocità in bit molto bassa, è possibile che non si avvii la riproduzione nel punto di pubblicazione per alcuni secondi.</span><span class="sxs-lookup"><span data-stu-id="c9b2b-133">If you are sending a very-low-bit-rate video-only file, it might not start playing on the publishing point for several seconds.</span></span> <span data-ttu-id="c9b2b-134">Questo problema può verificarsi in diversi casi, ad esempio quando un singolo pacchetto contiene molti piccoli fotogrammi video e nessun audio, oppure quando si verifica un periodo di tempo prolungato tra il primo pacchetto e il secondo pacchetto in un file di solo video a bassa velocità.</span><span class="sxs-lookup"><span data-stu-id="c9b2b-134">This can happen in various cases, for example when a single packet contains many small video frames and no audio, or when there is a long time gap between the first packet and the second packet in a low-bit-rate video-only file.</span></span> <span data-ttu-id="c9b2b-135">Per evitare questo problema, inserire un flusso audio invisibile all'utente nel file.</span><span class="sxs-lookup"><span data-stu-id="c9b2b-135">To avoid this problem, insert a silent audio stream into the file.</span></span>

 

## <a name="authentication"></a><span data-ttu-id="c9b2b-136">Authentication</span><span class="sxs-lookup"><span data-stu-id="c9b2b-136">Authentication</span></span>

<span data-ttu-id="c9b2b-137">L'autenticazione al server viene gestita automaticamente dall'oggetto sink di push.</span><span class="sxs-lookup"><span data-stu-id="c9b2b-137">Authentication to the server is automatically handled by the push sink object.</span></span> <span data-ttu-id="c9b2b-138">Tuttavia, potrebbe essere necessario specificare le credenziali per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c9b2b-138">However, the application may need to supply credentials.</span></span> <span data-ttu-id="c9b2b-139">Questa operazione viene eseguita tramite l'interfaccia di callback **IWMCredentialCallback** , come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="c9b2b-139">This is done through the **IWMCredentialCallback** callback interface, as follows:</span></span>

1.  <span data-ttu-id="c9b2b-140">Implementare l'interfaccia [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) e [**IWMCredentialCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback) nell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c9b2b-140">Implement the [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) and [**IWMCredentialCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback) interface in your application.</span></span>
2.  <span data-ttu-id="c9b2b-141">Eseguire una query sull'oggetto sink push per l'interfaccia [**IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) .</span><span class="sxs-lookup"><span data-stu-id="c9b2b-141">Query the push sink object for the [**IWMRegisterCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback) interface.</span></span>
3.  <span data-ttu-id="c9b2b-142">Chiamare [**IWMRegisterCallback:: Advise**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistercallback-advise) con un puntatore all'interfaccia **IWMStatusCallback** dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c9b2b-142">Call [**IWMRegisterCallback::Advise**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistercallback-advise) with a pointer to your application's **IWMStatusCallback** interface.</span></span>
4.  <span data-ttu-id="c9b2b-143">Se il sink di push deve ottenere le credenziali dall'applicazione, esegue una query sul puntatore **IWMStatusCallback** per l'interfaccia **IWMCredentialCallback** e chiama [**IWMCredentialCallback:: AcquireCredentials**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcredentialcallback-acquirecredentials).</span><span class="sxs-lookup"><span data-stu-id="c9b2b-143">If the push sink needs to get credentials from the application, it queries the **IWMStatusCallback** pointer for the **IWMCredentialCallback** interface and calls [**IWMCredentialCallback::AcquireCredentials**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcredentialcallback-acquirecredentials).</span></span> <span data-ttu-id="c9b2b-144">Per informazioni su questo metodo, vedere [Authentication](authentication.md).</span><span class="sxs-lookup"><span data-stu-id="c9b2b-144">For information about this method, see [Authentication](authentication.md).</span></span>
5.  <span data-ttu-id="c9b2b-145">Al termine, chiamare [**IWMRegisterCallback:: Unadvise**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistercallback-unadvise) per arrestare il recupero delle notifiche degli eventi dal sink di push.</span><span class="sxs-lookup"><span data-stu-id="c9b2b-145">When you are done, call [**IWMRegisterCallback::Unadvise**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistercallback-unadvise) to stop getting event notifications from the push sink.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c9b2b-146">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c9b2b-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9b2b-147">**Invio di dati ASF in una rete**</span><span class="sxs-lookup"><span data-stu-id="c9b2b-147">**Sending ASF Data Over a Network**</span></span>](sending-asf-data-over-a-network.md)
</dt> <dt>

[<span data-ttu-id="c9b2b-148">**Utilizzo dei sink di writer**</span><span class="sxs-lookup"><span data-stu-id="c9b2b-148">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> <dt>

[<span data-ttu-id="c9b2b-149">**Oggetto sink push writer**</span><span class="sxs-lookup"><span data-stu-id="c9b2b-149">**Writer Push Sink Object**</span></span>](writer-push-sink-object.md)
</dt> </dl>

 

 




