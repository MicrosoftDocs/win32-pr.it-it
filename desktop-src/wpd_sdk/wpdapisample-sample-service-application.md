---
description: Applicazione WpdServicesApiSample
ms.assetid: 857753f7-bca1-4f4a-a8f9-0b2232e2f0dc
title: Applicazione WpdServicesApiSample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54cbf6c6e4647744ae45f43b5d4139cbf7f9dc55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312469"
---
# <a name="wpdservicesapisample-application"></a><span data-ttu-id="7007f-103">Applicazione WpdServicesApiSample</span><span class="sxs-lookup"><span data-stu-id="7007f-103">WpdServicesApiSample Application</span></span>

<span data-ttu-id="7007f-104">Un servizio del dispositivo è un'estensione di un oggetto funzionale, oltre a raggruppare logicamente le funzionalità del dispositivo, un servizio del dispositivo offre alle applicazioni la possibilità di individuare tali funzionalità a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="7007f-104">A device service is an extension of a functional object: In addition to logically grouping device capabilities, a device service provides applications with the ability to programmatically discover those capabilities.</span></span>

<span data-ttu-id="7007f-105">L'applicazione di esempio WpdServicesApiSample è un'applicazione desktop da riga di comando che è possibile utilizzare per esplorare i servizi dei contatti sui dispositivi collegati al computer.</span><span class="sxs-lookup"><span data-stu-id="7007f-105">The WpdServicesApiSample sample application is a command-line desktop application that you can use to explore Contacts services on devices attached to your computer.</span></span> <span data-ttu-id="7007f-106">È possibile esplorare questi servizi elencando supportati: formati, eventi, metodi e servizi astratti.</span><span class="sxs-lookup"><span data-stu-id="7007f-106">You can explore these services by listing supported: formats, events, methods, and abstract services.</span></span> <span data-ttu-id="7007f-107">È anche possibile usare questa applicazione per recuperare le proprietà in un determinato servizio di contatto e per richiamare i metodi supportati da tale servizio.</span><span class="sxs-lookup"><span data-stu-id="7007f-107">You can also use this application retrieve the properties on a given Contact service and to invoke methods supported by that service.</span></span>

<span data-ttu-id="7007f-108">Se non si dispone ancora di un dispositivo che supporta i servizi contatti, è comunque possibile eseguire WpdServicesApiSample se si installa prima il WpdServiceSampleDriver incluso in Windows Driver Kit.</span><span class="sxs-lookup"><span data-stu-id="7007f-108">If you don't yet have a device that supports Contacts services, you can still run the WpdServicesApiSample if you first install the WpdServiceSampleDriver that is included in the Windows Driver Kit.</span></span>

<span data-ttu-id="7007f-109">L'applicazione di esempio WpdServicesApiSample include i file seguenti:</span><span class="sxs-lookup"><span data-stu-id="7007f-109">The WpdServicesApiSample sample application includes the following files:</span></span>



| <span data-ttu-id="7007f-110">**File**</span><span class="sxs-lookup"><span data-stu-id="7007f-110">**File**</span></span>                | <span data-ttu-id="7007f-111">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="7007f-111">**Description**</span></span>                                                                                                                                                                                           |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7007f-112">ContentEnumeration. cpp</span><span class="sxs-lookup"><span data-stu-id="7007f-112">ContentEnumeration.cpp</span></span>  | <span data-ttu-id="7007f-113">Contiene metodi che enumerano il contenuto di un determinato servizio contatti.</span><span class="sxs-lookup"><span data-stu-id="7007f-113">Contains methods that enumerate the content on a given Contacts service.</span></span>                                                                                                                                  |
| <span data-ttu-id="7007f-114">ContentProperties. cpp</span><span class="sxs-lookup"><span data-stu-id="7007f-114">ContentProperties.cpp</span></span>   | <span data-ttu-id="7007f-115">Contiene metodi che leggono e scrivono le proprietà in un servizio di contatti specificato.</span><span class="sxs-lookup"><span data-stu-id="7007f-115">Contains methods that read and write properties on a given Contacts service.</span></span>                                                                                                                              |
| <span data-ttu-id="7007f-116">ServiceCapabilities. cpp</span><span class="sxs-lookup"><span data-stu-id="7007f-116">ServiceCapabilities.cpp</span></span> | <span data-ttu-id="7007f-117">Contiene i metodi che recuperano i formati, gli eventi e i servizi astratti supportati supportati da un determinato servizio di contatti.</span><span class="sxs-lookup"><span data-stu-id="7007f-117">Contains the methods that retrieve the supported formats, events, and abstract services that are supported by a given Contacts service.</span></span>                                                                   |
| <span data-ttu-id="7007f-118">ServiceEnumeration. cpp</span><span class="sxs-lookup"><span data-stu-id="7007f-118">ServiceEnumeration.cpp</span></span>  | <span data-ttu-id="7007f-119">Contiene le funzioni di supporto che recuperano informazioni sul dispositivo, ad esempio il nome descrittivo del dispositivo o i servizi di contatti supportati.</span><span class="sxs-lookup"><span data-stu-id="7007f-119">Contains the helper functions that retrieve device information such as the device-friendly name or the supported Contacts services.</span></span>                                                                       |
| <span data-ttu-id="7007f-120">ServiceMethods. cpp</span><span class="sxs-lookup"><span data-stu-id="7007f-120">ServiceMethods.cpp</span></span>      | <span data-ttu-id="7007f-121">Contiene i metodi che recuperano e richiamano i metodi supportati da un determinato servizio contatti.</span><span class="sxs-lookup"><span data-stu-id="7007f-121">Contains the methods that retrieve and invoke methods supported by a given Contacts service.</span></span>                                                                                                              |
| <span data-ttu-id="7007f-122">stdafx.cpp</span><span class="sxs-lookup"><span data-stu-id="7007f-122">Stdafx.cpp</span></span>              | <span data-ttu-id="7007f-123">Include i file standard.</span><span class="sxs-lookup"><span data-stu-id="7007f-123">Includes the standard files.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="7007f-124">WpdServiceApiSample. cpp</span><span class="sxs-lookup"><span data-stu-id="7007f-124">WpdServiceApiSample.cpp</span></span> | <span data-ttu-id="7007f-125">Ospita la funzione di avvio **\_ tmain** , che chiama la funzione **DoMenu** locale che visualizza un elenco di dispositivi e attività disponibili e chiama la funzione appropriata per la selezione di menu dell'utente.</span><span class="sxs-lookup"><span data-stu-id="7007f-125">Hosts the **\_tmain** startup function, which calls the local **DoMenu** function, which displays a list of available devices and tasks and calls the function appropriate for the user's menu selection.</span></span> |



 


## <a name="related-topics"></a><span data-ttu-id="7007f-126">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="7007f-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7007f-127">Esempi</span><span class="sxs-lookup"><span data-stu-id="7007f-127">Samples</span></span>](sample.md)
</dt> </dl>

 

 



