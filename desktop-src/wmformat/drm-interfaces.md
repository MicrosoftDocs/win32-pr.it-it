---
title: Interfacce client DRM di Microsoft Windows Media
description: Interfacce client DRM di Microsoft Windows Media
ms.assetid: 27bbc33f-8102-4db2-bbc6-1a1da92bac80
keywords:
- Windows Media Format SDK, interfacce
- Digital Rights Management (DRM), interfacce
- DRM (Digital Rights Management), interfacce
- API estese del client DRM, interfacce
- API estese client, interfacce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b4e259ef5b8ef410db072a7f942d139f682bc90
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104400085"
---
# <a name="microsoft-windows-media-drm-client-interfaces"></a><span data-ttu-id="21a7a-108">Interfacce client DRM di Microsoft Windows Media</span><span class="sxs-lookup"><span data-stu-id="21a7a-108">Microsoft Windows Media DRM Client Interfaces</span></span>

<span data-ttu-id="21a7a-109">Nella tabella seguente vengono descritte le interfacce supportate dalle API client DRM di Windows Media.</span><span class="sxs-lookup"><span data-stu-id="21a7a-109">The following table describes the interfaces supported by the Windows Media DRM Client APIs.</span></span>



| <span data-ttu-id="21a7a-110">Interfaccia</span><span class="sxs-lookup"><span data-stu-id="21a7a-110">Interface</span></span>                                                                    | <span data-ttu-id="21a7a-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="21a7a-111">Description</span></span>                                                                                                     |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="21a7a-112">**IDRMStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="21a7a-112">**IDRMStatusCallback**</span></span>](idrmstatuscallback.md)                             | <span data-ttu-id="21a7a-113">Fornisce la definizione per un callback di stato che è possibile implementare per gestire le operazioni DRM asincrone.</span><span class="sxs-lookup"><span data-stu-id="21a7a-113">Provides the definition for a status callback that you can implement to handle asynchronous DRM operations.</span></span>     |
| [<span data-ttu-id="21a7a-114">**IWMDRMDecrypt**</span><span class="sxs-lookup"><span data-stu-id="21a7a-114">**IWMDRMDecrypt**</span></span>](iwmdrmdecrypt.md)                                       | <span data-ttu-id="21a7a-115">Fornisce un metodo per la decrittografia del contenuto.</span><span class="sxs-lookup"><span data-stu-id="21a7a-115">Provides a method for decrypting content.</span></span>                                                                       |
| [<span data-ttu-id="21a7a-116">**IWMDRMEncrypt**</span><span class="sxs-lookup"><span data-stu-id="21a7a-116">**IWMDRMEncrypt**</span></span>](iwmdrmencrypt.md)                                       | <span data-ttu-id="21a7a-117">Fornisce un metodo per la crittografia dei dati sul posto.</span><span class="sxs-lookup"><span data-stu-id="21a7a-117">Provides a method for encrypting data in place.</span></span>                                                                 |
| [<span data-ttu-id="21a7a-118">**IWMDRMEncryptScatter**</span><span class="sxs-lookup"><span data-stu-id="21a7a-118">**IWMDRMEncryptScatter**</span></span>](iwmdrmencryptscatter.md)                         | <span data-ttu-id="21a7a-119">Crittografa i dati da blocchi non contigui.</span><span class="sxs-lookup"><span data-stu-id="21a7a-119">Encrypts data from non-contiguous blocks.</span></span>                                                                       |
| [<span data-ttu-id="21a7a-120">**IWMDRMEventGenerator**</span><span class="sxs-lookup"><span data-stu-id="21a7a-120">**IWMDRMEventGenerator**</span></span>](iwmdrmeventgenerator.md)                         | <span data-ttu-id="21a7a-121">Estensione dell'interfaccia **IMFMediaEventGenerator** che fornisce un metodo per annullare le operazioni asincrone.</span><span class="sxs-lookup"><span data-stu-id="21a7a-121">Extension of the **IMFMediaEventGenerator** interface that provides a method to cancel asynchronous operations.</span></span> |
| [<span data-ttu-id="21a7a-122">**IWMDRMIndividualizationStatus**</span><span class="sxs-lookup"><span data-stu-id="21a7a-122">**IWMDRMIndividualizationStatus**</span></span>](iwmdrmindividualizationstatus.md)       | <span data-ttu-id="21a7a-123">Consente il recupero delle informazioni sullo stato avanzate sullo stato di individualizzazione.</span><span class="sxs-lookup"><span data-stu-id="21a7a-123">Enables retrieval of advanced status information about the progress of individualization.</span></span>                       |
| [<span data-ttu-id="21a7a-124">**IWMDRMLicense**</span><span class="sxs-lookup"><span data-stu-id="21a7a-124">**IWMDRMLicense**</span></span>](iwmdrmlicense.md)                                       | <span data-ttu-id="21a7a-125">Rappresenta una o più licenze nell'archivio licenze locale.</span><span class="sxs-lookup"><span data-stu-id="21a7a-125">Represents one or more licenses in the local license store.</span></span>                                                     |
| [<span data-ttu-id="21a7a-126">**IWMDRMLicenseBackupRestoreStatus**</span><span class="sxs-lookup"><span data-stu-id="21a7a-126">**IWMDRMLicenseBackupRestoreStatus**</span></span>](iwmdrmlicensebackuprestorestatus.md) | <span data-ttu-id="21a7a-127">Consente il recupero di informazioni dettagliate sullo stato di un'operazione di backup o ripristino delle licenze.</span><span class="sxs-lookup"><span data-stu-id="21a7a-127">Enables retrieval of detailed status information about a license backup or restore operation.</span></span>                   |
| [<span data-ttu-id="21a7a-128">**IWMDRMLicenseManagement**</span><span class="sxs-lookup"><span data-stu-id="21a7a-128">**IWMDRMLicenseManagement**</span></span>](iwmdrmlicensemanagement.md)                   | <span data-ttu-id="21a7a-129">Abilita le operazioni di gestione per l'archivio licenze locale.</span><span class="sxs-lookup"><span data-stu-id="21a7a-129">Enables management operations for the local license store.</span></span>                                                      |
| [<span data-ttu-id="21a7a-130">**IWMDRMLicenseManagement**</span><span class="sxs-lookup"><span data-stu-id="21a7a-130">**IWMDRMLicenseManagement**</span></span>](iwmdrmlicensemanagement.md)                   | <span data-ttu-id="21a7a-131">Fornisce opzioni di gestione aggiuntive per l'archivio licenze locale.</span><span class="sxs-lookup"><span data-stu-id="21a7a-131">Provides additional management options for the local license store.</span></span>                                             |
| [<span data-ttu-id="21a7a-132">**IWMDRMLicenseQuery**</span><span class="sxs-lookup"><span data-stu-id="21a7a-132">**IWMDRMLicenseQuery**</span></span>](iwmdrmlicensequery.md)                             | <span data-ttu-id="21a7a-133">Consente alle applicazioni di eseguire query sui diritti e sullo stato di licenza per un file protetto.</span><span class="sxs-lookup"><span data-stu-id="21a7a-133">Enables applications to query the rights and license state for a protected file.</span></span>                                |
| [<span data-ttu-id="21a7a-134">**IWMDRMNetReceiver**</span><span class="sxs-lookup"><span data-stu-id="21a7a-134">**IWMDRMNetReceiver**</span></span>](iwmdrmnetreceiver.md)                               | <span data-ttu-id="21a7a-135">Fornisce i metodi necessari per creare un'applicazione del ricevitore di dispositivi di rete DRM di Microsoft Windows Media.</span><span class="sxs-lookup"><span data-stu-id="21a7a-135">Provides methods needed create a Microsoft Windows Media DRM for Network Devices receiver application.</span></span>          |
| [<span data-ttu-id="21a7a-136">**IWMDRMNetTransmitter**</span><span class="sxs-lookup"><span data-stu-id="21a7a-136">**IWMDRMNetTransmitter**</span></span>](iwmdrmnettransmitter.md)                         | <span data-ttu-id="21a7a-137">Fornisce i metodi necessari per creare un'applicazione trasmittente Microsoft Windows Media DRM per dispositivi di rete.</span><span class="sxs-lookup"><span data-stu-id="21a7a-137">Provides methods needed create a Microsoft Windows Media DRM for Network Devices transmitter application.</span></span>       |
| [<span data-ttu-id="21a7a-138">**IWMDRMNonSilentLicenseAquisition**</span><span class="sxs-lookup"><span data-stu-id="21a7a-138">**IWMDRMNonSilentLicenseAquisition**</span></span>](iwmdrmnonsilentlicenseaquisition.md) | <span data-ttu-id="21a7a-139">Fornisce metodi che consentono l'acquisizione di licenze con l'intervento dell'utente.</span><span class="sxs-lookup"><span data-stu-id="21a7a-139">Provides methods that enable license acquisition with user intervention.</span></span>                                        |
| [<span data-ttu-id="21a7a-140">**IWMDRMProvider**</span><span class="sxs-lookup"><span data-stu-id="21a7a-140">**IWMDRMProvider**</span></span>](iwmdrmprovider.md)                                     | <span data-ttu-id="21a7a-141">Crea gli altri oggetti delle API estese del client DRM di Microsoft Windows Media.</span><span class="sxs-lookup"><span data-stu-id="21a7a-141">Creates the other objects of the Microsoft Windows Media DRM Client Extended APIs.</span></span>                              |
| [<span data-ttu-id="21a7a-142">**IWMDRMSecurity**</span><span class="sxs-lookup"><span data-stu-id="21a7a-142">**IWMDRMSecurity**</span></span>](iwmdrmsecurity.md)                                     | <span data-ttu-id="21a7a-143">Gestisce vari processi correlati alla sicurezza per il computer client e il sottosistema DRM.</span><span class="sxs-lookup"><span data-stu-id="21a7a-143">Manages various security-related processes for the client computer and DRM subsystem.</span></span>                           |
| [<span data-ttu-id="21a7a-144">**IWMDRMSecurity**</span><span class="sxs-lookup"><span data-stu-id="21a7a-144">**IWMDRMSecurity**</span></span>](iwmdrmsecurity.md)                                     | <span data-ttu-id="21a7a-145">Gestisce la revoca e il rinnovo dei componenti.</span><span class="sxs-lookup"><span data-stu-id="21a7a-145">Manages component revocation and renewal.</span></span>                                                                       |
| [<span data-ttu-id="21a7a-146">**IWMSecureBuffer**</span><span class="sxs-lookup"><span data-stu-id="21a7a-146">**IWMSecureBuffer**</span></span>](iwmsecurebuffer.md)                                   | <span data-ttu-id="21a7a-147">Consente la crittografia e la decrittografia dei buffer.</span><span class="sxs-lookup"><span data-stu-id="21a7a-147">Enables encryption and decryption of buffers.</span></span>                                                                   |



 

## <a name="related-topics"></a><span data-ttu-id="21a7a-148">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="21a7a-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21a7a-149">**Guida di riferimento alla programmazione**</span><span class="sxs-lookup"><span data-stu-id="21a7a-149">**Programming Reference**</span></span>](drm-programming-reference.md)
</dt> </dl>

 

 




