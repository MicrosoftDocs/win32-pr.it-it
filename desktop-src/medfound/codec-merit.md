---
description: Meriti codec
ms.assetid: 4ed594a0-2cc2-40d2-9b5c-dee59916fa1b
title: Meriti codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ecd177c3c32084a030ce75c15cecd5d4c04fc3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104567828"
---
# <a name="codec-merit"></a><span data-ttu-id="01a06-103">Meriti codec</span><span class="sxs-lookup"><span data-stu-id="01a06-103">Codec Merit</span></span>

<span data-ttu-id="01a06-104">A partire da Windows 7, è possibile assegnare un valore *Merit* a un codec Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="01a06-104">Starting in Windows 7, a Media Foundation codec can be assigned a *merit* value.</span></span> <span data-ttu-id="01a06-105">Quando vengono enumerati i codec, i codec con maggiore merito sono preferiti rispetto ai codec con un valore più basso.</span><span class="sxs-lookup"><span data-stu-id="01a06-105">When codecs are enumerated, codecs with higher merit are preferred over codecs with lower merit.</span></span> <span data-ttu-id="01a06-106">I codec con qualsiasi valore di merito sono preferiti rispetto ai codec senza un merito assegnato.</span><span class="sxs-lookup"><span data-stu-id="01a06-106">Codecs with any merit value are preferred over codecs without an assigned merit.</span></span> <span data-ttu-id="01a06-107">Per informazioni dettagliate sull'enumerazione dei codec, vedere [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span><span class="sxs-lookup"><span data-stu-id="01a06-107">For details about codec enumeration, see [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span></span>

<span data-ttu-id="01a06-108">I valori di Merit sono assegnati da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="01a06-108">Merit values are assigned by Microsoft.</span></span> <span data-ttu-id="01a06-109">Attualmente, solo i codec hardware sono idonei a ricevere un valore di merito.</span><span class="sxs-lookup"><span data-stu-id="01a06-109">Currently, only hardware codecs are eligible to receive a merit value.</span></span> <span data-ttu-id="01a06-110">Al fornitore di codec viene anche emesso un certificato digitale, che viene usato per verificare il valore di Merit del codec.</span><span class="sxs-lookup"><span data-stu-id="01a06-110">The codec vendor is also issued a digital certificate, which is used to verify the codec's merit value.</span></span> <span data-ttu-id="01a06-111">Per ottenere un certificato, inviare una richiesta di posta elettronica a wmla@microsoft.com .</span><span class="sxs-lookup"><span data-stu-id="01a06-111">To obtain a certificate, send an email request to wmla@microsoft.com.</span></span> <span data-ttu-id="01a06-112">Il processo per ottenere un certificato include la firma di una licenza e la fornitura di un set di file di informazioni a Microsoft.</span><span class="sxs-lookup"><span data-stu-id="01a06-112">The process for obtaining a certificate includes signing a license and providing a set of information files to Microsoft.</span></span>

<span data-ttu-id="01a06-113">Il merito del codec funziona nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="01a06-113">Codec merit works as follows:</span></span>

1.  <span data-ttu-id="01a06-114">Il fornitore del codec implementa uno dei seguenti elementi:</span><span class="sxs-lookup"><span data-stu-id="01a06-114">The codec vendor implements one of the following:</span></span>
    -   <span data-ttu-id="01a06-115">Un mini driver AVStream.</span><span class="sxs-lookup"><span data-stu-id="01a06-115">An AVStream mini-driver.</span></span> <span data-ttu-id="01a06-116">Media Foundation fornisce un proxy standard MFT per i driver AVStream.</span><span class="sxs-lookup"><span data-stu-id="01a06-116">Media Foundation provides an standard proxy MFT for AVStream drivers.</span></span> <span data-ttu-id="01a06-117">È consigliabile selezionare questa opzione.</span><span class="sxs-lookup"><span data-stu-id="01a06-117">This is the recommended option.</span></span>
    -   <span data-ttu-id="01a06-118">Una trasformazione Media Foundation (MFT) che funge da proxy per l'hardware.</span><span class="sxs-lookup"><span data-stu-id="01a06-118">A Media Foundation transform (MFT) that acts as a proxy to the hardware.</span></span> <span data-ttu-id="01a06-119">Per ulteriori informazioni, vedere [hardware MFTS](hardware-mfts.md).</span><span class="sxs-lookup"><span data-stu-id="01a06-119">For more information, see [Hardware MFTs](hardware-mfts.md).</span></span>
2.  <span data-ttu-id="01a06-120">Il valore Merit del codec viene archiviato nel registro di sistema per la ricerca rapida.</span><span class="sxs-lookup"><span data-stu-id="01a06-120">The codec's merit value is stored in the registry for quick lookup.</span></span>
3.  <span data-ttu-id="01a06-121">La funzione [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) Ordina i codec in ordine di merito.</span><span class="sxs-lookup"><span data-stu-id="01a06-121">The [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function sorts codecs in order of merit.</span></span> <span data-ttu-id="01a06-122">I codec con valori di Merit vengono visualizzati nell'elenco dietro i codec registrati localmente (vedere [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal)), ma prima di altri codec.</span><span class="sxs-lookup"><span data-stu-id="01a06-122">Codecs with merit values appear in the list behind locally registered codecs (see [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal)), but ahead of other codecs.</span></span>
4.  <span data-ttu-id="01a06-123">Quando viene creata la MFT, il merito del codec viene verificato tramite l'API di [Output Protection Manager](output-protection-manager.md) (OPM).</span><span class="sxs-lookup"><span data-stu-id="01a06-123">When the MFT is created, the codec's merit is verified using the [Output Protection Manager](output-protection-manager.md) (OPM) API.</span></span>
5.  <span data-ttu-id="01a06-124">Per un proxy MFT, il codec implementa l'interfaccia [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) .</span><span class="sxs-lookup"><span data-stu-id="01a06-124">For a proxy MFT, the codec implements the [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) interface.</span></span> <span data-ttu-id="01a06-125">Per un driver AVStream, il codec implementa il \_ set di proprietà KSPROPSETID OPMVideoOutput.</span><span class="sxs-lookup"><span data-stu-id="01a06-125">For an AVStream driver, the codec implements the KSPROPSETID\_OPMVideoOutput property set.</span></span>

<span data-ttu-id="01a06-126">Il diagramma seguente mostra in che modo Merit viene verificato in entrambi i casi:</span><span class="sxs-lookup"><span data-stu-id="01a06-126">The following diagram shows how merit is verified in both cases:</span></span>

![diagramma che mostra due processi: uno conduce attraverso i driver di Media Foundation Proxy MFT e AVstream, l'altro tramite il proxy personalizzato MFT](images/codecmerit.png)

## <a name="custom-proxy-mft"></a><span data-ttu-id="01a06-128">MFT proxy personalizzato</span><span class="sxs-lookup"><span data-stu-id="01a06-128">Custom Proxy MFT</span></span>

<span data-ttu-id="01a06-129">Se si fornisce un proxy MFT per il codec hardware, implementare il codec Merit value come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="01a06-129">If you provide a proxy MFT for the hardware codec, implement the codec merit value as follows:</span></span>

1.  <span data-ttu-id="01a06-130">Implementare l'interfaccia [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) in MFT.</span><span class="sxs-lookup"><span data-stu-id="01a06-130">Implement the [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) interface in the MFT.</span></span> <span data-ttu-id="01a06-131">Il codice di esempio è illustrato nella sezione successiva di questo argomento.</span><span class="sxs-lookup"><span data-stu-id="01a06-131">Example code is shown in the next section of this topic.</span></span>
2.  <span data-ttu-id="01a06-132">Aggiungere l'attributo [MFT \_ codec \_ Merit \_ attribute](mft-codec-merit-attribute.md) al registro di sistema, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="01a06-132">Add the [MFT\_CODEC\_MERIT\_Attribute](mft-codec-merit-attribute.md) attribute to the registry, as follows:</span></span>

    1.  <span data-ttu-id="01a06-133">Chiamare [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) per creare un nuovo archivio di attributi.</span><span class="sxs-lookup"><span data-stu-id="01a06-133">Call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create a new attribute store.</span></span>
    2.  <span data-ttu-id="01a06-134">Chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) SetAttribute per impostare l'attributo [dell' \_ \_ \_ attributo Merit codec MFT](mft-codec-merit-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="01a06-134">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) to set the [MFT\_CODEC\_MERIT\_Attribute](mft-codec-merit-attribute.md) attribute.</span></span> <span data-ttu-id="01a06-135">Il valore dell'attributo è il merito assegnato del codec.</span><span class="sxs-lookup"><span data-stu-id="01a06-135">The value of the attribute is the codec's assigned merit.</span></span>
    3.  <span data-ttu-id="01a06-136">Chiamare [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister) per registrare il MFT.</span><span class="sxs-lookup"><span data-stu-id="01a06-136">Call [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister) to register the MFT.</span></span> <span data-ttu-id="01a06-137">Passare l'archivio di attributi nel parametro *pAttributes* .</span><span class="sxs-lookup"><span data-stu-id="01a06-137">Pass the attribute store in the *pAttributes* parameter.</span></span>

3.  <span data-ttu-id="01a06-138">L'applicazione chiama [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span><span class="sxs-lookup"><span data-stu-id="01a06-138">The application calls [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span></span> <span data-ttu-id="01a06-139">Questa funzione restituisce una matrice di puntatori [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , uno per ogni codec che corrisponde ai criteri di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="01a06-139">This function returns an array of [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers, one for each codec that matches the enumeration criteria.</span></span>
4.  <span data-ttu-id="01a06-140">L'applicazione chiama [**IMFActivate:: ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) per creare il MFT.</span><span class="sxs-lookup"><span data-stu-id="01a06-140">The application calls [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) to create the MFT.</span></span>
5.  <span data-ttu-id="01a06-141">Il metodo [**ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) chiama la funzione [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) per verificare il certificato e il valore Merit.</span><span class="sxs-lookup"><span data-stu-id="01a06-141">The [**ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) method calls the [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) function to verify the certificate and the merit value.</span></span>
6.  <span data-ttu-id="01a06-142">La funzione [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) chiama [**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) e invia una richiesta di stato per [**\_ ottenere \_ \_ informazioni sul codec di OPM**](opm-get-codec-info.md) .</span><span class="sxs-lookup"><span data-stu-id="01a06-142">The [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) function calls [**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) and sends an [**OPM\_GET\_CODEC\_INFO**](opm-get-codec-info.md) status request.</span></span> <span data-ttu-id="01a06-143">Questa richiesta di stato restituisce il valore di Merit assegnato del codec.</span><span class="sxs-lookup"><span data-stu-id="01a06-143">This status request returns the codec's assigned merit value.</span></span> <span data-ttu-id="01a06-144">Se questo valore non corrisponde al valore del registro di sistema, [**ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) potrebbe non riuscire.</span><span class="sxs-lookup"><span data-stu-id="01a06-144">If this value does not match the registry value, [**ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) may fail.</span></span>

<span data-ttu-id="01a06-145">Il codice seguente illustra come aggiungere il valore Merit al registro di sistema quando si registra la tabella MFT:</span><span class="sxs-lookup"><span data-stu-id="01a06-145">The following code shows how to add the merit value to the registry when you register the MFT:</span></span>


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



### <a name="implementing-iopmvideooutput-for-codec-merit"></a><span data-ttu-id="01a06-146">Implementazione di IOPMVideoOutput per il merito del codec</span><span class="sxs-lookup"><span data-stu-id="01a06-146">Implementing IOPMVideoOutput for Codec Merit</span></span>

<span data-ttu-id="01a06-147">Il codice seguente illustra come implementare [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) per il merito del codec.</span><span class="sxs-lookup"><span data-stu-id="01a06-147">The following code shows how to implement [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) for codec merit.</span></span> <span data-ttu-id="01a06-148">Per informazioni più generali sull'API OPM, vedere [Output Protection Manager](output-protection-manager.md).</span><span class="sxs-lookup"><span data-stu-id="01a06-148">For a more general discussion of the OPM API, see [Output Protection Manager](output-protection-manager.md).</span></span>

> [!Note]  
> <span data-ttu-id="01a06-149">Il codice riportato di seguito non include offuscamenti o altri meccanismi di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="01a06-149">The code shown here has no obfuscation or other security mechanisms.</span></span> <span data-ttu-id="01a06-150">Ha lo scopo di mostrare l'implementazione di base della richiesta di handshake e dello stato di OPM.</span><span class="sxs-lookup"><span data-stu-id="01a06-150">It is meant to show the basic implementation of the OPM handshake and status request.</span></span>

 

<span data-ttu-id="01a06-151">Questo esempio si basa sul presupposto che *g \_ testCert* sia una matrice di byte che contiene la catena di certificati del codec e *g \_ PrivateKey* è una matrice di byte che contiene la chiave privata del certificato:</span><span class="sxs-lookup"><span data-stu-id="01a06-151">This example assumes that *g\_TestCert* is a byte array that contains the codec's certificate chain, and *g\_PrivateKey* is a byte array that contains the private key from the certificate:</span></span>


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



<span data-ttu-id="01a06-152">Nel metodo [**IOPMVideoOutput:: StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) generare un numero casuale per l'handshake.</span><span class="sxs-lookup"><span data-stu-id="01a06-152">In the [**IOPMVideoOutput::StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) method, generate a random number for the handshake.</span></span> <span data-ttu-id="01a06-153">Restituire questo numero e il certificato al chiamante:</span><span class="sxs-lookup"><span data-stu-id="01a06-153">Return this number and the certificate to the caller:</span></span>


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



<span data-ttu-id="01a06-154">Il metodo [**IOPMVideoOutput:: FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) completa l'handshake di OPM:</span><span class="sxs-lookup"><span data-stu-id="01a06-154">The [**IOPMVideoOutput::FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) method completes the OPM handshake:</span></span>


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



<span data-ttu-id="01a06-155">Nel metodo [**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) implementare la richiesta di stato per [**\_ ottenere \_ \_ informazioni sul codec di OPM**](opm-get-codec-info.md) .</span><span class="sxs-lookup"><span data-stu-id="01a06-155">In the [**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) method, implement the [**OPM\_GET\_CODEC\_INFO**](opm-get-codec-info.md) status request.</span></span> <span data-ttu-id="01a06-156">I dati di input sono una struttura del [**\_ parametro OPM Get \_ codec \_ info \_**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters) che contiene il CLSID della MFT.</span><span class="sxs-lookup"><span data-stu-id="01a06-156">The input data is an [**OPM\_GET\_CODEC\_INFO\_PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters) structure that contains the CLSID of your MFT.</span></span> <span data-ttu-id="01a06-157">I dati di output sono una struttura di [**\_ informazioni sul codec per ottenere \_ \_ \_ informazioni sul codec**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information) che contiene il merito del codec.</span><span class="sxs-lookup"><span data-stu-id="01a06-157">The output data is an [**OPM\_GET\_CODEC\_INFO\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information) structure that contains the codec merit.</span></span>


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



<span data-ttu-id="01a06-158">Il metodo [**GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) deve calcolare un Message Authentication Code (Mac) usando l'algoritmo OMAC-1; vedere [calcolo del valore OMAC-1](opm-example-code.md).</span><span class="sxs-lookup"><span data-stu-id="01a06-158">The [**GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) method must compute a Message Authentication Code (MAC) using the OMAC-1 algorithm; see [Computing the OMAC-1 Value](opm-example-code.md).</span></span>

<span data-ttu-id="01a06-159">Non è necessario supportare altre richieste di stato di OPM.</span><span class="sxs-lookup"><span data-stu-id="01a06-159">It is not necessary to support any other OPM status requests.</span></span>

<span data-ttu-id="01a06-160">I metodi [**IOPMVideoOutput:: COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation) e [**IOPMVideoOutput:: Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) non sono necessari per il merito del codec, quindi questi metodi possono restituire **E \_ NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="01a06-160">The [**IOPMVideoOutput::COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation) and [**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) methods are not required for codec merit, so these methods can return **E\_NOTIMPL**.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="01a06-161">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="01a06-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="01a06-162">Trasformazioni Media Foundation</span><span class="sxs-lookup"><span data-stu-id="01a06-162">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> <dt>

[<span data-ttu-id="01a06-163">Scrittura di un MFT personalizzato</span><span class="sxs-lookup"><span data-stu-id="01a06-163">Writing a Custom MFT</span></span>](writing-a-custom-mft.md)
</dt> </dl>

 

 



