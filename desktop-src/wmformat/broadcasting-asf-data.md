---
title: Trasmissione di dati ASF
description: Trasmissione di dati ASF
ms.assetid: 1b04f361-8147-4f6a-8c9d-d8eeed28550a
keywords:
- Windows Media Format SDK, trasmissione di dati ASF
- Formato di sistemi avanzati (ASF), trasmissione di dati
- ASF (Advanced Systems Format), trasmissione di dati
- Windows Media Format SDK, invio di dati ASF
- Formato di sistemi avanzati (ASF), invio di dati
- ASF (Advanced Systems Format), invio di dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42339b4a3e60666c1ea0cb69a07dfdc836b19409
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/21/2020
ms.locfileid: "104046419"
---
# <a name="broadcasting-asf-data"></a><span data-ttu-id="1b483-109">Trasmissione di dati ASF</span><span class="sxs-lookup"><span data-stu-id="1b483-109">Broadcasting ASF Data</span></span>

<span data-ttu-id="1b483-110">In questo argomento viene descritto come inviare dati ASF in una rete utilizzando il protocollo HTTP.</span><span class="sxs-lookup"><span data-stu-id="1b483-110">This topic describes how to send ASF data across a network using the HTTP protocol.</span></span> <span data-ttu-id="1b483-111">Per l'invio di file in una rete è necessario utilizzare l'oggetto writer, pertanto è necessario avere una conoscenza generale di questo oggetto prima di leggere questo argomento.</span><span class="sxs-lookup"><span data-stu-id="1b483-111">Sending files over a network requires the use of the writer object, so you should have a general understanding of this object before reading this topic.</span></span> <span data-ttu-id="1b483-112">Per ulteriori informazioni, vedere la pagina relativa alla [scrittura di file ASF](writing-asf-files.md).</span><span class="sxs-lookup"><span data-stu-id="1b483-112">For more information, see [Writing ASF Files](writing-asf-files.md).</span></span>

<span data-ttu-id="1b483-113">Se si inizia con dati non compressi, procedere come segue:</span><span class="sxs-lookup"><span data-stu-id="1b483-113">If you are starting with uncompressed data, do the following:</span></span>

1.  <span data-ttu-id="1b483-114">Creare l'oggetto writer chiamando la funzione [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) .</span><span class="sxs-lookup"><span data-stu-id="1b483-114">Create the writer object by calling the [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) function.</span></span> <span data-ttu-id="1b483-115">Questa funzione restituisce un puntatore **IWMWriter** .</span><span class="sxs-lookup"><span data-stu-id="1b483-115">This function returns an **IWMWriter** pointer.</span></span>
    ```C++
    IWMWriter *pWriter;
    hr = WMCreateWriter(NULL, &pWriter);
    ```

    

2.  <span data-ttu-id="1b483-116">Creare l'oggetto sink di rete chiamando la funzione [**WMCreateWriterNetworkSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink) , che restituisce un puntatore **IWMWriterNetworkSink** .</span><span class="sxs-lookup"><span data-stu-id="1b483-116">Create the network sink object by calling the [**WMCreateWriterNetworkSink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink) function, which returns an **IWMWriterNetworkSink** pointer.</span></span>
    ```C++
    IWMWriterNetworkSink *pNetSink;
    hr = WMCreateWriterNetworkSink(&pNetSink);
    ```

    

3.  <span data-ttu-id="1b483-117">Chiamare [**IWMWriterNetworkSink:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-open) nel sink di rete e specificare il numero di porta da aprire. ad esempio, 8080.</span><span class="sxs-lookup"><span data-stu-id="1b483-117">Call [**IWMWriterNetworkSink::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-open) on the network sink and specify the port number to open; for example, 8080.</span></span> <span data-ttu-id="1b483-118">Facoltativamente, chiamare [**IWMWriterNetworkSink:: GetHostURL**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-gethosturl) per ottenere l'URL dell'host.</span><span class="sxs-lookup"><span data-stu-id="1b483-118">Optionally, call [**IWMWriterNetworkSink::GetHostURL**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-gethosturl) to get the URL of the host.</span></span> <span data-ttu-id="1b483-119">I client accedono al contenuto da questo URL.</span><span class="sxs-lookup"><span data-stu-id="1b483-119">Clients will access the content from this URL.</span></span> <span data-ttu-id="1b483-120">È anche possibile chiamare [**IWMWriterNetworkSink:: SetMaximumClients**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-setmaximumclients) per limitare il numero di client.</span><span class="sxs-lookup"><span data-stu-id="1b483-120">You can also call [**IWMWriterNetworkSink::SetMaximumClients**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-setmaximumclients) to restrict the number of clients.</span></span>
    ```C++
    DWORD dwPortNum = 8080;
    hr = pNetSink->Open( &dwPortNum)
    ```

    

4.  <span data-ttu-id="1b483-121">Collegare il sink di rete al writer chiamando [**IWMWriterAdvanced:: AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) sul writer, con un puntatore all'interfaccia **IWMWriterNetworkSink** del sink di rete.</span><span class="sxs-lookup"><span data-stu-id="1b483-121">Attach the network sink to the writer by calling [**IWMWriterAdvanced::AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) on the writer, with a pointer to the network sink's **IWMWriterNetworkSink** interface.</span></span>
    ```C++
    IWMWriterAdvanced *pWriterAdvanced;
    hr = pWriter->QueryInterface(IID_IWMWriterAdvanced, ( void** ) pWriterAdvanced );
    if (SUCCEEDED(hr))
    {
        pWriterAdvanced->AddSink(pNetSink);
    }
    ```

    

5.  <span data-ttu-id="1b483-122">Impostare il profilo ASF chiamando il metodo [**IWMWriter:: seprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) sull'oggetto writer con un puntatore [**IWMProfile**](iwmprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="1b483-122">Set the ASF profile by calling the [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) method on the writer object, with an [**IWMProfile**](iwmprofile.md) pointer.</span></span> <span data-ttu-id="1b483-123">Per informazioni sulla creazione di un profilo, vedere [utilizzo dei profili](working-with-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="1b483-123">For information about creating a profile, see [Working with Profiles](working-with-profiles.md).</span></span>
6.  <span data-ttu-id="1b483-124">Facoltativamente, specificare i metadati usando l'interfaccia [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) nel writer.</span><span class="sxs-lookup"><span data-stu-id="1b483-124">Optionally, specify metadata using the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface on the writer.</span></span>
7.  <span data-ttu-id="1b483-125">Chiamare [**IWMWriter:: BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting) sul writer.</span><span class="sxs-lookup"><span data-stu-id="1b483-125">Call [**IWMWriter::BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting) on the writer.</span></span>
    ```C++
    hr = pWriter->BeginWriting();
    ```

    

8.  <span data-ttu-id="1b483-126">Per ogni esempio, chiamare il metodo [**IWMWriter:: WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) .</span><span class="sxs-lookup"><span data-stu-id="1b483-126">For each sample, call the [**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) method.</span></span> <span data-ttu-id="1b483-127">Specificare il numero di flusso, l'ora di presentazione, la durata dell'esempio e un puntatore al buffer di esempio.</span><span class="sxs-lookup"><span data-stu-id="1b483-127">Specify the stream number, the presentation time, the duration of the sample, and a pointer to the sample buffer.</span></span> <span data-ttu-id="1b483-128">Il metodo **WriteSample** comprime gli esempi.</span><span class="sxs-lookup"><span data-stu-id="1b483-128">The **WriteSample** method compresses the samples.</span></span>
9.  <span data-ttu-id="1b483-129">Al termine, chiamare [**IWMWriter:: EndWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-endwriting) sul writer.</span><span class="sxs-lookup"><span data-stu-id="1b483-129">When you are done, call [**IWMWriter::EndWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-endwriting) on the writer.</span></span>
    ```C++
    hr = pWriter->EndWriting();
    ```

    

10. <span data-ttu-id="1b483-130">Chiamare [**IWMWriterAdvanced:: RemoveSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink) sul writer per scollegare l'oggetto sink di rete.</span><span class="sxs-lookup"><span data-stu-id="1b483-130">Call [**IWMWriterAdvanced::RemoveSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink) on the writer to detach the network sink object.</span></span>
    ```C++
    hr = pWriterAdvanced->RemoveSink(pNetSink);
    ```

    

11. <span data-ttu-id="1b483-131">Chiamare [**IWMWriterNetworkSink:: Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-close) sul sink di rete per rilasciare la porta.</span><span class="sxs-lookup"><span data-stu-id="1b483-131">Call [**IWMWriterNetworkSink::Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-close) on the network sink to release the port.</span></span>
    ```C++
    hr = pNetSink->Close();
    ```

    

<span data-ttu-id="1b483-132">Un altro modo per eseguire lo streaming di contenuto ASF in una rete consiste nel leggerlo da un file ASF esistente.</span><span class="sxs-lookup"><span data-stu-id="1b483-132">Another way to stream ASF content over a network is to read it from an existing ASF file.</span></span> <span data-ttu-id="1b483-133">Questo approccio è illustrato nell'esempio WMVNetWrite fornito nell'SDK.</span><span class="sxs-lookup"><span data-stu-id="1b483-133">The WMVNetWrite sample provided in the SDK demonstrates this approach.</span></span> <span data-ttu-id="1b483-134">Oltre ai passaggi elencati in precedenza, eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="1b483-134">In addition to the steps listed previously, do the following:</span></span>

1.  <span data-ttu-id="1b483-135">Creare un oggetto Reader e chiamare il metodo **Open** con il nome del file.</span><span class="sxs-lookup"><span data-stu-id="1b483-135">Create a reader object and call the **Open** method with the name of the file.</span></span>
2.  <span data-ttu-id="1b483-136">Chiamare [**IWMReaderAdvanced:: SetManualStreamSelection**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setmanualstreamselection) sull'oggetto Reader, con il valore **true**.</span><span class="sxs-lookup"><span data-stu-id="1b483-136">Call [**IWMReaderAdvanced::SetManualStreamSelection**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setmanualstreamselection) on the reader object, with the value **TRUE**.</span></span> <span data-ttu-id="1b483-137">Ciò consente all'applicazione di leggere tutti i flussi nel file, inclusi i flussi con esclusione reciproca.</span><span class="sxs-lookup"><span data-stu-id="1b483-137">This enables the application to read every stream in the file, including streams with mutual exclusion.</span></span>
3.  <span data-ttu-id="1b483-138">Eseguire una query sul Reader per l'interfaccia [**IWMProfile**](iwmprofile.md) .</span><span class="sxs-lookup"><span data-stu-id="1b483-138">Query the reader for the [**IWMProfile**](iwmprofile.md) interface.</span></span> <span data-ttu-id="1b483-139">Utilizzare questo puntatore quando si chiama [**IWMWriter:: Seprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) nell'oggetto writer (passaggio 5 nella procedura precedente).</span><span class="sxs-lookup"><span data-stu-id="1b483-139">Use this pointer when you call [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) on the writer object (step 5 in the previous procedure).</span></span>
4.  <span data-ttu-id="1b483-140">Per ogni flusso definito nel profilo, chiamare [**IWMProfile:: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) per ottenere il numero di flusso.</span><span class="sxs-lookup"><span data-stu-id="1b483-140">For every stream defined in the profile, call [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) to get the stream number.</span></span> <span data-ttu-id="1b483-141">Passare questo numero di flusso al metodo [**IWMReaderAdvanced:: SetReceiveStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples) del Reader.</span><span class="sxs-lookup"><span data-stu-id="1b483-141">Pass this stream number to the reader's [**IWMReaderAdvanced::SetReceiveStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples) method.</span></span> <span data-ttu-id="1b483-142">Questo metodo comunica al lettore di fornire esempi compressi, anziché decodificarli.</span><span class="sxs-lookup"><span data-stu-id="1b483-142">This method informs the reader to deliver compressed samples, rather than decoding them.</span></span> <span data-ttu-id="1b483-143">Gli esempi verranno recapitati all'applicazione tramite il metodo di callback [**IWMReaderCallbackAdvanced:: OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1b483-143">The samples will be delivered to the application through the application's [**IWMReaderCallbackAdvanced::OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) callback method.</span></span>

    <span data-ttu-id="1b483-144">È necessario ottenere informazioni sui codec per ogni flusso letto non compresso e aggiungerlo all'intestazione prima della trasmissione.</span><span class="sxs-lookup"><span data-stu-id="1b483-144">You must obtain codec information for every stream that you read uncompressed and add it to the header before broadcast.</span></span> <span data-ttu-id="1b483-145">Per ottenere le informazioni sul codec, chiamare [**IWMHeaderInfo2:: GetCodecInfoCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) e [**IWMHeaderInfo2:: GetCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) per enumerare i codec associati al file nel lettore.</span><span class="sxs-lookup"><span data-stu-id="1b483-145">To obtain the codec information, call [**IWMHeaderInfo2::GetCodecInfoCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) and [**IWMHeaderInfo2::GetCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) to enumerate the codecs associated with the file in the reader.</span></span> <span data-ttu-id="1b483-146">Selezionare le informazioni sul codec che corrispondono alla configurazione del flusso.</span><span class="sxs-lookup"><span data-stu-id="1b483-146">Select the codec information that matches the stream configuration.</span></span> <span data-ttu-id="1b483-147">Impostare quindi le informazioni sul codec nel writer chiamando [**IWMHeaderInfo3:: AddCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo), passando le informazioni ottenute dal reader.</span><span class="sxs-lookup"><span data-stu-id="1b483-147">Then set the codec information in the writer by calling [**IWMHeaderInfo3::AddCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo), passing the information obtained from the reader.</span></span>

5.  <span data-ttu-id="1b483-148">Dopo aver impostato il profilo nel writer, chiamare [**IWMWriter:: GetInputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputcount) sul writer per ottenere il numero di input.</span><span class="sxs-lookup"><span data-stu-id="1b483-148">After you set the profile on the writer, call [**IWMWriter::GetInputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputcount) on the writer to get the number of inputs.</span></span> <span data-ttu-id="1b483-149">Per ogni input, chiamare [**IWMWriter:: SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) con il valore **null**.</span><span class="sxs-lookup"><span data-stu-id="1b483-149">For each input, call [**IWMWriter::SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) with the value **NULL**.</span></span> <span data-ttu-id="1b483-150">Ciò indica all'oggetto writer che l'applicazione fornirà esempi compressi, quindi il writer non deve usare alcun codec per comprimere i dati.</span><span class="sxs-lookup"><span data-stu-id="1b483-150">This indicates to the writer object that the application will deliver compressed samples, so the writer does not have to use any codecs to compress the data.</span></span> <span data-ttu-id="1b483-151">Assicurarsi di chiamare **SetInputProps** prima di chiamare **BeginWriting**.</span><span class="sxs-lookup"><span data-stu-id="1b483-151">Make sure to call **SetInputProps** before calling **BeginWriting**.</span></span>
6.  <span data-ttu-id="1b483-152">Facoltativamente, copiare gli attributi di metadati dal reader al writer</span><span class="sxs-lookup"><span data-stu-id="1b483-152">Optionally, copy the metadata attributes from the reader to the writer</span></span>
7.  <span data-ttu-id="1b483-153">Poiché gli esempi dal reader sono già compressi, usare il metodo [**IWMWriterAdvanced:: WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) per scrivere gli esempi, anziché il metodo **WriteSample** .</span><span class="sxs-lookup"><span data-stu-id="1b483-153">Because the samples from the reader are already compressed, use the [**IWMWriterAdvanced::WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) method to write the samples, instead of the **WriteSample** method.</span></span> <span data-ttu-id="1b483-154">Il metodo **WriteStreamSample** ignora le normali procedure di compressione dell'oggetto writer.</span><span class="sxs-lookup"><span data-stu-id="1b483-154">The **WriteStreamSample** method bypasses the writer object's usual compression procedures.</span></span>
8.  <span data-ttu-id="1b483-155">Quando il lettore raggiunge la fine del file, invia una \_ notifica WMT EOF all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1b483-155">When the reader reaches the end of the file, it sends a WMT\_EOF notification to the application.</span></span>

<span data-ttu-id="1b483-156">Inoltre, l'applicazione deve guidare l'orologio sull'oggetto Reader, in modo che il lettore estragga i dati dal file nel minor tempo possibile.</span><span class="sxs-lookup"><span data-stu-id="1b483-156">In addition, the application should drive the clock on the reader object, so that the reader pulls data from the file as quickly as possible.</span></span> <span data-ttu-id="1b483-157">A tale scopo, chiamare il metodo [**IWMReaderAdvanced:: SetUserProvidedClock**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setuserprovidedclock) sul Reader, con il valore **true**.</span><span class="sxs-lookup"><span data-stu-id="1b483-157">To do this, call the [**IWMReaderAdvanced::SetUserProvidedClock**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setuserprovidedclock) method on the reader, with the value **TRUE**.</span></span> <span data-ttu-id="1b483-158">Quando il lettore Invia la \_ notifica avviata da WMT, chiamare [**IWMReaderAdvanced::D elivertime**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-delivertime) e specificare l'intervallo di tempo che il lettore deve recapitare.</span><span class="sxs-lookup"><span data-stu-id="1b483-158">After the reader sends the WMT\_STARTED notification, call [**IWMReaderAdvanced::DeliverTime**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-delivertime) and specify the time interval that the reader should deliver.</span></span> <span data-ttu-id="1b483-159">Al termine della lettura di questo intervallo di tempo, il lettore chiama il metodo [**IWMReaderCallbackAdvanced:: OnTime**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-ontime) callback dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="1b483-159">After the reader is done reading this time interval, it calls the application's [**IWMReaderCallbackAdvanced::OnTime**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-ontime) callback method.</span></span> <span data-ttu-id="1b483-160">L'applicazione deve chiamare nuovamente **DeliverTime** per leggere l'intervallo di tempo successivo.</span><span class="sxs-lookup"><span data-stu-id="1b483-160">The application should call **DeliverTime** again to read the next time interval.</span></span> <span data-ttu-id="1b483-161">Ad esempio, per leggere da un file a intervalli di un secondo:</span><span class="sxs-lookup"><span data-stu-id="1b483-161">For example, to read from the file in one-second intervals:</span></span>


```C++
// Initial call to DeliverTime.
QWORD m_qwTime = 10000000; // 1 second.
hr = m_pReaderAdvanced->DeliverTime(m_qwTime);

// In the callback:
HRESULT CNetWrite::OnTime(QWORD cnsCurrentTime, void *pvContext)
{
    HRESULT hr = S_OK;
    // Continue calling DeliverTime until the end of the file.
    if(!m_bEOF)
    {
        m_qwTime += 10000000; // 1 second.
        hr = m_pReaderAdvanced->DeliverTime(m_qwTime);
    }
    return S_OK;
}
```



## <a name="related-topics"></a><span data-ttu-id="1b483-162">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1b483-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b483-163">**Invio di dati ASF in una rete**</span><span class="sxs-lookup"><span data-stu-id="1b483-163">**Sending ASF Data Over a Network**</span></span>](sending-asf-data-over-a-network.md)
</dt> <dt>

[<span data-ttu-id="1b483-164">**Utilizzo dei sink di writer**</span><span class="sxs-lookup"><span data-stu-id="1b483-164">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 




