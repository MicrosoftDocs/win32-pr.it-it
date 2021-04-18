---
description: In questo argomento viene illustrato un codice di esempio che esegue il wrapping del codificatore Windows Media Audio (WMA) in una classe C++ denominata CWmaEncoder.
ms.assetid: 59bd5b6a-86fe-4d39-ab7c-9563ac1a8e94
title: Codice di esempio del codificatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfa38e779a7751c22f2c463999619e77e05ef09b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305390"
---
# <a name="encoder-example-code"></a>Codice di esempio del codificatore

In questo argomento viene illustrato un codice di esempio che esegue il wrapping del codificatore Windows Media Audio (WMA) in una classe C++ denominata `CWmaEncoder` .

-   [Dichiarazione di classe](#class-declaration)
-   [Inizializzare](#initialize)
-   [SetEncodingType](#setencodingtype)
-   [SetInputType](#setinputtype)
-   [GetOutputType](#getoutputtype)
-   [GetLeakyBucket1](#getleakybucket1)
-   [ProcessInput](#processinput)
-   [ProcessOutput](#processoutput)
-   [Scarico](#drain)
-   [Argomenti correlati](#related-topics)

Questo codice fa riferimento a diversi argomenti:

-   [Esercitazione: scrittura di un file WMA usando la codifica CBR](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)

In Media Foundation i codificatori vengono implementati come [trasformazioni di Media Foundation](media-foundation-transforms.md) (MFTS) ed espongono l'interfaccia [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) .

## <a name="class-declaration"></a>Dichiarazione di classe


```C++
enum EncodeMode
{
    EncodeMode_CBR,
    EncodeMode_VBR_Quality,
    EncodeMode_VBR_Peak,
    EncodeMode_VBR_Unconstrained,
};

struct LeakyBucket
{
    DWORD dwBitrate;
    DWORD msBufferSize;
    DWORD msInitialBufferFullness;
};

class CWmaEncoder 
{
public:

    CWmaEncoder() 
        : m_pMFT(NULL), m_dwInputID(0), m_dwOutputID(0), m_pOutputType(NULL)
    {
    }

    ~CWmaEncoder()
    {
        SafeRelease(&m_pMFT);
        SafeRelease(&m_pOutputType);
    }

    HRESULT Initialize();
    HRESULT SetEncodingType(EncodeMode mode);
    HRESULT SetInputType(IMFMediaType* pMediaType);
    HRESULT GetOutputType(IMFMediaType** ppMediaType);
    HRESULT GetLeakyBucket1(LeakyBucket *pBucket);
    HRESULT ProcessInput(IMFSample* pSample);
    HRESULT ProcessOutput(IMFSample **ppSample);
    HRESULT Drain();
       
protected:
    DWORD           m_dwInputID;     // Input stream ID.
    DWORD           m_dwOutputID;    // Output stream ID.

    IMFTransform    *m_pMFT;         // Pointer to the encoder MFT.
    IMFMediaType    *m_pOutputType;  // Output media type of the encoder.

};
```



## <a name="initialize"></a>Inizializzare

Il `Initialize` metodo crea un'istanza del codificatore wma.


```C++
HRESULT CWmaEncoder::Initialize() 
{
    CLSID *pCLSIDs = NULL;   // Pointer to an array of CLISDs. 
    UINT32 count = 0;      // Size of the array.

    IMFMediaType* pOutMediaType = NULL;
    
    // Look for a encoder.
    MFT_REGISTER_TYPE_INFO toutinfo;
    toutinfo.guidMajorType = MFMediaType_Audio;
    toutinfo.guidSubtype = MFAudioFormat_WMAudioV9;

    HRESULT hr = S_OK;

    hr = MFTEnum(
        MFT_CATEGORY_AUDIO_ENCODER,
        0,                  // Reserved
        NULL,               // Input type to match. 
        &toutinfo,          // Output type to match.
        NULL,               // Attributes to match. (None.)
        &pCLSIDs,           // Receives a pointer to an array of CLSIDs.
        &count              // Receives the size of the array.
        );
    
    if (SUCCEEDED(hr))
    {
        if (count == 0)
        {
            hr = MF_E_TOPO_CODEC_NOT_FOUND;
        }
    }

    //Create the MFT decoder
    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(pCLSIDs[0], NULL, 
            CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&m_pMFT));
    }

    return hr;
}
```



## <a name="setencodingtype"></a>SetEncodingType


```C++
HRESULT CWmaEncoder::SetEncodingType(EncodeMode mode)
{
    if (!m_pMFT)
    {
        return MF_E_NOT_INITIALIZED;
    }

    IPropertyStore* pProp = NULL;

    PROPVARIANT var;

    //Query the encoder for its property store

    HRESULT hr = m_pMFT->QueryInterface(IID_PPV_ARGS(&pProp));
    if (FAILED(hr))
    {
        goto done;
    }

    switch (mode)
    {
    case EncodeMode_CBR:
        //Set the VBR property to FALSE, which indicates CBR encoding
        //By default, encoding mode is set to CBR
        var.vt = VT_BOOL;
        var.boolVal = FALSE;
        hr = pProp->SetValue(MFPKEY_VBRENABLED, var);
        break;


    default:
        hr = E_NOTIMPL;
    }
    
done:
    SafeRelease(&pProp);
    return hr;
}
```



## <a name="setinputtype"></a>SetInputType


```C++
HRESULT CWmaEncoder::SetInputType(IMFMediaType* pMediaType)
{
    if (!m_pMFT)
    {
        return MF_E_NOT_INITIALIZED;
    }

    SafeRelease(&m_pOutputType);

    IMFMediaType *pOutputType = NULL;

    HRESULT hr = m_pMFT->GetStreamIDs(1, &m_dwInputID, 1, &m_dwOutputID);

    if (hr == E_NOTIMPL)
    {
        // The stream identifiers are zero-based.
        m_dwInputID = 0;
        m_dwOutputID = 0;
        hr = S_OK;
    }
    else if (FAILED(hr))
    {
        goto done;
    }

    // Set the input type to the one passed by the application
    hr = m_pMFT->SetInputType(m_dwInputID, pMediaType, 0);
    if (FAILED(hr))
    {
        goto done;
    }

    // Loop through the available output types
    for (DWORD iType = 0; ; iType++)
    {
        hr = m_pMFT->GetOutputAvailableType(m_dwOutputID, iType, &pOutputType);
        if (FAILED(hr))
        {
            goto done;
        }
        
        hr = m_pMFT->SetOutputType(m_dwOutputID, pOutputType, 0);

        if (SUCCEEDED(hr))
        {
            m_pOutputType = pOutputType;
            m_pOutputType->AddRef();
            break;
        }

        SafeRelease(&pOutputType);
    }

done:
    SafeRelease(&pOutputType);
    return hr;
}
```



## <a name="getoutputtype"></a>GetOutputType


```C++
HRESULT CWmaEncoder::GetOutputType(IMFMediaType** ppMediaType)
{
    if (m_pOutputType == NULL)
    {
        return MF_E_TRANSFORM_TYPE_NOT_SET;
    }
        
    *ppMediaType = m_pOutputType;
    (*ppMediaType)->AddRef();

    return S_OK;
};
```



## <a name="getleakybucket1"></a>GetLeakyBucket1


```C++
HRESULT CWmaEncoder::GetLeakyBucket1(LeakyBucket *pBucket)
{
    if (m_pMFT == NULL || m_pOutputType == NULL)
    {
        return MF_E_NOT_INITIALIZED;
    }

    ZeroMemory(pBucket, sizeof(*pBucket));

    // Get the bit rate.

    pBucket->dwBitrate = 8 * MFGetAttributeUINT32(
        m_pOutputType, MF_MT_AUDIO_AVG_BYTES_PER_SECOND, 0);


    // Get the buffer window.

    IWMCodecLeakyBucket *pLeakyBuckets = NULL;

    HRESULT hr = m_pMFT->QueryInterface(IID_PPV_ARGS(&pLeakyBuckets));
    if (SUCCEEDED(hr))
    {
        ULONG ulBuffer = 0;

        hr = pLeakyBuckets->GetBufferSizeBits(&ulBuffer);

        if (SUCCEEDED(hr))
        {
            pBucket->msBufferSize = ulBuffer / (pBucket->dwBitrate / 1000);    
        }

        pLeakyBuckets->Release();
    }

    return S_OK;
}
```



## <a name="processinput"></a>ProcessInput


```C++
HRESULT CWmaEncoder::ProcessInput(IMFSample* pSample)
{
    if (m_pMFT == NULL)
    {
        return MF_E_NOT_INITIALIZED;
    }

    return m_pMFT->ProcessInput(m_dwInputID, pSample, 0);
}
```



## <a name="processoutput"></a>ProcessOutput


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



## <a name="drain"></a>Scarico


```C++
HRESULT CWmaEncoder::Drain()
{
    if (m_pMFT == NULL)
    {
        return MF_E_NOT_INITIALIZED;
    }

    return m_pMFT->ProcessMessage(MFT_MESSAGE_COMMAND_DRAIN, m_dwInputID);
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esercitazione: scrittura di un file WMA usando la codifica CBR](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> <dt>

[Codec Windows Media](windows-media-codecs.md)
</dt> </dl>

 

 



