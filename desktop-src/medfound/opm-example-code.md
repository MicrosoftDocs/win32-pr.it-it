---
description: Questo argomento contiene codice di esempio per l'utilizzo di output Protection Manager.
ms.assetid: ad2303a0-f3f3-43a0-83eb-023640da2ece
title: Codice di esempio di OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9883643829815d27725c392e2c4f13f34e816988
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309066"
---
# <a name="opm-example-code"></a><span data-ttu-id="6d6ad-103">Codice di esempio di OPM</span><span class="sxs-lookup"><span data-stu-id="6d6ad-103">OPM Example Code</span></span>

<span data-ttu-id="6d6ad-104">Questo argomento contiene codice di esempio per l'utilizzo di [Output Protection Manager](output-protection-manager.md).</span><span class="sxs-lookup"><span data-stu-id="6d6ad-104">This topic contains example code for using [Output Protection Manager](output-protection-manager.md).</span></span>

<span data-ttu-id="6d6ad-105">Il codice di esempio in questo argomento illustra come eseguire l'handshake di OPM, inviare una richiesta di stato e inviare un comando OPM.</span><span class="sxs-lookup"><span data-stu-id="6d6ad-105">The example code in this topic demonstrates how to perform the OPM handshake, send a status request, and send an OPM command.</span></span> <span data-ttu-id="6d6ad-106">Per le operazioni di crittografia, il codice USA Cryptography API: Next Generation (CNG).</span><span class="sxs-lookup"><span data-stu-id="6d6ad-106">For cryptographic operations, the code uses Cryptography API: Next Generation (CNG).</span></span> <span data-ttu-id="6d6ad-107">L'obiettivo di questo argomento è mostrare le funzionalità di OPM, quindi le attività correlate al certificato X. 509, ad esempio l'analisi e la convalida del certificato, non vengono visualizzate.</span><span class="sxs-lookup"><span data-stu-id="6d6ad-107">The focus of this topic is to show OPM functionality, so tasks related to the X.509 certificate, such as parsing and validating the certificate, are not shown.</span></span>

<span data-ttu-id="6d6ad-108">Le procedure illustrate in questo argomento sono illustrate in modo più dettagliato in [utilizzo di output Protection Manager](using-output-protection-manager.md).</span><span class="sxs-lookup"><span data-stu-id="6d6ad-108">The procedures shown in this topic are explained in more detail in [Using Output Protection Manager](using-output-protection-manager.md).</span></span>

-   [<span data-ttu-id="6d6ad-109">Esecuzione dell'handshake di OPM</span><span class="sxs-lookup"><span data-stu-id="6d6ad-109">Performing the OPM Handshake</span></span>](#performing-the-opm-handshake)
-   [<span data-ttu-id="6d6ad-110">Invio di una richiesta di stato di OPM</span><span class="sxs-lookup"><span data-stu-id="6d6ad-110">Sending an OPM Status Request</span></span>](#sending-an-opm-status-request)
-   [<span data-ttu-id="6d6ad-111">Invio di un comando OPM</span><span class="sxs-lookup"><span data-stu-id="6d6ad-111">Sending an OPM Command</span></span>](#sending-an-opm-command)
-   [<span data-ttu-id="6d6ad-112">Calcolo del valore OMAC-1</span><span class="sxs-lookup"><span data-stu-id="6d6ad-112">Computing the OMAC-1 Value</span></span>](#computing-the-omac-1-value)
-   [<span data-ttu-id="6d6ad-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6d6ad-113">Related topics</span></span>](#related-topics)

## <a name="performing-the-opm-handshake"></a><span data-ttu-id="6d6ad-114">Esecuzione dell'handshake di OPM</span><span class="sxs-lookup"><span data-stu-id="6d6ad-114">Performing the OPM Handshake</span></span>

1.  <span data-ttu-id="6d6ad-115">Dopo aver enumerato i dispositivi OPM e selezionato un output video (non mostrato), il primo passaggio consiste nel chiamare [**IOPMVideoOutput:: StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) per ottenere la catena di certificati X. 509 del dispositivo:</span><span class="sxs-lookup"><span data-stu-id="6d6ad-115">After enumerating the OPM devices and selecting a video output (not shown), the first step is to call [**IOPMVideoOutput::StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) to get the device's X.509 certificate chain:</span></span>

    ```C++
        OPM_RANDOM_NUMBER random;   // Random number from driver.
        ZeroMemory(&random, sizeof(random));

        BYTE *pbCertificate = NULL; // Pointer to a buffer to hold the certificate.
        ULONG cbCertificate = 0;    // Size of the certificate in bytes.

        PUBLIC_KEY_VALUES *pKey = NULL; // The driver's public key.

        // Get the driver's certificate chain + random number
        hr = pVideoOutput->StartInitialization(
            &random, 
            &pbCertificate, 
            &cbCertificate
            );

        if (FAILED(hr))
        {
            goto done;
        }

        // Validate the X.509 certificate. (Not shown.)
        hr = ValidateX509Certificate(pbCertificate, cbCertificate);

        if (FAILED(hr))
        {
            goto done;
        }

        // Get the public key from the certificate. (Not shown.)
        hr = GetPublicKeyFromCertificate(
            pbCertificate,
            cbCertificate,
            &pKey
            );

        if (FAILED(hr))
        {
            goto done;
        }

        // Load and initialize a CNG provider (Cryptography API: Next Generation)

        BCRYPT_ALG_HANDLE hAlg = 0;

        hr = BCryptOpenAlgorithmProvider(
            &hAlg, 
            BCRYPT_RSA_ALGORITHM, 
            MS_PRIMITIVE_PROVIDER, 
            0
            );

        if (FAILED(hr))
        {
            goto done;
        }

        // Import the public key into the CNG provider.

        BCRYPT_KEY_HANDLE hPublicKey = 0;

        // Import the RSA public key.
        hr = ImportRsaPublicKey(hAlg, pKey, &hPublicKey);

        if (FAILED(hr))
        {
            goto done;
        }
    
    ```

    

2.  <span data-ttu-id="6d6ad-116">L'applicazione deve convalidare la catena di certificati e ottenere la chiave pubblica dal certificato foglia nella catena.</span><span class="sxs-lookup"><span data-stu-id="6d6ad-116">The application must validate the certificate chain and get the public key from the leaf certificate in the chain.</span></span> <span data-ttu-id="6d6ad-117">Questi passaggi non vengono visualizzati qui.</span><span class="sxs-lookup"><span data-stu-id="6d6ad-117">Those steps are not shown here.</span></span>
3.  <span data-ttu-id="6d6ad-118">Quando si dispone della chiave pubblica, è possibile importare la chiave in un provider di algoritmi CNG.</span><span class="sxs-lookup"><span data-stu-id="6d6ad-118">Once you have the public key, you can import the key into a CNG algorithm provider.</span></span> <span data-ttu-id="6d6ad-119">Chiamare la funzione **BCryptOpenAlgorithmProvider** per caricare il provider.</span><span class="sxs-lookup"><span data-stu-id="6d6ad-119">Call the **BCryptOpenAlgorithmProvider** function to load the provider.</span></span> <span data-ttu-id="6d6ad-120">La funzione definita dall'applicazione `ImportRsaPublicKey` Importa la chiave e restituisce un handle alla chiave importata:</span><span class="sxs-lookup"><span data-stu-id="6d6ad-120">The application-defined `ImportRsaPublicKey` function imports the key and returns a handle to the imported key:</span></span>
    ```C++
    void ReverseMemCopy(BYTE *pbDest, BYTE const *pbSource, DWORD cb)
    {
        for (DWORD i = 0; i < cb; i++) 
        {
            pbDest[cb - 1 - i] = pbSource[i];
        }
    }
    ```

    

    ```C++
    //------------------------------------------------------------------------
    //
    // ImportRsaPublicKey
    //
    // Converts an RSA public key from an RSAPUBKEY blob into an 
    // BCRYPT_RSAKEY_BLOB and sets the public key on the CNG provider.
    //
    //------------------------------------------------------------------------

    HRESULT ImportRsaPublicKey(
        BCRYPT_ALG_HANDLE hAlg,     // CNG provider
        PUBLIC_KEY_VALUES *pKey,    // Pointer to the RSAPUBKEY blob.
        BCRYPT_KEY_HANDLE *phKey    // Receives a handle the imported public key.
        )
    {
        HRESULT hr = S_OK;

        BYTE *pbPublicKey = NULL;
        DWORD cbKey = 0;

        // Layout of the RSA public key blob:

        //  +----------------------------------------------------------------+
        //  |     BCRYPT_RSAKEY_BLOB    | BE( dwExp ) |   BE( Modulus )      |
        //  +----------------------------------------------------------------+
        //
        //  sizeof(BCRYPT_RSAKEY_BLOB)       cbExp           cbModulus 
        //  <--------------------------><------------><---------------------->
        //
        //   BE = Big Endian Format                                                     

        DWORD cbModulus = (pKey->rsapubkey.bitlen + 7) / 8;
        DWORD dwExp = pKey->rsapubkey.pubexp;
        DWORD cbExp = (dwExp & 0xFF000000) ? 4 :
                      (dwExp & 0x00FF0000) ? 3 :
                      (dwExp & 0x0000FF00) ? 2 : 1;

        BCRYPT_RSAKEY_BLOB *pRsaBlob;
        PBYTE pbCurrent;

        hr = DWordAdd(cbModulus, sizeof(BCRYPT_RSAKEY_BLOB), &cbKey);

        if (FAILED(hr))
        {
            goto done;
        }

        cbKey += cbExp;

        pbPublicKey = (BYTE*)CoTaskMemAlloc(cbKey);
        if (NULL == pbPublicKey) 
        {
            hr = E_OUTOFMEMORY;
            goto done;
        }    
        
        ZeroMemory(pbPublicKey, cbKey);
        pRsaBlob = (BCRYPT_RSAKEY_BLOB *)(pbPublicKey);
        
        // Make the Public Key Blob Header
        pRsaBlob->Magic = BCRYPT_RSAPUBLIC_MAGIC;
        pRsaBlob->BitLength = pKey->rsapubkey.bitlen;
        pRsaBlob->cbPublicExp = cbExp;
        pRsaBlob->cbModulus = cbModulus;
        pRsaBlob->cbPrime1 = 0;
        pRsaBlob->cbPrime2 = 0;

        pbCurrent = (PBYTE)(pRsaBlob + 1);
        
        // Copy pubExp Big Endian 
        ReverseMemCopy(pbCurrent, (PBYTE)&dwExp, cbExp);
        pbCurrent += cbExp;

        // Copy Modulus Big Endian 
        ReverseMemCopy(pbCurrent, pKey->modulus, cbModulus);

        // Set the key.
        hr = BCryptImportKeyPair(
            hAlg, 
            NULL, 
            BCRYPT_RSAPUBLIC_BLOB, 
            phKey,
            (PUCHAR)pbPublicKey,
            cbKey,
            0
            );

    done:
        CoTaskMemFree(pbPublicKey);
        return hr;
    }
    ```

    

4.  <span data-ttu-id="6d6ad-121">Preparare quindi il buffer che contiene i numeri di sequenza iniziali e la chiave della sessione AES.</span><span class="sxs-lookup"><span data-stu-id="6d6ad-121">Next, prepare the buffer that contains the starting sequence numbers and the AES session key.</span></span>
    ```C++
    void CopyAndAdvancePtr(BYTE*& pDest, const BYTE* pSrc, DWORD cb)
    {
        memcpy(pDest, pSrc, cb);
        pDest += cb;
    }
    ```

    

    ```C++
        //--------------------------------------------------------------------
        // Prepare the signature for key exchnage.
        //--------------------------------------------------------------------

        UINT uStatusSeq = 0;     // Status sequence number.
        UINT uCommandSeq = 0;    // Command sequence number.

        OPM_RANDOM_NUMBER AesKey;   // Session key

        // Generate the starting sequence number for queries.
        hr = BCryptGenRandom(
            NULL, 
            (BYTE*)&uStatusSeq, 
            sizeof(UINT), 
            BCRYPT_USE_SYSTEM_PREFERRED_RNG
            );

        if (FAILED(hr))
        {
            goto done;
        }


        // Generate the starting sequence number for commands.
        hr = BCryptGenRandom(
            NULL, 
            (BYTE*)&uCommandSeq, 
            sizeof(UINT), 
            BCRYPT_USE_SYSTEM_PREFERRED_RNG
            );

        if (FAILED(hr))
        {
            goto done;
        }

        // Generate the AES session key.
        hr = BCryptGenRandom(
            NULL, 
            (BYTE*)&AesKey, 
            sizeof(AesKey), 
            BCRYPT_USE_SYSTEM_PREFERRED_RNG
            );

        if (FAILED(hr))
        {
            goto done;
        }

        // Fill in the initialization structure.
        OPM_ENCRYPTED_INITIALIZATION_PARAMETERS initParams;
        ZeroMemory(&initParams, sizeof(initParams));
        
        // Use a temporary pointer for copying into the array.
        BYTE *pBuffer = &initParams.abEncryptedInitializationParameters[0];

        CopyAndAdvancePtr(pBuffer, random.abRandomNumber, sizeof(random)); // Random number from the friver.
        CopyAndAdvancePtr(pBuffer, AesKey.abRandomNumber, sizeof(AesKey)); // Session key.
        CopyAndAdvancePtr(pBuffer, (BYTE*)&uStatusSeq, sizeof(uStatusSeq));
        CopyAndAdvancePtr(pBuffer, (BYTE*)&uCommandSeq, sizeof(uCommandSeq));
    ```

    

5.  <span data-ttu-id="6d6ad-122">Crittografare questo buffer con la crittografia RSAES-OAEP, utilizzando la chiave pubblica del driver.</span><span class="sxs-lookup"><span data-stu-id="6d6ad-122">Encrypt this buffer with RSAES-OAEP encryption, using the driver's public key.</span></span>
    ```C++
        //--------------------------------------------------------------------
        // RSAES-OAEP encrypt the signature. Use SHA2 hashing algorithm.
        //--------------------------------------------------------------------

        PBYTE pbDataIn = &initParams.abEncryptedInitializationParameters[0];
        ULONG cbDataIn = (ULONG)(pBuffer - pbDataIn);  

        DWORD cbOutput = 0;
        DWORD cbDataOut= 0;

        BYTE *pbDataOut = NULL;

        BCRYPT_OAEP_PADDING_INFO paddingInfo;
        ZeroMemory(&paddingInfo, sizeof(paddingInfo));

        paddingInfo.pszAlgId = BCRYPT_SHA512_ALGORITHM;

        //Encrypt the signature.
        hr = BCryptEncrypt(
            hPublicKey,
            (PUCHAR)pbDataIn,
            cbDataIn,
            &paddingInfo,
            NULL,
            0,
            NULL,
            0,
            &cbOutput,
            BCRYPT_PAD_OAEP
            );

        if (FAILED(hr))
        {
            goto done;
        }


        pbDataOut = new (std::nothrow) BYTE[cbOutput];
        if (NULL == pbDataOut) 
        {
            hr = E_OUTOFMEMORY;
            goto done;
        }
        
        hr = BCryptEncrypt(
            hPublicKey,
            (PUCHAR)pbDataIn,
            cbDataIn,
            &paddingInfo,
            NULL,
            0,
            pbDataOut,
            cbOutput,
            &cbDataOut,
            BCRYPT_PAD_OAEP
            );

        if (FAILED(hr))
        {
            goto done;
        }
    ```

    

6.  <span data-ttu-id="6d6ad-123">Chiamare [**IOPMVideoOutput:: FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) per completare l'handshake.</span><span class="sxs-lookup"><span data-stu-id="6d6ad-123">Call [**IOPMVideoOutput::FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) to complete the handshake.</span></span>
    ```C++
        // Complete the handshake.
        hr = pVideoOutput->FinishInitialization(
            (OPM_ENCRYPTED_INITIALIZATION_PARAMETERS *)pbDataOut
            );

        if (FAILED(hr))
        {
            goto done;
        }
    ```

    

## <a name="sending-an-opm-status-request"></a><span data-ttu-id="6d6ad-124">Invio di una richiesta di stato di OPM</span><span class="sxs-lookup"><span data-stu-id="6d6ad-124">Sending an OPM Status Request</span></span>

<span data-ttu-id="6d6ad-125">Nell'esempio seguente viene illustrato come inviare la richiesta di stato del [**\_ tipo di \_ connettore \_ OPM Get**](opm-get-connector-type.md) .</span><span class="sxs-lookup"><span data-stu-id="6d6ad-125">The next example shows how to send the [**OPM\_GET\_CONNECTOR\_TYPE**](opm-get-connector-type.md) status request.</span></span>

1.  <span data-ttu-id="6d6ad-126">Compilare una struttura [**del \_ \_ \_ parametro OPM Get Info**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) con le informazioni per la richiesta di stato.</span><span class="sxs-lookup"><span data-stu-id="6d6ad-126">Fill in an [**OPM\_GET\_INFO\_PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) structure with the information for the status request.</span></span>
    ```C++
        //--------------------------------------------------------------------
        // Prepare the status request structure.
        //--------------------------------------------------------------------

        OPM_GET_INFO_PARAMETERS     StatusInput;
        OPM_REQUESTED_INFORMATION   StatusOutput;

        ZeroMemory(&StatusInput, sizeof(StatusInput));
        ZeroMemory(&StatusOutput, sizeof(StatusOutput));

        hr = BCryptGenRandom(
            NULL, 
            (BYTE*)&(StatusInput.rnRandomNumber), 
            OPM_128_BIT_RANDOM_NUMBER_SIZE, 
            BCRYPT_USE_SYSTEM_PREFERRED_RNG
            );

        if (FAILED(hr))
        {
            goto done;
        }

        StatusInput.guidInformation = OPM_GET_CONNECTOR_TYPE; // Request GUID.
        StatusInput.ulSequenceNumber = uStatusSeq;            // Sequence number.

        //  Sign the request structure, not including the omac field.

        hr = ComputeOMAC(
            AesKey,                                             // Session key.
            (BYTE*)&StatusInput + OPM_OMAC_SIZE,                // Data
            sizeof(OPM_GET_INFO_PARAMETERS) - OPM_OMAC_SIZE,    // Size
            &StatusInput.omac                                   // Receives the OMAC
            );

        if (FAILED(hr))
        {
            goto done;
        }
    
    ```

    

2.  <span data-ttu-id="6d6ad-127">Il membro **OMAC** della struttura [**OPM \_ get \_ info \_ Parameters**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) è un valore Mac CBC (OMAC) a una chiave calcolato per il resto della struttura.</span><span class="sxs-lookup"><span data-stu-id="6d6ad-127">The **omac** member of the [**OPM\_GET\_INFO\_PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) structure is a one-key CBC MAC (OMAC) computed for the rest of the structure.</span></span> <span data-ttu-id="6d6ad-128">La funzione ComputeOMAC (illustrata più avanti) viene dichiarata come segue:</span><span class="sxs-lookup"><span data-stu-id="6d6ad-128">The ComputeOMAC function (shown later) is declared as follows:</span></span>
    ```C++
    HRESULT ComputeOMAC(
        OPM_RANDOM_NUMBER&  AesKey,     // Session key
        PUCHAR pb,                      // Data
        DWORD cb,                       // Size
        OPM_OMAC *pTag                  // Receives the OMAC
        );
    ```

    

3.  <span data-ttu-id="6d6ad-129">Chiamare [**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) per inviare la richiesta di stato.</span><span class="sxs-lookup"><span data-stu-id="6d6ad-129">Call [**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) to send the status request.</span></span>
    ```C++
        //  Send the status request.
        hr = pVideoOutput->GetInformation(&StatusInput, &StatusOutput);

        if (FAILED(hr))
        {
            goto done;
        }
    
    ```

    

4.  <span data-ttu-id="6d6ad-130">Il driver scrive la risposta nella struttura [**di \_ \_ informazioni richiesta da OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) .</span><span class="sxs-lookup"><span data-stu-id="6d6ad-130">The driver writes the response to the [**OPM\_REQUESTED\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) structure.</span></span> <span data-ttu-id="6d6ad-131">La struttura della risposta include un valore OMAC, calcolato per il resto della struttura.</span><span class="sxs-lookup"><span data-stu-id="6d6ad-131">The response structure includes an OMAC value, computed for the remainder of the structure.</span></span> <span data-ttu-id="6d6ad-132">Verificare questo valore prima di considerare attendibile i dati di risposta:</span><span class="sxs-lookup"><span data-stu-id="6d6ad-132">Verify this value before trusting the response data:</span></span>
    ```C++
        //--------------------------------------------------------------------
        // Verify the signature.
        //--------------------------------------------------------------------

        OPM_OMAC rgbSignature = { 0 };

        // Calculate our own signature.

        hr = ComputeOMAC(
            AesKey,
            (BYTE*)&StatusOutput + OPM_OMAC_SIZE, 
            sizeof(OPM_REQUESTED_INFORMATION) - OPM_OMAC_SIZE, 
            &rgbSignature
            );

        if (FAILED(hr))
        {
            goto done;
        }

        if (memcmp(StatusOutput.omac.abOMAC, rgbSignature.abOMAC, OPM_OMAC_SIZE))
        {
            // The signature does not match.
            hr = E_FAIL; 
            goto done;
        }

        // Update the sequence number.
        uStatusSeq++;
    ```

    

5.  <span data-ttu-id="6d6ad-133">Il membro **abRequestedInformation** della struttura [**di \_ \_ informazioni richiesta da OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) contiene i dati di risposta.</span><span class="sxs-lookup"><span data-stu-id="6d6ad-133">The **abRequestedInformation** member of the [**OPM\_REQUESTED\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) structure contains the response data.</span></span> <span data-ttu-id="6d6ad-134">Per la richiesta di [**\_ tipo di \_ connettore \_ OPM Get**](opm-get-connector-type.md) , i dati di risposta sono costituiti da una struttura di [**\_ \_ informazioni standard OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) .</span><span class="sxs-lookup"><span data-stu-id="6d6ad-134">For the [**OPM\_GET\_CONNECTOR\_TYPE**](opm-get-connector-type.md) request, the response data consists of a [**OPM\_STANDARD\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information) structure.</span></span>
    ```C++
        // Examine the response. 
        // The response data is an OPM_STANDARD_INFORMATION structure.

        OPM_STANDARD_INFORMATION StatusInfo;
        ZeroMemory(&StatusInfo, sizeof(StatusInfo));

        ULONG cbLen = min(sizeof(OPM_STANDARD_INFORMATION), StatusOutput.cbRequestedInformationSize);    

        if (cbLen != 0)
        {
            // Copy the repinse into the array.
            CopyMemory((BYTE*)&StatusInfo, StatusOutput.abRequestedInformation, cbLen);
        }
        
        //  Verify the random number.
        if (0!= memcmp(
            (BYTE*)&StatusInfo.rnRandomNumber, 
            (BYTE*)&StatusInput.rnRandomNumber, 
            sizeof(OPM_RANDOM_NUMBER)) 
            ) 
        {
            hr = E_FAIL;
            goto done;
        }    

        // Verify the status of the OPM session.
        if (StatusInfo.ulStatusFlags != OPM_STATUS_NORMAL)
        {
            // Abnormal status
            hr = E_FAIL;
            goto done;
        }    
        
        ULONG ConnectorType = StatusInfo.ulInformation & OPM_BUS_TYPE_MASK;
    ```

    

## <a name="sending-an-opm-command"></a><span data-ttu-id="6d6ad-135">Invio di un comando OPM</span><span class="sxs-lookup"><span data-stu-id="6d6ad-135">Sending an OPM Command</span></span>

<span data-ttu-id="6d6ad-136">Nell'esempio seguente viene illustrato come abilitare High-Bandwidth Digital protezione del contenuto (HDCP) inviando il comando [**OPM \_ set \_ Protection \_ Level**](opm-set-protection-level.md) .</span><span class="sxs-lookup"><span data-stu-id="6d6ad-136">The next example shows how to enable High-Bandwidth Digital Content Protection (HDCP) by sending the [**OPM\_SET\_PROTECTION\_LEVEL**](opm-set-protection-level.md) command.</span></span>

1.  <span data-ttu-id="6d6ad-137">Tutti i comandi di OPM usano la struttura di [**\_ configurazione dei \_ parametri di OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) per i dati di input.</span><span class="sxs-lookup"><span data-stu-id="6d6ad-137">All OPM commands use the [**OPM\_CONFIGURE\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) structure for input data.</span></span> <span data-ttu-id="6d6ad-138">La matrice **abParameters** in questa struttura contiene dati specifici del comando.</span><span class="sxs-lookup"><span data-stu-id="6d6ad-138">The **abParameters** array in this structure contains command-specific data.</span></span> <span data-ttu-id="6d6ad-139">Per il comando di [**\_ impostazione del \_ \_ livello di protezione di OPM**](opm-set-protection-level.md) , la matrice **abParameters** contiene una struttura di parametri del [**\_ \_ \_ livello \_ di protezione set di OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters) .</span><span class="sxs-lookup"><span data-stu-id="6d6ad-139">For the [**OPM\_SET\_PROTECTION\_LEVEL**](opm-set-protection-level.md) command, the **abParameters** array contains an [**OPM\_SET\_PROTECTION\_LEVEL\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters) structure.</span></span> <span data-ttu-id="6d6ad-140">Compilare la struttura come segue:</span><span class="sxs-lookup"><span data-stu-id="6d6ad-140">Fill in this structure as follows:</span></span>
    ```C++
        //--------------------------------------------------------------------
        // Prepare the command structure.
        //--------------------------------------------------------------------

        // Data specific to the OPM_SET_PROTECTION_LEVEL command.
        OPM_SET_PROTECTION_LEVEL_PARAMETERS CommandInput;

        ZeroMemory(&CommandInput, sizeof(CommandInput));

        CommandInput.ulProtectionType = OPM_PROTECTION_TYPE_HDCP;   
        CommandInput.ulProtectionLevel = OPM_HDCP_ON;        

        ULONG ulAdditionalParametersSize = 0;
        BYTE* pbAdditionalParameters = NULL;
    ```

    

2.  <span data-ttu-id="6d6ad-141">Successivamente, compilare la struttura [**dei \_ \_ parametri di configurazione di OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) e calcolare il OMAC.</span><span class="sxs-lookup"><span data-stu-id="6d6ad-141">Next, fill in the [**OPM\_CONFIGURE\_PARAMETERS**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters) structure and compute the OMAC.</span></span>
    ```C++
        // Common command parameters
        OPM_CONFIGURE_PARAMETERS Command;
        ZeroMemory(&Command, sizeof(Command));

        Command.guidSetting = OPM_SET_PROTECTION_LEVEL;
        Command.ulSequenceNumber = uCommandSeq;
        Command.cbParametersSize = sizeof(OPM_SET_PROTECTION_LEVEL_PARAMETERS);
        CopyMemory(&Command.abParameters[0], (BYTE*)&CommandInput, Command.cbParametersSize);

        //  Sign the command structure, not including the omac field.
        hr = ComputeOMAC(
            AesKey,
            (BYTE*)&Command + OPM_OMAC_SIZE, 
            sizeof(OPM_CONFIGURE_PARAMETERS) - OPM_OMAC_SIZE,
            &Command.omac
            );

        if (FAILED(hr))
        {
            goto done;
        }
    
    ```

    

3.  <span data-ttu-id="6d6ad-142">Per inviare il comando, chiamare [**IOPMVideoOutput:: Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure).</span><span class="sxs-lookup"><span data-stu-id="6d6ad-142">To send the command, call [**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure).</span></span> <span data-ttu-id="6d6ad-143">Ricordarsi di incrementare il numero di sequenza del comando dopo ogni comando.</span><span class="sxs-lookup"><span data-stu-id="6d6ad-143">Remember to increment the command sequence number after each command.</span></span>
    ```C++
        //  Send the command.
        hr = pVideoOutput->Configure(
            &Command, 
            0,      // Size of additional command data.
            NULL    // Additional command data.
            );

        if (FAILED(hr))
        {
            goto done;
        }

        //  Update the sequence number.
        uCommandSeq++;    
    ```

    

4.  <span data-ttu-id="6d6ad-144">Per verificare che la funzionalità HDCP sia abilitata, inviare una richiesta di stato del [**\_ \_ \_ \_ livello di protezione virtuale OPM Get**](opm-get-virtual-protection-level.md) (non visualizzata).</span><span class="sxs-lookup"><span data-stu-id="6d6ad-144">To verify that HDCP is enabled, send an [**OPM\_GET\_VIRTUAL\_PROTECTION\_LEVEL**](opm-get-virtual-protection-level.md) status request (not shown).</span></span>

## <a name="computing-the-omac-1-value"></a><span data-ttu-id="6d6ad-145">Calcolo del valore OMAC-1</span><span class="sxs-lookup"><span data-stu-id="6d6ad-145">Computing the OMAC-1 Value</span></span>

<span data-ttu-id="6d6ad-146">Il codice seguente illustra come calcolare il valore OMAC-1 usato per firmare le strutture di richiesta e di comando di OPM.</span><span class="sxs-lookup"><span data-stu-id="6d6ad-146">The following code shows how to compute the OMAC-1 value that is used to sign the OPM command and request structures.</span></span>


```C++
// Helper functions for some bitwise operations.

#define AES_BLOCKLEN    (16)
#define AES_KEYSIZE_128 (16)

inline void XOR( 
    BYTE *lpbLHS, 
    const BYTE *lpbRHS, 
    DWORD cbSize = AES_BLOCKLEN 
    )
{
    for( DWORD i = 0; i < cbSize; i++ )
    {
        lpbLHS[i] ^= lpbRHS[i];
    }
}

inline void LShift(const BYTE *lpbOpd, BYTE *lpbRes)
{
    for( DWORD i = 0; i < AES_BLOCKLEN; i++ )
    {
        lpbRes[i] = lpbOpd[i] << 1;
        if( i < AES_BLOCKLEN - 1 )
        {
            lpbRes[i] |= ( (unsigned char)lpbOpd[i+1] ) >> 7;
        }
    }
}

//  Generate OMAC1 signature using AES128

HRESULT ComputeOMAC(
    OPM_RANDOM_NUMBER&  AesKey,     // Session key
    PUCHAR pb,                      // Data
    DWORD cb,                       // Size of the data
    OPM_OMAC *pTag                  // Receives the OMAC
    )
{
    HRESULT hr = S_OK;
    BCRYPT_ALG_HANDLE hAlg = NULL;
    BCRYPT_KEY_HANDLE hKey = NULL;
    DWORD cbKeyObject = 0;
    DWORD cbData = 0;
    PBYTE pbKeyObject = NULL;

    PUCHAR Key = (PUCHAR)AesKey.abRandomNumber;

    struct 
    {
        BCRYPT_KEY_DATA_BLOB_HEADER Header;
        UCHAR Key[AES_KEYSIZE_128];
    } KeyBlob;

    KeyBlob.Header.dwMagic = BCRYPT_KEY_DATA_BLOB_MAGIC;
    KeyBlob.Header.dwVersion = BCRYPT_KEY_DATA_BLOB_VERSION1;
    KeyBlob.Header.cbKeyData = AES_KEYSIZE_128;
    CopyMemory(KeyBlob.Key, Key, sizeof(KeyBlob.Key));

    BYTE rgbLU[OPM_OMAC_SIZE];
    BYTE rgbLU_1[OPM_OMAC_SIZE];
    BYTE rBuffer[OPM_OMAC_SIZE];

    hr = BCryptOpenAlgorithmProvider(
        &hAlg, 
        BCRYPT_AES_ALGORITHM, 
        MS_PRIMITIVE_PROVIDER, 
        0
        );

    //  Get the size needed for the key data
    if (S_OK == hr) 
    {
        hr = BCryptGetProperty(
            hAlg, 
            BCRYPT_OBJECT_LENGTH, 
            (PBYTE)&cbKeyObject, 
            sizeof(DWORD), 
            &cbData, 
            0
            );
    }

    //  Allocate the key data object
    if (S_OK == hr) 
    {
        pbKeyObject = new (std::nothrow) BYTE[cbKeyObject];
        if (NULL == pbKeyObject) 
        {
            hr = E_OUTOFMEMORY;
        }
    }

    //  Set to CBC chain mode
    if (S_OK == hr) 
    {
        hr = BCryptSetProperty(
            hAlg, 
            BCRYPT_CHAINING_MODE, 
            (PBYTE)BCRYPT_CHAIN_MODE_CBC, 
            sizeof(BCRYPT_CHAIN_MODE_CBC), 
            0
            );
    }

    //  Set the key
    if (S_OK == hr) 
    {
        hr = BCryptImportKey(hAlg, NULL, BCRYPT_KEY_DATA_BLOB, &hKey, 
            pbKeyObject, cbKeyObject, (PUCHAR)&KeyBlob, sizeof(KeyBlob), 0);
    }

    //  Encrypt 0s
    if (S_OK == hr) 
    {
        DWORD cbBuffer = sizeof(rBuffer);
        ZeroMemory(rBuffer, sizeof(rBuffer));

        hr = BCryptEncrypt(hKey, rBuffer, cbBuffer, NULL, NULL, 0, 
            rBuffer, sizeof(rBuffer), &cbBuffer, 0);
    }

    //  Compute OMAC1 parameters
    if (S_OK == hr)
    {
        const BYTE bLU_ComputationConstant = 0x87;
        LPBYTE pbL = rBuffer;

        LShift( pbL, rgbLU );
        if( pbL[0] & 0x80 )
        {
            rgbLU[OPM_OMAC_SIZE - 1] ^= bLU_ComputationConstant;
        }
        LShift( rgbLU, rgbLU_1 );
        if( rgbLU[0] & 0x80 )
        {
            rgbLU_1[OPM_OMAC_SIZE - 1] ^= bLU_ComputationConstant;
        }
    }

    //  Generate the hash. 
    if (S_OK == hr) 
    {
        // Redo the key to restart the CBC.

        BCryptDestroyKey(hKey);
        hKey = NULL;

        hr = BCryptImportKey(hAlg, NULL, BCRYPT_KEY_DATA_BLOB, &hKey,
            pbKeyObject, cbKeyObject, (PUCHAR)&KeyBlob, sizeof(KeyBlob), 0);
    }

    if (S_OK == hr) 
    {
        PUCHAR pbDataInCur = pb;
        cbData = cb;
        do
        {
            DWORD cbBuffer = 0;

            if (cbData > OPM_OMAC_SIZE) 
            {
                CopyMemory( rBuffer, pbDataInCur, OPM_OMAC_SIZE );

                hr = BCryptEncrypt(hKey, rBuffer, sizeof(rBuffer), NULL, 
                    NULL, 0, rBuffer, sizeof(rBuffer), &cbBuffer, 0);

                pbDataInCur += OPM_OMAC_SIZE;
                cbData -= OPM_OMAC_SIZE;
            }
            else 
            {   
                if (cbData == OPM_OMAC_SIZE)
                {
                    CopyMemory(rBuffer, pbDataInCur, OPM_OMAC_SIZE);
                    XOR(rBuffer, rgbLU);
                }
                else 
                {
                    ZeroMemory( rBuffer, OPM_OMAC_SIZE );
                    CopyMemory( rBuffer, pbDataInCur, cbData );
                    rBuffer[ cbData ] = 0x80;

                    XOR(rBuffer, rgbLU_1);
                }

                hr = BCryptEncrypt(hKey, rBuffer, sizeof(rBuffer), NULL, NULL, 
                    0, (PUCHAR)pTag->abOMAC, OPM_OMAC_SIZE, &cbBuffer, 0);

                cbData = 0;
            }
                
        } while( S_OK == hr && cbData > 0 );
    }

    //  Clean up
    if (hKey)
    {
        BCryptDestroyKey(hKey);
    }
    if (hAlg)
    {
        BCryptCloseAlgorithmProvider(hAlg, 0);
    }
    delete [] pbKeyObject;
    return hr;
}
```



<span data-ttu-id="6d6ad-147">L'algoritmo OMAC-1 viene descritto in dettaglio in <https://www.nuee.nagoya-u.ac.jp/labs/tiwata/omac/omac.html> .</span><span class="sxs-lookup"><span data-stu-id="6d6ad-147">The OMAC-1 algorithm is described in detail at <https://www.nuee.nagoya-u.ac.jp/labs/tiwata/omac/omac.html>.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6d6ad-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6d6ad-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d6ad-149">Gestione protezione output</span><span class="sxs-lookup"><span data-stu-id="6d6ad-149">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> </dl>

 

 



