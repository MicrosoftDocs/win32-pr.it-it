---
title: Strumenti per lo sviluppo
description: Strumenti per lo sviluppo
ms.assetid: 7932f599-a073-4fc8-82da-c0e7001c1809
keywords:
- Windows Media Gestione dispositivi, strumenti di sviluppo
- Gestione dispositivi, strumenti di sviluppo
- Windows Media Gestione dispositivi, certificati
- Gestione dispositivi, certificati
- Windows Media Gestione dispositivi, chiavi
- Gestione dispositivi, chiavi
- Windows Media Gestione dispositivi, librerie
- Gestione dispositivi, librerie
- Windows Media Gestione dispositivi, Software Development Kit (SDK)
- Gestione dispositivi, Software Development Kit (SDK)
- Windows Media Gestione dispositivi SDK
- SDK di Gestione dispositivi
- Windows Media Player SDK
- Windows Media Format SDK
- Windows Media Rights Manager SDK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d45a3e419b87c56a447ad2412234a80432b1598e
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "106300620"
---
# <a name="tools-for-development"></a><span data-ttu-id="0106b-118">Strumenti per lo sviluppo</span><span class="sxs-lookup"><span data-stu-id="0106b-118">Tools for Development</span></span>

<span data-ttu-id="0106b-119">In questa sezione vengono descritti i vari certificati e chiavi, le librerie e gli SDK necessari per programmare mediante Windows Media Gestione dispositivi SDK.</span><span class="sxs-lookup"><span data-stu-id="0106b-119">This section describes the various certificates and keys, libraries, and SDKs you will need to program using the Windows Media Device Manager SDK.</span></span>

<span data-ttu-id="0106b-120">Certificati e chiavi</span><span class="sxs-lookup"><span data-stu-id="0106b-120">Certificates and Keys</span></span>

<span data-ttu-id="0106b-121">Windows Media Gestione dispositivi SDK viene fornito con una coppia chiave/certificato di test (nel file Key. c) che può essere usata da un'applicazione o da un provider di servizi per usare i metodi di Windows Media Gestione dispositivi su contenuto non protetto.</span><span class="sxs-lookup"><span data-stu-id="0106b-121">The Windows Media Device Manager SDK ships with a test key/certificate pair (in the key.c file) that can be used by an application or a service provider to use Windows Media Device Manager methods on unprotected content.</span></span> <span data-ttu-id="0106b-122">Questa coppia chiave/certificato consente all'applicazione o al provider di servizi di utilizzare la maggior parte delle funzionalità Windows Media Gestione dispositivi.</span><span class="sxs-lookup"><span data-stu-id="0106b-122">This key/certificate pair allows the application or service provider to use most of the Windows Media Device Manager functionality.</span></span>

<span data-ttu-id="0106b-123">Tuttavia, per sviluppare un'applicazione o un provider di servizi in grado di gestire contenuti protetti da DRM, è necessario richiedere uno o più certificati (ognuno con una chiave) dalla [pagina Windows Media Licensing](https://www.microsoft.com/licensing/default).</span><span class="sxs-lookup"><span data-stu-id="0106b-123">However, to develop an application or service provider that can handle DRM-protected content, you must request one or more certificates (each with a key) from the [Windows Media Licensing Page](https://www.microsoft.com/licensing/default).</span></span> <span data-ttu-id="0106b-124">I certificati sono necessari per le applicazioni o gli oggetti seguenti:</span><span class="sxs-lookup"><span data-stu-id="0106b-124">Certificates are required for the following applications or objects:</span></span>

-   <span data-ttu-id="0106b-125">I provider di servizi che gestiscono il contenuto protetto con DRM richiedono un certificato del provider di servizi Windows Media Gestione dispositivi (e una chiave)</span><span class="sxs-lookup"><span data-stu-id="0106b-125">Service Providers that handle DRM-protected content require a Windows Media Device Manager Service Provider Certificate (and key)</span></span>
-   <span data-ttu-id="0106b-126">Le applicazioni che trasferiscono contenuti protetti con DRM richiedono un certificato di trasferimento Gestione dispositivi Windows Media (e una chiave)</span><span class="sxs-lookup"><span data-stu-id="0106b-126">Applications that transfer DRM-protected content require a Windows Media Device Manager Transfer Certificate (and key)</span></span>
-   <span data-ttu-id="0106b-127">Le applicazioni che svolgono contenuti protetti con DRM richiedono un certificato DRM (e una chiave).</span><span class="sxs-lookup"><span data-stu-id="0106b-127">Applications that play DRM-protected content require a DRM Certificate (and key).</span></span>
-   <span data-ttu-id="0106b-128">I componenti di misurazione delle licenze richiedono un certificato di misurazione.</span><span class="sxs-lookup"><span data-stu-id="0106b-128">License metering components require a metering certificate.</span></span> <span data-ttu-id="0106b-129">Questa operazione viene fornita da un servizio di controllo delle licenze creato in Windows Media Rights Manager SDK, che può essere richiesto nella pagina Windows Media Licensing.</span><span class="sxs-lookup"><span data-stu-id="0106b-129">This is provided by a license metering service built on the Windows Media Rights Manager SDK, which can be requested on the Windows Media Licensing Page.</span></span>

<span data-ttu-id="0106b-130">Librerie e intestazioni</span><span class="sxs-lookup"><span data-stu-id="0106b-130">Libraries and Headers</span></span>

<span data-ttu-id="0106b-131">Oltre alle librerie e alle intestazioni indicate nei [file di intestazione e di libreria necessari per un'applicazione](required-library-and-header-files-for-an-application.md) o le [librerie e le intestazioni obbligatorie per un provider di servizi](required-libraries-and-headers-for-a-service-provider.md), qualsiasi applicazione o plug-in precedentemente collegato a WMDRMSDK. lib per chiamare le funzioni di Windows Media Format SDK dovrebbe ora eseguire il collegamento a WMDRMSDKStub. lib.</span><span class="sxs-lookup"><span data-stu-id="0106b-131">In addition to the libraries and headers mentioned in [Required Library and Header Files for an Application](required-library-and-header-files-for-an-application.md) or [Required Libraries and Headers for a Service Provider](required-libraries-and-headers-for-a-service-provider.md), any application or plug-in that formerly linked to WMDRMSDK.lib to call Windows Media Format SDK functions should now instead link to WMDRMSDKStub.Lib.</span></span> <span data-ttu-id="0106b-132">Questo file di libreria viene utilizzato per accedere ai file protetti da DRM.</span><span class="sxs-lookup"><span data-stu-id="0106b-132">This library file is used to access DRM-protected files.</span></span> <span data-ttu-id="0106b-133">È possibile richiedere questa libreria anche dalla pagina Windows Media Licensing.</span><span class="sxs-lookup"><span data-stu-id="0106b-133">You can request this library from the Windows Media Licensing Page as well.</span></span>

<span data-ttu-id="0106b-134">SDK correlati</span><span class="sxs-lookup"><span data-stu-id="0106b-134">Related SDKs</span></span>

<span data-ttu-id="0106b-135">Gli SDK Microsoft seguenti forniscono elementi che potrebbero essere necessari per la progettazione di soluzioni per i dispositivi multimediali portatili.</span><span class="sxs-lookup"><span data-stu-id="0106b-135">The following Microsoft SDKs provide elements you may need in designing solutions for portable media devices.</span></span>



| <span data-ttu-id="0106b-136">SDK obbligatorio</span><span class="sxs-lookup"><span data-stu-id="0106b-136">SDK Required</span></span>                     | <span data-ttu-id="0106b-137">Obbligatorio per...</span><span class="sxs-lookup"><span data-stu-id="0106b-137">Required for...</span></span>                                                                                                                                                                                                                       |
|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0106b-138">Windows Media Gestione dispositivi SDK</span><span class="sxs-lookup"><span data-stu-id="0106b-138">Windows Media Device Manager SDK</span></span> | <span data-ttu-id="0106b-139">Applicazioni desktop media player che comunicano con dispositivi portatili</span><span class="sxs-lookup"><span data-stu-id="0106b-139">Desktop media player applications that communicate with portable devices</span></span><br/> <span data-ttu-id="0106b-140">Applicazioni desktop che possono scambiare file o informazioni con i dispositivi portatili</span><span class="sxs-lookup"><span data-stu-id="0106b-140">Desktop applications that can exchange files or information with portable devices</span></span><br/> <span data-ttu-id="0106b-141">Oggetti COM di controllo Media Player di Windows</span><span class="sxs-lookup"><span data-stu-id="0106b-141">Windows Media Player metering COM objects</span></span><br/> |
| <span data-ttu-id="0106b-142">Windows Media Player SDK</span><span class="sxs-lookup"><span data-stu-id="0106b-142">Windows Media Player SDK</span></span>         | <span data-ttu-id="0106b-143">Plug-in di Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="0106b-143">Windows Media Player plug-ins</span></span><br/> <span data-ttu-id="0106b-144">Oggetti COM di controllo Media Player di Windows</span><span class="sxs-lookup"><span data-stu-id="0106b-144">Windows Media Player metering COM objects</span></span><br/> <span data-ttu-id="0106b-145">Interfacce di Media Player Windows</span><span class="sxs-lookup"><span data-stu-id="0106b-145">Windows Media Player skins</span></span><br/>                                                                                                   |
| <span data-ttu-id="0106b-146">Windows Media Format SDK</span><span class="sxs-lookup"><span data-stu-id="0106b-146">Windows Media Format SDK</span></span>         | <span data-ttu-id="0106b-147">Lettori audio o video in grado di creare o riprodurre file (in particolare file ASF)</span><span class="sxs-lookup"><span data-stu-id="0106b-147">Audio or video players that can create or play files (particularly ASF files)</span></span><br/> <span data-ttu-id="0106b-148">Applicazioni di modifica audio o video</span><span class="sxs-lookup"><span data-stu-id="0106b-148">Audio or video editing applications</span></span><br/>                                                                                               |
| <span data-ttu-id="0106b-149">Windows Media Rights Manager SDK</span><span class="sxs-lookup"><span data-stu-id="0106b-149">Windows Media Rights Manager SDK</span></span> | <span data-ttu-id="0106b-150">Applicazioni o plug-in che controllano la riproduzione del contatore sul desktop o sul dispositivo.</span><span class="sxs-lookup"><span data-stu-id="0106b-150">Applications or plug-ins that meter play counts on the desktop or device.</span></span>                                                                                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="0106b-151">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0106b-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0106b-152">**Introduzione**</span><span class="sxs-lookup"><span data-stu-id="0106b-152">**Getting Started**</span></span>](getting-started.md)
</dt> </dl>

 

 





