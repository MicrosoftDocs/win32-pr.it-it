---
title: Revoca e rinnovo automatici dei componenti
description: Revoca e rinnovo automatici dei componenti
ms.assetid: be4899d7-1d87-4450-8c0e-75cf112ca66a
keywords:
- Windows Media Format SDK, revoca e rinnovo automatici
- Windows Media Format SDK, revoca
- Windows Media Format SDK, rinnovo
- Digital Rights Management (DRM), revoca e rinnovo automatici
- DRM (Digital Rights Management), revoca e rinnovo automatici
- Digital Rights Management (DRM), revoca
- DRM (Digital Rights Management), revoca
- Digital Rights Management (DRM), rinnovo
- DRM (Digital Rights Management), rinnovo
- API estese del client DRM, revoca e rinnovo automatici
- API estese client, revoca e rinnovo automatici
- API estese del client DRM, revoca
- API estese client, revoca
- API estese del client DRM, rinnovo
- API estese client, rinnovo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b9046d04d8ca7a138a06cba4d26cd82bc5a12b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338630"
---
# <a name="automated-component-revocation-and-renewal"></a><span data-ttu-id="ad86d-118">Revoca e rinnovo automatici dei componenti</span><span class="sxs-lookup"><span data-stu-id="ad86d-118">Automated Component Revocation and Renewal</span></span>

<span data-ttu-id="ad86d-119">Le applicazioni software o i componenti considerati compromessi possono essere revocati da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ad86d-119">Software applications or components that are considered compromised can be revoked by Microsoft.</span></span> <span data-ttu-id="ad86d-120">L'API estesa client Windows Media Format fornisce un meccanismo per la revoca e il rinnovo automatici dei componenti.</span><span class="sxs-lookup"><span data-stu-id="ad86d-120">The Windows Media Format Client Extended API provides a mechanism for the automated revocation and renewal of components.</span></span>

<span data-ttu-id="ad86d-121">I componenti revocati sono elencati in un elenco di revoche di certificati, pubblicato da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ad86d-121">Revoked components are listed in a certificate revocation list, which is published by Microsoft.</span></span> <span data-ttu-id="ad86d-122">Quando un componente viene revocato, il certificato viene aggiunto all'elenco di revoche di certificati e il BLOB delle informazioni di revoca \_ viene aggiornato sui server Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ad86d-122">When a component is revoked, its certificate is added to the certificate revocation list, and the revocation information BLOB (REV\_INFO) is updated on the Microsoft servers.</span></span>

<span data-ttu-id="ad86d-123">Per eseguire la revoca e il rinnovo automatici quando un utente tenta di elaborare contenuti protetti da DRM di Windows Media, l'applicazione deve eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="ad86d-123">To perform automated revocation and renewal when a user attempts to process Windows Media DRM protected content, your application must do the following:</span></span>

1.  <span data-ttu-id="ad86d-124">Estrarre la \_ versione di Rev info dalla licenza.</span><span class="sxs-lookup"><span data-stu-id="ad86d-124">Extract the REV\_INFO version from the license.</span></span> <span data-ttu-id="ad86d-125">Il numero di versione di REV \_ info si trova nel percorso seguente in una licenza XMR:</span><span class="sxs-lookup"><span data-stu-id="ad86d-125">The REV\_INFO version number is located in the following location in an XMR license:</span></span>
    ```C++
    <LICENSE version="2.0.0.0">
        <LICENSORINFO/>
        <DATA>
            <LID>...</LID>
            <KID>...</KID>
            <RevInfoVersion>42</RevInfoVersion>
            ...
         </DATA>
    ....
    </LICENSE>
    ```

    

2.  <span data-ttu-id="ad86d-126">Confrontare il \_ numero di versione di Rev info della licenza con il \_ numero di versione di Rev info nell'archivio locale chiamando il metodo [**IWMDRMSecurity:: GetRevocationDataVersion**](iwmdrmsecurity-getrevocationdataversion.md) .</span><span class="sxs-lookup"><span data-stu-id="ad86d-126">Compare the REV\_INFO version number of the license with the REV\_INFO version number in the local store by calling the [**IWMDRMSecurity::GetRevocationDataVersion**](iwmdrmsecurity-getrevocationdataversion.md) method.</span></span>
3.  <span data-ttu-id="ad86d-127">Se la \_ versione di Rev info non è aggiornata, chiamare il metodo [**IWMDRMSecurity::P erformsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md) , passando il \_ \_ \_ \_ flag di aggiornamento di revoca della sicurezza WMDRM nel parametro *dwFlags* .</span><span class="sxs-lookup"><span data-stu-id="ad86d-127">If the REV\_INFO version is not up to date, call the [**IWMDRMSecurity::PerformSecurityUpdate**](iwmdrmsecurity-performsecurityupdate.md) method, passing the WMDRM\_SECURITY\_PERFORM\_REVOCATION\_REFRESH flag in the *dwFlags* parameter.</span></span>
4.  <span data-ttu-id="ad86d-128">Recuperare l'elenco di revoche di certificati dall'archivio locale chiamando il metodo [**IWMDRMSecurity:: GetRevocationData**](iwmdrmsecurity-getrevocationdata.md) .</span><span class="sxs-lookup"><span data-stu-id="ad86d-128">Retrieve the certificate revocation list from the local store by calling the [**IWMDRMSecurity::GetRevocationData**](iwmdrmsecurity-getrevocationdata.md) method.</span></span>
5.  <span data-ttu-id="ad86d-129">Analizzare l'elenco di revoche e verificare la presenza di revoche DRM Windows Media.</span><span class="sxs-lookup"><span data-stu-id="ad86d-129">Parse the revocation list, and check for Windows Media DRM revocations.</span></span> <span data-ttu-id="ad86d-130">Per ulteriori informazioni, vedere [controllo della revoca del certificato](checking-certificate-revocation.md).</span><span class="sxs-lookup"><span data-stu-id="ad86d-130">For more information, see [Checking Certificate Revocation](checking-certificate-revocation.md).</span></span>
6.  <span data-ttu-id="ad86d-131">Se sono presenti revoche DRM di Windows Media:</span><span class="sxs-lookup"><span data-stu-id="ad86d-131">If there are any Windows Media DRM revocations:</span></span>
    1.  <span data-ttu-id="ad86d-132">Creare un Enabler di contenuto per rinnovare i componenti revocati chiamando il metodo [**IWMDRMSecurity:: GetContentEnablersForRevocations**](iwmdrmsecurity-getcontentenablersforrevocations.md) .</span><span class="sxs-lookup"><span data-stu-id="ad86d-132">Create a content enabler to renew the revoked components by calling the [**IWMDRMSecurity::GetContentEnablersForRevocations**](iwmdrmsecurity-getcontentenablersforrevocations.md) method.</span></span>
    2.  <span data-ttu-id="ad86d-133">Chiamare **IMFContentEnabler:: AutomaticEnable** che indirizza l'utente a un URL che contiene informazioni di rinnovo dei componenti.</span><span class="sxs-lookup"><span data-stu-id="ad86d-133">Call **IMFContentEnabler::AutomaticEnable** which directs the user to a URL that contains component renewal information.</span></span> <span data-ttu-id="ad86d-134">Questo metodo è documentato nell' [SDK Media Foundation](../medfound/microsoft-media-foundation-sdk.md) ( https://msdn.microsoft.com/library/ms694197(VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="ad86d-134">This method is documented in the [Media Foundation SDK](../medfound/microsoft-media-foundation-sdk.md) (https://msdn.microsoft.com/library/ms694197(VS.85).aspx).</span></span>
        > [!Note]  
        > <span data-ttu-id="ad86d-135">È necessario chiarire questo processo all'utente tramite l'utilizzo di un'informativa sulla privacy, perché il processo di aggiornamento Invia le informazioni dal computer client a un sito Web Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ad86d-135">You must clarify this process to the user through the use of a privacy statement because the update process sends information from the client computer to a Microsoft Web site.</span></span>

         

    3.  <span data-ttu-id="ad86d-136">Se possibile, l'utente rinnova il componente dall'URL, in modo automatico o seguendo istruzioni specifiche.</span><span class="sxs-lookup"><span data-stu-id="ad86d-136">If possible, the user will renew the component from the URL, either automatically or by following specific instructions.</span></span> <span data-ttu-id="ad86d-137">In alcune situazioni il componente non può essere rinnovato.</span><span class="sxs-lookup"><span data-stu-id="ad86d-137">There will be some situations in which the component cannot be renewed.</span></span>
    4.  <span data-ttu-id="ad86d-138">Provare ad accedere di nuovo al contenuto fino a quando non sono presenti altre revoche oppure il processo viene interrotto per qualche motivo.</span><span class="sxs-lookup"><span data-stu-id="ad86d-138">Try to access the content again until there are no more revocations, or the process is halted for some reason.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ad86d-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ad86d-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad86d-140">**Guida per programmatori**</span><span class="sxs-lookup"><span data-stu-id="ad86d-140">**Programming Guide**</span></span>](drm-programming-guide.md)
</dt> </dl>

 

 