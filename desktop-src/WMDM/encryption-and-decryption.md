---
title: Crittografia e decrittografia
description: Crittografia e decrittografia
ms.assetid: 6aef4138-0391-4edd-b4fc-d6d0ec3c735b
keywords:
- Windows Media Gestione dispositivi, crittografia
- Gestione dispositivi, crittografia
- applicazioni desktop, crittografia
- provider di servizi, crittografia
- Guida per programmatori, crittografia
- Crittografia
- Windows Media Gestione dispositivi, decrittografia
- Gestione dispositivi, decrittografia
- applicazioni desktop, decrittografia
- provider di servizi, decrittografia
- Guida per programmatori, decrittografia
- decrittografia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78688c1b4ca9991d8b322c6991de96a51e7e8d22
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399623"
---
# <a name="encryption-and-decryption"></a><span data-ttu-id="57823-115">Crittografia e decrittografia</span><span class="sxs-lookup"><span data-stu-id="57823-115">Encryption and Decryption</span></span>

<span data-ttu-id="57823-116">Windows Media Gestione dispositivi richiede la crittografia dei file inviati tra il provider di servizi e l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="57823-116">Windows Media Device Manager requires encryption of files sent between the service provider and the application.</span></span> <span data-ttu-id="57823-117">Questa operazione può essere eseguita in uno dei due modi seguenti:</span><span class="sxs-lookup"><span data-stu-id="57823-117">This can be done in one of two ways:</span></span>

-   <span data-ttu-id="57823-118">Se il provider di servizi supporta solo [**IMDSPObject:: Read**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read) e [**IMDSPObject:: Write**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write), i dati devono essere crittografati e decrittografati dall'applicazione e dal provider di servizi utilizzando rispettivamente i metodi [CSecureChannelClient](csecurechannelclient-class.md) e [CSecureChannelServer](csecurechannelserver-class.md) .</span><span class="sxs-lookup"><span data-stu-id="57823-118">If the service provider supports only [**IMDSPObject::Read**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read) and [**IMDSPObject::Write**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write), the data must be encrypted and decrypted by the application and service provider by using [CSecureChannelClient](csecurechannelclient-class.md) and [CSecureChannelServer](csecurechannelserver-class.md) methods respectively.</span></span>
-   <span data-ttu-id="57823-119">Se il provider di servizi supporta [**IMDSPObject2:: ReadOnClearChannel**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject2-readonclearchannel) e [**IMDSPObject2:: WriteOnClearChannel**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject2-writeonclearchannel), l'applicazione può evitare costi di autenticazione dei messaggi del canale sicuro.</span><span class="sxs-lookup"><span data-stu-id="57823-119">If the service provider supports [**IMDSPObject2::ReadOnClearChannel**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject2-readonclearchannel) and [**IMDSPObject2::WriteOnClearChannel**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject2-writeonclearchannel), your application can avoid costly secure channel message authentication.</span></span> <span data-ttu-id="57823-120">Il canale protetto viene mantenuto in modo che i provider di servizi legacy che non implementano [**IMDSPObject2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2) possano continuare a funzionare.</span><span class="sxs-lookup"><span data-stu-id="57823-120">(The secure channel is retained so that legacy service providers that do not implement [**IMDSPObject2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2) can still continue to function.)</span></span>

<span data-ttu-id="57823-121">Il requisito di crittografia impedisce alle applicazioni dannose di ottenere i dati passati tra i componenti software e protegge anche l'integrità dei dati inviati da o verso il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="57823-121">The encryption requirement prevents malicious applications from obtaining data that is being passed between software components, and also protects the integrity of data being sent to or from the device.</span></span>

<span data-ttu-id="57823-122">I tre metodi seguenti richiedono la crittografia o la decrittografia.</span><span class="sxs-lookup"><span data-stu-id="57823-122">The following three methods require encryption or decryption.</span></span>



| <span data-ttu-id="57823-123">Metodo</span><span class="sxs-lookup"><span data-stu-id="57823-123">Method</span></span>                                                                          | <span data-ttu-id="57823-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="57823-124">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="57823-125">**IWMDMOperation::TransferObjectData**</span><span class="sxs-lookup"><span data-stu-id="57823-125">**IWMDMOperation::TransferObjectData**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-transferobjectdata) | <span data-ttu-id="57823-126">Applicazione Crittografia o decrittografia, a seconda che l'applicazione stia inviando o ricevendo dati.</span><span class="sxs-lookup"><span data-stu-id="57823-126">(Application) Encryption or decryption, depending on whether the application is sending or receiving data.</span></span> |
| [<span data-ttu-id="57823-127">**IMDSPObject:: Read**</span><span class="sxs-lookup"><span data-stu-id="57823-127">**IMDSPObject::Read**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read)                                   | <span data-ttu-id="57823-128">(Provider di servizi) Crittografia.</span><span class="sxs-lookup"><span data-stu-id="57823-128">(Service provider) Encryption.</span></span>                                                                             |
| [<span data-ttu-id="57823-129">**IMDSPObject:: Write**</span><span class="sxs-lookup"><span data-stu-id="57823-129">**IMDSPObject::Write**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write)                                 | <span data-ttu-id="57823-130">(Provider di servizi) Decrittografia.</span><span class="sxs-lookup"><span data-stu-id="57823-130">(Service Provider) Decryption.</span></span>                                                                             |



 

<span data-ttu-id="57823-131">La crittografia e la decrittografia sono entrambe eseguite da singole chiamate al metodo.</span><span class="sxs-lookup"><span data-stu-id="57823-131">Encryption and decryption are both done by single method calls.</span></span> <span data-ttu-id="57823-132">La crittografia viene eseguita da [**CSecureChannelClient:: EncryptParam**](/previous-versions/bb231587(v=vs.85)) per le applicazioni o da [**CSecureChannelServer:: EncryptParam**](/previous-versions/ms868509(v=msdn.10)) per i provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="57823-132">Encryption is done by [**CSecureChannelClient::EncryptParam**](/previous-versions/bb231587(v=vs.85)) for applications or by [**CSecureChannelServer::EncryptParam**](/previous-versions/ms868509(v=msdn.10)) for service providers.</span></span> <span data-ttu-id="57823-133">La decrittografia viene eseguita da [**CSecureChannelClient::D ecryptparam**](/previous-versions/bb231586(v=vs.85)) for Applications o [**CSecureChannelServer::D ecryptparam**](/previous-versions/bb231598(v=vs.85)) per i provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="57823-133">Decryption is done by [**CSecureChannelClient::DecryptParam**](/previous-versions/bb231586(v=vs.85)) for applications or [**CSecureChannelServer::DecryptParam**](/previous-versions/bb231598(v=vs.85)) for service providers.</span></span> <span data-ttu-id="57823-134">I parametri sono identici tra i metodi client e server.</span><span class="sxs-lookup"><span data-stu-id="57823-134">The parameters are identical between the client and server methods.</span></span>

<span data-ttu-id="57823-135">I passaggi seguenti illustrano come crittografare e decrittografare i dati.</span><span class="sxs-lookup"><span data-stu-id="57823-135">The following steps show how to encrypt and decrypt data.</span></span> <span data-ttu-id="57823-136">Questi passaggi sono importanti solo se l'applicazione comunica con un provider di servizi legacy che non implementa [IWMDMOperation3:: TransferObjectDataOnClearChannel](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation3-transferobjectdataonclearchannel).</span><span class="sxs-lookup"><span data-stu-id="57823-136">(These steps are important only if your application communicates with a legacy service provider that does not implement [IWMDMOperation3::TransferObjectDataOnClearChannel](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation3-transferobjectdataonclearchannel).)</span></span>

<span data-ttu-id="57823-137">**Crittografia**</span><span class="sxs-lookup"><span data-stu-id="57823-137">**Encryption**</span></span>

1.  <span data-ttu-id="57823-138">Creare la chiave MAC per i dati crittografati, come descritto in [autenticazione del messaggio](message-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="57823-138">Create the MAC key for the encrypted data, as described in [Message Authentication](message-authentication.md).</span></span>
2.  <span data-ttu-id="57823-139">Chiamare **EncryptParam** con i dati da crittografare per eseguire la crittografia sul posto.</span><span class="sxs-lookup"><span data-stu-id="57823-139">Call **EncryptParam** with the data to encrypt, to perform in-place encryption.</span></span>

<span data-ttu-id="57823-140">Nell'esempio di codice seguente viene illustrata l'implementazione di [**IMDSPObject:: Read**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read)di un provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="57823-140">The following code example demonstrates a service provider's implementation of [**IMDSPObject::Read**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-read).</span></span> <span data-ttu-id="57823-141">Questo metodo crea la chiave MAC usando i dati da crittografare e le dimensioni dei dati e li invia all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="57823-141">This method creates the MAC key using the data to encrypt and the size of the data, and sends them both to the application.</span></span>


```C++
HRESULT CMyStorage::Read(
    BYTE  *pData,
    DWORD *pdwSize,
    BYTE   abMac[WMDM_MAC_LENGTH])
{
    HRESULT  hr;
    DWORD    dwToRead;         // Bytes to read.
    DWORD    dwRead   = NULL;  // Bytes read.
    BYTE    *pTmpData = NULL;  // Temporary buffer to hold data before 
                               // it is copied to pData.

    // Use a global CSecureChannelServer member to verify that 
    // the client is authenticated.
    if (!(g_pAppSCServer->fIsAuthenticated()))
    {
        return WMDM_E_NOTCERTIFIED;
    }
    

    // Verify that the handle to the file to read is valid.
    if(m_hFile == INVALID_HANDLE_VALUE)
    {
        return E_FAIL;
    }

    // Create a buffer to hold the data read.    
    dwToRead = *pdwSize;
    pTmpData = new BYTE [dwToRead] ;
    if(!pTmpData)
        return E_OUTOFMEMORY;

    // Read data into the temporary buffer.
    if(ReadFile(m_hFile,(LPVOID)pTmpData,dwToRead,&dwRead,NULL)) 
    { 
        *pdwSize = dwRead; 

        if( dwRead )
        {
            // Create a MAC from all the parameters.
            // CORg is a macro that goes to Error label on failure.
            // MAC consists of data and size of data.
            HMAC hMAC;
            
            CORg(g_pAppSCServer->MACInit(&hMAC));
            CORg(g_pAppSCServer->MACUpdate(hMAC, (BYTE*)(pTmpData), dwRead));
            CORg(g_pAppSCServer->MACUpdate(hMAC, (BYTE*)(pdwSize), sizeof(DWORD)));
            CORg(g_pAppSCServer->MACFinal(hMAC, abMac));
            
            // Encrypt the data.
            CORg(g_pAppSCServer->EncryptParam(pTmpData, dwRead));
            
            // Copy data from the temporary buffer into the out parameter.
            memcpy(pData, pTmpData, dwRead);
        }
    
        hr = S_OK; 
    }
    else
    { 
        *pdwSize = 0; 

        hr = E_FAIL; 
    }

Error:

    if(pTmpData) 
    {
        delete [] pTmpData;
    }

    return hr;
} 
```



<span data-ttu-id="57823-142">**Decrittografia**</span><span class="sxs-lookup"><span data-stu-id="57823-142">**Decryption**</span></span>

1.  <span data-ttu-id="57823-143">Chiamare **DecryptParam** con i dati da crittografare per eseguire la decrittografia sul posto.</span><span class="sxs-lookup"><span data-stu-id="57823-143">Call **DecryptParam** with the data to encrypt, to perform in-place decryption.</span></span>
2.  <span data-ttu-id="57823-144">Verificare la chiave MAC per i dati decrittografati, come descritto in [autenticazione del messaggio](message-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="57823-144">Verify the MAC key for the decrypted data, as described in [Message Authentication](message-authentication.md).</span></span>

<span data-ttu-id="57823-145">Nell'esempio di codice seguente viene illustrata l'implementazione di [**IMDSPObject:: Write**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write)di un provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="57823-145">The following code example demonstrates a service provider's implementation of [**IMDSPObject::Write**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspobject-write).</span></span> <span data-ttu-id="57823-146">Questo metodo crea la chiave MAC usando i dati da crittografare e le dimensioni dei dati e li invia all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="57823-146">This method creates the MAC key using the data to encrypt and the size of the data, and sends them both to the application.</span></span>


```C++
HRESULT CMyStorage::Write(BYTE *pData, DWORD *pdwSize,
                                 BYTE abMac[WMDM_MAC_LENGTH])
{
    HRESULT  hr;
    DWORD    dwWritten = 0;
    BYTE    *pTmpData  = NULL;          // Temporary buffer to hold the 
                                        // data during decryption.
    BYTE     pTempMac[WMDM_MAC_LENGTH]; // Temporary MAC that will be 
                                        // copied into the abMac
                                        // out parameter.

    if( m_hFile == INVALID_HANDLE_VALUE )
    {
        return E_FAIL;
    }

    // Allocate the temporary buffer and copy the encrypted data into it.
    pTmpData = new BYTE [*pdwSize];
    if(!pTmpData)
        return E_OUTOFMEMORY;
    memcpy(pTmpData, pData, *pdwSize);

    // Decrypt the data.
    CHRg(g_pAppSCServer->DecryptParam(pTmpData, *pdwSize));

    // Check the MAC passed to the method. The MAC is built from
    // the data and data size parameters.
    // CORg is a macro that goes to the Error label on failure.
    HMAC hMAC;
    CORg(g_pAppSCServer->MACInit(&hMAC));
    CORg(g_pAppSCServer->MACUpdate(hMAC, (BYTE*)(pTmpData), *pdwSize));
    CORg(g_pAppSCServer->MACUpdate(hMAC, (BYTE*)(pdwSize), sizeof(*pdwSize)));
    CORg(g_pAppSCServer->MACFinal(hMAC, pTempMac));

    // If the MAC values don't match, return an error.
    if (memcmp(abMac, pTempMac, WMDM_MAC_LENGTH) != 0)
    {
        hr = WMDM_E_MAC_CHECK_FAILED;
        goto Error;
    }

    // The MAC values matched, so write the decrypted data to a local file.
    if( WriteFile(m_hFile,pTmpData,*pdwSize,&dwWritten,NULL) ) 
    {
        hr = S_OK;
    }
    else 
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
    }

    *pdwSize = dwWritten;

Error:

    if( pTmpData )
    {
        delete [] pTmpData;
    }

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="57823-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="57823-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57823-148">**Uso di canali con autenticazione sicura**</span><span class="sxs-lookup"><span data-stu-id="57823-148">**Using Secure Authenticated Channels**</span></span>](using-secure-authenticated-channels.md)
</dt> </dl>

 

 