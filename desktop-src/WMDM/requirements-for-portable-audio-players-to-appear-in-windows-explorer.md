---
title: Requisiti per la visualizzazione dei lettori audio portatili in Esplora risorse
description: Requisiti per la visualizzazione dei lettori audio portatili in Esplora risorse
ms.assetid: 94227ed8-56e7-4366-9c38-9b5dbf907e16
keywords:
- Windows Media Gestione dispositivi, lettori audio portatili
- Gestione dispositivi, lettori audio portatili
- Guida per programmatori, lettori audio portatili
- provider di servizi, lettori audio portatili
- creazione di provider di servizi, lettori audio portatili
- lettori audio portatili
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a163bf04f4185bc1325aa12ea6acddd43191529
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298317"
---
# <a name="requirements-for-portable-audio-players-to-appear-in-windows-explorer"></a><span data-ttu-id="a9d36-109">Requisiti per la visualizzazione dei lettori audio portatili in Esplora risorse</span><span class="sxs-lookup"><span data-stu-id="a9d36-109">Requirements for Portable Audio Players to Appear in Windows Explorer</span></span>

<span data-ttu-id="a9d36-110">L'estensione dello spazio dei nomi della shell portatile audio player consente agli utenti di Windows di gestire in modo coerente i dispositivi audio gestiti da Windows Media Gestione dispositivi.</span><span class="sxs-lookup"><span data-stu-id="a9d36-110">The portable audio player shell namespace extension provides Windows users with a consistent way to manage audio devices that are managed by Windows Media Device Manager.</span></span> <span data-ttu-id="a9d36-111">Se si creano i componenti del provider di servizi e del driver in base alle linee guida seguenti, il dispositivo viene visualizzato nello spazio dei nomi della shell.</span><span class="sxs-lookup"><span data-stu-id="a9d36-111">If you author your service provider and driver components according to the following guidelines, your device will show up in the shell namespace.</span></span> <span data-ttu-id="a9d36-112">Gli utenti potranno interagire con il contenuto del dispositivo in modo coerente in Esplora risorse per eseguire operazioni di base, ad esempio la copia, l'eliminazione e la ridenominazione.</span><span class="sxs-lookup"><span data-stu-id="a9d36-112">Users will be able to interact with the contents of your device in a consistent manner in Windows Explorer to perform basic operations such as copy, delete, and rename.</span></span>

<span data-ttu-id="a9d36-113">I requisiti della shell seguenti per i componenti del provider di servizi e dei driver hanno lo scopo di integrare le linee guida generali di Windows Media Gestione dispositivi.</span><span class="sxs-lookup"><span data-stu-id="a9d36-113">The following shell requirements for service provider and driver components are intended to supplement the general Windows Media Device Manager guidelines.</span></span>

<span data-ttu-id="a9d36-114">Funzionalità del dispositivo</span><span class="sxs-lookup"><span data-stu-id="a9d36-114">Device Capabilities</span></span>

<span data-ttu-id="a9d36-115">I provider di servizi Windows Media Gestione dispositivi devono essere espliciti nelle funzionalità supportate.</span><span class="sxs-lookup"><span data-stu-id="a9d36-115">Windows Media Device Manager service providers should be explicit in their supported capabilities.</span></span> <span data-ttu-id="a9d36-116">Se una chiamata non è supportata, deve essere restituito un codice di errore.</span><span class="sxs-lookup"><span data-stu-id="a9d36-116">If a call is not supported, an error code must be returned.</span></span> <span data-ttu-id="a9d36-117">È necessario impostare i campi appropriati per la presenza o l'assenza di funzionalità al ritorno dalle funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="a9d36-117">The appropriate fields must be set for the presence or absence of capabilities on return from the following functions:</span></span>

-   [<span data-ttu-id="a9d36-118">**IMDSPStorageGlobals:: GetCapabilities**</span><span class="sxs-lookup"><span data-stu-id="a9d36-118">**IMDSPStorageGlobals::GetCapabilities**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getcapabilities)
-   [<span data-ttu-id="a9d36-119">**IMDSPStorage:: GetAttributes**</span><span class="sxs-lookup"><span data-stu-id="a9d36-119">**IMDSPStorage::GetAttributes**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getattributes)
-   [<span data-ttu-id="a9d36-120">**IMDSPDevice::GetFormatSupport**</span><span class="sxs-lookup"><span data-stu-id="a9d36-120">**IMDSPDevice::GetFormatSupport**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getformatsupport)

<span data-ttu-id="a9d36-121">I provider di servizi devono supportare le funzionalità seguenti per essere compatibili con la Shell:</span><span class="sxs-lookup"><span data-stu-id="a9d36-121">Service providers must support the following capabilities to be compatible with the shell:</span></span>

-   <span data-ttu-id="a9d36-122">Copia nel dispositivo (con supporto per callback di annullamento e di stato)</span><span class="sxs-lookup"><span data-stu-id="a9d36-122">Copy to device (with support for cancel and progress callbacks)</span></span>
-   <span data-ttu-id="a9d36-123">Elimina file dal dispositivo (con supporto per callback di annullamento e di stato)</span><span class="sxs-lookup"><span data-stu-id="a9d36-123">Delete file from device (with support for cancel and progress callbacks)</span></span>
-   <span data-ttu-id="a9d36-124">Rinomina file nel dispositivo</span><span class="sxs-lookup"><span data-stu-id="a9d36-124">Rename file on device</span></span>
-   <span data-ttu-id="a9d36-125">Segnalazione spazio (spazio totale, spazio disponibile, spazio inutilizzabile)</span><span class="sxs-lookup"><span data-stu-id="a9d36-125">Space reporting (total space, free space, unusable space)</span></span>
-   <span data-ttu-id="a9d36-126">Plug and Play (vedere [Abilitazione di PNP per i dispositivi](enabling-pnp-for-devices.md))</span><span class="sxs-lookup"><span data-stu-id="a9d36-126">Plug and Play (see [Enabling PnP for Devices](enabling-pnp-for-devices.md))</span></span>
-   <span data-ttu-id="a9d36-127">Formato (preferibilmente con supporto per callback di annullamento e di stato)</span><span class="sxs-lookup"><span data-stu-id="a9d36-127">Format (preferably with support for cancel and progress callbacks)</span></span>

<span data-ttu-id="a9d36-128">Se i metadati sono supportati, i campi seguenti devono essere supportati per i singoli file.</span><span class="sxs-lookup"><span data-stu-id="a9d36-128">If metadata is supported, the following fields must be supported for individual files.</span></span> <span data-ttu-id="a9d36-129">Se non sono disponibili dati, il campo deve essere inizializzato come una stringa vuota:</span><span class="sxs-lookup"><span data-stu-id="a9d36-129">If no data is available, the field should be initialized as an empty string:</span></span>



| <span data-ttu-id="a9d36-130">Campo</span><span class="sxs-lookup"><span data-stu-id="a9d36-130">Field</span></span>        | <span data-ttu-id="a9d36-131">Costante (definita in WMDM. idl)</span><span class="sxs-lookup"><span data-stu-id="a9d36-131">Constant (defined in WMDM.idl)</span></span> | <span data-ttu-id="a9d36-132">Tag dei metadati</span><span class="sxs-lookup"><span data-stu-id="a9d36-132">Metadata tag</span></span>    |
|--------------|--------------------------------|-----------------|
| <span data-ttu-id="a9d36-133">Titolo del brano</span><span class="sxs-lookup"><span data-stu-id="a9d36-133">Song Title</span></span>   | <span data-ttu-id="a9d36-134">g \_ wszWMDMTitle</span><span class="sxs-lookup"><span data-stu-id="a9d36-134">g\_wszWMDMTitle</span></span>                | <span data-ttu-id="a9d36-135">WMDM/title</span><span class="sxs-lookup"><span data-stu-id="a9d36-135">WMDM/Title</span></span>      |
| <span data-ttu-id="a9d36-136">Numero di traccia</span><span class="sxs-lookup"><span data-stu-id="a9d36-136">Track Number</span></span> | <span data-ttu-id="a9d36-137">g \_ wszWMDMTrack</span><span class="sxs-lookup"><span data-stu-id="a9d36-137">g\_wszWMDMTrack</span></span>                | <span data-ttu-id="a9d36-138">WMDM/Track</span><span class="sxs-lookup"><span data-stu-id="a9d36-138">WMDM/Track</span></span>      |
| <span data-ttu-id="a9d36-139">Artista</span><span class="sxs-lookup"><span data-stu-id="a9d36-139">Artist</span></span>       | <span data-ttu-id="a9d36-140">g \_ wszWMDMAuthor</span><span class="sxs-lookup"><span data-stu-id="a9d36-140">g\_wszWMDMAuthor</span></span>               | <span data-ttu-id="a9d36-141">WMDM/autore</span><span class="sxs-lookup"><span data-stu-id="a9d36-141">WMDM/Author</span></span>     |
| <span data-ttu-id="a9d36-142">Album</span><span class="sxs-lookup"><span data-stu-id="a9d36-142">Album</span></span>        | <span data-ttu-id="a9d36-143">g \_ wszWMDMAlbumTitle</span><span class="sxs-lookup"><span data-stu-id="a9d36-143">g\_wszWMDMAlbumTitle</span></span>           | <span data-ttu-id="a9d36-144">WMDM/AlbumTitle</span><span class="sxs-lookup"><span data-stu-id="a9d36-144">WMDM/AlbumTitle</span></span> |
| <span data-ttu-id="a9d36-145">Year</span><span class="sxs-lookup"><span data-stu-id="a9d36-145">Year</span></span>         | <span data-ttu-id="a9d36-146">g \_ wszWMDMYear</span><span class="sxs-lookup"><span data-stu-id="a9d36-146">g\_wszWMDMYear</span></span>                 | <span data-ttu-id="a9d36-147">WMDM/anno</span><span class="sxs-lookup"><span data-stu-id="a9d36-147">WMDM/Year</span></span>       |
| <span data-ttu-id="a9d36-148">Genre</span><span class="sxs-lookup"><span data-stu-id="a9d36-148">Genre</span></span>        | <span data-ttu-id="a9d36-149">g \_ wszWMDMGenre</span><span class="sxs-lookup"><span data-stu-id="a9d36-149">g\_wszWMDMGenre</span></span>                | <span data-ttu-id="a9d36-150">WMDM/genre</span><span class="sxs-lookup"><span data-stu-id="a9d36-150">WMDM/Genre</span></span>      |



 

<span data-ttu-id="a9d36-151">Concorrenza</span><span class="sxs-lookup"><span data-stu-id="a9d36-151">Concurrency</span></span>

<span data-ttu-id="a9d36-152">I driver in modalità kernel per Windows Media Gestione dispositivi devono essere affidabili per la gestione dell'accesso simultaneo.</span><span class="sxs-lookup"><span data-stu-id="a9d36-152">Kernel mode drivers for Windows Media Device Manager need to be robust in handling concurrent access.</span></span> <span data-ttu-id="a9d36-153">Ad esempio, un utente può accedere contemporaneamente al dispositivo tramite la shell e il lettore multimediale o semplicemente attraverso più finestre della shell.</span><span class="sxs-lookup"><span data-stu-id="a9d36-153">For example, a user can be concurrently accessing the device through both the shell and media player or simply through multiple windows in the shell.</span></span> <span data-ttu-id="a9d36-154">Come parte della gestione della concorrenza, i driver non dovrebbero presumere, solo perché il provider di servizi è caricato, che il dispositivo è in uso.</span><span class="sxs-lookup"><span data-stu-id="a9d36-154">As part of handling concurrency, drivers should not assume, just because the service provider is loaded, that the device is in use.</span></span> <span data-ttu-id="a9d36-155">Devono invece implementare un meccanismo di blocco per serializzare l'accesso al dispositivo in base alle esigenze per le singole operazioni.</span><span class="sxs-lookup"><span data-stu-id="a9d36-155">Instead, they should implement a locking mechanism to serialize access to the device as needed for individual operations.</span></span>

<span data-ttu-id="a9d36-156">Interfaccia utente</span><span class="sxs-lookup"><span data-stu-id="a9d36-156">UI</span></span>

<span data-ttu-id="a9d36-157">I provider di servizi per Windows Media Gestione dispositivi non devono visualizzare alcuna interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="a9d36-157">Service providers for Windows Media Device Manager should not show any user interface.</span></span> <span data-ttu-id="a9d36-158">Eventuali errori devono essere restituiti dalle chiamate al metodo come specifici codici di errore di Windows Media Gestione dispositivi, laddove possibile.</span><span class="sxs-lookup"><span data-stu-id="a9d36-158">Any errors should be returned from method calls as specific Windows Media Device Manager error codes whenever possible.</span></span>

<span data-ttu-id="a9d36-159">Abilitazione nella shell</span><span class="sxs-lookup"><span data-stu-id="a9d36-159">Enabling in the Shell</span></span>

<span data-ttu-id="a9d36-160">Se il pacchetto soddisfa tutti i requisiti della shell, è possibile abilitare il dispositivo in modo che venga visualizzato nella shell impostando il valore *ShowInShell* su 1 nei parametri del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a9d36-160">If your package meets all of the shell requirements, you can enable your device to be shown in the shell by setting the *ShowInShell* value to 1 under the device parameters.</span></span> <span data-ttu-id="a9d36-161">Per altre informazioni, vedere [parametri del dispositivo](device-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="a9d36-161">For more information, see [Device Parameters](device-parameters.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a9d36-162">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a9d36-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a9d36-163">**Creazione di un provider di servizi**</span><span class="sxs-lookup"><span data-stu-id="a9d36-163">**Creating a Service Provider**</span></span>](creating-a-service-provider.md)
</dt> </dl>

 

 




