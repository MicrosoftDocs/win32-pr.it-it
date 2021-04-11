---
description: Generazione di esempi di flusso da un oggetto dati ASF esistente
ms.assetid: eb27f122-d958-495d-98ea-8befd105a9a8
title: Generazione di esempi di flusso da un oggetto dati ASF esistente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee612c9352e3295d6b4957922e385de40a9a1fa3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127883"
---
# <a name="generating-stream-samples-from-an-existing-asf-data-object"></a><span data-ttu-id="1f54f-103">Generazione di esempi di flusso da un oggetto dati ASF esistente</span><span class="sxs-lookup"><span data-stu-id="1f54f-103">Generating Stream Samples from an Existing ASF Data Object</span></span>

<span data-ttu-id="1f54f-104">L'oggetto *splitter* ASF è un componente di livello WMContainer che analizza l'oggetto dati ASF di un file di formato Advanced Systems (ASF).</span><span class="sxs-lookup"><span data-stu-id="1f54f-104">The ASF *splitter* object is a WMContainer layer component that parses the ASF Data Object of an Advanced Systems Format (ASF) file.</span></span>

<span data-ttu-id="1f54f-105">Prima di passare i pacchetti di dati alla barra di divisione, l'applicazione deve inizializzare, configurare e selezionare i flussi nella barra di divisione per prepararla per il processo di analisi.</span><span class="sxs-lookup"><span data-stu-id="1f54f-105">Before passing data packets to the splitter, the application must initialize, configure, and select streams on the splitter in order to prepare it for the parsing process.</span></span> <span data-ttu-id="1f54f-106">Per informazioni, vedere [Creating the ASF Splitter Object](creating-the-asf-splitter-object.md) e [Configuring the ASF Splitter Object](configuring-the-asf-splitter-object.md).</span><span class="sxs-lookup"><span data-stu-id="1f54f-106">For information, see [Creating the ASF Splitter Object](creating-the-asf-splitter-object.md) and [Configuring the ASF Splitter Object](configuring-the-asf-splitter-object.md).</span></span>

<span data-ttu-id="1f54f-107">I metodi necessari per l'analisi dell'oggetto dati ASF sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="1f54f-107">The methods required for parsing the ASF Data Object are:</span></span>

-   <span data-ttu-id="1f54f-108">[**IMFASFSplitter::P arsedata**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) che avvia il processo di analisi effettuando il push del buffer contenente i pacchetti di dati nella barra di divisione.</span><span class="sxs-lookup"><span data-stu-id="1f54f-108">[**IMFASFSplitter::ParseData**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) that starts the parsing process by pushing the buffer containing data packets to the splitter.</span></span>
-   <span data-ttu-id="1f54f-109">[**IMFASFSplitter:: GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) che raccoglie gli esempi di flusso generati dal buffer passato alla barra di divisione.</span><span class="sxs-lookup"><span data-stu-id="1f54f-109">[**IMFASFSplitter::GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) that collects stream samples that were generated from the buffer passed to splitter.</span></span>

## <a name="finding-the-data-offset"></a><span data-ttu-id="1f54f-110">Ricerca dell'offset dei dati</span><span class="sxs-lookup"><span data-stu-id="1f54f-110">Finding the Data Offset</span></span>

<span data-ttu-id="1f54f-111">Prima di avviare il processo di analisi, l'applicazione deve individuare l'oggetto dati all'interno del file ASF.</span><span class="sxs-lookup"><span data-stu-id="1f54f-111">Before starting the parsing process, the application must locate the Data Object within the ASF file.</span></span> <span data-ttu-id="1f54f-112">Esistono due modi per ottenere l'offset dell'oggetto dati dall'inizio del file:</span><span class="sxs-lookup"><span data-stu-id="1f54f-112">There are two ways to get the offset of the Data Object from the start of the file:</span></span>

-   <span data-ttu-id="1f54f-113">Prima di avere inizializzato l'oggetto ContentInfo, è possibile chiamare il metodo [**IMFASFContentInfo:: GetHeaderSize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) .</span><span class="sxs-lookup"><span data-stu-id="1f54f-113">Before you have initialized the ContentInfo object, you can call the [**IMFASFContentInfo::GetHeaderSize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) method.</span></span> <span data-ttu-id="1f54f-114">Questo metodo richiede un buffer che contiene i primi 30 byte dell'intestazione ASF.</span><span class="sxs-lookup"><span data-stu-id="1f54f-114">This method requires a buffer that contains the first 30 bytes of the ASF header.</span></span> <span data-ttu-id="1f54f-115">Restituisce la dimensione dell'intera intestazione che indica l'offset al primo pacchetto di dati.</span><span class="sxs-lookup"><span data-stu-id="1f54f-115">It returns the size of the entire header that indicates the offset to the first data packet.</span></span> <span data-ttu-id="1f54f-116">Questo valore include anche le dimensioni dell'intestazione dell'oggetto dati di 50 byte.</span><span class="sxs-lookup"><span data-stu-id="1f54f-116">This value also includes the Data Object header size of 50 bytes.</span></span>
-   <span data-ttu-id="1f54f-117">Dopo avere inizializzato l'oggetto ContentInfo, è possibile ottenere il descrittore di presentazione chiamando [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)e quindi eseguendo una query sul descrittore di presentazione per l'attributo di [**\_ \_ \_ \_ \_ offset iniziale dei dati MF PD ASF**](mf-pd-asf-data-start-offset-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="1f54f-117">After you have initialized the ContentInfo object, you can get the presentation descriptor by calling [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor), and then querying the presentation descriptor for the [**MF\_PD\_ASF\_DATA\_START\_OFFSET**](mf-pd-asf-data-start-offset-attribute.md) attribute.</span></span> <span data-ttu-id="1f54f-118">Il valore di questo attributo è la dimensione dell'intestazione.</span><span class="sxs-lookup"><span data-stu-id="1f54f-118">The value of this attribute is the header size.</span></span>
    > [!Note]  
    > <span data-ttu-id="1f54f-119">L'attributo di [**\_ lunghezza dei dati MF PD \_ ASF \_ \_**](mf-pd-asf-data-length-attribute.md) nel descrittore di presentazione specifica la lunghezza dell'oggetto dati ASF.</span><span class="sxs-lookup"><span data-stu-id="1f54f-119">The [**MF\_PD\_ASF\_DATA\_LENGTH**](mf-pd-asf-data-length-attribute.md) attribute on the presentation descriptor specifies the length of the ASF Data Object.</span></span>

     

<span data-ttu-id="1f54f-120">In entrambi i casi, il valore restituito è la dimensione dell'oggetto intestazione più le dimensioni della sezione dell'intestazione dell'oggetto dati.</span><span class="sxs-lookup"><span data-stu-id="1f54f-120">In both cases, the returned value is the size of the Header Object plus the size of the header section of the Data Object.</span></span> <span data-ttu-id="1f54f-121">Pertanto, il valore risultante è l'offset all'inizio dei pacchetti di dati nell'oggetto dati ASF.</span><span class="sxs-lookup"><span data-stu-id="1f54f-121">Therefore, the resulting value is the offset to the start of the data packets in the ASF Data Object.</span></span> <span data-ttu-id="1f54f-122">Quando si inizia a inviare dati alla barra di divisione, i dati devono iniziare in corrispondenza di questo offset dall'inizio del file ASF.</span><span class="sxs-lookup"><span data-stu-id="1f54f-122">When you begin sending data to the splitter, the data must start at this offset from the beginning of the ASF file.</span></span>

<span data-ttu-id="1f54f-123">Il valore di offset viene passato come parametro a **ParseData** che avvia il processo di analisi.</span><span class="sxs-lookup"><span data-stu-id="1f54f-123">The offset value is passed as a parameter to **ParseData** that starts the parsing process.</span></span>

<span data-ttu-id="1f54f-124">L'oggetto dati è suddiviso in pacchetti di dati.</span><span class="sxs-lookup"><span data-stu-id="1f54f-124">The Data Object is divided into data packets.</span></span> <span data-ttu-id="1f54f-125">Ogni pacchetto di dati contiene un'intestazione del pacchetto di dati che fornisce informazioni sull'analisi dei pacchetti e i dati di payload, ovvero i dati multimediali digitali effettivi.</span><span class="sxs-lookup"><span data-stu-id="1f54f-125">Each data packet contains a data packet header that provides packet parsing information and the payload data—the actual digital media data.</span></span> <span data-ttu-id="1f54f-126">In uno scenario di ricerca, l'applicazione potrebbe volere che la barra di divisione avvii l'analisi in un particolare pacchetto di dati.</span><span class="sxs-lookup"><span data-stu-id="1f54f-126">In a seeking scenario, the application might want the splitter to start parsing at a particular data packet.</span></span> <span data-ttu-id="1f54f-127">A tale scopo, è possibile usare l'indicizzatore ASF per recuperare l'offset.</span><span class="sxs-lookup"><span data-stu-id="1f54f-127">To do this, you can use the ASF Indexer is used to retrieve the offset.</span></span> <span data-ttu-id="1f54f-128">L'indicizzatore restituisce un valore di offset che inizia in corrispondenza del limite del pacchetto.</span><span class="sxs-lookup"><span data-stu-id="1f54f-128">The indexer returns an offset value that starts at the packet boundary.</span></span> <span data-ttu-id="1f54f-129">Se non si utilizza l'indicizzatore, verificare che l'offset venga avviato all'inizio dell'intestazione del pacchetto di dati.</span><span class="sxs-lookup"><span data-stu-id="1f54f-129">If you are not using the indexer, make sure that the offset starts at the start of the data packet header.</span></span> <span data-ttu-id="1f54f-130">Se un offset non valido viene passato alla barra di divisione, ad esempio se il valore non punta al limite del pacchetto, le chiamate a **ParseHeader** e **GetNextSample** hanno esito positivo, ma **GetNextSample** non recupera alcun campione e il valore **null** viene ricevuto nel parametro *pSample* .</span><span class="sxs-lookup"><span data-stu-id="1f54f-130">If an invalid offset is passed to the splitter, such as the value does not point at the packet boundary, **ParseHeader** and **GetNextSample** calls succeed but **GetNextSample** does not retrieve any samples and **NULL** is received in the *pSample* parameter.</span></span>

<span data-ttu-id="1f54f-131">Se la barra di divisione è configurata in modo da essere analizzata nella direzione inversa, la barra di divisione inizia sempre l'analisi alla fine del buffer multimediale passato a **ParseData**.</span><span class="sxs-lookup"><span data-stu-id="1f54f-131">If the splitter is configured to parse in the reverse direction, then the splitter always starts parsing at the end of the media buffer that is passed to **ParseData**.</span></span> <span data-ttu-id="1f54f-132">Pertanto, per l'analisi inversa nella chiamata a **ParseData**, passare l'offset nel parametro *cbLength* , che specifica la lunghezza dei dati e impostare *cbBufferOffset* su zero.</span><span class="sxs-lookup"><span data-stu-id="1f54f-132">Therefore, for reverse parsing in the call to **ParseData**, pass the offset in the *cbLength* parameter, which specifies the length of the data and set *cbBufferOffset* to zero.</span></span>

## <a name="generating-samples-for-asf-data-packets"></a><span data-ttu-id="1f54f-133">Generazione di esempi per i pacchetti di dati ASF</span><span class="sxs-lookup"><span data-stu-id="1f54f-133">Generating Samples for ASF Data Packets</span></span>

<span data-ttu-id="1f54f-134">Un'applicazione avvia il processo di analisi passando i pacchetti di dati alla barra di divisione.</span><span class="sxs-lookup"><span data-stu-id="1f54f-134">An application starts the parsing process by passing the data packets to the splitter.</span></span> <span data-ttu-id="1f54f-135">L'input per la barra di divisione è costituito da una serie di buffer multimediali che contengono l'intero oggetto o frammenti dell'oggetto dati.</span><span class="sxs-lookup"><span data-stu-id="1f54f-135">The input to the splitter is a series of media buffers that contain the entire or fragments of the Data Object.</span></span> <span data-ttu-id="1f54f-136">L'output della barra di divisione è costituito da una serie di esempi di supporti che contengono i dati dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="1f54f-136">The output from the splitter is a series of media samples that contain the packet data.</span></span>

<span data-ttu-id="1f54f-137">Per passare i dati di input alla barra di divisione, creare un buffer multimediale e riempirlo con i dati della sezione oggetto dati del file ASF.</span><span class="sxs-lookup"><span data-stu-id="1f54f-137">To pass input data to the splitter, create a media buffer and fill it with data from the Data Object section of the ASF file.</span></span> <span data-ttu-id="1f54f-138">Per ulteriori informazioni sui buffer multimediali, vedere [buffer multimediali](media-buffers.md). Passare quindi il buffer multimediale al metodo [**IMFASFSplitter::P arsedata**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) .</span><span class="sxs-lookup"><span data-stu-id="1f54f-138">(For more information about media buffers, see [Media Buffers](media-buffers.md).) Then, pass the media buffer to the [**IMFASFSplitter::ParseData**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) method.</span></span> <span data-ttu-id="1f54f-139">È inoltre possibile specificare:</span><span class="sxs-lookup"><span data-stu-id="1f54f-139">You can also specify:</span></span>

-   <span data-ttu-id="1f54f-140">Offset nel buffer in cui deve iniziare l'analisi della barra di divisione.</span><span class="sxs-lookup"><span data-stu-id="1f54f-140">The offset into the buffer where the splitter should start parsing.</span></span> <span data-ttu-id="1f54f-141">Se l'offset è zero, l'analisi inizia all'inizio del buffer.</span><span class="sxs-lookup"><span data-stu-id="1f54f-141">If the offset is zero, parsing begins at the start of the buffer.</span></span> <span data-ttu-id="1f54f-142">Per informazioni sull'impostazione dell'offset dei dati, vedere la sezione "ricerca dell'offset dei dati" in questo argomento.</span><span class="sxs-lookup"><span data-stu-id="1f54f-142">For information about setting the data offset, see the "Finding the Data Offset" section in this topic.</span></span>
-   <span data-ttu-id="1f54f-143">Quantità di dati da analizzare.</span><span class="sxs-lookup"><span data-stu-id="1f54f-143">The amount of data to parse.</span></span> <span data-ttu-id="1f54f-144">Se questo valore è zero, la barra di divisione viene analizzata fino a quando non raggiunge la fine del buffer, come specificato dal metodo [**IMFMediaBuffer:: GetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getcurrentlength) .</span><span class="sxs-lookup"><span data-stu-id="1f54f-144">If this value is zero, the splitter parses until it reaches the end of the buffer, as specified by the [**IMFMediaBuffer::GetCurrentLength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getcurrentlength) method.</span></span>

<span data-ttu-id="1f54f-145">La barra di divisione genera esempi di supporti facendo riferimento ai dati nei buffer multimediali.</span><span class="sxs-lookup"><span data-stu-id="1f54f-145">The splitter generates media samples by referencing the data in the media buffers.</span></span> <span data-ttu-id="1f54f-146">Il client può recuperare gli esempi di output chiamando [**IMFASFSplitter:: GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) in un ciclo fino a quando non sono presenti altri dati da analizzare.</span><span class="sxs-lookup"><span data-stu-id="1f54f-146">The client can retrieve the output samples by calling [**IMFASFSplitter::GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) in a loop until there is no more data to parse.</span></span> <span data-ttu-id="1f54f-147">Se **GetNextSample** restituisce il \_ flag ASF STATUSFLAGS \_ incompleto nel parametro *pdwStatusFlags* , significa che sono disponibili altri esempi da recuperare e che l'applicazione può chiamare nuovamente **GetNextSample** .</span><span class="sxs-lookup"><span data-stu-id="1f54f-147">If **GetNextSample** returns the ASF\_STATUSFLAGS\_INCOMPLETE flag in the *pdwStatusFlags* parameter, it means there are more samples to retrieve, and the application can call **GetNextSample** again.</span></span> <span data-ttu-id="1f54f-148">In caso contrario, chiamare **ParseData** per passare più dati alla barra di divisione.</span><span class="sxs-lookup"><span data-stu-id="1f54f-148">Otherwise, call **ParseData** to pass more data to the splitter.</span></span> <span data-ttu-id="1f54f-149">Per gli esempi generati, la barra di divisione imposta le informazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="1f54f-149">For the generated samples, the splitter sets the following information:</span></span>

-   <span data-ttu-id="1f54f-150">La barra di divisione imposta un timestamp per tutti gli esempi generati.</span><span class="sxs-lookup"><span data-stu-id="1f54f-150">The splitter sets a time stamp on all the samples that it generates.</span></span> <span data-ttu-id="1f54f-151">L'ora di esempio rappresenta l'ora di presentazione e non include il tempo di preiscrizione.</span><span class="sxs-lookup"><span data-stu-id="1f54f-151">The sample time represents the presentation time and does not include the preroll time.</span></span> <span data-ttu-id="1f54f-152">L'applicazione può chiamare [**IMFSample:: GetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) per ottenere l'ora di presentazione, in unità di 100 nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="1f54f-152">The application can call [**IMFSample::GetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) to get the presentation time, in 100-nanosecond units.</span></span>
-   <span data-ttu-id="1f54f-153">Se si verifica un'interruzione durante la generazione del campione, la barra di divisione imposta l'attributo di [**\_ discontinuità MFSampleExtension**](mfsampleextension-discontinuity-attribute.md) sul primo campione dopo la discontinuità.</span><span class="sxs-lookup"><span data-stu-id="1f54f-153">If a break occurs during sample generation, the splitter sets the [**MFSampleExtension\_Discontinuity**](mfsampleextension-discontinuity-attribute.md) attribute on the first sample after the discontinuity.</span></span> <span data-ttu-id="1f54f-154">Le discontinuità sono in genere dovute a pacchetti eliminati in una connessione di rete, a dati di file danneggiati o al cambio di barra di divisione da un flusso di origine a un altro.</span><span class="sxs-lookup"><span data-stu-id="1f54f-154">Discontinuities are usually caused by dropped packets on a network connection, corrupt file data, or the splitter switching from one source stream to another.</span></span>
-   <span data-ttu-id="1f54f-155">Per video, la barra di divisione controlla se l'esempio contiene un fotogramma chiave.</span><span class="sxs-lookup"><span data-stu-id="1f54f-155">For video, the splitter checks whether the sample contains a key frame.</span></span> <span data-ttu-id="1f54f-156">In caso contrario, la barra di divisione imposta l'attributo [**MFSampleExtension \_ CleanPoint**](mfsampleextension-cleanpoint-attribute.md) nell'esempio.</span><span class="sxs-lookup"><span data-stu-id="1f54f-156">If it does, the splitter sets the [**MFSampleExtension\_CleanPoint**](mfsampleextension-cleanpoint-attribute.md) attribute on the sample.</span></span>

<span data-ttu-id="1f54f-157">Se la barra di divisione analizza i pacchetti di dati ricevuti da un server multimediale, è possibile che la lunghezza del pacchetto sia variabile.</span><span class="sxs-lookup"><span data-stu-id="1f54f-157">If the splitter is parsing data packets that are received from a media server, it is possible that the packet length is variable.</span></span> <span data-ttu-id="1f54f-158">In questo caso, il client deve chiamare **ParseData** per ogni pacchetto e impostare l' [**attributo \_ \_ limite del pacchetto MFASFSPLITTER**](mfasfsplitter-packet-boundary-attribute.md) in ogni buffer inviato al separatore.</span><span class="sxs-lookup"><span data-stu-id="1f54f-158">In this case, the client must call **ParseData** for each packet and set the [**MFASFSPLITTER\_PACKET\_BOUNDARY**](mfasfsplitter-packet-boundary-attribute.md) attribute on each buffer that is sent to the splitter.</span></span> <span data-ttu-id="1f54f-159">Questo attributo indica alla barra di divisione se il buffer multimediale contiene l'inizio di un pacchetto ASF.</span><span class="sxs-lookup"><span data-stu-id="1f54f-159">This attribute indicates to the splitter whether the media buffer contains the start of an ASF packet.</span></span> <span data-ttu-id="1f54f-160">Impostare l'attributo su **true** se il buffer contiene l'inizio di un nuovo pacchetto.</span><span class="sxs-lookup"><span data-stu-id="1f54f-160">Set the attribute to **TRUE** if the buffer contains the start of a new packet.</span></span> <span data-ttu-id="1f54f-161">Se il buffer contiene una continuazione del pacchetto precedente, impostare l'attributo su **false**.</span><span class="sxs-lookup"><span data-stu-id="1f54f-161">If the buffer contains a continuation of the previous packet, set the attribute to **FALSE**.</span></span> <span data-ttu-id="1f54f-162">I buffer non possono estendersi su più pacchetti.</span><span class="sxs-lookup"><span data-stu-id="1f54f-162">The buffers cannot span multiple packets.</span></span>

<span data-ttu-id="1f54f-163">Prima di passare i nuovi buffer multimediali alla barra di divisione, l'applicazione deve chiamare [**IMFASFSplitter:: Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-flush).</span><span class="sxs-lookup"><span data-stu-id="1f54f-163">Before passing new media buffers to the splitter, the application must call [**IMFASFSplitter::Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-flush).</span></span> <span data-ttu-id="1f54f-164">Questo metodo reimposta la barra di divisione e cancella tutti i frame parziali in attesa di essere completati.</span><span class="sxs-lookup"><span data-stu-id="1f54f-164">This method resets the splitter and clears any partial frame that is waiting to be completed.</span></span> <span data-ttu-id="1f54f-165">Questa operazione è utile in uno scenario di ricerca in cui l'offset si trova in una posizione diversa.</span><span class="sxs-lookup"><span data-stu-id="1f54f-165">This is useful in a seeking scenario where the offset is at a different location.</span></span>

### <a name="example"></a><span data-ttu-id="1f54f-166">Esempio</span><span class="sxs-lookup"><span data-stu-id="1f54f-166">Example</span></span>

<span data-ttu-id="1f54f-167">Nell'esempio di codice seguente viene illustrato come analizzare i pacchetti di dati.</span><span class="sxs-lookup"><span data-stu-id="1f54f-167">The following code example shows how to parse data packets.</span></span> <span data-ttu-id="1f54f-168">In questo esempio viene analizzato dall'inizio dell'oggetto dati alla fine del flusso e vengono visualizzate informazioni sugli esempi contenenti fotogrammi chiave.</span><span class="sxs-lookup"><span data-stu-id="1f54f-168">This example parses from the beginning of the Data Object to the end of the stream and displays information about the samples that contain key frames.</span></span> <span data-ttu-id="1f54f-169">Per un esempio completo in cui viene usato questo codice, vedere [esercitazione: lettura di un file ASF](tutorial--reading-an-asf-file.md).</span><span class="sxs-lookup"><span data-stu-id="1f54f-169">For a complete example that uses this code, see [Tutorial: Reading an ASF File](tutorial--reading-an-asf-file.md).</span></span>


```C++
// Parse the video stream and display information about the video samples.
//
// The current read position of the byte stream must be at the start of the ASF
// Data Object.

HRESULT DisplayKeyFrames(IMFByteStream *pStream, IMFASFSplitter *pSplitter)
{
    const DWORD cbReadSize = 2048;  // Read size (arbitrary value)

    IMFMediaBuffer *pBuffer = NULL;
    IMFSample *pSample = NULL;

    HRESULT hr = S_OK;
    while (SUCCEEDED(hr))
    {
        // The parser must get a newly allocated buffer each time.
        hr = MFCreateMemoryBuffer(cbReadSize, &pBuffer);
        if (FAILED(hr))
        {
            break;
        }

        // Read data into the buffer.
        hr = ReadFromByteStream(pStream, pBuffer, cbReadSize);
        if (FAILED(hr)) 
        {
            break; 
        }

        // Get the amound of data that was read.
        DWORD cbData;
        hr = pBuffer->GetCurrentLength(&cbData);
        if (FAILED(hr)) 
        { 
            break; 
        }

        if (cbData == 0)
        {
            break; // End of file.
        }

        // Send the data to the ASF splitter.
        hr = pSplitter->ParseData(pBuffer, 0, 0);
        SafeRelease(&pBuffer);
        if (FAILED(hr)) 
        { 
            break; 
        }

        // Pull samples from the splitter.
        DWORD parsingStatus = 0;
        do
        {
            WORD streamID;
            hr = pSplitter->GetNextSample(&parsingStatus, &streamID, &pSample);
            if (FAILED(hr)) 
            { 
                break; 
            }
            if (pSample == NULL)
            {
                // No samples yet. Parse more data.
                break;
            }
            if (IsRandomAccessPoint(pSample))
            {
                DisplayKeyFrame(pSample);
            }
            SafeRelease(&pSample);
            
        } while (parsingStatus & ASF_STATUSFLAGS_INCOMPLETE);
    }
    SafeRelease(&pSample);
    SafeRelease(&pBuffer);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="1f54f-170">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1f54f-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f54f-171">Barra di divisione ASF</span><span class="sxs-lookup"><span data-stu-id="1f54f-171">ASF Splitter</span></span>](asf-splitter.md)
</dt> </dl>

 

 



