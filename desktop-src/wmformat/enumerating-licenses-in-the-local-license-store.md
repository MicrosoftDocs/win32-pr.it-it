---
title: Enumerazione delle licenze nell'archivio licenze locale
description: Enumerazione delle licenze nell'archivio licenze locale
ms.assetid: 1f380b9e-85e4-4190-a809-65dfd4658b7c
keywords:
- Windows Media Format SDK, enumerazione delle licenze
- Windows Media Format SDK, licenze
- Windows Media Format SDK, archivio licenze locale
- Digital Rights Management (DRM), enumerazione delle licenze
- DRM (Digital Rights Management), enumerazione delle licenze
- Digital Rights Management (DRM), licenze
- DRM (Digital Rights Management), licenze
- Digital Rights Management (DRM), archivio licenze locale
- DRM (Digital Rights Management), archivio licenze locale
- API estese del client DRM, enumerazione delle licenze
- API estese client, enumerazione delle licenze
- API estese del client DRM, licenze
- API estese client, licenze
- API estese del client DRM, archivio licenze locale
- API estese client, archivio licenze locale
- licenze, enumerazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29b1384e08a6789fedca9704f36ad8da1e31b4ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395619"
---
# <a name="enumerating-licenses-in-the-local-license-store"></a><span data-ttu-id="1fe89-119">Enumerazione delle licenze nell'archivio licenze locale</span><span class="sxs-lookup"><span data-stu-id="1fe89-119">Enumerating Licenses in the Local License Store</span></span>

<span data-ttu-id="1fe89-120">L'enumerazione è un processo che consente di ottenere informazioni sulle licenze nell'archivio licenze locale, eseguendone un'istruzione alla volta.</span><span class="sxs-lookup"><span data-stu-id="1fe89-120">Enumeration is a process of getting information about the licenses in the local license store, by stepping through them one by one.</span></span> <span data-ttu-id="1fe89-121">È possibile creare un'enumerazione delle licenze chiamando [**IWMDRMLicenseManagement:: CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md).</span><span class="sxs-lookup"><span data-stu-id="1fe89-121">You can create a license enumeration by calling the [**IWMDRMLicenseManagement::CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md).</span></span>

<span data-ttu-id="1fe89-122">Il motivo più comune per l'enumerazione delle licenze nell'archivio è quello di trovare una licenza particolare per la decrittografia di alcuni contenuti.</span><span class="sxs-lookup"><span data-stu-id="1fe89-122">The most common reason for enumerating through licenses in the store is to find a particular license for decryption of some content.</span></span>

<span data-ttu-id="1fe89-123">L'interfaccia [**IWMDRMLicense**](iwmdrmlicense.md) funge da portale per i singoli risultati della licenza e come enumeratore.</span><span class="sxs-lookup"><span data-stu-id="1fe89-123">The [**IWMDRMLicense**](iwmdrmlicense.md) interface serves as both a portal to the individual license results and as the enumerator.</span></span> <span data-ttu-id="1fe89-124">Quando viene creata l'enumerazione delle licenze, la prima licenza nell'elenco viene caricata nell'interfaccia **IWMDRMLicense** .</span><span class="sxs-lookup"><span data-stu-id="1fe89-124">When the license enumeration is created, the first license in the list is loaded into the **IWMDRMLicense** interface.</span></span> <span data-ttu-id="1fe89-125">La maggior parte dei metodi di **IWMDRMLicense** consente di ottenere informazioni sulla licenza o creare oggetti per crittografare o decrittografare il contenuto in base alla licenza.</span><span class="sxs-lookup"><span data-stu-id="1fe89-125">Most of the methods of **IWMDRMLicense** enable you to get information about the license or to create objects to encrypt or decrypt content based on the license.</span></span> <span data-ttu-id="1fe89-126">Esistono tuttavia due metodi che controllano l'enumerazione: [**GetNext**](iwmdrmlicense-getnext.md) e [**ResetEnumeration**](iwmdrmlicense-resetenumeration.md).</span><span class="sxs-lookup"><span data-stu-id="1fe89-126">However, there are two methods that control the enumeration: [**GetNext**](iwmdrmlicense-getnext.md) and [**ResetEnumeration**](iwmdrmlicense-resetenumeration.md).</span></span> <span data-ttu-id="1fe89-127">**GetNext** carica la licenza successiva nell'elenco nell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="1fe89-127">**GetNext** loads the next license in the list into the interface.</span></span> <span data-ttu-id="1fe89-128">**ResetEnumeration** restituisce l'enumerazione allo stato in cui si trovava al momento della creazione.</span><span class="sxs-lookup"><span data-stu-id="1fe89-128">**ResetEnumeration** returns the enumeration to the state it was in when it was first created.</span></span> <span data-ttu-id="1fe89-129">Quando l'enumerazione viene reimpostata, la prima licenza nell'elenco viene ricaricata nell'interfaccia **IWMDRMLicense** .</span><span class="sxs-lookup"><span data-stu-id="1fe89-129">When the enumeration is reset, the first license in the list is loaded back into the **IWMDRMLicense** interface.</span></span>

<span data-ttu-id="1fe89-130">Una volta raggiunta l'ultima licenza nell'elenco, la chiamata successiva a **GetNext** restituisce l'errore \_ non \_ più \_ elementi.</span><span class="sxs-lookup"><span data-stu-id="1fe89-130">When you have reached the last license in the list, the next call to **GetNext** returns ERROR\_NO\_MORE\_ITEMS.</span></span>

<span data-ttu-id="1fe89-131">Se l'applicazione esegue un'azione con il contenuto coperto da DRM, è necessario controllare le licenze nell'archivio licenze locale per i diritti e per altri fattori di limitazione, ad esempio i livelli di protezione dell'output (OPLs).</span><span class="sxs-lookup"><span data-stu-id="1fe89-131">If your application performs an action with the content that is covered by DRM, you should check the licenses in the local license store for the rights and for other limiting factors, such as output protection levels (OPLs).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1fe89-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1fe89-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1fe89-133">**Recupero di informazioni dalle licenze nell'archivio licenze locale**</span><span class="sxs-lookup"><span data-stu-id="1fe89-133">**Getting Information from Licenses in the Local License Store**</span></span>](getting-information-from-licenses-in-the-local-license-store.md)
</dt> </dl>

 

 




