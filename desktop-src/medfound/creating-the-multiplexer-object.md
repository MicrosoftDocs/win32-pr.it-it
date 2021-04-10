---
description: Creazione dell'oggetto multiplexer
ms.assetid: a5adc40c-abb4-4012-b6f2-eb871eaed7b9
title: Creazione dell'oggetto multiplexer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b28dd7933bdd7c3a8587c96cb490c4e4122ecc04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225825"
---
# <a name="creating-the-multiplexer-object"></a><span data-ttu-id="93e28-103">Creazione dell'oggetto multiplexer</span><span class="sxs-lookup"><span data-stu-id="93e28-103">Creating the Multiplexer Object</span></span>

<span data-ttu-id="93e28-104">Il multiplexing ASF è un oggetto livello WMContainer che funziona con l' [oggetto dati ASF](asf-file-structure.md) e fornisce a un'applicazione la possibilità di generare pacchetti di dati ASF per flussi multimediali.</span><span class="sxs-lookup"><span data-stu-id="93e28-104">The ASF multiplexer is a WMContainer layer object that works with the [ASF Data Object](asf-file-structure.md) and gives an application the ability to generate ASF data packets for media streams.</span></span>

<span data-ttu-id="93e28-105">L'oggetto multiplexer espone l'interfaccia [**IMFASFMultiplexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmultiplexer) .</span><span class="sxs-lookup"><span data-stu-id="93e28-105">The multiplexer object exposes the [**IMFASFMultiplexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfmultiplexer) interface.</span></span> <span data-ttu-id="93e28-106">Per creare il multiplexer, chiamare [**MFCreateASFMultiplexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmultiplexer).</span><span class="sxs-lookup"><span data-stu-id="93e28-106">To create the multiplexer, call [**MFCreateASFMultiplexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmultiplexer).</span></span> <span data-ttu-id="93e28-107">Questa funzione restituisce un puntatore a un oggetto vuoto.</span><span class="sxs-lookup"><span data-stu-id="93e28-107">This function returns a pointer to an empty object.</span></span> <span data-ttu-id="93e28-108">Se l'applicazione sta scrivendo un nuovo file ASF, l'applicazione deve inizializzare il multiplexer con un oggetto ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="93e28-108">If the application is writing a new ASF file, the application must initialize the multiplexer with a ContentInfo object.</span></span> <span data-ttu-id="93e28-109">A tale scopo, chiamare [**IMFASFMultiplexer:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize).</span><span class="sxs-lookup"><span data-stu-id="93e28-109">To do this, call [**IMFASFMultiplexer::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize).</span></span> <span data-ttu-id="93e28-110">L'oggetto ContentInfo specificato rappresenta l'oggetto intestazione ASF del nuovo file.</span><span class="sxs-lookup"><span data-stu-id="93e28-110">The specified ContentInfo object represents the ASF Header Object of the new file.</span></span> <span data-ttu-id="93e28-111">Per informazioni sulla creazione e l'inizializzazione dell'oggetto ContentInfo per un nuovo file, vedere [inizializzazione dell'oggetto ContentInfo di un nuovo file ASF](initializing-the-contentinfo-object-of-a-new-asf-file.md).</span><span class="sxs-lookup"><span data-stu-id="93e28-111">For information about creating and initializing the ContentInfo object for a new file, see [Initializing the ContentInfo Object of a New ASF File](initializing-the-contentinfo-object-of-a-new-asf-file.md).</span></span>

<span data-ttu-id="93e28-112">Il metodo [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) analizza l'oggetto ContentInfo per raccogliere informazioni sulla configurazione del flusso, ad esempio il numero di flussi, le dimensioni del pacchetto e la preroll.</span><span class="sxs-lookup"><span data-stu-id="93e28-112">The [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) method parses the ContentInfo object to collect stream configuration information such as the number of streams, packet size, preroll.</span></span> <span data-ttu-id="93e28-113">Facoltativamente, il multiplexer potrebbe avere anche bisogno di parametri di bucket a perdita e delle unità di estensione del payload.</span><span class="sxs-lookup"><span data-stu-id="93e28-113">Optionally, the multiplexer might also need leaky bucket parameters, and the payload extension units.</span></span> <span data-ttu-id="93e28-114">Queste informazioni sono necessarie per generare pacchetti di dati che soddisfano i requisiti definiti nell'oggetto intestazione ASF.</span><span class="sxs-lookup"><span data-stu-id="93e28-114">This information is required in order to generate data packets that match the requirements defined in the ASF Header Object.</span></span> <span data-ttu-id="93e28-115">Il metodo **Initialize** configura il multiplexer in base al tipo di supporto e alle impostazioni di configurazione dei flussi.</span><span class="sxs-lookup"><span data-stu-id="93e28-115">The **Initialize** method configures the multiplexer based on the media type and configuration settings of the streams.</span></span> <span data-ttu-id="93e28-116">Ad esempio, se un flusso è configurato per avere estensioni del payload (vedere [creazione e configurazione di flussi ASF](creating-and-configuring-asf-streams.md)), il multiplexer è configurato per aggiungere tali valori ai pacchetti di dati generati.</span><span class="sxs-lookup"><span data-stu-id="93e28-116">For example, if a stream is configured to have payload extensions (see [Creating and Configuring ASF Streams](creating-and-configuring-asf-streams.md)), and then the multiplexer is configured to add those values to the generated data packets.</span></span>

<span data-ttu-id="93e28-117">Il metodo [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) ottiene anche un handle per l'oggetto dati iniziale creato durante la creazione dell'oggetto ContentInfo per la scrittura.</span><span class="sxs-lookup"><span data-stu-id="93e28-117">The [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) method also gets a handle to the initial data object that was created during the creation of the ContentInfo object for writing.</span></span> <span data-ttu-id="93e28-118">Durante la generazione dei pacchetti di dati, il multiplexer aggiunge pacchetti all'oggetto dati e li aggiorna in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="93e28-118">During data packet generation, the multiplexer adds packets to the data object and updates it appropriately.</span></span> <span data-ttu-id="93e28-119">Dopo che il multiplexer ha generato tutti i pacchetti di dati, aggiorna l'oggetto ContentInfo fornito in modo che vengano aggiornati determinati valori, ad esempio il numero di pacchetti di dati.</span><span class="sxs-lookup"><span data-stu-id="93e28-119">After the multiplexer generates all the data packets, it updates the supplied ContentInfo object so that certain values, such as number of data packets, are updated.</span></span>

<span data-ttu-id="93e28-120">Nell'esempio di codice seguente viene illustrato come creare un multiplexer e come inizializzarlo con un oggetto ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="93e28-120">The following code example shows how to create a multiplexer and initialize it with a ContentInfo object.</span></span>


```C++
//-------------------------------------------------------------------
// CreateOutputGenerators
//
// Creates the ASF mux and the ASF Content Info object for the 
// output file.
//-------------------------------------------------------------------

HRESULT CreateOutputGenerators(
    IMFASFProfile *pProfile, 
    IMFASFContentInfo **ppContentInfo, 
    IMFASFMultiplexer **ppMux
    )
{
    IMFASFContentInfo *pContentInfo = NULL;
    IMFASFMultiplexer *pMux = NULL;

    // Use the ASF profile to create the ContentInfo object.
    HRESULT hr = MFCreateASFContentInfo(&pContentInfo);

    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->SetProfile(pProfile);
    }

    // Create the ASF Multiplexer object.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateASFMultiplexer(&pMux);
    }
    
    // Initialize it using the new ContentInfo object.
    if (SUCCEEDED(hr))
    {
        hr = pMux->Initialize(pContentInfo);
    }

    // Return the pointers to the caller.
    if (SUCCEEDED(hr))
    {
        *ppContentInfo = pContentInfo;
        (*ppContentInfo)->AddRef();

        *ppMux = pMux;
        (*ppMux)->AddRef();
    }

    SafeRelease(&pContentInfo);
    SafeRelease(&pMux);

    return hr;
}
```



<span data-ttu-id="93e28-121">Per visualizzare questa funzione utilizzata in un'applicazione completa, vedere [esercitazione: copia di flussi ASF da un file a un altro](tutorial--copying-asf-streams-from-one-file-to-another.md).</span><span class="sxs-lookup"><span data-stu-id="93e28-121">To see this function used in a complete application, see [Tutorial: Copying ASF Streams from One File to Another](tutorial--copying-asf-streams-from-one-file-to-another.md).</span></span>

## <a name="multiplexer-initialization-and-leaky-bucket-settings"></a><span data-ttu-id="93e28-122">Impostazioni di inizializzazione del multiplexer e bucket a perdita</span><span class="sxs-lookup"><span data-stu-id="93e28-122">Multiplexer Initialization and Leaky Bucket Settings</span></span>

<span data-ttu-id="93e28-123">Il metodo [**IMFASFMultiplexer:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) configura il multiplexer per determinare il flusso di dati del bucket di perdita.</span><span class="sxs-lookup"><span data-stu-id="93e28-123">The [**IMFASFMultiplexer::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) method configures the multiplexer to determine the leaky bucket data flow.</span></span> <span data-ttu-id="93e28-124">Per configurare questi parametri, verificare che i valori di proprietà seguenti siano impostati sull'oggetto ContentInfo specificato.</span><span class="sxs-lookup"><span data-stu-id="93e28-124">To configure these parameters, make sure that the following property values are set on the specified ContentInfo object.</span></span> <span data-ttu-id="93e28-125">Per informazioni sull'impostazione di queste proprietà, vedere [impostazione delle proprietà nell'oggetto ContentInfo](setting-properties-in-the-contentinfo-object.md).</span><span class="sxs-lookup"><span data-stu-id="93e28-125">For information about setting these properties, see [Setting Properties in the ContentInfo Object](setting-properties-in-the-contentinfo-object.md).</span></span>

-   <span data-ttu-id="93e28-126">[**MFPKEY \_ ASFMEDIASINK \_ AutoAdjust \_ bitrate**](mfpkey-asfmediasink-autoadjust-bitrate-property.md) Property: indica se il multiplexer deve modificare automaticamente la velocità in bit per mantenere il flusso di dati nel bucket.</span><span class="sxs-lookup"><span data-stu-id="93e28-126">[**MFPKEY\_ASFMEDIASINK\_AUTOADJUST\_BITRATE**](mfpkey-asfmediasink-autoadjust-bitrate-property.md) property: This indicates whether the multiplexer needs to adjust the bit rate automatically, to maintain the data flow in the leaky bucket.</span></span> <span data-ttu-id="93e28-127">Questa impostazione può essere modificata dall'applicazione chiamando [**IMFASFMultiplexer:: Seflags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags) e passando il flag **MFASF \_ multiplexer \_ AutoAdjust \_ bitrate** .</span><span class="sxs-lookup"><span data-stu-id="93e28-127">This setting can be changed by the application by calling [**IMFASFMultiplexer::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags) and passing the **MFASF\_MULTIPLEXER\_AUTOADJUST\_BITRATE** flag.</span></span>

-   <span data-ttu-id="93e28-128">[**MFPKEY \_ ASFMEDIASINK \_ base \_ SENDTIME**](mfpkey-asfmediasink-base-sendtime-property.md) Property: il tempo di invio indica quando verrà rilasciato il payload all'interno del bucket Leaky.</span><span class="sxs-lookup"><span data-stu-id="93e28-128">[**MFPKEY\_ASFMEDIASINK\_BASE\_SENDTIME**](mfpkey-asfmediasink-base-sendtime-property.md) property: The send time indicates when the payload inside the leaky bucket will be released.</span></span> <span data-ttu-id="93e28-129">L'ora di invio deve essere uguale o precedente all'ora di presentazione perché il payload deve avere tempo per arrivare alla destinazione prima dell'ora di presentazione.</span><span class="sxs-lookup"><span data-stu-id="93e28-129">Send times must be equal to or earlier than the presentation time because the payload must have time to get to the destination before the presentation time.</span></span>

    <span data-ttu-id="93e28-130">Il valore di questa proprietà è il primo tempo di invio.</span><span class="sxs-lookup"><span data-stu-id="93e28-130">This property value is the first send time.</span></span> <span data-ttu-id="93e28-131">Il multiplexer usa questo valore per calcolare i tempi di invio successivi per assicurarsi che i dati scorrano regolarmente nel bucket.</span><span class="sxs-lookup"><span data-stu-id="93e28-131">The multiplexer uses this value to calculate the subsequent send times to ensure that data flows through the bucket steadily.</span></span> <span data-ttu-id="93e28-132">Se sul multiplexer è stato impostato il flag di velocità in bit di regolazione automatica di **MFASF \_ multiplexer \_ \_** , il multiplexer modificherà la velocità in bit in modo che il payload venga inviato quando la finestra del buffer è quasi piena.</span><span class="sxs-lookup"><span data-stu-id="93e28-132">If the **MFASF\_MULTIPLEXER\_AUTOADJUST\_BITRATE** flag has been set on the multiplexer, the multiplexer will adjust the bit rate so that the payload is sent out when the buffer window is close to being full.</span></span> <span data-ttu-id="93e28-133">Se il flag non è impostato, il multiplexer non riesce a generare pacchetti di dati a causa del sovraccarico della larghezza di banda.</span><span class="sxs-lookup"><span data-stu-id="93e28-133">If the flag is not set, the multiplexer fails to generate data packets due to bandwidth overrun.</span></span>

<span data-ttu-id="93e28-134">Il multiplexer ottiene le informazioni di configurazione del flusso dal profilo ASF associato all'oggetto ContentInfo specificato nel metodo [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) .</span><span class="sxs-lookup"><span data-stu-id="93e28-134">The multiplexer obtains stream configuration information from the ASF profile associated with the ContentInfo object specified in the [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) method.</span></span> <span data-ttu-id="93e28-135">Le informazioni di configurazione del flusso includono parametri di bucket persi.</span><span class="sxs-lookup"><span data-stu-id="93e28-135">The stream configuration information includes leaky bucket parameters.</span></span> <span data-ttu-id="93e28-136">Questo valore è richiesto dal multiplexer per generare pacchetti di dati.</span><span class="sxs-lookup"><span data-stu-id="93e28-136">This value is required by the multiplexer to generate data packets.</span></span>

<span data-ttu-id="93e28-137">Per specificare i parametri del bucket di perdita, impostare i valori nell'attributo [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) nell'oggetto di configurazione del flusso che rappresenta il flusso nel profilo.</span><span class="sxs-lookup"><span data-stu-id="93e28-137">To specify the leaky bucket parameters, set the values in the [**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) attribute on the stream configuration object that represents the stream in the profile.</span></span> <span data-ttu-id="93e28-138">Per utilizzare il valore della finestra del buffer, utilizzato dal codificatore, chiamare [**IWMCodecLeakyBucket:: GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md).</span><span class="sxs-lookup"><span data-stu-id="93e28-138">To use the buffer window value, which is used by the encoder, call [**IWMCodecLeakyBucket::GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md).</span></span> <span data-ttu-id="93e28-139">Il valore effettivo della finestra del buffer è noto solo dopo l'impostazione del tipo di supporto di output del codificatore.</span><span class="sxs-lookup"><span data-stu-id="93e28-139">The actual buffer window value is known only after setting the output media type of the encoder.</span></span> <span data-ttu-id="93e28-140">Per informazioni sull'impostazione del tipo di supporto di output, vedere [Media Type Negotiation sul codificatore](media-type-negotiation-on-the-encoder.md).</span><span class="sxs-lookup"><span data-stu-id="93e28-140">For information about setting the output media type, see [Media Type Negotiation on the Encoder](media-type-negotiation-on-the-encoder.md).</span></span>

> [!Note]  
> <span data-ttu-id="93e28-141">I valori dei bucket con perdita di tempo utilizzati dal codificatore potrebbero essere diversi nell'oggetto ContentInfo fornito dal profilo ASF utilizzato per creare il multiplexer.</span><span class="sxs-lookup"><span data-stu-id="93e28-141">The leaky bucket values used by the encoder might be different in the ContentInfo object that was provided by the ASF Profile that was used to create the multiplexer.</span></span>

 

<span data-ttu-id="93e28-142">Il metodo [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) aggiorna l'oggetto ContentInfo in modo che i valori corretti vengano riflessi nell'oggetto intestazione ASF finale.</span><span class="sxs-lookup"><span data-stu-id="93e28-142">The [**Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) method updates the ContentInfo object so that the correct values are reflected in the final ASF Header Object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="93e28-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="93e28-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93e28-144">Multiplexer ASF</span><span class="sxs-lookup"><span data-stu-id="93e28-144">ASF Multiplexer</span></span>](asf-multiplexer.md)
</dt> <dt>

[<span data-ttu-id="93e28-145">Generazione di nuovi pacchetti di dati ASF</span><span class="sxs-lookup"><span data-stu-id="93e28-145">Generating New ASF Data Packets</span></span>](generating-new-asf-data-packets.md)
</dt> </dl>

 

 
