---
title: Informazioni sulla sincronizzazione dei dispositivi
description: Informazioni sulla sincronizzazione dei dispositivi
ms.assetid: 87976357-f819-41ac-9645-36e799876881
keywords:
- Windows Media Player, sincronizzazione dei dispositivi
- Modello a oggetti di Windows Media Player, sincronizzazione dei dispositivi
- modello a oggetti, sincronizzazione dei dispositivi
- Controllo ActiveX di Windows Media Player, sincronizzazione dei dispositivi
- Controllo ActiveX, sincronizzazione dei dispositivi
- Controllo ActiveX Windows Media Player Mobile, sincronizzazione dei dispositivi
- Windows Media Player Mobile, sincronizzazione dei dispositivi
- sincronizzazione dei dispositivi, informazioni
- sincronizzazione dei dispositivi, informazioni
- sincronizzazione dei dispositivi, trasferimento manuale
- sincronizzazione dei dispositivi, trasferimento manuale
- sincronizzazione dei dispositivi, sincronizzazione automatica
- sincronizzazione dei dispositivi, sincronizzazione automatica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0ad6b6526698def2f7d58ec7afc04c8e22e89c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298115"
---
# <a name="about-device-synchronization"></a><span data-ttu-id="42893-116">Informazioni sulla sincronizzazione dei dispositivi</span><span class="sxs-lookup"><span data-stu-id="42893-116">About Device Synchronization</span></span>

<span data-ttu-id="42893-117">Windows Media Player 10 ha introdotto un nuovo modello per sincronizzare il contenuto multimediale digitale con i dispositivi portatili.</span><span class="sxs-lookup"><span data-stu-id="42893-117">Windows Media Player 10 introduced a new model for synchronizing digital media content with portable devices.</span></span> <span data-ttu-id="42893-118">Dal punto di vista dell'utente, ciò significa che è possibile specificare le playlist (incluse le playlist automatiche) sincronizzate automaticamente con i dispositivi.</span><span class="sxs-lookup"><span data-stu-id="42893-118">From the user's perspective, this means you can specify which playlists (including auto playlists) synchronize automatically with devices.</span></span> <span data-ttu-id="42893-119">È anche possibile trasferire manualmente il contenuto multimediale digitale ai dispositivi.</span><span class="sxs-lookup"><span data-stu-id="42893-119">You can also manually transfer digital media content to devices.</span></span> <span data-ttu-id="42893-120">Dal punto di vista dello sviluppatore, ciò significa che sono presenti nuove funzionalità esposte che è possibile utilizzare nelle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="42893-120">From the developer's perspective, this means there is new functionality exposed that you can take advantage of in your applications.</span></span> <span data-ttu-id="42893-121">A tale scopo, è necessario creare un'istanza remota del controllo Media Player di Windows.</span><span class="sxs-lookup"><span data-stu-id="42893-121">To do this, you must create a remoted instance of the Windows Media Player control.</span></span>

<span data-ttu-id="42893-122">Esistono due modi in cui un utente può copiare il contenuto multimediale digitale in un dispositivo:</span><span class="sxs-lookup"><span data-stu-id="42893-122">There are two ways a user can copy digital media content to a device:</span></span>

-   <span data-ttu-id="42893-123">**Trasferimento manuale.**</span><span class="sxs-lookup"><span data-stu-id="42893-123">**Manual transfer.**</span></span> <span data-ttu-id="42893-124">L'utente seleziona il contenuto multimediale digitale nella libreria e quindi avvia il trasferimento del contenuto al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="42893-124">The user selects digital media content in the library and then initiates a transfer of the content to the device.</span></span> <span data-ttu-id="42893-125">Questa funzionalità è simile a quella fornita dalle versioni precedenti di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="42893-125">This is similar to the functionality provided by previous versions of Windows Media Player.</span></span> <span data-ttu-id="42893-126">Windows Media Player SDK non fornisce metodi per il trasferimento di file multimediali digitali a un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="42893-126">The Windows Media Player SDK does not provide methods for transferring digital media to a device.</span></span>
-   <span data-ttu-id="42893-127">**Sincronizzazione automatica.**</span><span class="sxs-lookup"><span data-stu-id="42893-127">**Automatic synchronization.**</span></span> <span data-ttu-id="42893-128">L'utente specifica le playlist che vengono sincronizzate automaticamente con il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="42893-128">The user specifies playlists that automatically synchronize with the device.</span></span> <span data-ttu-id="42893-129">Si tratta di una funzionalità di Windows Media Player 10 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="42893-129">This is a feature of Windows Media Player 10 or later.</span></span> <span data-ttu-id="42893-130">Windows Media Player SDK fornisce funzionalità per la gestione della sincronizzazione automatica.</span><span class="sxs-lookup"><span data-stu-id="42893-130">The Windows Media Player SDK provides functionality for managing automatic synchronization.</span></span> <span data-ttu-id="42893-131">Questa funzionalità è progettata per consentire di creare un'interfaccia utente personalizzata per l'applicazione per specificare la modalità di sincronizzazione dei dispositivi e per fornire informazioni sullo stato agli utenti.</span><span class="sxs-lookup"><span data-stu-id="42893-131">This functionality is designed to let you build a custom user interface for your application to specify how device synchronization happens and to provide status information to users.</span></span>

<span data-ttu-id="42893-132">Per il corretto funzionamento della sincronizzazione automatica, è necessario stabilire una relazione speciale tra Windows Media Player e il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="42893-132">For automatic synchronization to work, a special relationship must be established between Windows Media Player and the device.</span></span> <span data-ttu-id="42893-133">Questa relazione è detta *collaborazione*.</span><span class="sxs-lookup"><span data-stu-id="42893-133">This relationship is called a *partnership*.</span></span>

<span data-ttu-id="42893-134">Le sezioni seguenti forniscono altre informazioni sulla sincronizzazione dei dispositivi.</span><span class="sxs-lookup"><span data-stu-id="42893-134">The following sections provide more information about device synchronization.</span></span>

-   [<span data-ttu-id="42893-135">Informazioni sui dispositivi</span><span class="sxs-lookup"><span data-stu-id="42893-135">About Devices</span></span>](about-devices.md)
-   [<span data-ttu-id="42893-136">Informazioni sulle relazioni</span><span class="sxs-lookup"><span data-stu-id="42893-136">About Partnerships</span></span>](about-partnerships.md)
-   [<span data-ttu-id="42893-137">Informazioni sul motore di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="42893-137">About the Synchronization Engine</span></span>](about-the-synchronization-engine.md)
-   [<span data-ttu-id="42893-138">Informazioni sulla sincronizzazione della playlist</span><span class="sxs-lookup"><span data-stu-id="42893-138">About Playlist Synchronization</span></span>](about-playlist-synchronization.md)

## <a name="related-topics"></a><span data-ttu-id="42893-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="42893-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42893-140">**Informazioni sul modello a oggetti del lettore**</span><span class="sxs-lookup"><span data-stu-id="42893-140">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> <dt>

[<span data-ttu-id="42893-141">**Gestione remota del controllo di Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="42893-141">**Remoting the Windows Media Player Control**</span></span>](remoting-the-windows-media-player-control.md)
</dt> <dt>

[<span data-ttu-id="42893-142">**Uso dei dispositivi portatili**</span><span class="sxs-lookup"><span data-stu-id="42893-142">**Working with Portable Devices**</span></span>](working-with-portable-devices.md)
</dt> </dl>

 

 




