---
title: Installazione offline
description: Installazione offline
ms.assetid: 29d80b6b-161d-44a7-b91e-70766b849c55
keywords:
- Windows Media Player Online Stores, installazione offline
- negozi online, installazione offline
- digitare 1 negozi online, installazione offline
- digitare 2 archivi online, installazione offline
- Windows Media Player Online Stores, installazioni offline
- archivi online, installazioni offline
- digitare 1 archivi online, installazioni offline
- digitare 2 archivi online, installazioni offline
- installazione di archivi online offline
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cad7048926f218ea7be74a2522eb32c58241a017
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856365"
---
# <a name="installing-while-offline"></a><span data-ttu-id="24936-112">Installazione offline</span><span class="sxs-lookup"><span data-stu-id="24936-112">Installing While Offline</span></span>

<span data-ttu-id="24936-113">Gli utenti possono installare Windows Media Player mentre non sono connessi a Internet.</span><span class="sxs-lookup"><span data-stu-id="24936-113">Users can install Windows Media Player while not connected to the Internet.</span></span> <span data-ttu-id="24936-114">In tal caso, il programma di installazione di Windows Media Player individua il documento ServiceInfo.xml specificato dal parametro della riga di comando *ServiceInfo* .</span><span class="sxs-lookup"><span data-stu-id="24936-114">When this happens, Windows Media Player setup locates the ServiceInfo.xml document specified by the *ServiceInfo* command line parameter.</span></span> <span data-ttu-id="24936-115">Se l'attributo **chiave** corrisponde al parametro della riga di comando *DefaultService* , il programma di installazione applica le informazioni dei seguenti elementi a Windows Media Player:</span><span class="sxs-lookup"><span data-stu-id="24936-115">If the **Key** attribute matches the *DefaultService* command line parameter, setup applies information from the following elements to Windows Media Player:</span></span>

-   <span data-ttu-id="24936-116">FriendlyName.</span><span class="sxs-lookup"><span data-stu-id="24936-116">FriendlyName.</span></span> <span data-ttu-id="24936-117">Il nome descrittivo dello Store online viene visualizzato nell'interfaccia utente di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="24936-117">The friendly name of the online store is shown in the Windows Media Player user interface.</span></span>
-   <span data-ttu-id="24936-118">Colore.</span><span class="sxs-lookup"><span data-stu-id="24936-118">Color.</span></span> <span data-ttu-id="24936-119">I colori specificati vengono applicati alla barra delle applicazioni e ai pulsanti.</span><span class="sxs-lookup"><span data-stu-id="24936-119">The specified colors are applied to the taskbar and buttons.</span></span>
-   <span data-ttu-id="24936-120">ServiceTask1, ServiceTask2 e ServiceTask3.</span><span class="sxs-lookup"><span data-stu-id="24936-120">ServiceTask1, ServiceTask2, and ServiceTask3.</span></span> <span data-ttu-id="24936-121">Gli elementi figlio ButtonText e ButtonTip sono impostati.</span><span class="sxs-lookup"><span data-stu-id="24936-121">The ButtonText and ButtonTip child elements are set.</span></span> <span data-ttu-id="24936-122">L'attributo URL non è impostato.</span><span class="sxs-lookup"><span data-stu-id="24936-122">The URL attribute is not set.</span></span> <span data-ttu-id="24936-123">L'URL viene impostato quando l'utente si connette a Internet e Windows Media Player recupera l'elenco dei negozi online in modo normale.</span><span class="sxs-lookup"><span data-stu-id="24936-123">URL is set once the user connects to the Internet and Windows Media Player retrieves its list of online stores in the normal fashion.</span></span>
-   <span data-ttu-id="24936-124">Immagine.</span><span class="sxs-lookup"><span data-stu-id="24936-124">Image.</span></span> <span data-ttu-id="24936-125">Gli attributi MenuURL e ServiceLargeURL sono impostati.</span><span class="sxs-lookup"><span data-stu-id="24936-125">The MenuURL and ServiceLargeURL attributes are set.</span></span> <span data-ttu-id="24936-126">Questi URL devono puntare alle immagini installate sul disco rigido dell'utente usando il protocollo file://.</span><span class="sxs-lookup"><span data-stu-id="24936-126">These URLs must point to images you installed on the user's hard disk by using the file:// protocol.</span></span>

<span data-ttu-id="24936-127">Quando l'utente tenta di visualizzare lo Store online, Windows Media Player visualizza un messaggio che informa l'utente che è necessaria una connessione Internet.</span><span class="sxs-lookup"><span data-stu-id="24936-127">When the user attempts to view the online store, Windows Media Player displays a message informing the user that an Internet connection is required.</span></span>

## <a name="related-topics"></a><span data-ttu-id="24936-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="24936-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24936-129">**Elemento color**</span><span class="sxs-lookup"><span data-stu-id="24936-129">**Color Element**</span></span>](color-element.md)
</dt> <dt>

[<span data-ttu-id="24936-130">**Elemento FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="24936-130">**FriendlyName Element**</span></span>](friendlyname-element.md)
</dt> <dt>

[<span data-ttu-id="24936-131">**Elemento immagine**</span><span class="sxs-lookup"><span data-stu-id="24936-131">**Image Element**</span></span>](image-element.md)
</dt> <dt>

[<span data-ttu-id="24936-132">**Informazioni comuni ai negozi online di tipo 1 e di tipo 2**</span><span class="sxs-lookup"><span data-stu-id="24936-132">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="24936-133">**Elemento ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="24936-133">**ServiceInfo Element**</span></span>](serviceinfo-element.md)
</dt> <dt>

[<span data-ttu-id="24936-134">**Elemento ServiceTask1**</span><span class="sxs-lookup"><span data-stu-id="24936-134">**ServiceTask1 Element**</span></span>](servicetask1-element.md)
</dt> <dt>

[<span data-ttu-id="24936-135">**Elemento ServiceTask2**</span><span class="sxs-lookup"><span data-stu-id="24936-135">**ServiceTask2 Element**</span></span>](servicetask2-element.md)
</dt> <dt>

[<span data-ttu-id="24936-136">**Elemento ServiceTask3**</span><span class="sxs-lookup"><span data-stu-id="24936-136">**ServiceTask3 Element**</span></span>](servicetask3-element.md)
</dt> <dt>

[<span data-ttu-id="24936-137">**Impostazione dell'archivio online iniziale**</span><span class="sxs-lookup"><span data-stu-id="24936-137">**Setting the Initial Online Store**</span></span>](setting-the-initial-online-store.md)
</dt> <dt>

[<span data-ttu-id="24936-138">**Configurare i parametri della riga di comando per i negozi online**</span><span class="sxs-lookup"><span data-stu-id="24936-138">**Setup Command-line Parameters for Online Stores**</span></span>](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




