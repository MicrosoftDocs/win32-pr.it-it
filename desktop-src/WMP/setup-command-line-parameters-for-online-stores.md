---
title: Configurare i parametri della riga di comando per i negozi online
description: Configurare i parametri della riga di comando per i negozi online
ms.assetid: 26224d7c-ca12-43b9-9150-3d39bccb85d3
keywords:
- Windows Media Player Online Stores, configurare i parametri della riga di comando
- negozi online, parametri della riga di comando di installazione
- digitare 1 archivi online, impostare i parametri della riga di comando
- digitare 2 archivi online, impostare i parametri della riga di comando
- Imposta parametri della riga di comando
- Windows Media Player Online Store, parametri della riga di comando
- archivi online, parametri della riga di comando
- digitare 1 archivi online, parametri della riga di comando
- digitare 2 archivi online, parametri della riga di comando
- parametri da riga di comando
- Windows Media Player Online Stores, parametri
- negozi online, parametri
- digitare 1 archivi online, parametri
- digitare 2 archivi online, parametri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0605814d3f8ce5e3015cf67d38f213a6b6f07500
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044647"
---
# <a name="setup-command-line-parameters-for-online-stores"></a><span data-ttu-id="d9865-117">Configurare i parametri della riga di comando per i negozi online</span><span class="sxs-lookup"><span data-stu-id="d9865-117">Setup Command-line Parameters for Online Stores</span></span>

> [!Note]  
> <span data-ttu-id="d9865-118">In questa sezione viene descritta la funzionalità progettata per l'utilizzo da parte degli archivi online.</span><span class="sxs-lookup"><span data-stu-id="d9865-118">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="d9865-119">L'uso di questa funzionalità al di fuori del contesto di un archivio online non è supportato.</span><span class="sxs-lookup"><span data-stu-id="d9865-119">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="d9865-120">Quando si installa Windows Media Player 10 o Windows Media Player 11 in Windows XP, è possibile aggiungere i parametri della riga di comando per specificare il primo negozio online visualizzato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="d9865-120">When installing Windows Media Player 10 or Windows Media Player 11 on Windows XP, you can append command-line parameters to specify the first online store that the user sees.</span></span>

<span data-ttu-id="d9865-121">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d9865-121">Syntax</span></span>


```C++
MP10Setup.exe /q:A /c:"setup_wm.exe /Q /R:N /DefaultService:serviceKey /ServiceInfo:documentPath /ServiceExtra:queryString"
```



<span data-ttu-id="d9865-122">Parametri</span><span class="sxs-lookup"><span data-stu-id="d9865-122">Parameters</span></span>

<span data-ttu-id="d9865-123">DefaultService (obbligatorio)</span><span class="sxs-lookup"><span data-stu-id="d9865-123">DefaultService (required)</span></span>

<span data-ttu-id="d9865-124">Nome della chiave per l'archivio online.</span><span class="sxs-lookup"><span data-stu-id="d9865-124">The key name for the online store.</span></span> <span data-ttu-id="d9865-125">Questo valore deve corrispondere al nome della chiave nell'attributo **chiave** dell'elemento **ServiceInfo** del documento ServiceInfo.</span><span class="sxs-lookup"><span data-stu-id="d9865-125">This value must match the key name in the **Key** attribute of the **ServiceInfo** element of the ServiceInfo document.</span></span>

<span data-ttu-id="d9865-126">ServiceInfo (obbligatorio)</span><span class="sxs-lookup"><span data-stu-id="d9865-126">ServiceInfo (required)</span></span>

<span data-ttu-id="d9865-127">Percorso completo di un documento ServiceInfo installato nel computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="d9865-127">The fully qualified path to a ServiceInfo document installed on the user's computer.</span></span>

<span data-ttu-id="d9865-128">ServiceExtra (facoltativo)</span><span class="sxs-lookup"><span data-stu-id="d9865-128">ServiceExtra (optional)</span></span>

<span data-ttu-id="d9865-129">Stringa di query che verrà aggiunta da Windows Media Player 10 all'URL del documento ServiceInfo quando il documento viene recuperato in linea.</span><span class="sxs-lookup"><span data-stu-id="d9865-129">A query string that Windows Media Player 10 will append to the URL for the ServiceInfo document when it retrieves the document online.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9865-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="d9865-130">Remarks</span></span>

<span data-ttu-id="d9865-131">Per informazioni dettagliate sulla ridistribuzione del software Windows Media Player con l'applicazione, vedere [ridistribuzione del software windows media player](redistributing-windows-media-player-software.md).</span><span class="sxs-lookup"><span data-stu-id="d9865-131">For details about redistributing Windows Media Player software with your application, see [Redistributing Windows Media Player Software](redistributing-windows-media-player-software.md).</span></span>

<span data-ttu-id="d9865-132">Quando il computer dell'utente non è connesso a Internet, le informazioni contenute nel documento ServiceInfo locale vengono usate per configurare Windows Media Player per il servizio attivo iniziale.</span><span class="sxs-lookup"><span data-stu-id="d9865-132">When the user's computer is not connected to the Internet, the information contained in the local ServiceInfo document is used to configure Windows Media Player for the initial active service.</span></span>

<span data-ttu-id="d9865-133">I parametri della riga di comando fanno distinzione tra maiuscole e minuscole</span><span class="sxs-lookup"><span data-stu-id="d9865-133">Command-line parameters are case sensitive.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d9865-134">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d9865-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d9865-135">**Negozi online di co-branding**</span><span class="sxs-lookup"><span data-stu-id="d9865-135">**Co-Branding Online Stores**</span></span>](co-branding-online-stores.md)
</dt> <dt>

[<span data-ttu-id="d9865-136">**Informazioni comuni ai negozi online di tipo 1 e di tipo 2**</span><span class="sxs-lookup"><span data-stu-id="d9865-136">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="d9865-137">**Elemento install**</span><span class="sxs-lookup"><span data-stu-id="d9865-137">**Install Element**</span></span>](install-element.md)
</dt> <dt>

[<span data-ttu-id="d9865-138">**Impostazione dell'archivio online iniziale**</span><span class="sxs-lookup"><span data-stu-id="d9865-138">**Setting the Initial Online Store**</span></span>](setting-the-initial-online-store.md)
</dt> </dl>

 

 




