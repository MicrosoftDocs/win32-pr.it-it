---
title: Informazioni sulla sincronizzazione della playlist
description: Informazioni sulla sincronizzazione della playlist
ms.assetid: bc7d52e0-7906-4b5b-82e6-a84e9c4f0ff0
keywords:
- Windows Media Player, sincronizzazione playlist
- Modello a oggetti di Windows Media Player, sincronizzazione della playlist
- modello a oggetti, sincronizzazione della playlist
- Controllo ActiveX Windows Media Player, sincronizzazione playlist
- Controllo ActiveX, sincronizzazione playlist
- Controllo ActiveX Windows Media Player Mobile, sincronizzazione playlist
- Windows Media Player Mobile, sincronizzazione playlist
- sincronizzazione di dispositivi, playlist
- sincronizzazione dei dispositivi, playlist
- playlist, sincronizzazione
- Playlist di Windows Media Metafile, sincronizzazione
- playlist di metafile, sincronizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecc019b31518fda1a49c8d3ae86f2d03c4ecefc8
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104336289"
---
# <a name="about-playlist-synchronization"></a><span data-ttu-id="d15b2-115">Informazioni sulla sincronizzazione della playlist</span><span class="sxs-lookup"><span data-stu-id="d15b2-115">About Playlist Synchronization</span></span>

<span data-ttu-id="d15b2-116">Windows Media Player 10 o versione successiva è progettato per sincronizzare il contenuto multimediale digitale con i dispositivi usando un modello di sincronizzazione della playlist.</span><span class="sxs-lookup"><span data-stu-id="d15b2-116">Windows Media Player 10 or later is designed to synchronize digital media content to devices using a playlist synchronization model.</span></span> <span data-ttu-id="d15b2-117">Ciò significa che il contenuto destinato a essere copiato in un dispositivo deve essere parte di una playlist.</span><span class="sxs-lookup"><span data-stu-id="d15b2-117">This means that content intended to be copied to a device must be part of a playlist.</span></span> <span data-ttu-id="d15b2-118">Quando l'utente sceglie di trasferire singoli contenuti multimediali digitali dal proprio computer a un dispositivo, Windows Media Player aggiunge il contenuto a una playlist predefinita per la copia.</span><span class="sxs-lookup"><span data-stu-id="d15b2-118">When the user chooses to transfer individual digital media content from his or her computer to a device, Windows Media Player adds the content to a default playlist for copying.</span></span>

<span data-ttu-id="d15b2-119">Le API di sincronizzazione dei dispositivi Windows Media Player sono progettate per funzionare anche in questo modo.</span><span class="sxs-lookup"><span data-stu-id="d15b2-119">The Windows Media Player device synchronization APIs are designed to work like this as well.</span></span> <span data-ttu-id="d15b2-120">Analogamente a Windows Media Player, il programma può presentare all'utente un elenco di playlist che ha definito.</span><span class="sxs-lookup"><span data-stu-id="d15b2-120">Like Windows Media Player, your program can present the user with a list of playlists that he or she has defined.</span></span> <span data-ttu-id="d15b2-121">È quindi possibile consentire all'utente di scegliere quali playlist sincronizzare con un determinato dispositivo e impostare l'ordine di priorità per il processo di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="d15b2-121">You can then enable the user to choose which playlists to synchronize with a particular device and to set the priority order for the synchronization process.</span></span>

<span data-ttu-id="d15b2-122">Poiché i dispositivi portatili hanno una capacità di archiviazione limitata, è possibile che l'utente scelga di sincronizzare un contenuto multimediale più digitale rispetto a quello che il dispositivo può archiviare.</span><span class="sxs-lookup"><span data-stu-id="d15b2-122">Because portable devices have a limited storage capacity, it is possible for the user to choose to synchronize more digital media content than the device can store.</span></span> <span data-ttu-id="d15b2-123">Windows Media Player sincronizza il contenuto in ordine di priorità.</span><span class="sxs-lookup"><span data-stu-id="d15b2-123">Windows Media Player synchronizes content in priority order.</span></span> <span data-ttu-id="d15b2-124">L'utente può definire l'ordine di priorità utilizzando una finestra di dialogo a cui è possibile accedere dalla funzionalità **dispositivi** .</span><span class="sxs-lookup"><span data-stu-id="d15b2-124">The user can define the priority order by using a dialog box that can be accessed from the **Devices** feature.</span></span> <span data-ttu-id="d15b2-125">In risposta all'input dell'utente per il programma, è possibile modificare l'ordine di priorità a livello di codice modificando i valori di determinati attributi della playlist.</span><span class="sxs-lookup"><span data-stu-id="d15b2-125">In response to user input to your program, you can change the priority order programmatically by changing the values of certain playlist attributes.</span></span> <span data-ttu-id="d15b2-126">Insieme, questi attributi sono detti attributi di *sincronizzazione* .</span><span class="sxs-lookup"><span data-stu-id="d15b2-126">Collectively, these attributes are called the *Sync* attributes.</span></span>

<span data-ttu-id="d15b2-127">Ogni playlist in una raccolta ha 16 attributi di sincronizzazione: da **Sync01** a **Sync16**.</span><span class="sxs-lookup"><span data-stu-id="d15b2-127">Each playlist in a library has 16 synchronization attributes: **Sync01** through **Sync16**.</span></span> <span data-ttu-id="d15b2-128">Ogni attributo rappresenta il dispositivo con l'indice di partnership corrispondente.</span><span class="sxs-lookup"><span data-stu-id="d15b2-128">Each attribute represents the device that has the corresponding partnership index.</span></span> <span data-ttu-id="d15b2-129">Il valore di ogni attributo indica due elementi:</span><span class="sxs-lookup"><span data-stu-id="d15b2-129">The value of each attribute tells you two things:</span></span>

-   <span data-ttu-id="d15b2-130">Indica se la playlist deve essere sincronizzata con il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d15b2-130">Whether the playlist should be synchronized with the device.</span></span>
-   <span data-ttu-id="d15b2-131">Valore di priorità per la playlist.</span><span class="sxs-lookup"><span data-stu-id="d15b2-131">The priority value for the playlist.</span></span>

<span data-ttu-id="d15b2-132">Un valore pari a zero indica che Windows Media Player non deve tentare di sincronizzare la playlist con il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d15b2-132">A value of zero indicates that Windows Media Player should not attempt to synchronize the playlist with the device.</span></span> <span data-ttu-id="d15b2-133">Qualsiasi altro valore è un numero di priorità.</span><span class="sxs-lookup"><span data-stu-id="d15b2-133">Any other value is a priority number.</span></span> <span data-ttu-id="d15b2-134">I valori inferiori ricevono una priorità più elevata al momento della sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="d15b2-134">Lower values receive higher priority at synchronization time.</span></span>

<span data-ttu-id="d15b2-135">Le playlist hanno anche un attributo **SyncOnly** che indica se la playlist è disponibile solo per la sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="d15b2-135">Playlists also have a **SyncOnly** attribute that indicates whether the playlist is available only for synchronization.</span></span>

<span data-ttu-id="d15b2-136">I singoli elementi del contenuto multimediale digitale contengono anche i metadati relativi alla sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="d15b2-136">Individual items of digital media content contain metadata about synchronization as well.</span></span> <span data-ttu-id="d15b2-137">Quando si recupera un oggetto **multimediale** dalla libreria, è possibile controllare il valore dell'attributo **SyncState** .</span><span class="sxs-lookup"><span data-stu-id="d15b2-137">When you retrieve a **Media** object from the library, you can inspect the value of the **SyncState** attribute.</span></span> <span data-ttu-id="d15b2-138">Questo attributo fornisce informazioni estese sul fatto che il contenuto sia stato copiato correttamente nel dispositivo o che la copia del contenuto non sia riuscita perché non è sufficiente.</span><span class="sxs-lookup"><span data-stu-id="d15b2-138">This attribute provides extended information about whether the content has been successfully copied to the device or whether copying the content failed because it would not fit.</span></span>

> [!Note]  
> <span data-ttu-id="d15b2-139">È consigliabile evitare di fornire elementi dell'interfaccia utente che consentono all'utente di creare playlist da tutto il contenuto della libreria per la sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="d15b2-139">You should avoid providing user interface elements that enable the user to create playlists from all library content for synchronization.</span></span>

 

<span data-ttu-id="d15b2-140">Per ottimizzare le prestazioni, Windows Media Player impone un set di regole per la creazione di playlist di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="d15b2-140">To optimize performance, Windows Media Player enforces a set of rules for creating synchronization playlists.</span></span> <span data-ttu-id="d15b2-141">Il programma deve creare solo playlist di sincronizzazione per il contenuto fornito.</span><span class="sxs-lookup"><span data-stu-id="d15b2-141">Your program should only create synchronization playlists for content you provided.</span></span> <span data-ttu-id="d15b2-142">Consenti a Windows Media Player di creare playlist di sincronizzazione per il contenuto aggiunto dall'utente alla libreria da altre origini.</span><span class="sxs-lookup"><span data-stu-id="d15b2-142">Allow Windows Media Player to create synchronization playlists for content that the user added to the library from other sources.</span></span>

<span data-ttu-id="d15b2-143">In alternativa alla creazione di una propria interfaccia utente della playlist, è possibile presentare agli utenti una finestra di dialogo predefinita per la scelta delle playlist e la gestione della partnership per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d15b2-143">As an alternative to creating your own playlist user interface, you can present users with a default dialog box for choosing playlists and managing the partnership for a device.</span></span> <span data-ttu-id="d15b2-144">A tale scopo, chiamare [IWMPSyncDevice:: ShowSettings](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-showsettings).</span><span class="sxs-lookup"><span data-stu-id="d15b2-144">To do this, call [IWMPSyncDevice::showSettings](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-showsettings).</span></span> <span data-ttu-id="d15b2-145">Quando si richiama questo metodo, Windows Media Player Visualizza la finestra di dialogo Impostazioni di sincronizzazione.</span><span class="sxs-lookup"><span data-stu-id="d15b2-145">When you invoke this method, Windows Media Player displays its synchronization settings dialog box.</span></span> <span data-ttu-id="d15b2-146">Quando l'utente chiude la finestra di dialogo, Windows Media Player torna automaticamente allo stato di ancoraggio precedente e passa di nuovo il controllo al programma remoto.</span><span class="sxs-lookup"><span data-stu-id="d15b2-146">When the user closes the dialog box, Windows Media Player automatically returns to its prior docking state and passes control back to your remoted program.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d15b2-147">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d15b2-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d15b2-148">**Informazioni sulla sincronizzazione dei dispositivi**</span><span class="sxs-lookup"><span data-stu-id="d15b2-148">**About Device Synchronization**</span></span>](about-device-synchronization.md)
</dt> <dt>

[<span data-ttu-id="d15b2-149">**Gestione delle playlist di sincronizzazione**</span><span class="sxs-lookup"><span data-stu-id="d15b2-149">**Managing Synchronization Playlists**</span></span>](managing-synchronization-playlists.md)
</dt> <dt>

[<span data-ttu-id="d15b2-150">**Attributi della playlist**</span><span class="sxs-lookup"><span data-stu-id="d15b2-150">**Playlist Attributes**</span></span>](playlist-attributes.md)
</dt> </dl>

 

 




