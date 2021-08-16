---
description: Codec Merit
ms.assetid: 4ed594a0-2cc2-40d2-9b5c-dee59916fa1b
title: Codec Merit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b56112942aa8378b2016616d0e090e17eb7225ca27b363c96e37eb7cccb6286e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118065125"
---
# <a name="codec-merit"></a>Codec Merit

A partire da Windows 7, a un codec Media Foundation può essere assegnato un valore di insoddrà valore.  Quando i codec vengono enumerati, i codec con maggiore pregio sono preferiti rispetto ai codec con più basso livello di priorità. I codec con qualsiasi valore di pregio sono preferiti rispetto ai codec senza un valore assegnato. Per informazioni dettagliate sull'enumerazione dei codec, vedere [**MFTEnumEx.**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)

I valori di inevaso vengono assegnati da Microsoft. Attualmente, solo i codec hardware sono idonei a ricevere un valore di insidità. Il fornitore del codec emesso anche un certificato digitale, che viene usato per verificare il valore di pregio del codec. Per ottenere un certificato, inviare una richiesta di posta elettronica a wmla@microsoft.com . Il processo per ottenere un certificato include la firma di una licenza e la fornitura di un set di file di informazioni a Microsoft.

Il codec funziona come segue:

1.  Il fornitore del codec implementa uno degli elementi seguenti:
    -   Mini driver AVStream. Media Foundation fornisce un MFT proxy standard per i driver AVStream. È consigliabile selezionare questa opzione.
    -   Una Media Foundation (MFT) che funge da proxy per l'hardware. Per altre informazioni, vedere [Hardware MFTs](hardware-mfts.md).
2.  Il valore di pregio del codec viene archiviato nel Registro di sistema per la ricerca rapida.
3.  La [**funzione MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) ordina i codec in ordine di merito. I codec con valori di merito vengono visualizzati nell'elenco dietro i codec registrati in locale (vedere [**MFTRegisterLocal),**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal)ma prima degli altri codec.
4.  Quando viene creato il MFT, il merito del codec viene verificato tramite l'API [OPM (Output Protection Manager).](output-protection-manager.md)
5.  Per un proxy MFT, il codec implementa [**l'interfaccia IOPMVideoOutput.**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) Per un driver AVStream, il codec implementa il set di proprietà KSPROPSETID \_ OPMVideoOutput.

Il diagramma seguente illustra come viene verificato il merito in entrambi i casi:

![diagramma che mostra due processi: uno passa attraverso media foundation proxy mft e il driver avstream, l'altro tramite il proxy personalizzato mft](images/codecmerit.png)

## <a name="custom-proxy-mft"></a>MFT del proxy personalizzato

Se si fornisce un proxy MFT per il codec hardware, implementare il valore di codec codec come indicato di seguito:

1.  Implementare [**l'interfaccia IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) in MFT. Il codice di esempio è illustrato nella sezione successiva di questo argomento.
2.  Aggiungere [l'attributo \_ MFT CODEC \_ REGISTRY \_ ](mft-codec-merit-attribute.md) al Registro di sistema, come indicato di seguito:

    1.  Chiamare [**MFCreateAttributes per**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) creare un nuovo archivio attributi.
    2.  Chiamare [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) per impostare [l'attributo MFT CODEC CODEC \_ \_ \_ Attribute.](mft-codec-merit-attribute.md) Il valore dell'attributo è il valore assegnato del codec.
    3.  Chiamare [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister) per registrare MFT. Passare l'archivio di attributi nel *parametro pAttributes.*

3.  L'applicazione [**chiama MFTEnumEx.**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) Questa funzione restituisce una matrice di [**puntatori IMFActivate,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) uno per ogni codec che corrisponde ai criteri di enumerazione.
4.  L'applicazione [**chiama IMFActivate::ActivateObject per**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) creare il MFT.
5.  Il [**metodo ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) chiama la [**funzione MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) per verificare il certificato e il valore di insiddisfazione.
6.  La [**funzione MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) chiama [**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) e invia una richiesta di stato [**OPM GET CODEC \_ \_ \_ INFO.**](opm-get-codec-info.md) Questa richiesta di stato restituisce il valore di merito assegnato del codec. Se questo valore non corrisponde al valore del Registro di sistema, [**ActivateObject potrebbe**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) non riuscire.

Il codice seguente illustra come aggiungere il valore di insidro al Registro di sistema quando si registra MFT:


```C++
// Shows how to register an MFT with a merit value.

HRESULT RegisterMFTWithMerit()
{
    // The following media types would apply to an H.264 decoder, 
    // and are used here as an example.

    MFT_REGISTER_TYPE_INFO aDecoderInputTypes[] = 
    {
        { MFMediaType_Video, MFVideoFormat_H264 },
    };

    MFT_REGISTER_TYPE_INFO aDecoderOutputTypes[] = 
    {
        { MFMediaType_Video, MFVideoFormat_RGB32 }
    };
    
    // Create an attribute store to hold the merit attribute.
    HRESULT hr = S_OK;
    IMFAttributes *pAttributes = NULL;

    hr = MFCreateAttributes(&pAttributes, 1);

    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(
            MFT_CODEC_MERIT_Attribute, 
            DECODER_MERIT   // Use the codec's assigned merit value.
            );
    }

    // Register the decoder for MFTEnum(Ex).
    if (SUCCEEDED(hr))
    {
        hr = MFTRegister(
            CLSID_MPEG1SampleDecoder,                   // CLSID
            MFT_CATEGORY_VIDEO_DECODER,                 // Category
            const_cast<LPWSTR>(SZ_DECODER_NAME),        // Friendly name
            0,                                          // Flags
            ARRAYSIZE(aDecoderInputTypes),              // Number of input types
            aDecoderInputTypes,                         // Input types
            ARRAYSIZE(aDecoderOutputTypes),             // Number of output types
            aDecoderOutputTypes,                        // Output types
            pAttributes                                 // Attributes 
            );
    }

    SafeRelease(&pAttributes);
    return hr;
}
```



### <a name="implementing-iopmvideooutput-for-codec-merit"></a>Implementazione di IOPMVideoOutput per Codec Codec Codec

Il codice seguente illustra come implementare [**IOPMVideoOutput per**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) il codec. Per una descrizione più generale dell'API OPM, vedere [Output Protection Manager.](output-protection-manager.md)

> [!Note]  
> Il codice illustrato di seguito non presenta offuscamento o altri meccanismi di sicurezza. Lo scopo è mostrare l'implementazione di base dell'handshake OPM e della richiesta di stato.

 

Questo esempio presuppone che *g \_ TestCert* sia una matrice di byte che contiene la catena di certificati del codec e *g \_ PrivateKey* sia una matrice di byte che contiene la chiave privata del certificato:


```C++
// Byte array that contains the codec's certificate.

const BYTE g_TestCert[] =
{
    // ... (certificate not shown)
```




```C++
// Byte array that contains the private key from the certificate.

const BYTE g_PrivateKey[] = 
{
    // .... (key not shown)
```



Nel metodo [**IOPMVideoOutput::StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) generare un numero casuale per l'handshake. Restituire questo numero e il certificato al chiamante:


```C++
STDMETHODIMP CodecMerit::StartInitialization(
    OPM_RANDOM_NUMBER *prnRandomNumber,
    BYTE **ppbCertificate,
    ULONG *pulCertificateLength
    )
{
    HRESULT hr = S_OK;

    DWORD cbCertificate = sizeof(g_TestCert);
    const BYTE *pCertificate = g_TestCert;

    // Generate the random number for the OPM handshake.
    hr = BCryptGenRandom(
        NULL,  
        (PUCHAR)&m_RandomNumber, 
        sizeof(m_RandomNumber),
        BCRYPT_USE_SYSTEM_PREFERRED_RNG
        );

    // Allocate the buffer to copy the certificate.
    if (SUCCEEDED(hr))
    {
        *ppbCertificate = (PBYTE)CoTaskMemAlloc(cbCertificate);

        if (*ppbCertificate == NULL) 
        {
            hr = E_OUTOFMEMORY;
        }
    }

    // Copy the certificate and the random number.
    if (SUCCEEDED(hr))
    {
        *pulCertificateLength = cbCertificate;
        CopyMemory(*ppbCertificate, pCertificate, cbCertificate);
        *prnRandomNumber = m_RandomNumber;
    }
    return hr;
}
```



Il [**metodo IOPMVideoOutput::FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) completa l'handshake OPM:


```C++
STDMETHODIMP CodecMerit::FinishInitialization(
    const OPM_ENCRYPTED_INITIALIZATION_PARAMETERS *pParameters
    )
{
    HRESULT hr = S_OK;
    BCRYPT_ALG_HANDLE hAlg = NULL;
    BCRYPT_KEY_HANDLE hKey = NULL;
    BCRYPT_OAEP_PADDING_INFO paddingInfo = {0};
    DWORD DecryptedLength = 0;
    PBYTE pbDecryptedParams = NULL;

    // The caller should pass the following structure in
    // pParameters:

    typedef struct {
        GUID  guidCOPPRandom;   // Our random number.
        GUID  guidKDI;          // AES signing key.
        DWORD StatusSeqStart;   // Status sequence number.
        DWORD CommandSeqStart;  // Command sequence number.
    } InitParams;

    paddingInfo.pszAlgId = BCRYPT_SHA512_ALGORITHM;

    //  Decrypt the input using the decoder's private key.

    hr = BCryptOpenAlgorithmProvider(
        &hAlg,
        BCRYPT_RSA_ALGORITHM,
        MS_PRIMITIVE_PROVIDER,
        0
        );

    //  Import the private key.
    if (SUCCEEDED(hr))
    {
        hr = BCryptImportKeyPair(
            hAlg,
            NULL,
            BCRYPT_RSAPRIVATE_BLOB,
            &hKey,
            (PUCHAR)g_PrivateKey, //pbData,
            sizeof(g_PrivateKey), //cbData,
            0
            );
    }

    //  Decrypt the input data.

    if (SUCCEEDED(hr))
    {
        hr = BCryptDecrypt(
            hKey,
            (PBYTE)pParameters,
            OPM_ENCRYPTED_INITIALIZATION_PARAMETERS_SIZE,
            &paddingInfo,
            NULL,
            0,
            NULL,
            0,
            &DecryptedLength,
            BCRYPT_PAD_OAEP
            );
    }

    if (SUCCEEDED(hr))
    {
        pbDecryptedParams = new (std::nothrow) BYTE[DecryptedLength];

        if (pbDecryptedParams == NULL) 
        {
            hr = E_OUTOFMEMORY;
        }
    }

    if (SUCCEEDED(hr))
    {
         hr = BCryptDecrypt(
             hKey,
             (PBYTE)pParameters,
             OPM_ENCRYPTED_INITIALIZATION_PARAMETERS_SIZE,
             &paddingInfo,
             NULL,
             0,
             pbDecryptedParams,
             DecryptedLength,
             &DecryptedLength,
             BCRYPT_PAD_OAEP
             );
    }

    if (SUCCEEDED(hr))
    {
        InitParams *Params = (InitParams *)pbDecryptedParams;
        
        //  Check the random number.
        if (0 != memcmp(&m_RandomNumber, &Params->guidCOPPRandom, sizeof(m_RandomNumber)))
        {
            hr = E_ACCESSDENIED;
        } 
        else 
        {
            //  Save the key and the sequence numbers.

            CopyMemory(m_AESKey.abRandomNumber, &Params->guidKDI, sizeof(m_AESKey));
            m_StatusSequenceNumber = Params->StatusSeqStart;
            m_CommandSequenceNumber = Params->CommandSeqStart;
        }
    }

    //  Clean up.

    if (hKey)
    {
        BCryptDestroyKey(hKey);
    }
    if (hAlg)
    {
        BCryptCloseAlgorithmProvider(hAlg, 0);
    }
    delete [] pbDecryptedParams;

    return hr;
}
```



Nel metodo [**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) implementare la richiesta di stato [**OPM \_ GET CODEC \_ \_ INFO.**](opm-get-codec-info.md) I dati di input sono una [**struttura OPM \_ GET CODEC \_ INFO \_ \_ PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters) che contiene il CLSID del MFT. I dati di output sono una [**struttura OPM \_ GET CODEC \_ INFO \_ \_ INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information) che contiene il codec codec.


```C++
STDMETHODIMP CodecMerit::GetInformation( 
    const OPM_GET_INFO_PARAMETERS *Parameters,
    OPM_REQUESTED_INFORMATION *pRequest
    )
{

    HRESULT hr = S_OK;
    OPM_GET_CODEC_INFO_PARAMETERS *CodecInfoParameters;

    //  Check the MAC.
    OPM_OMAC Tag = { 0 };

    hr = ComputeOMAC(
        m_AESKey, 
        (PBYTE)Parameters + OPM_OMAC_SIZE, 
        sizeof(OPM_GET_INFO_PARAMETERS) - OPM_OMAC_SIZE, 
        &Tag
        );

    if (SUCCEEDED(hr))
    {
        if (0 != memcmp(Tag.abOMAC, &Parameters->omac, OPM_OMAC_SIZE))
        {
            hr = E_ACCESSDENIED;
        }
    }

    // Validate the status sequence number. This must be consecutive
    // from the previous sequence number.

    if (SUCCEEDED(hr))
    {
        if (Parameters->ulSequenceNumber != m_StatusSequenceNumber++)
        {
            hr = E_ACCESSDENIED;
        }
    }

    //  Check the status request.

    if (SUCCEEDED(hr))
    {
        if (Parameters->guidInformation != OPM_GET_CODEC_INFO) 
        {
            hr = E_NOTIMPL;
        }
    }

    //  Check parameters.

    if (SUCCEEDED(hr))
    {
        CodecInfoParameters = (OPM_GET_CODEC_INFO_PARAMETERS *)Parameters->abParameters;

        if (Parameters->cbParametersSize > OPM_GET_INFORMATION_PARAMETERS_SIZE ||
            Parameters->cbParametersSize < sizeof(ULONG) ||
            Parameters->cbParametersSize - sizeof(ULONG) != CodecInfoParameters->cbVerifier
            ) 
        {
            hr = E_INVALIDARG;
        }
    }

    //  The input data should consist of the CLSID of the decoder.

    if (SUCCEEDED(hr))
    {
        CodecInfoParameters = (OPM_GET_CODEC_INFO_PARAMETERS *)Parameters->abParameters;
    
        if (CodecInfoParameters->cbVerifier != sizeof(CLSID) ||
            0 != memcmp(&CLSID_MPEG1SampleDecoder,
                        CodecInfoParameters->Verifier,
                        CodecInfoParameters->cbVerifier)) 
        {
            hr = E_ACCESSDENIED;
        }
    }

    if (SUCCEEDED(hr))
    {
        // Now return the decoder merit to the caller.

        ZeroMemory(pRequest, sizeof(OPM_REQUESTED_INFORMATION));

        OPM_GET_CODEC_INFO_INFORMATION *pInfo = 
            (OPM_GET_CODEC_INFO_INFORMATION *)pRequest->abRequestedInformation;

        pInfo->Merit = DECODER_MERIT;
        pInfo->rnRandomNumber = Parameters->rnRandomNumber;

        pRequest->cbRequestedInformationSize = sizeof(OPM_GET_CODEC_INFO_INFORMATION);

        //  Sign it with the key.

        hr = ComputeOMAC(
            m_AESKey, 
            (PBYTE)pRequest + OPM_OMAC_SIZE, 
            sizeof(OPM_REQUESTED_INFORMATION) - OPM_OMAC_SIZE, 
            &pRequest->omac
            );
    }

    return hr;
}
```



Il [**metodo GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) deve calcolare un Message Authentication Code (MAC) usando l'algoritmo OMAC-1. Vedere [Calcolo del valore OMAC-1.](opm-example-code.md)

Non è necessario supportare altre richieste di stato OPM.

I metodi [**IOPMVideoOutput::COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation) e [**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) non sono necessari per il codec, quindi questi metodi possono restituire **E \_ NOTIMPL.**


```C++
STDMETHODIMP CodecMerit::COPPCompatibleGetInformation( 
    const OPM_COPP_COMPATIBLE_GET_INFO_PARAMETERS *pParameters,
    OPM_REQUESTED_INFORMATION *pRequestedInformation)
{
    return E_NOTIMPL;
}

STDMETHODIMP CodecMerit::Configure( 
    const OPM_CONFIGURE_PARAMETERS *pParameters,
    ULONG ulAdditionalParametersSize,
    const BYTE *pbAdditionalParameters)
{
    return E_NOTIMPL;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Media Foundation trasformazioni](media-foundation-transforms.md)
</dt> <dt>

[Scrittura di un MFT personalizzato](writing-a-custom-mft.md)
</dt> </dl>

 

 



