---
title: Autenticazione del messaggio
description: Autenticazione del messaggio
ms.assetid: 6cb49f6b-e303-4840-9343-9891e75e07a4
keywords:
- Windows Media Gestione dispositivi, autenticazione del messaggio
- Gestione dispositivi, autenticazione del messaggio
- applicazioni desktop, autenticazione del messaggio
- provider di servizi, autenticazione del messaggio
- Guida per programmatori, autenticazione del messaggio
- autenticazione del messaggio
- codice di autenticazione messaggi (MAC)
- MAC (codice di autenticazione messaggi)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14805e2074509e918902aae9eb9e9680ca52a6d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297839"
---
# <a name="message-authentication"></a><span data-ttu-id="5bf75-111">Autenticazione del messaggio</span><span class="sxs-lookup"><span data-stu-id="5bf75-111">Message Authentication</span></span>

<span data-ttu-id="5bf75-112">L'autenticazione del messaggio è un processo che consente alle applicazioni e ai provider di servizi di verificare che i dati passati tra di essi non siano stati manomessi.</span><span class="sxs-lookup"><span data-stu-id="5bf75-112">Message authentication is a process that enables applications and service providers to verify that data passed between them has not been tampered with.</span></span> <span data-ttu-id="5bf75-113">Windows Media Gestione dispositivi consente alle applicazioni e ai provider di servizi di eseguire l'autenticazione dei messaggi usando i codici Mac (Message Authentication Code).</span><span class="sxs-lookup"><span data-stu-id="5bf75-113">Windows Media Device Manager allows applications and service providers to perform message authentication by using message authentication codes (MACs).</span></span> <span data-ttu-id="5bf75-114">Ecco come funziona l'autenticazione MAC:</span><span class="sxs-lookup"><span data-stu-id="5bf75-114">Here is how MAC authentication works:</span></span>

<span data-ttu-id="5bf75-115">Il mittente dei dati, in genere il provider di servizi, passa una o più parti di dati tramite una funzione di crittografia unidirezionale che produce una singola firma, il MAC, per tutti i dati.</span><span class="sxs-lookup"><span data-stu-id="5bf75-115">The data sender, usually the service provider, passes one or more pieces of data through a one-way cryptographic function that produces a single signature, the MAC, for all the data.</span></span> <span data-ttu-id="5bf75-116">Il mittente invia quindi tutte le parti di dati firmate insieme al MAC al ricevitore, in genere l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5bf75-116">The sender then sends all the signed pieces of data together with the MAC to the receiver (usually the application).</span></span> <span data-ttu-id="5bf75-117">Il ricevitore passa i dati attraverso la stessa funzione di crittografia per generare un MAC e lo confronta con il MAC che è stato inviato.</span><span class="sxs-lookup"><span data-stu-id="5bf75-117">The receiver passes the data through the same cryptographic function to generate a MAC and compares it to the MAC that was sent.</span></span> <span data-ttu-id="5bf75-118">Se il MAC corrisponde, i dati non sono stati modificati.</span><span class="sxs-lookup"><span data-stu-id="5bf75-118">If the MAC matches, the data has not been modified.</span></span>

<span data-ttu-id="5bf75-119">Per eseguire l'autenticazione MAC, l'applicazione o il provider di servizi richiede una chiave di crittografia e un certificato corrispondente.</span><span class="sxs-lookup"><span data-stu-id="5bf75-119">To perform MAC authentication, the application or service provider requires an encryption key and a matching certificate.</span></span> <span data-ttu-id="5bf75-120">Per informazioni su dove ottenere questi dati, vedere [strumenti per lo sviluppo](tools-for-development.md).</span><span class="sxs-lookup"><span data-stu-id="5bf75-120">For information on where to get these, see [Tools for Development](tools-for-development.md).</span></span>

<span data-ttu-id="5bf75-121">Nei passaggi seguenti viene descritto il modo in cui i dati vengono firmati dal mittente e successivamente controllati dal ricevitore.</span><span class="sxs-lookup"><span data-stu-id="5bf75-121">The following steps describe how data is signed by the sender, and later checked by the receiver.</span></span> <span data-ttu-id="5bf75-122">In Windows Media Gestione dispositivi, il provider di servizi usa la classe [CSecureChannelServer](csecurechannelserver-class.md) per generare i computer Mac e l'applicazione usa la classe [CSecureChannelClient](csecurechannelclient-class.md) .</span><span class="sxs-lookup"><span data-stu-id="5bf75-122">In Windows Media Device Manager, the service provider uses the [CSecureChannelServer](csecurechannelserver-class.md) class to generate MACs, and the application uses the [CSecureChannelClient](csecurechannelclient-class.md) class.</span></span> <span data-ttu-id="5bf75-123">Entrambe le classi forniscono funzioni identiche con parametri identici, quindi i passaggi seguenti si applicano a entrambe le classi.</span><span class="sxs-lookup"><span data-stu-id="5bf75-123">Both classes provide identical functions with identical parameters, so the following steps apply to both classes.</span></span>

<span data-ttu-id="5bf75-124">Mittente, in genere il provider di servizi:</span><span class="sxs-lookup"><span data-stu-id="5bf75-124">The sender (typically the service provider):</span></span>

1.  <span data-ttu-id="5bf75-125">Ottiene i dati da firmare.</span><span class="sxs-lookup"><span data-stu-id="5bf75-125">Get the data to be signed.</span></span>
2.  <span data-ttu-id="5bf75-126">Creare un nuovo handle MAC chiamando **MACInit**.</span><span class="sxs-lookup"><span data-stu-id="5bf75-126">Create a new MAC handle by calling **MACInit**.</span></span>
3.  <span data-ttu-id="5bf75-127">Aggiungere una porzione di dati da firmare all'handle chiamando **MACUpdate**.</span><span class="sxs-lookup"><span data-stu-id="5bf75-127">Add a piece of data to be signed to the handle by calling **MACUpdate**.</span></span> <span data-ttu-id="5bf75-128">Questa funzione accetta l'handle creato in precedenza, oltre a una parte di dati che devono essere firmati.</span><span class="sxs-lookup"><span data-stu-id="5bf75-128">This function accepts the previously created handle, plus a piece of data that must be signed.</span></span>
4.  <span data-ttu-id="5bf75-129">Ripetere il passaggio 3 con tutti i dati aggiuntivi che devono essere firmati.</span><span class="sxs-lookup"><span data-stu-id="5bf75-129">Repeat step 3 with each additional piece of data that must be signed.</span></span> <span data-ttu-id="5bf75-130">Non sono importanti i dati degli ordini aggiunti al MAC.</span><span class="sxs-lookup"><span data-stu-id="5bf75-130">It does not matter in what order data is added to the MAC.</span></span>
5.  <span data-ttu-id="5bf75-131">Copiare il MAC dall'handle in un nuovo buffer di byte chiamando **MACFinal**.</span><span class="sxs-lookup"><span data-stu-id="5bf75-131">Copy the MAC from the handle to a new byte buffer by calling **MACFinal**.</span></span> <span data-ttu-id="5bf75-132">Questa funzione accetta l'handle MAC e un buffer allocato e copia il MAC dall'handle nel buffer fornito.</span><span class="sxs-lookup"><span data-stu-id="5bf75-132">This function accepts the MAC handle and a buffer that you allocate, and copies the MAC from the handle into the provided buffer.</span></span>

<span data-ttu-id="5bf75-133">Quando si esegue l'autenticazione MAC, è importante che sia il mittente che il ricevitore stiano inserendo gli stessi dati nel MAC.</span><span class="sxs-lookup"><span data-stu-id="5bf75-133">When performing MAC authentication, it is important that both the sender and the receiver are putting the same data into the MAC.</span></span> <span data-ttu-id="5bf75-134">Per i metodi dell'applicazione che forniscono un MAC, in genere tutti i parametri sono inclusi nel valore MAC (ad eccezione del MAC stesso, ovviamente).</span><span class="sxs-lookup"><span data-stu-id="5bf75-134">For the application methods that provide a MAC, typically all parameters are included in the MAC value (except for the MAC itself, of course).</span></span> <span data-ttu-id="5bf75-135">Si consideri, ad esempio, il metodo **IWMDMOperation:: TransferObjectData** :</span><span class="sxs-lookup"><span data-stu-id="5bf75-135">For example, consider the **IWMDMOperation::TransferObjectData** method:</span></span>

`HRESULT TransferObjectData(BYTE* pData, DWORD* pdwSize, BYTE[WMDM_MAC_LENGTH] abMac);`

<span data-ttu-id="5bf75-136">In questo metodo, il MAC include *pData* e *pdwSize*.</span><span class="sxs-lookup"><span data-stu-id="5bf75-136">In this method, the MAC would include *pData* and *pdwSize*.</span></span> <span data-ttu-id="5bf75-137">Se non vengono inclusi entrambi i parametri, il MAC creato non corrisponderà al MAC passato a *abMac*.</span><span class="sxs-lookup"><span data-stu-id="5bf75-137">If you do not include both the parameters, the MAC you create will not match the MAC passed to *abMac*.</span></span> <span data-ttu-id="5bf75-138">Un provider di servizi deve assicurarsi di inserire tutti i parametri richiesti nel metodo dell'applicazione nel valore MAC.</span><span class="sxs-lookup"><span data-stu-id="5bf75-138">A service provider must be sure to put all the required parameters in the application method into the MAC value.</span></span>

<span data-ttu-id="5bf75-139">Nel codice C++ riportato di seguito viene illustrata la creazione di un MAC nell'implementazione di un provider di servizi di [**IMDSPStorageGlobals:: GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getserialnumber).</span><span class="sxs-lookup"><span data-stu-id="5bf75-139">The following C++ code demonstrates creating a MAC in a service provider's implementation of [**IMDSPStorageGlobals::GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getserialnumber).</span></span>


```C++
HRESULT CMyDevice::GetSerialNumber(
    PWMDMID pSerialNumber, 
    BYTE abMac[WMDM_MAC_LENGTH])
{
    HRESULT hr;

    // g_pSecureChannelServer is a global CSecureChannelServer object
    // created earlier.

    // Standard check that the CSecureChannelServer was authenticated previously.
    if ( !(g_pSecureChannelServer->fIsAuthenticated()) )
    {
        return WMDM_E_NOTCERTIFIED;
    }

    // Call a helper function to get the device serial number.
    hr = UtilGetSerialNumber(m_wcsName, pSerialNumber, TRUE);
    if(hr == HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED))
    {
        hr = WMDM_E_NOTSUPPORTED;
    }

    if(hr == S_OK)
    {
        // Create the MAC handle.
        HMAC hMAC;
        hr = g_pSecureChannelServer->MACInit(&hMAC);
        if(FAILED(hr))
            return hr;

        // Add the serial number to the MAC.
        g_pSecureChannelServer->MACUpdate(hMAC, (BYTE*)(pSerialNumber), sizeof(WMDMID));
        if(FAILED(hr))
            return hr;

        // Get the created MAC value from the handle.
        g_pSecureChannelServer->MACFinal(hMAC, abMac);
        if(FAILED(hr))
            return hr;
    }

    return hr;
}
```



<span data-ttu-id="5bf75-140">Il ricevitore (in genere l'applicazione):</span><span class="sxs-lookup"><span data-stu-id="5bf75-140">The receiver (typically the application):</span></span>

<span data-ttu-id="5bf75-141">Se il ricevitore non ha implementato l'interfaccia [**IWMDMOperation3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation3) , deve eseguire gli stessi passaggi del mittente, quindi confrontare i due valori Mac.</span><span class="sxs-lookup"><span data-stu-id="5bf75-141">If the receiver has not implemented the [**IWMDMOperation3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation3) interface, it should perform the same steps as the sender, and then compare the two MAC values.</span></span> <span data-ttu-id="5bf75-142">Nell'esempio di codice C++ riportato di seguito viene illustrato il modo in cui un'applicazione controlla il MAC ricevuto in una chiamata a [**IWMDMStorageGlobals:: GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-getserialnumber) per assicurarsi che il numero di serie non sia stato alterato in transito.</span><span class="sxs-lookup"><span data-stu-id="5bf75-142">The following C++ code example shows how an application would check the MAC received in a call to [**IWMDMStorageGlobals::GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-getserialnumber) to ensure that the serial number was not tampered with in transit.</span></span>


```C++
//
// Get and verify the serial number.
//
WMDMID serialNumber;
BYTE receivedMAC[WMDM_MAC_LENGTH];
hr = pIWMDMDevice->GetSerialNumber(&serialNumber, receivedMAC);

// Check the MAC to guarantee the serial number has not been tampered with.
if (hr == S_OK)
{
    // Initialize a MAC handle, 
    // add all parameters to the MAC,
    // and retrieve the calculated MAC value.
    // m_pSAC is a global CSecureChannelClient object created earlier.
    HMAC hMAC;
    BYTE calculatedMAC[WMDM_MAC_LENGTH];
    hr = m_pSAC->MACInit(&hMAC);
    if(FAILED(hr))
        return hr;

    hr = m_pSAC->MACUpdate(hMAC, (BYTE*)(&serialNumber), sizeof(serialNumber));
    if(FAILED(hr))
        return hr;

    hr = m_pSAC->MACFinal(hMAC, (BYTE*)calculatedMAC);
    if(FAILED(hr))
        return hr;

    // If the two MAC values match, the MAC is authentic. 
    if (memcmp(calculatedMAC, receivedMAC, sizeof(calculatedMAC)) == 0)
    {
        // The MAC is authentic; print the serial number.
        CHAR* serialNumberBuffer = 
            new CHAR[serialNumber.SerialNumberLength + 1];
        ZeroMemory(serialNumberBuffer, 
            (serialNumber.SerialNumberLength + 1) * sizeof(CHAR));
        memcpy(serialNumberBuffer, serialNumber.pID, 
            serialNumber.SerialNumberLength * sizeof(CHAR));
        // TODO: Display the serial number.
        delete serialNumberBuffer;
    }
    else
    {
        // TODO: Display a message indicating that the serial number MAC 
        // does not match.
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="5bf75-143">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5bf75-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5bf75-144">**Uso di canali con autenticazione sicura**</span><span class="sxs-lookup"><span data-stu-id="5bf75-144">**Using Secure Authenticated Channels**</span></span>](using-secure-authenticated-channels.md)
</dt> </dl>

 

 




