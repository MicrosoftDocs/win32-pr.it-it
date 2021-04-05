---
title: Riferimento per negozi online di tipo 2
description: Riferimento per negozi online di tipo 2
ms.assetid: b3f580cc-b02d-4312-a7a1-a35778a222bc
keywords:
- Windows Media Player Online Stores, informazioni di riferimento
- negozi online, informazioni di riferimento
- digitare 2 archivi online, informazioni di riferimento
- informazioni di riferimento per i negozi online di tipo 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c164ad74481030a52cd31605b29833d3bfbd3f1d
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2020
ms.locfileid: "103724187"
---
# <a name="reference-for-type-2-online-stores"></a><span data-ttu-id="bbdaa-107">Riferimento per negozi online di tipo 2</span><span class="sxs-lookup"><span data-stu-id="bbdaa-107">Reference for Type 2 Online Stores</span></span>

> [!Note]  
> <span data-ttu-id="bbdaa-108">In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online.</span><span class="sxs-lookup"><span data-stu-id="bbdaa-108">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="bbdaa-109">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="bbdaa-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="bbdaa-110">Windows Media Player 10 o versioni successive fornisce oggetti, interfacce, proprietà e metodi che supportano gli archivi online di tipo 2.</span><span class="sxs-lookup"><span data-stu-id="bbdaa-110">Windows Media Player 10 or later provides objects, interfaces, properties, and methods that support type 2 online stores.</span></span> <span data-ttu-id="bbdaa-111">Le sezioni seguenti illustrano in dettaglio questi argomenti.</span><span class="sxs-lookup"><span data-stu-id="bbdaa-111">The following sections document these in detail.</span></span>



| <span data-ttu-id="bbdaa-112">Sezione</span><span class="sxs-lookup"><span data-stu-id="bbdaa-112">Section</span></span>                                                                                                        | <span data-ttu-id="bbdaa-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bbdaa-113">Description</span></span>                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bbdaa-114">Interfaccia IWMPSubscriptionService</span><span class="sxs-lookup"><span data-stu-id="bbdaa-114">IWMPSubscriptionService Interface</span></span>](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice)                                               | <span data-ttu-id="bbdaa-115">Fornisce metodi per aumentare Digital Rights Management (DRM) e avviare processi in background.</span><span class="sxs-lookup"><span data-stu-id="bbdaa-115">Provides methods to augment digital rights management (DRM) and initiate background processes.</span></span>                                                                              |
| [<span data-ttu-id="bbdaa-116">Interfaccia IWMPSubscriptionService2</span><span class="sxs-lookup"><span data-stu-id="bbdaa-116">IWMPSubscriptionService2 Interface</span></span>](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2)                                             | <span data-ttu-id="bbdaa-117">Fornisce metodi per avviare i processi in background, per fornire informazioni sull'attività di archivio online e per fornire un puntatore all'interfaccia di base di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="bbdaa-117">Provides methods to initiate background processes, to provide information about online store activity, and to provide a pointer to the Windows Media Player core interface.</span></span> |
| [<span data-ttu-id="bbdaa-118">Interfaccia IWMPSubscriptionServiceCallback</span><span class="sxs-lookup"><span data-stu-id="bbdaa-118">IWMPSubscriptionServiceCallback Interface</span></span>](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservicecallback)                               | <span data-ttu-id="bbdaa-119">Definisce un metodo utilizzato dagli archivi online per notificare a Windows Media Player quando viene completato un processo in background.</span><span class="sxs-lookup"><span data-stu-id="bbdaa-119">Defines a method that online stores use to notify Windows Media Player when a background process is completed.</span></span>                                                              |
| [<span data-ttu-id="bbdaa-120">WMPNotifySubscriptionPluginAddRemove</span><span class="sxs-lookup"><span data-stu-id="bbdaa-120">WMPNotifySubscriptionPluginAddRemove</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-wmpnotifysubscriptionpluginaddremove)                               | <span data-ttu-id="bbdaa-121">Funzione utilizzata per notificare a Windows Media Player che è stato installato o disinstallato un plug-in.</span><span class="sxs-lookup"><span data-stu-id="bbdaa-121">A function used to notify Windows Media Player that a plug-in has been installed or uninstalled.</span></span>                                                                            |
| [<span data-ttu-id="bbdaa-122">Download (oggetto)</span><span class="sxs-lookup"><span data-stu-id="bbdaa-122">DownloadCollection Object</span></span>](downloadcollection-object.md)                                                     | <span data-ttu-id="bbdaa-123">Fornisce metodi e proprietà per gestire le raccolte di elementi di download.</span><span class="sxs-lookup"><span data-stu-id="bbdaa-123">Provides methods and properties to manage collections of download items.</span></span>                                                                                                    |
| [<span data-ttu-id="bbdaa-124">Oggetto DownloadItem</span><span class="sxs-lookup"><span data-stu-id="bbdaa-124">DownloadItem Object</span></span>](downloaditem-object.md)                                                                 | <span data-ttu-id="bbdaa-125">Fornisce metodi e proprietà correlati alle richieste di download.</span><span class="sxs-lookup"><span data-stu-id="bbdaa-125">Provides methods and properties relating to download requests.</span></span>                                                                                                              |
| [<span data-ttu-id="bbdaa-126">Oggetto DownloadManager</span><span class="sxs-lookup"><span data-stu-id="bbdaa-126">DownloadManager Object</span></span>](downloadmanager-object.md)                                                           | <span data-ttu-id="bbdaa-127">Fornisce metodi per gestire le raccolte di download.</span><span class="sxs-lookup"><span data-stu-id="bbdaa-127">Provides methods to manage download collections.</span></span>                                                                                                                            |
| [<span data-ttu-id="bbdaa-128">Oggetto esterno per i negozi di tipo 2 online</span><span class="sxs-lookup"><span data-stu-id="bbdaa-128">External Object for Type 2 Online Stores</span></span>](external-object-for-type-2-online-stores.md)                       | <span data-ttu-id="bbdaa-129">Fornisce proprietà, metodi e un evento accessibile da pagine Web di archivio online.</span><span class="sxs-lookup"><span data-stu-id="bbdaa-129">Provides properties, methods, and an event accessible from online store webpages.</span></span>                                                                                           |
| [<span data-ttu-id="bbdaa-130">Enumerazioni per i negozi di tipo 2 online</span><span class="sxs-lookup"><span data-stu-id="bbdaa-130">Enumerations for Type 2 Online Stores</span></span>](enumerations-for-type-2-online-stores.md)                             | <span data-ttu-id="bbdaa-131">Descrive le enumerazioni usate dagli archivi online.</span><span class="sxs-lookup"><span data-stu-id="bbdaa-131">Describes enumerations used by online stores.</span></span>                                                                                                                               |
| [<span data-ttu-id="bbdaa-132">Convenzione di processo di Windows Media Player BITS</span><span class="sxs-lookup"><span data-stu-id="bbdaa-132">Windows Media Player BITS Job Convention</span></span>](windows-media-player-bits-job-convention.md)                       | <span data-ttu-id="bbdaa-133">Viene descritta una convenzione per l'utilizzo del Servizio trasferimento intelligente in background (BITS).</span><span class="sxs-lookup"><span data-stu-id="bbdaa-133">Describes a convention for using the Background Intelligent Transfer Service (BITS).</span></span>                                                                                        |
| [<span data-ttu-id="bbdaa-134">Chiavi del registro di sistema e voci per un archivio di tipo 2 online</span><span class="sxs-lookup"><span data-stu-id="bbdaa-134">Registry Keys and Entries for a Type 2 Online Store</span></span>](registry-keys-and-entries-for-a-type-2-online-store.md) | <span data-ttu-id="bbdaa-135">Descrive le voci del registro di sistema che un archivio online deve creare nel registro di sistema nel computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="bbdaa-135">Describes registry entries that an online store must create in the registry on the user's computer.</span></span>                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="bbdaa-136">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="bbdaa-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbdaa-137">**Digitare 2 archivi online**</span><span class="sxs-lookup"><span data-stu-id="bbdaa-137">**Type 2 Online Stores**</span></span>](type-2-online-stores.md)
</dt> </dl>

 

 




