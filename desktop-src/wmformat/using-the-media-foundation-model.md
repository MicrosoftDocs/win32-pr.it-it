---
title: Uso del modello di eventi Media Foundation
description: Uso del modello di eventi Media Foundation
ms.assetid: c07425dc-25d0-430b-a1f6-6373303a0cc7
keywords:
- Windows Media Format SDK, DRM Media Foundation modello di eventi
- Windows Media Format SDK, Media Foundation modello di eventi
- Windows Media Format SDK, modello di eventi DRM
- Digital Rights Management (DRM) Media Foundation modello di eventi
- DRM (Digital Rights Management), modello di eventi Media Foundation
- Digital Rights Management (DRM), modello di eventi
- DRM (Digital Rights Management), modello di eventi
- Digital Rights Management (DRM), interfaccia IWMDRMEventGenerator
- DRM (Digital Rights Management), interfaccia IWMDRMEventGenerator
- Media Foundation
- IWMDRMEventGenerator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d58d48157072cf8814ff8ac74d97a965f9e772e3
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104046378"
---
# <a name="using-the-media-foundation-event-model"></a><span data-ttu-id="c6ac5-114">Uso del modello di eventi Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c6ac5-114">Using the Media Foundation Event Model</span></span>

<span data-ttu-id="c6ac5-115">I metodi asincroni supportati dalle API estese del client Windows Media DRM usano lo stesso modello di eventi usato da Media Foundation SDK.</span><span class="sxs-lookup"><span data-stu-id="c6ac5-115">The asynchronous methods supported by the Windows Media DRM Client Extended APIs use the same event model that is used by the Media Foundation SDK.</span></span> <span data-ttu-id="c6ac5-116">Ogni oggetto che supporta i metodi asincroni implementa l'interfaccia [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md) , che può essere utilizzata per recuperare un evento quando viene completata un'operazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="c6ac5-116">Each object that supports asynchronous methods implements the [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md) interface, which can be used to retrieve an event when an asynchronous operation is complete.</span></span>

<span data-ttu-id="c6ac5-117">L'interfaccia **IWMDRMEventGenerator** eredita dall'interfaccia **IMFMediaEventGenerator** , documentata nella documentazione di Media Foundation SDK.</span><span class="sxs-lookup"><span data-stu-id="c6ac5-117">The **IWMDRMEventGenerator** interface inherits from the **IMFMediaEventGenerator** interface, which is documented in the Media Foundation SDK documentation.</span></span>

<span data-ttu-id="c6ac5-118">Il codice di esempio nell' [esempio di individualizzazione DRM](drm-individualization-example.md) usa il metodo **IMFMediaEventGenerator:: GetEvent** per recuperare gli eventi dalla coda uno alla volta.</span><span class="sxs-lookup"><span data-stu-id="c6ac5-118">The example code in the [DRM Individualization Example](drm-individualization-example.md) uses the **IMFMediaEventGenerator::GetEvent** method to retrieve events from the queue one at a time.</span></span> <span data-ttu-id="c6ac5-119">L'uso di **GetEvent** è più semplice rispetto all'uso di **IMFMediaEventGenerator:: BeginGetEvent** e **IMFMediaEventGenerator:: EndGetEvent** con un callback che rende gli esempi di codice più facili da comprendere.</span><span class="sxs-lookup"><span data-stu-id="c6ac5-119">Using **GetEvent** is more straightforward than using **IMFMediaEventGenerator::BeginGetEvent** and **IMFMediaEventGenerator::EndGetEvent** with a callback, which makes the code examples easier to understand.</span></span> <span data-ttu-id="c6ac5-120">Se si usa **GetEvent** nel codice o si implementa **IMFAsyncCallback** e si usano **BeginGetEvent** e **EndGetEvent**, la logica per gestire l'evento dopo che è stata ricevuta è la stessa.</span><span class="sxs-lookup"><span data-stu-id="c6ac5-120">Whether you use **GetEvent** in your code or implement **IMFAsyncCallback** and use **BeginGetEvent** and **EndGetEvent**, the logic to handle the event after it has been received is the same.</span></span>

<span data-ttu-id="c6ac5-121">Molti dei metodi asincroni generano eventi che contengono riferimenti a oggetti che possono essere utilizzati per ottenere informazioni più dettagliate sullo stato.</span><span class="sxs-lookup"><span data-stu-id="c6ac5-121">Several of the asynchronous methods generate events that contain references to objects that can be used to obtain more detailed status information.</span></span> <span data-ttu-id="c6ac5-122">In questi casi, l'evento generato ha un puntatore **IUnknown** come valore, su cui è possibile eseguire query per recuperare l'interfaccia di stato.</span><span class="sxs-lookup"><span data-stu-id="c6ac5-122">In these cases, the generated event has an **IUnknown** pointer as its value, which can be queried to retrieve the status interface.</span></span> <span data-ttu-id="c6ac5-123">Nell'elenco seguente sono riepilogate le relazioni tra le chiamate asincrone, gli eventi generati e altre interfacce.</span><span class="sxs-lookup"><span data-stu-id="c6ac5-123">The following list summarizes the relationships between asynchronous calls, generated events, and other interfaces.</span></span>

-   <span data-ttu-id="c6ac5-124">Il metodo [**IWMDRMLicenseManagement:: BackupLicenses**](iwmdrmlicensemanagement-backuplicenses.md) genera eventi **MEWMDRMLicenseBackupProgress** con le interfacce [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) associate.</span><span class="sxs-lookup"><span data-stu-id="c6ac5-124">The [**IWMDRMLicenseManagement::BackupLicenses**](iwmdrmlicensemanagement-backuplicenses.md) method generates **MEWMDRMLicenseBackupProgress** events with associated [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) interfaces.</span></span>
-   <span data-ttu-id="c6ac5-125">Il metodo [**IWMDRMLicenseManagement:: RestoreLicenses**](iwmdrmlicensemanagement-restorelicenses.md) genera eventi **MEWMDRMLicenseRestoreProgress** con le interfacce [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) associate.</span><span class="sxs-lookup"><span data-stu-id="c6ac5-125">The [**IWMDRMLicenseManagement::RestoreLicenses**](iwmdrmlicensemanagement-restorelicenses.md) method generates **MEWMDRMLicenseRestoreProgress** events with associated [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) interfaces.</span></span>
-   <span data-ttu-id="c6ac5-126">Il metodo [**IWMDRMSecurity::P erformsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md) , quando viene usato per eseguire l'individualizzazione, genera eventi **MEWMDRMIndividualizationProgress** con le interfacce [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md) associate.</span><span class="sxs-lookup"><span data-stu-id="c6ac5-126">The [**IWMDRMSecurity::PerformSecurityUpdate**](iwmdrmsecurity-performsecurityupdate.md) method, when used to perform individualization, generates **MEWMDRMIndividualizationProgress** events with associated [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md) interfaces.</span></span>
-   <span data-ttu-id="c6ac5-127">Il metodo [**IWMDRMLicenseManagement:: AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) , quando viene usato per preparare i dati per l'acquisizione di una licenza non invisibile all'utente, genera un evento **MEWMDRMLicenseAcquisitionCompleted** con un'interfaccia [**IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md) associata.</span><span class="sxs-lookup"><span data-stu-id="c6ac5-127">The [**IWMDRMLicenseManagement::AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) method, when used to prepare data for non-silent license acquisition, generates an **MEWMDRMLicenseAcquisitionCompleted** event with an associated [**IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md) interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c6ac5-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c6ac5-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6ac5-129">**Esempio di individualizzazione DRM**</span><span class="sxs-lookup"><span data-stu-id="c6ac5-129">**DRM Individualization Example**</span></span>](drm-individualization-example.md)
</dt> <dt>

[<span data-ttu-id="c6ac5-130">**Per iniziare**</span><span class="sxs-lookup"><span data-stu-id="c6ac5-130">**Getting Started**</span></span>](drm-getting-started.md)
</dt> <dt>

[<span data-ttu-id="c6ac5-131">Documentazione di Media Foundation SDK</span><span class="sxs-lookup"><span data-stu-id="c6ac5-131">Media Foundation SDK Documentation</span></span>](https://www.microsoft.com/?ref=go)
</dt> </dl>

 

 




