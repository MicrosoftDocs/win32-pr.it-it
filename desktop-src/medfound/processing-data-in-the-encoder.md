---
description: Elaborazione dei dati nel codificatore
ms.assetid: 7be4c5e7-db2c-4063-8e5c-af6ffb861aa5
title: Elaborazione dei dati nel codificatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99b7fedef50df61851408d084b511497eacd0288
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309032"
---
# <a name="processing-data-in-the-encoder"></a><span data-ttu-id="85570-103">Elaborazione dei dati nel codificatore</span><span class="sxs-lookup"><span data-stu-id="85570-103">Processing Data in the Encoder</span></span>

<span data-ttu-id="85570-104">Dopo aver negoziato il tipo di input e il tipo di output per il codificatore MFT, come descritto in [Media Type Negotiation sul codificatore](media-type-negotiation-on-the-encoder.md), è possibile avviare l'elaborazione degli esempi di dati multimediali.</span><span class="sxs-lookup"><span data-stu-id="85570-104">After you have negotiated the input type and output type for the encoder MFT, as described in [Media Type Negotiation on the Encoder](media-type-negotiation-on-the-encoder.md), you can start processing media data samples.</span></span> <span data-ttu-id="85570-105">I dati vengono passati sotto forma di esempi di supporto (interfaccia [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) ) e ricevuti anche dall'output come esempi di supporti.</span><span class="sxs-lookup"><span data-stu-id="85570-105">The data is passed in form of media samples ([**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface) and also received from the output as media samples.</span></span>

<span data-ttu-id="85570-106">Prima di inviare dati al codificatore per l'elaborazione, è necessario allocare un esempio di supporto e aggiungere uno o più buffer multimediali contenenti i dati multimediali che devono essere codificati.</span><span class="sxs-lookup"><span data-stu-id="85570-106">Before sending data to the encoder for processing, you must allocate a media sample and add one of more media buffers containing media data that needs to be encoded.</span></span> <span data-ttu-id="85570-107">Chiamare [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) e passare un puntatore all'esempio di supporto allocato.</span><span class="sxs-lookup"><span data-stu-id="85570-107">Call [**IMFTransform::ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) and pass a pointer to the allocated media sample.</span></span> <span data-ttu-id="85570-108">Oltre all'esempio multimediale, **ProcessInput** richiede anche l'identificatore del flusso di input.</span><span class="sxs-lookup"><span data-stu-id="85570-108">In addition to the media sample, **ProcessInput** also needs the input stream identifier.</span></span> <span data-ttu-id="85570-109">Per ottenere l'identificatore del flusso, chiamare [**IMFTransform:: GetStreamIDs**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamids).</span><span class="sxs-lookup"><span data-stu-id="85570-109">To get the stream identifier, call [**IMFTransform::GetStreamIDs**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamids).</span></span> <span data-ttu-id="85570-110">Poiché un codificatore è progettato per avere solo uno e un output, questi identificatori di flusso hanno sempre il valore 0.</span><span class="sxs-lookup"><span data-stu-id="85570-110">Because an encoder is designed to have only one and one output, these stream identifiers always have the value of 0.</span></span>

<span data-ttu-id="85570-111">Per ottenere dati dal codificatore, chiamare [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).</span><span class="sxs-lookup"><span data-stu-id="85570-111">To get data from the encoder, call [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).</span></span> <span data-ttu-id="85570-112">Prima di chiamare [**ProcessOutput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessoutput), è necessario verificare se il codificatore alloca gli esempi di supporti di output oppure è necessario eseguire questa operazione in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="85570-112">Before you call [**ProcessOutput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessoutput), you need to find out whether the encoder allocates the output media samples or you must do so explicitly.</span></span> <span data-ttu-id="85570-113">A tale scopo, chiamare [**IMFTransform:: GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo).</span><span class="sxs-lookup"><span data-stu-id="85570-113">To do this, call [**IMFTransform::GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo).</span></span> <span data-ttu-id="85570-114">Restituisce le informazioni di esempio sui supporti di output nella struttura di [**informazioni del flusso di output di MFT \_ \_ \_**](/windows/desktop/api/mftransform/ns-mftransform-mft_output_stream_info) .</span><span class="sxs-lookup"><span data-stu-id="85570-114">This returns output media sample information in the [**MFT\_OUTPUT\_STREAM\_INFO**](/windows/desktop/api/mftransform/ns-mftransform-mft_output_stream_info) structure.</span></span> <span data-ttu-id="85570-115">Se il codificatore alloca esempi di supporti, restituisce il \_ flag di output MFT che \_ fornisce il \_ \_ flag Samples nel membro **dwFlags** e il membro **cbSize** contiene zero.</span><span class="sxs-lookup"><span data-stu-id="85570-115">If the encoder allocates media samples, it returns the MFT\_OUTPUT\_STREAM\_PROVIDES\_SAMPLES flag in the **dwFlags** member and the **cbSize** member contains zero.</span></span> <span data-ttu-id="85570-116">Se il codificatore prevede di allocare il buffer di output, creare l'esempio di supporto di output e il buffer multimediale associato in base alle dimensioni restituite in **cbSize**.</span><span class="sxs-lookup"><span data-stu-id="85570-116">If the encoder expects you to allocate the output buffer, create the output media sample and the associated media buffer based on the size returned in **cbSize**.</span></span> <span data-ttu-id="85570-117">Quando si chiama [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample), passare un puntatore all'esempio di supporto appena creato.</span><span class="sxs-lookup"><span data-stu-id="85570-117">When you call [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample), pass a pointer to the newly created media sample.</span></span> <span data-ttu-id="85570-118">Durante la sessione di codifica, il codificatore riempie i buffer multimediali, a cui punta l'esempio del supporto di output, con i dati codificati.</span><span class="sxs-lookup"><span data-stu-id="85570-118">During the encoding session, the encoder fills the media buffers, pointed by the output media sample, with the encoded data.</span></span>

<span data-ttu-id="85570-119">Per avviare la sessione di codifica, passare l'esempio di supporto di input al codificatore chiamando [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).</span><span class="sxs-lookup"><span data-stu-id="85570-119">To start the encoding session, pass the input media sample to the encoder by calling [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).</span></span> <span data-ttu-id="85570-120">Il codificatore avvia l'elaborazione e i dati e produce uno o più esempi di supporti di output che devono essere recuperati da [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) , a condizione che restituisca la trasformazione MF e la necessità di un \_ \_ \_ \_ maggiore \_ input.</span><span class="sxs-lookup"><span data-stu-id="85570-120">The encoder starts processing and the data and produces one or more output media samples that must be retrieved by [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) as long as it returns MF\_E\_TRANSFORM\_NEED\_MORE\_INPUT.</span></span> <span data-ttu-id="85570-121">Se si chiama **ProcessInput** per passare più input finché sono presenti dati di output da recuperare, **ProcessInput** ha esito negativo con MF \_ E \_ NOTACCEPTING.</span><span class="sxs-lookup"><span data-stu-id="85570-121">If you call **ProcessInput** to pass more input as long as there is output data to be retrieved, **ProcessInput** fails with MF\_E\_NOTACCEPTING.</span></span> <span data-ttu-id="85570-122">Il codificatore non accetta più input finché il client non chiama **ProcessOutput** almeno una volta.</span><span class="sxs-lookup"><span data-stu-id="85570-122">The encoder does not accept any more input until the client calls **ProcessOutput** at least once.</span></span>

<span data-ttu-id="85570-123">È necessario impostare indicatori di tempo e durate accurati per tutti gli esempi di input passati.</span><span class="sxs-lookup"><span data-stu-id="85570-123">You should set accurate time stamps and durations for all input samples passed.</span></span> <span data-ttu-id="85570-124">I timestamp non sono strettamente necessari, ma consentono di mantenere la sincronizzazione audio/video.</span><span class="sxs-lookup"><span data-stu-id="85570-124">Time stamps are not strictly required but help maintain audio/video synchronization.</span></span> <span data-ttu-id="85570-125">Se non si dispone dei timestamp per gli esempi, è preferibile lasciarli invariati rispetto all'utilizzo di valori incerti.</span><span class="sxs-lookup"><span data-stu-id="85570-125">If you do not have the time stamps for your samples it is better to leave them out than to use uncertain values.</span></span>

## <a name="encoder-processing-example"></a><span data-ttu-id="85570-126">Esempio di elaborazione del codificatore</span><span class="sxs-lookup"><span data-stu-id="85570-126">Encoder Processing Example</span></span>

<span data-ttu-id="85570-127">Il codice di esempio seguente mostra come chiamare [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) per ottenere un esempio codificato.</span><span class="sxs-lookup"><span data-stu-id="85570-127">The following example code shows how to call [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) to get an encoded sample.</span></span> <span data-ttu-id="85570-128">Per il contesto completo di questo esempio, vedere [codice di esempio del codificatore](encoder-example-code.md).</span><span class="sxs-lookup"><span data-stu-id="85570-128">For the complete context of this example, see [Encoder Example Code](encoder-example-code.md).</span></span>


```C++
HRESULT CWmaEncoder::ProcessOutput(IMFSample **ppSample)
{
    if (m_pMFT == NULL)
    {
        return MF_E_NOT_INITIALIZED;
    }

    *ppSample = NULL;

    IMFMediaBuffer* pBufferOut = NULL;
    IMFSample* pSampleOut = NULL;

    DWORD dwStatus;
  
    MFT_OUTPUT_STREAM_INFO mftStreamInfo = { 0 };
    MFT_OUTPUT_DATA_BUFFER mftOutputData = { 0 };

    HRESULT hr = m_pMFT->GetOutputStreamInfo(m_dwOutputID, &mftStreamInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    //create a buffer for the output sample
    hr = MFCreateMemoryBuffer(mftStreamInfo.cbSize, &pBufferOut);
    if (FAILED(hr))
    {
        goto done;
    }

    //Create the output sample
    hr = MFCreateSample(&pSampleOut);
    if (FAILED(hr))
    {
        goto done;
    }

    //Add the output buffer 
    hr = pSampleOut->AddBuffer(pBufferOut);
    if (FAILED(hr))
    {
        goto done;
    }
 
    //Set the output sample
    mftOutputData.pSample = pSampleOut;

    //Set the output id
    mftOutputData.dwStreamID = m_dwOutputID;

    //Generate the output sample
    hr = m_pMFT->ProcessOutput(0, 1, &mftOutputData, &dwStatus);
    if (hr == MF_E_TRANSFORM_NEED_MORE_INPUT)
    {
        hr = S_OK;
        goto done;
    }

    // TODO: Handle MF_E_TRANSFORM_STREAM_CHANGE

    if (FAILED(hr))
    {
        goto done;
    }

    *ppSample = pSampleOut;
    (*ppSample)->AddRef();

done:
    SafeRelease(&pBufferOut);
    SafeRelease(&pSampleOut);
    return hr;
};
```



## <a name="related-topics"></a><span data-ttu-id="85570-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="85570-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85570-130">Multiplexer ASF</span><span class="sxs-lookup"><span data-stu-id="85570-130">ASF Multiplexer</span></span>](asf-multiplexer.md)
</dt> <dt>

[<span data-ttu-id="85570-131">Creazione di un'istanza di un codificatore MFT</span><span class="sxs-lookup"><span data-stu-id="85570-131">Instantiating an Encoder MFT</span></span>](instantiating-the-encoder-mft.md)
</dt> <dt>

[<span data-ttu-id="85570-132">Codificatori Windows Media</span><span class="sxs-lookup"><span data-stu-id="85570-132">Windows Media Encoders</span></span>](windows-media-encoders.md)
</dt> </dl>

 

 



