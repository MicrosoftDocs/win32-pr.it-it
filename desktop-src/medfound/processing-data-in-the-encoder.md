---
description: Elaborazione dei dati nel codificatore
ms.assetid: 7be4c5e7-db2c-4063-8e5c-af6ffb861aa5
title: Elaborazione dei dati nel codificatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 666c2a2ff2139aadcb489022eb9b324eff1de523551244c2fd12ad0e11f68f1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118238732"
---
# <a name="processing-data-in-the-encoder"></a>Elaborazione dei dati nel codificatore

Dopo aver negoziato il tipo di input e il tipo di output per il codificatore MFT, come descritto in [Negoziazione](media-type-negotiation-on-the-encoder.md)del tipo di supporto nel codificatore , è possibile iniziare a elaborare esempi di dati multimediali. I dati vengono passati sotto forma di esempi multimediali [**(interfaccia IMFSample)**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) e ricevuti anche dall'output come esempi di supporti.

Prima di inviare dati al codificatore per l'elaborazione, è necessario allocare un campione di supporti e aggiungere uno o più buffer multimediali contenenti dati multimediali che devono essere codificati. Chiamare [**IMFTransform::P rocessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) e passare un puntatore all'esempio di supporto allocato. Oltre all'esempio multimediale, **ProcessInput** richiede anche l'identificatore del flusso di input. Per ottenere l'identificatore del flusso, chiamare [**IMFTransform::GetStreamIDs**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamids). Poiché un codificatore è progettato per avere un solo output e un output, questi identificatori di flusso hanno sempre il valore 0.

Per ottenere dati dal codificatore, chiamare [**IMFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput). Prima di chiamare [**ProcessOutput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessoutput), è necessario determinare se il codificatore alloca i campioni di supporti di output oppure è necessario eseguire questa operazione in modo esplicito. A tale scopo, chiamare [**IMFTransform::GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo). Vengono restituite informazioni di esempio sui supporti di output nella [**struttura MFT \_ OUTPUT STREAM \_ \_ INFO.**](/windows/desktop/api/mftransform/ns-mftransform-mft_output_stream_info) Se il codificatore alloca campioni multimediali, restituisce il flag MFT OUTPUT STREAM PROVIDES SAMPLES nel membro \_ \_ \_ \_ **dwFlags** e il membro **cbSize** contiene zero. Se il codificatore prevede di allocare il buffer di output, creare il campione di supporti di output e il buffer multimediale associato in base alle dimensioni restituite in **cbSize**. Quando si chiama [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample), passare un puntatore all'esempio multimediale appena creato. Durante la sessione di codifica, il codificatore riempie i buffer multimediali, a cui punta il campione di supporti di output, con i dati codificati.

Per avviare la sessione di codifica, passare l'esempio di supporto di input al codificatore chiamando [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput). Il codificatore avvia l'elaborazione e i dati e produce uno o più campioni di supporti di output che devono essere recuperati da [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) purché restituisca MF \_ E TRANSFORM NEED MORE \_ \_ \_ \_ INPUT. Se si chiama **ProcessInput per** passare più input, purché siano presenti dati di output da recuperare, **ProcessInput** ha esito negativo con MF \_ E \_ NOTACCEPTING. Il codificatore non accetta più input finché il client non chiama **ProcessOutput** almeno una volta.

È necessario impostare timestamp e durate accurate per tutti i campioni di input passati. I timestamp non sono strettamente necessari, ma consentono di mantenere la sincronizzazione audio/video. Se non si dispone dei timestamp per i campioni, è meglio lasciarli fuori che usare valori incerti.

## <a name="encoder-processing-example"></a>Esempio di elaborazione del codificatore

Il codice di esempio seguente illustra come chiamare [**IMFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) per ottenere un esempio codificato. Per il contesto completo di questo esempio, vedere [Codice di esempio del codificatore](encoder-example-code.md).


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



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[ASF Multiplexer](asf-multiplexer.md)
</dt> <dt>

[Creazione di un'istanza di un codificatore MFT](instantiating-the-encoder-mft.md)
</dt> <dt>

[Windows Codificatori multimediali](windows-media-encoders.md)
</dt> </dl>

 

 



