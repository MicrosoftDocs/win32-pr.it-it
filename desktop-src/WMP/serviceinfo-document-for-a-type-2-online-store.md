---
title: Documento ServiceInfo per un negozio online di tipo 2
description: Documento ServiceInfo per un negozio online di tipo 2
ms.assetid: ca83e9bf-c7fb-4212-8fa2-1fae11ed26e9
keywords:
- Windows Media Player Online Stores, documento ServiceInfo
- archivi online, documento ServiceInfo
- digitare 2 archivi online, documento ServiceInfo
- Documento ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fb558661332ab08edd2057fa024a1a0e2034b9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044859"
---
# <a name="serviceinfo-document-for-a-type-2-online-store"></a><span data-ttu-id="91c19-107">Documento ServiceInfo per un negozio online di tipo 2</span><span class="sxs-lookup"><span data-stu-id="91c19-107">ServiceInfo Document for a Type 2 Online Store</span></span>

<span data-ttu-id="91c19-108">I provider di archivio online di tipo 2 devono fornire a Microsoft l'URL di un documento XML che descrive l'archivio online.</span><span class="sxs-lookup"><span data-stu-id="91c19-108">Type 2 online store providers must provide Microsoft with the URL of an XML document that describes the online store.</span></span> <span data-ttu-id="91c19-109">Windows Media Player 10 e Windows Media Player 11 usano questo documento per determinare come configurare l'interfaccia utente per ospitare lo Store online.</span><span class="sxs-lookup"><span data-stu-id="91c19-109">Windows Media Player 10 and Windows Media Player 11 use this document to determine how to configure the user interface to host the online store.</span></span>

<span data-ttu-id="91c19-110">In Windows Media Player 10, il documento ServiceInfo offre quanto segue:</span><span class="sxs-lookup"><span data-stu-id="91c19-110">In Windows Media Player 10, the ServiceInfo document provides the following:</span></span>

-   <span data-ttu-id="91c19-111">Informazioni su come configurare i riquadri attività visualizzati da Windows Media Player quando lo Store online è attivo.</span><span class="sxs-lookup"><span data-stu-id="91c19-111">Information about how to configure the task panes that Windows Media Player displays when the online store is active.</span></span> <span data-ttu-id="91c19-112">Un archivio online può avere uno, due o tre riquadri attività.</span><span class="sxs-lookup"><span data-stu-id="91c19-112">An online store can have one, two, or three task panes.</span></span>
-   <span data-ttu-id="91c19-113">Informazioni utilizzate per configurare i pulsanti del riquadro attività, ad esempio il testo del pulsante, il colore del pulsante e le descrizioni comandi per i pulsanti.</span><span class="sxs-lookup"><span data-stu-id="91c19-113">Information used to configure the task pane buttons, such as the button text, the button color, and tool tips for the buttons.</span></span>
-   <span data-ttu-id="91c19-114">URL per le immagini visualizzate da Windows Media Player per identificare il negozio online.</span><span class="sxs-lookup"><span data-stu-id="91c19-114">URLs for images that Windows Media Player displays to identify the online store.</span></span>
-   <span data-ttu-id="91c19-115">URL di pagine Web, fornite dallo Store online, che Windows Media Player ospita nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="91c19-115">URLs of webpages, provided by the online store, that Windows Media Player hosts in its user interface.</span></span>
-   <span data-ttu-id="91c19-116">Informazioni sul modo in cui il programma di installazione di Windows Media Player deve configurare il primo negozio online visualizzato dall'utente.</span><span class="sxs-lookup"><span data-stu-id="91c19-116">Information about how Windows Media Player setup should configure the first online store the user sees.</span></span>

<span data-ttu-id="91c19-117">In Windows Media Player 11, il documento ServiceInfo offre quanto segue:</span><span class="sxs-lookup"><span data-stu-id="91c19-117">In Windows Media Player 11, the ServiceInfo document provides the following:</span></span>

-   <span data-ttu-id="91c19-118">Informazioni utilizzate per configurare il pulsante per la scheda Store online, ad esempio il testo del pulsante e la descrizione comando per il pulsante.</span><span class="sxs-lookup"><span data-stu-id="91c19-118">Information used to configure the button for Online Stores tab, such as the button text and the tool tip for the button.</span></span>
-   <span data-ttu-id="91c19-119">URL per le immagini visualizzate da Windows Media Player per identificare il negozio online.</span><span class="sxs-lookup"><span data-stu-id="91c19-119">URLs for images that Windows Media Player displays to identify the online store.</span></span>
-   <span data-ttu-id="91c19-120">URL di pagine Web, fornite dallo Store online, che Windows Media Player ospita nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="91c19-120">URLs of webpages, provided by the online store, that Windows Media Player hosts in its user interface.</span></span>

<span data-ttu-id="91c19-121">Quando si inizia a sviluppare lo Store online, è necessario fornire a Microsoft l'URL del documento ServiceInfo.</span><span class="sxs-lookup"><span data-stu-id="91c19-121">When you start developing your online store, you must provide Microsoft with the URL to your ServiceInfo document.</span></span> <span data-ttu-id="91c19-122">Durante la fase di sviluppo, il negozio online verrà visualizzato in Windows Media Player solo quando viene impostata una speciale chiave del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="91c19-122">During the development phase, your online store will appear in Windows Media Player only when a special registry key is set.</span></span>

<span data-ttu-id="91c19-123">Dopo la pubblicazione del negozio online, lo scenario ususal è che Windows Media Player recupera automaticamente il documento ServiceInfo dal Web.</span><span class="sxs-lookup"><span data-stu-id="91c19-123">After your online store is published, the ususal scenario is that Windows Media Player retrieves your ServiceInfo document from the Web automatically.</span></span> <span data-ttu-id="91c19-124">In alcuni casi, tuttavia, Windows Media Player Recupera il documento ServiceInfo dal computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="91c19-124">In some cases, however, Windows Media Player retrieves the ServiceInfo document from the user's computer.</span></span> <span data-ttu-id="91c19-125">Per ulteriori informazioni, vedere [impostazione dell'archivio online iniziale](setting-the-initial-online-store.md).</span><span class="sxs-lookup"><span data-stu-id="91c19-125">For more information, see [Setting the Initial Online Store](setting-the-initial-online-store.md).</span></span>

<span data-ttu-id="91c19-126">Quando Windows Media Player Recupera il documento ServiceInfo dal Web, aggiunge una stringa di query all'URL.</span><span class="sxs-lookup"><span data-stu-id="91c19-126">When Windows Media Player retrieves the ServiceInfo document from the Web, it appends a query string to the URL.</span></span> <span data-ttu-id="91c19-127">La stringa di query contiene parametri che forniscono informazioni sulle impostazioni locali dell'utente e sulla versione di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="91c19-127">The query string contains parameters that provide information about the user's locale and the Windows Media Player version.</span></span>

<span data-ttu-id="91c19-128">È possibile creare documenti ServiceInfo statici o dinamici.</span><span class="sxs-lookup"><span data-stu-id="91c19-128">You can create static or dynamic ServiceInfo documents.</span></span> <span data-ttu-id="91c19-129">Un documento ServiceInfo statico ha un'estensione di file XML.</span><span class="sxs-lookup"><span data-stu-id="91c19-129">A static ServiceInfo document has an .xml file name extension.</span></span> <span data-ttu-id="91c19-130">Un documento ServiceInfo dinamico è una pagina ASP con estensione di file ASP o aspx.</span><span class="sxs-lookup"><span data-stu-id="91c19-130">A dynamic ServiceInfo document is an ASP page and has an .asp or .aspx file name extension.</span></span>

<span data-ttu-id="91c19-131">Non tutti gli elementi disponibili per l'uso nel documento ServiceInfo possono essere usati da ogni negozio online e alcuni elementi sono facoltativi per tutti i negozi online.</span><span class="sxs-lookup"><span data-stu-id="91c19-131">Not all the elements available for use in the ServiceInfo document can be used by every online store, and some elements are optional for all online stores.</span></span> <span data-ttu-id="91c19-132">Per informazioni sui tipi di negozi online che è possibile creare e sulle funzionalità disponibili per ogni tipo, vedere [Windows Media Player Online Stores](windows-media-player-online-stores.md).</span><span class="sxs-lookup"><span data-stu-id="91c19-132">For information about the types of online stores you can create and the features available for each type, see [Windows Media Player Online Stores](windows-media-player-online-stores.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="91c19-133">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="91c19-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91c19-134">**Informazioni sui negozi online di tipo 2**</span><span class="sxs-lookup"><span data-stu-id="91c19-134">**About Type 2 Online Stores**</span></span>](about-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="91c19-135">**Creazione dinamica del documento ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="91c19-135">**Creating the ServiceInfo Document Dynamically**</span></span>](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[<span data-ttu-id="91c19-136">**Documento ServiceInfo di esempio per un negozio online di tipo 2**</span><span class="sxs-lookup"><span data-stu-id="91c19-136">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="91c19-137">**Documento ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="91c19-137">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 




