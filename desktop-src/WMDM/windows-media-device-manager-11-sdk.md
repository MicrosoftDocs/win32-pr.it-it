---
title: Windows Media Gestione dispositivi 11 SDK
description: Windows Media Gestione dispositivi 11 SDK
ms.assetid: 9c0c9a96-1335-4ae2-9393-bfab0dfe24c6
keywords:
- Windows Media Gestione dispositivi, informazioni
- Gestione dispositivi, informazioni
- Protocollo MTP (Media Transfer Protocol)
- MTP (Media Transfer Protocol)
- Classe di archiviazione di massa (MSC)
- MSC (classe di archiviazione di massa)
- Windows Media Gestione dispositivi, applicazioni desktop
- Gestione dispositivi, applicazioni desktop
- applicazioni desktop, informazioni
- Windows Media Gestione dispositivi, provider di servizi
- Gestione dispositivi, provider di servizi
- provider di servizi, informazioni
- Windows Media Gestione dispositivi, plug-in
- Gestione dispositivi, plug-Insp
- plug-in, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2b167e8244fb6f03a584dfb71255eabfa359c8e
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/09/2020
ms.locfileid: "104399855"
---
# <a name="windows-media-device-manager-11-sdk"></a><span data-ttu-id="f42fc-118">Windows Media Gestione dispositivi 11 SDK</span><span class="sxs-lookup"><span data-stu-id="f42fc-118">Windows Media Device Manager 11 SDK</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f42fc-119">Le API di Windows Media Gestione dispositivi sono ora incluse nel Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="f42fc-119">The Windows Media Device Manager APIs are now included in the Windows SDK.</span></span> <span data-ttu-id="f42fc-120">Non sono necessari download aggiuntivi dell'SDK.</span><span class="sxs-lookup"><span data-stu-id="f42fc-120">No additional SDK downloads are required.</span></span>

 

<span data-ttu-id="f42fc-121">Microsoft Windows Media Gestione dispositivi Software Development Kit (SDK) consente di creare applicazioni desktop e componenti in grado di comunicare con i dispositivi portatili connessi.</span><span class="sxs-lookup"><span data-stu-id="f42fc-121">The Microsoft Windows Media Device Manager Software Development Kit (SDK) enables you to build desktop applications and components that can communicate with connected portable devices.</span></span> <span data-ttu-id="f42fc-122">Windows Media Gestione dispositivi consente all'applicazione o al componente di enumerare, esplorare ed effettuare lo scambio di file con un dispositivo, eseguire query per i metadati e richiedere informazioni sui conteggi di riproduzione.</span><span class="sxs-lookup"><span data-stu-id="f42fc-122">Windows Media Device Manager enables your application or component to enumerate, explore, and exchange files with a device, query for metadata, and request play count information.</span></span> <span data-ttu-id="f42fc-123">Le applicazioni o i componenti basati su Windows Media Gestione dispositivi hanno un'API coerente per la comunicazione con un'ampia gamma di dispositivi, tra cui il protocollo MTP (Media Transfer Protocol), la classe di archiviazione di massa (MSC), RAPI e altri dispositivi basati sulle versioni più recenti e precedenti della tecnologia Windows Media.</span><span class="sxs-lookup"><span data-stu-id="f42fc-123">Applications or components built on Windows Media Device Manager have a consistent API for communicating with a wide range of devices including Media Transfer Protocol (MTP), Mass Storage Class (MSC), RAPI, and other devices built on both the latest and previous versions of Windows Media technology.</span></span>

<span data-ttu-id="f42fc-124">È possibile compilare gli elementi seguenti utilizzando Windows Media Gestione dispositivi SDK:</span><span class="sxs-lookup"><span data-stu-id="f42fc-124">You can build the following items using the Windows Media Device Manager SDK:</span></span>

-   <span data-ttu-id="f42fc-125">Applicazioni desktop, ad esempio lettori multimediali personalizzati.</span><span class="sxs-lookup"><span data-stu-id="f42fc-125">Desktop applications, such as custom media players.</span></span> <span data-ttu-id="f42fc-126">Tutte le comunicazioni tra un'applicazione e un dispositivo portatile devono passare attraverso Windows Media Gestione dispositivi, che funge da broker tra l'applicazione, il sistema Microsoft Digital Rights Management e il provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="f42fc-126">All communication between an application and a portable device must go through Windows Media Device Manager, which acts as a broker between the application, the Microsoft digital rights management system, and the service provider.</span></span>
-   <span data-ttu-id="f42fc-127">Provider di servizi, che fungono da collegamento di comunicazione tra un dispositivo personalizzato e un'applicazione desktop.</span><span class="sxs-lookup"><span data-stu-id="f42fc-127">Service providers, which act as the communication link between a custom device and a desktop application.</span></span> <span data-ttu-id="f42fc-128">Sebbene Microsoft fornisca diversi provider di servizi in grado di comunicare con la maggior parte dei dispositivi, è possibile creare un provider di servizi personalizzato per personalizzare la comunicazione tra un dispositivo e un'applicazione desktop.</span><span class="sxs-lookup"><span data-stu-id="f42fc-128">Although Microsoft provides a number of service providers that can communicate with most devices out of the box, you can build a custom service provider to customize the communication between a device and a desktop application.</span></span>
-   <span data-ttu-id="f42fc-129">Plug-in, che possono eseguire attività quali la richiesta e la registrazione dei conteggi dei Play nei dispositivi.</span><span class="sxs-lookup"><span data-stu-id="f42fc-129">Plug-ins, which can perform tasks such as requesting and logging play counts on devices.</span></span> <span data-ttu-id="f42fc-130">Questi plug-in possono essere collegati ad altre applicazioni desktop, ad esempio Windows Media Player per inviare informazioni ai provider di contenuti per gestire i pagamenti di Royalty agli artisti.</span><span class="sxs-lookup"><span data-stu-id="f42fc-130">These plug-ins can be attached to other desktop applications, such as the Windows Media Player to send information to content providers to handle royalty payments to artists.</span></span>

<span data-ttu-id="f42fc-131">Per scaricare Windows Media Gestione dispositivi SDK, vedere [la pagina di download di Windows Media](https://msdn.microsoft.com/windows/desktop/aa904949) sul sito Web MSDN.</span><span class="sxs-lookup"><span data-stu-id="f42fc-131">To download the Windows Media Device Manager SDK, see [the Windows Media Download page](https://msdn.microsoft.com/windows/desktop/aa904949) on the MSDN Web site.</span></span>

<span data-ttu-id="f42fc-132">Questo SDK è un componente di Microsoft Windows Media Software Development Kit.</span><span class="sxs-lookup"><span data-stu-id="f42fc-132">This SDK is a component of the Microsoft Windows Media Software Development Kit.</span></span> <span data-ttu-id="f42fc-133">Altri componenti includono Windows Media Format SDK, Windows Media Services SDK, Windows Media Encoder SDK, Windows Media Rights Manager SDK e Windows Media Player SDK.</span><span class="sxs-lookup"><span data-stu-id="f42fc-133">Other components include the Windows Media Format SDK, the Windows Media Services SDK, the Windows Media Encoder SDK, the Windows Media Rights Manager SDK, and the Windows Media Player SDK.</span></span>

<span data-ttu-id="f42fc-134">Questa documentazione include le sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="f42fc-134">This documentation includes the following sections.</span></span>



| <span data-ttu-id="f42fc-135">Sezione</span><span class="sxs-lookup"><span data-stu-id="f42fc-135">Section</span></span>                                            | <span data-ttu-id="f42fc-136">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f42fc-136">Description</span></span>                                                                                                                                                                                                                                                     |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f42fc-137">Per iniziare</span><span class="sxs-lookup"><span data-stu-id="f42fc-137">Getting Started</span></span>](getting-started.md)             | <span data-ttu-id="f42fc-138">Descrive le novità di questa versione di Windows Media Gestione dispositivi, offre una panoramica del funzionamento di Windows Media Gestione dispositivi, descrive gli elementi necessari per lo sviluppo di un'applicazione o un provider di servizi e illustra gli esempi forniti con l'SDK.</span><span class="sxs-lookup"><span data-stu-id="f42fc-138">Describes what is new in this version of Windows Media Device Manager, gives an overview of how Windows Media Device Manager works, describes what will be needed to develop an application or service provider, and explains the samples shipped with the SDK.</span></span> |
| [<span data-ttu-id="f42fc-139">Guida per programmatori</span><span class="sxs-lookup"><span data-stu-id="f42fc-139">Programming Guide</span></span>](programming-guide.md)         | <span data-ttu-id="f42fc-140">Viene illustrato come compilare applicazioni e provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="f42fc-140">Discusses how to build applications and service providers.</span></span>                                                                                                                                                                                                      |
| [<span data-ttu-id="f42fc-141">Guida di riferimento alla programmazione</span><span class="sxs-lookup"><span data-stu-id="f42fc-141">Programming Reference</span></span>](programming-reference.md) | <span data-ttu-id="f42fc-142">Fornisce informazioni di riferimento su C++ per le interfacce, i metodi, le classi e le strutture supportate da Windows Media Gestione dispositivi SDK.</span><span class="sxs-lookup"><span data-stu-id="f42fc-142">Provides C++ reference information for the interfaces, methods, classes, and structures supported by the Windows Media Device Manager SDK.</span></span>                                                                                                                      |
| [<span data-ttu-id="f42fc-143">*Glossario*</span><span class="sxs-lookup"><span data-stu-id="f42fc-143">*Glossary*</span></span>](wmdm-glossary.md)                    | <span data-ttu-id="f42fc-144">Definisce i termini usati in questa documentazione.</span><span class="sxs-lookup"><span data-stu-id="f42fc-144">Defines terms used in this documentation.</span></span>                                                                                                                                                                                                                       |



 

 

 




