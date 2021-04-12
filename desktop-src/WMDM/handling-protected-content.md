---
title: Gestione del contenuto protetto
description: Gestione del contenuto protetto
ms.assetid: f218d69e-ac80-43ba-be31-af3abf2b8de9
keywords:
- Windows Media Gestione dispositivi, certificati
- Gestione dispositivi, certificati
- applicazioni desktop, certificati
- provider di servizi, certificati
- Guida per programmatori, certificati
- certificates
- Windows Media Gestione dispositivi, Secure Content Provider (SCP)
- Gestione dispositivi, Secure Content Provider (SCP)
- applicazioni desktop, Secure Content Provider (SCP)
- provider di servizi, Secure Content Provider (SCP)
- Guida per programmatori, Secure Content Provider (SCP)
- provider di contenuti protetti (SCP)
- SCP (provider di contenuti protetto)
- Windows Media Gestione dispositivi, contenuto protetto da DRM
- Gestione dispositivi, contenuto protetto da DRM
- Guida per programmatori, contenuto protetto da DRM
- applicazioni desktop, contenuto protetto da DRM
- provider di servizi, contenuto protetto da DRM
- Contenuto protetto da DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd0fb6ab155d08ed19eb84988709695f9ed63fd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104395702"
---
# <a name="handling-protected-content"></a><span data-ttu-id="6f4f4-122">Gestione del contenuto protetto</span><span class="sxs-lookup"><span data-stu-id="6f4f4-122">Handling Protected Content</span></span>

<span data-ttu-id="6f4f4-123">Se si compila un'applicazione o un provider di servizi che utilizzerà il contenuto protetto da Windows Media Digital Rights Management (DRM), è necessario disporre di una coppia chiave/certificato rilasciata da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6f4f4-123">If you are building an application or service provider that will consume content protected by Windows Media digital rights management (DRM), you must have a key/certificate pair issued by Microsoft.</span></span> <span data-ttu-id="6f4f4-124">Per informazioni su dove ottenere questo certificato, vedere [strumenti per lo sviluppo](tools-for-development.md).</span><span class="sxs-lookup"><span data-stu-id="6f4f4-124">To learn where to get this certificate, see [Tools for Development](tools-for-development.md).</span></span> <span data-ttu-id="6f4f4-125">Se non si prevede di gestire il contenuto protetto, è possibile usare la chiave fittizia e il certificato fornito con questo SDK in un file denominato Key. c.</span><span class="sxs-lookup"><span data-stu-id="6f4f4-125">If you do not intend to handle protected content, you can use the dummy key and certificate provided with this SDK in a file named key.c.</span></span>

<span data-ttu-id="6f4f4-126">Per tutti i file protetti dalla tecnologia DRM, Windows Media Gestione dispositivi richiede la presenza di un provider di contenuti protetto (SCP) per il formato di file.</span><span class="sxs-lookup"><span data-stu-id="6f4f4-126">For any file that is protected by DRM technology, Windows Media Device Manager requires the presence of a secure content provider (SCP) for that file format.</span></span> <span data-ttu-id="6f4f4-127">Microsoft fornisce un modulo SCP per i file WMA e WMV.</span><span class="sxs-lookup"><span data-stu-id="6f4f4-127">Microsoft provides an SCP module for WMA and WMV files.</span></span> <span data-ttu-id="6f4f4-128">Se l'applicazione o il provider di servizi gestisce contenuti protetti con DRM di un altro formato, è necessario fornire il proprio modulo SCP.</span><span class="sxs-lookup"><span data-stu-id="6f4f4-128">If your application or service provider will be handling DRM-protected content of another format, you must provide your own SCP module.</span></span> <span data-ttu-id="6f4f4-129">Un modulo SCP è un oggetto COM che implementa tutte le [interfacce per i provider di contenuti protetti](interfaces-for-secure-content-providers.md).</span><span class="sxs-lookup"><span data-stu-id="6f4f4-129">An SCP module is a COM object that implements all the [interfaces for Secure Content Providers](interfaces-for-secure-content-providers.md).</span></span>

<span data-ttu-id="6f4f4-130">Un'applicazione può inviare contenuto protetto da DRM ai dispositivi compilati in Windows Media DRM 10 per i dispositivi portatili o DRM (PDDRM).</span><span class="sxs-lookup"><span data-stu-id="6f4f4-130">An application can send DRM-protected content to devices built on either Windows Media DRM 10 for Portable Devices, or Portable Device DRM (PDDRM).</span></span> <span data-ttu-id="6f4f4-131">Tuttavia, è possibile creare solo un provider di servizi per i dispositivi basati su PDDRM; non è possibile creare un provider di servizi per i dispositivi basati su Windows Media DRM 10 per i dispositivi portatili.</span><span class="sxs-lookup"><span data-stu-id="6f4f4-131">However, you can only create a service provider for devices built on PDDRM; you cannot create a service provider for devices built on Windows Media DRM 10 for Portable Devices.</span></span> <span data-ttu-id="6f4f4-132">Questi ultimi dispositivi possono usare solo il provider di servizi MTP fornito da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6f4f4-132">These latter devices can only use the Microsoft-provided MTP service provider.</span></span>

<span data-ttu-id="6f4f4-133">I dispositivi basati su PDDRM possono supportare solo le licenze per il contenuto acquistato.</span><span class="sxs-lookup"><span data-stu-id="6f4f4-133">Devices built on PDDRM can only support licenses for purchased content.</span></span> <span data-ttu-id="6f4f4-134">Le licenze con condizioni di scadenza del tempo sono supportate solo dai dispositivi basati su Windows Media DRM 10 per i dispositivi portatili, che hanno requisiti speciali, ad esempio un orologio sicuro e una individualizzazione.</span><span class="sxs-lookup"><span data-stu-id="6f4f4-134">Licenses that have time-expiration conditions are only supported by devices built on Windows Media DRM 10 for Portable Devices, which have special requirements such as a secure clock and individualization.</span></span> <span data-ttu-id="6f4f4-135">Windows Media DRM 10 per i dispositivi portatili SDK fornisce informazioni dettagliate sui requisiti dei dispositivi per supportare la tecnologia versione 10.</span><span class="sxs-lookup"><span data-stu-id="6f4f4-135">Windows Media DRM 10 for Portable Devices SDK gives details on device requirements to support version 10 technology.</span></span>

<span data-ttu-id="6f4f4-136">Prima di inviare contenuto DRM al dispositivo, un'applicazione deve verificare diverse operazioni:</span><span class="sxs-lookup"><span data-stu-id="6f4f4-136">Before sending DRM content to the device, an application should verify several things:</span></span>

-   <span data-ttu-id="6f4f4-137">Il dispositivo supporta la tecnologia DRM.</span><span class="sxs-lookup"><span data-stu-id="6f4f4-137">That the device supports DRM technology.</span></span>
-   <span data-ttu-id="6f4f4-138">Versione della tecnologia DRM supportata (versione 10 o precedente).</span><span class="sxs-lookup"><span data-stu-id="6f4f4-138">What version of DRM technology it supports (version 10 or earlier).</span></span>
-   <span data-ttu-id="6f4f4-139">Se il dispositivo è basato sulla versione 10, tutti i relativi componenti sono aggiornati, ad esempio il clock sicuro e i requisiti di individualizzazione.</span><span class="sxs-lookup"><span data-stu-id="6f4f4-139">If the device is built on version 10, that all its components are up to date (such as the secure clock and any individualization requirements).</span></span>

<span data-ttu-id="6f4f4-140">Tutte le chiamate ai metodi per rispondere a queste domande vengono effettuate dal client e gestite da Windows Media Gestione dispositivi e dal componente del provider di contenuti protetto. il provider di servizi non gestisce nessuna di queste chiamate.</span><span class="sxs-lookup"><span data-stu-id="6f4f4-140">All method calls to answer these questions are made by the client and handled by Windows Media Device Manager and the secure content provider component; the service provider does not handle any of these calls.</span></span>

<span data-ttu-id="6f4f4-141">Se il dispositivo non supporta Windows Media DRM 10 per i dispositivi portatili, potrebbe comunque essere in grado di utilizzare contenuto protetto (a seconda della licenza del contenuto e della progettazione del dispositivo), ma qualsiasi contenuto inviato avrà una licenza d'uso semplificata con diritti limitati (ad esempio, nessuna scadenza dell'ora).</span><span class="sxs-lookup"><span data-stu-id="6f4f4-141">If the device does not support Windows Media DRM 10 for Portable Devices, it might still be able to consume protected content (depending on the content license and the device design), but any content sent to it will have a simplified use license with limited rights (for example, no time expiration).</span></span>

-   <span data-ttu-id="6f4f4-142">Per esempi che illustrano il modo in cui un'applicazione verifica se un dispositivo è in grado di gestire il contenuto protetto e se deve aggiornare i componenti DRM, vedere [gestione del contenuto protetto nell'applicazione](handling-protected-content-in-the-application.md).</span><span class="sxs-lookup"><span data-stu-id="6f4f4-142">For examples demonstrating how an application verifies whether a device can handle protected content, and whether it needs to update its DRM components, see [Handling Protected Content in the Application](handling-protected-content-in-the-application.md).</span></span>
-   <span data-ttu-id="6f4f4-143">Per ulteriori informazioni sulla compilazione di un provider di servizi in grado di gestire il contenuto protetto, vedere [gestione del contenuto protetto nel provider di servizi](handling-protected-content-in-the-service-provider.md).</span><span class="sxs-lookup"><span data-stu-id="6f4f4-143">For more information about building a service provider that can handle protected content, see [Handling Protected Content in the Service Provider](handling-protected-content-in-the-service-provider.md).</span></span>

> [!Note]  
> <span data-ttu-id="6f4f4-144">Molti Windows Media Gestione dispositivi il trasferimento di file o i diritti che richiedono metodi non riusciranno (spesso con un valore **HRESULT** misterioso) quando si gestiscono file protetti con DRM con un debugger collegato.</span><span class="sxs-lookup"><span data-stu-id="6f4f4-144">Many Windows Media Device Manager file transfer or rights requesting methods will fail (often with a mysterious **HRESULT** value) when handling DRM-protected files with a debugger attached.</span></span> <span data-ttu-id="6f4f4-145">Pertanto, è necessario utilizzare modi alternativi per eseguire il debug del codice, ad esempio la registrazione degli output in un Windows Form o in un file di log.</span><span class="sxs-lookup"><span data-stu-id="6f4f4-145">Therefore, you must use alternate ways to debug your code, such as logging outputs to a Windows form or a log file.</span></span> <span data-ttu-id="6f4f4-146">Per ulteriori informazioni sulle opzioni di registrazione, vedere [Abilitazione della registrazione](enabling-logging.md).</span><span class="sxs-lookup"><span data-stu-id="6f4f4-146">For more information on logging options, see [Enabling Logging](enabling-logging.md).</span></span> <span data-ttu-id="6f4f4-147">Se si esegue un debugger sul contenuto protetto, un metodo restituirà uno dei codici di errore elencati nella sezione DRM codici di [errore](error-codes.md)o un codice di errore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="6f4f4-147">If you are running a debugger on protected content, a method will return one of the error codes listed in the DRM section [Error Codes](error-codes.md), or possibly an unknown error code.</span></span> <span data-ttu-id="6f4f4-148">Se si ottengono valori **HRESULT** misteriosi quando si esegue un debugger su contenuto o metodi protetti, la protezione DRM potrebbe essere la stessa.</span><span class="sxs-lookup"><span data-stu-id="6f4f4-148">If you get mysterious **HRESULT** values when running a debugger on protected content or methods, DRM protection might be the cause.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="6f4f4-149">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6f4f4-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f4f4-150">**Guida per programmatori**</span><span class="sxs-lookup"><span data-stu-id="6f4f4-150">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 




