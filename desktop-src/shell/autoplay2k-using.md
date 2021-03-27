---
description: Quando la shell rileva l'inserimento di nuovi supporti o l'allegato di un dispositivo a collegamento a caldo, vengono determinati il contenuto del dispositivo o del supporto. AutoPlay, a seconda delle impostazioni correnti, esegue una delle operazioni seguenti.
title: Uso e configurazione di AutoPlay
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 096c7042-8cf0-4e4f-934f-274564218f4c
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 04a4f6dd09e03f26b13649e860beb7f2621ce952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750303"
---
# <a name="using-and-configuring-autoplay"></a><span data-ttu-id="33840-104">Uso e configurazione di AutoPlay</span><span class="sxs-lookup"><span data-stu-id="33840-104">Using and Configuring AutoPlay</span></span>

<span data-ttu-id="33840-105">Quando la shell rileva l'inserimento di nuovi supporti o l'allegato di un dispositivo a collegamento a caldo, vengono determinati il contenuto del dispositivo o del supporto.</span><span class="sxs-lookup"><span data-stu-id="33840-105">When the Shell detects the insertion of new media or the attachment of a hot-plug device, the contents of the device or media are determined.</span></span> <span data-ttu-id="33840-106">AutoPlay, a seconda delle impostazioni correnti, esegue una delle operazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="33840-106">AutoPlay, depending on its current settings, does one of the following.</span></span>

-   <span data-ttu-id="33840-107">Riproduce automaticamente il contenuto.</span><span class="sxs-lookup"><span data-stu-id="33840-107">Plays the content automatically.</span></span>
-   <span data-ttu-id="33840-108">Visualizza una finestra di dialogo in cui viene richiesto all'utente di scegliere un gestore predefinito per un singolo tipo di contenuto.</span><span class="sxs-lookup"><span data-stu-id="33840-108">Displays a dialog box prompting the user to choose a default handler for a single content type.</span></span>
-   <span data-ttu-id="33840-109">Presenta, nel caso di contenuto misto, un elenco di applicazioni di gestione disponibili da avviare.</span><span class="sxs-lookup"><span data-stu-id="33840-109">Presents, in the case of mixed content, a list of available handler applications to launch.</span></span> <span data-ttu-id="33840-110">Il gestore scelto quindi riproduce automaticamente il tipo di contenuto associato.</span><span class="sxs-lookup"><span data-stu-id="33840-110">The chosen handler then automatically plays its associated content type.</span></span>
-   <span data-ttu-id="33840-111">Visualizza una visualizzazione cartella standard dei file.</span><span class="sxs-lookup"><span data-stu-id="33840-111">Displays a standard folder view of the files.</span></span>
-   <span data-ttu-id="33840-112">Non esegue alcuna operazione se, in precedenza, l'utente ha scelto di **non eseguire alcuna azione** per quel tipo di contenuto, così come specificato, **eseguire sempre l'azione selezionata**.</span><span class="sxs-lookup"><span data-stu-id="33840-112">Does nothing if, earlier, the user had chosen **Take no action** for that content type as well as specified **Always do the selected action**.</span></span>

<span data-ttu-id="33840-113">Se il contenuto non soddisfa i criteri per AutoPlay, l'evento viene quindi passato a Windows Image Acquisition (WIA).</span><span class="sxs-lookup"><span data-stu-id="33840-113">If the contents do not meet the criteria for AutoPlay, the event is then passed to Windows Image Acquisition (WIA).</span></span>

<span data-ttu-id="33840-114">Gli argomenti seguenti illustrano l'installazione e l'uso di AutoPlay.</span><span class="sxs-lookup"><span data-stu-id="33840-114">The following topics discuss the setup and use of AutoPlay.</span></span>

-   [<span data-ttu-id="33840-115">Preparazione dell'hardware e del software per l'uso con AutoPlay</span><span class="sxs-lookup"><span data-stu-id="33840-115">Preparing Hardware and Software for Use with AutoPlay</span></span>](#preparing-hardware-and-software-for-use-with-autoplay)
-   [<span data-ttu-id="33840-116">Modalità di ricerca di AutoPlay nei supporti</span><span class="sxs-lookup"><span data-stu-id="33840-116">How AutoPlay Searches Media</span></span>](#how-autoplay-searches-media)
-   [<span data-ttu-id="33840-117">Definizione di tipi di contenuto singoli e misti</span><span class="sxs-lookup"><span data-stu-id="33840-117">Defining Single and Mixed Content Types</span></span>](#defining-single-and-mixed-content-types)
-   [<span data-ttu-id="33840-118">Scenari di esempio</span><span class="sxs-lookup"><span data-stu-id="33840-118">Sample Scenarios</span></span>](#sample-scenarios)
    -   [<span data-ttu-id="33840-119">AutoPlay per i dispositivi di archiviazione con supporti immagine</span><span class="sxs-lookup"><span data-stu-id="33840-119">AutoPlay for Storage Devices with Picture Media</span></span>](#autoplay-for-storage-devices-with-picture-media)
    -   [<span data-ttu-id="33840-120">AutoPlay per la riproduzione di file musicali e dispositivi di archiviazione contenenti supporti musicali</span><span class="sxs-lookup"><span data-stu-id="33840-120">AutoPlay for Music File Playback Devices and Storage Devices Containing Music Media</span></span>](#autoplay-for-music-file-playback-devices-and-storage-devices-containing-music-media)
    -   [<span data-ttu-id="33840-121">AutoPlay per la riproduzione video nella prima presentazione</span><span class="sxs-lookup"><span data-stu-id="33840-121">AutoPlay for Video Playback on First Presentation</span></span>](#autoplay-for-video-playback-on-first-presentation)
-   [<span data-ttu-id="33840-122">Assegnazione di applicazioni gestore predefinite</span><span class="sxs-lookup"><span data-stu-id="33840-122">Assigning Default Handler Applications</span></span>](#assigning-default-handler-applications)
-   [<span data-ttu-id="33840-123">Gestione di supporti contenenti tipi di contenuto misto</span><span class="sxs-lookup"><span data-stu-id="33840-123">Handling Media Containing Mixed Content Types</span></span>](#handling-media-containing-mixed-content-types)
-   [<span data-ttu-id="33840-124">Interfacce utente AutoPlay</span><span class="sxs-lookup"><span data-stu-id="33840-124">AutoPlay User Interfaces</span></span>](#autoplay-user-interfaces)
    -   [<span data-ttu-id="33840-125">Finestra di dialogo tipo di contenuto singolo</span><span class="sxs-lookup"><span data-stu-id="33840-125">Single Content Type Dialog Box</span></span>](#single-content-type-dialog-box)
    -   [<span data-ttu-id="33840-126">Finestra di dialogo supporto misto</span><span class="sxs-lookup"><span data-stu-id="33840-126">Mixed Media Dialog Box</span></span>](#mixed-media-dialog-box)
    -   [<span data-ttu-id="33840-127">Pagina Proprietà</span><span class="sxs-lookup"><span data-stu-id="33840-127">Property Page</span></span>](#property-page)

## <a name="preparing-hardware-and-software-for-use-with-autoplay"></a><span data-ttu-id="33840-128">Preparazione dell'hardware e del software per l'uso con AutoPlay</span><span class="sxs-lookup"><span data-stu-id="33840-128">Preparing Hardware and Software for Use with AutoPlay</span></span>

<span data-ttu-id="33840-129">Per il funzionamento di AutoPlay è necessario che nel registro di sistema siano presenti diverse informazioni.</span><span class="sxs-lookup"><span data-stu-id="33840-129">Several pieces of information need to appear in the registry for AutoPlay to function.</span></span> <span data-ttu-id="33840-130">Queste informazioni interagiscono e fanno riferimento l'uno all'altro per formare l'intero ambiente AutoPlay.</span><span class="sxs-lookup"><span data-stu-id="33840-130">These pieces of information interact and reference each other to form the full AutoPlay environment.</span></span> <span data-ttu-id="33840-131">In questo documento viene illustrata la configurazione di ognuna di queste informazioni come una singola procedura autonoma.</span><span class="sxs-lookup"><span data-stu-id="33840-131">This document presents the setup of each of these pieces of information as an individual stand-alone procedure.</span></span>

<span data-ttu-id="33840-132">Per altre istruzioni, vedere gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="33840-132">See the following topics for additional instructions.</span></span>

-   [<span data-ttu-id="33840-133">Come assegnare un gestore di dispositivo a un dispositivo</span><span class="sxs-lookup"><span data-stu-id="33840-133">How To Assign a Device Handler to a Device</span></span>](how-to-assign-a-device-handler-to-a-device.md)
-   [<span data-ttu-id="33840-134">Come specificare un'icona, un'etichetta o un gestore di dispositivo per un dispositivo usando un gruppo di dispositivi</span><span class="sxs-lookup"><span data-stu-id="33840-134">How To Specify an Icon, Label, or Device Handler for a Device Using a Device Group</span></span>](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-group.md)
-   [<span data-ttu-id="33840-135">Come specificare un'icona, un'etichetta o un gestore di dispositivo per un dispositivo usando una classe Device</span><span class="sxs-lookup"><span data-stu-id="33840-135">How To Specify an Icon, Label, or Device Handler for a Device Using a Device Class</span></span>](how-to-specify-an-icon--label--or-device-handler-for-a-device-using-a-device-class.md)
-   [<span data-ttu-id="33840-136">Come impedire AutoPlay per un componente</span><span class="sxs-lookup"><span data-stu-id="33840-136">How To Prevent AutoPlay for a Component</span></span>](how-to-prevent-autoplay-for-a-component.md)
-   [<span data-ttu-id="33840-137">Come registrare un gestore per un evento del dispositivo</span><span class="sxs-lookup"><span data-stu-id="33840-137">How To Register a Handler for a Device Event</span></span>](how-to-register-a-handler-for-a-device-event.md)
-   [<span data-ttu-id="33840-138">Come usare gli eventi AutoPlay nelle applicazioni in esecuzione</span><span class="sxs-lookup"><span data-stu-id="33840-138">How To Use AutoPlay Events in Running Applications</span></span>](how-to-use-autoplay-events-in-running-applications.md)
-   [<span data-ttu-id="33840-139">Come registrare un gestore eventi</span><span class="sxs-lookup"><span data-stu-id="33840-139">How To Register an Event Handler</span></span>](how-to-register-an-event-handler.md)

## <a name="how-autoplay-searches-media"></a><span data-ttu-id="33840-140">Modalità di ricerca di AutoPlay nei supporti</span><span class="sxs-lookup"><span data-stu-id="33840-140">How AutoPlay Searches Media</span></span>

<span data-ttu-id="33840-141">AutoPlay Cerca i media di quattro livelli di directory sotto la directory radice per trovare i tipi di file noti.</span><span class="sxs-lookup"><span data-stu-id="33840-141">AutoPlay searches for media four directory levels below the root directory to find known file types.</span></span> <span data-ttu-id="33840-142">Usa il valore PerceivedType associato a un'estensione del nome di file nel registro di sistema per determinare la categoria di file, sia che si tratti di un'immagine, di un file audio o di un file video.</span><span class="sxs-lookup"><span data-stu-id="33840-142">It uses the PerceivedType value associated with a file name extension in the registry to determine the file category, whether it is an image, an audio file, or a video file.</span></span> <span data-ttu-id="33840-143">Con queste informazioni, AutoPlay avvia il gestore appropriato per il dispositivo e il tipo di file.</span><span class="sxs-lookup"><span data-stu-id="33840-143">With this information, AutoPlay launches the appropriate handler for that device and file type.</span></span> <span data-ttu-id="33840-144">Per ulteriori informazioni, vedere la pagina relativa alla [registrazione delle applicazioni e dei tipi percepiti](fa-perceivedtypes.md).</span><span class="sxs-lookup"><span data-stu-id="33840-144">For more information, see [Perceived Types and Application Registration](fa-perceivedtypes.md).</span></span>

## <a name="defining-single-and-mixed-content-types"></a><span data-ttu-id="33840-145">Definizione di tipi di contenuto singoli e misti</span><span class="sxs-lookup"><span data-stu-id="33840-145">Defining Single and Mixed Content Types</span></span>

<span data-ttu-id="33840-146">AutoPlay definisce tre categorie di contenuto principali.</span><span class="sxs-lookup"><span data-stu-id="33840-146">AutoPlay defines three main content categories.</span></span>

-   <span data-ttu-id="33840-147">Immagini</span><span class="sxs-lookup"><span data-stu-id="33840-147">Pictures</span></span>
-   <span data-ttu-id="33840-148">Musica</span><span class="sxs-lookup"><span data-stu-id="33840-148">Music</span></span>
-   <span data-ttu-id="33840-149">Video</span><span class="sxs-lookup"><span data-stu-id="33840-149">Video</span></span>

<span data-ttu-id="33840-150">Se tutti i file nel supporto rientrano in una sola di queste tre categorie, viene considerato un supporto di tipo contenuto singolo.</span><span class="sxs-lookup"><span data-stu-id="33840-150">A medium is considered to contain a single content type if all of the files on the medium fall into only one of these three categories.</span></span> <span data-ttu-id="33840-151">Si noti che questo non significa che i file devono avere lo stesso tipo di *file* ; jpg, gif e BMP sono tipi di file diversi, ma un tipo di contenuto (immagini).</span><span class="sxs-lookup"><span data-stu-id="33840-151">Note that this does not mean that the files must be of the same *file* type; .jpg, .gif, and .bmp are different file types, but one content type (pictures).</span></span>

<span data-ttu-id="33840-152">Se i tipi di contenuto supportati sono presenti sul supporto, ma nessun tipo di contenuto singolo può tenere conto del 100% del totale, il supporto viene considerato che contiene il tipo di contenuto misto e viene gestito di conseguenza.</span><span class="sxs-lookup"><span data-stu-id="33840-152">If supported content types are present on the medium, but no single content type can account for 100 percent of the total, then the medium is considered to contain mixed content type and is handled accordingly.</span></span> <span data-ttu-id="33840-153">Per ulteriori informazioni, vedere [gestione di supporti contenenti tipi di contenuto misti](#handling-media-containing-mixed-content-types).</span><span class="sxs-lookup"><span data-stu-id="33840-153">For more information, see [Handling Media Containing Mixed Content Types](#handling-media-containing-mixed-content-types).</span></span>

## <a name="sample-scenarios"></a><span data-ttu-id="33840-154">Scenari di esempio</span><span class="sxs-lookup"><span data-stu-id="33840-154">Sample Scenarios</span></span>

<span data-ttu-id="33840-155">Negli scenari seguenti viene fornita una conoscenza di base di ciò che si prevede da AutoPlay.</span><span class="sxs-lookup"><span data-stu-id="33840-155">The following scenarios provide a basic understanding of what to expect from AutoPlay.</span></span>

### <a name="autoplay-for-storage-devices-with-picture-media"></a><span data-ttu-id="33840-156">AutoPlay per i dispositivi di archiviazione con supporti immagine</span><span class="sxs-lookup"><span data-stu-id="33840-156">AutoPlay for Storage Devices with Picture Media</span></span>

1.  <span data-ttu-id="33840-157">L'utente connette un dispositivo USB SanDisk CompactFlash Reader che dispone già di un supporto inserito contenente il tipo di contenuto immagine del 100% sotto forma di file con estensione jpg.</span><span class="sxs-lookup"><span data-stu-id="33840-157">The user attaches a USB SanDisk CompactFlash reader device that already has media inserted containing 100 percent picture content type in the form of .jpg files.</span></span>
2.  <span data-ttu-id="33840-158">Sono stati **trovati nuovi componenti hardware-SanDisk ImageMate**.</span><span class="sxs-lookup"><span data-stu-id="33840-158">Notification displays **Found New Hardware - SanDisk ImageMate**.</span></span>
3.  <span data-ttu-id="33840-159">AutoPlay avvia l'applicazione di immagine appropriata.</span><span class="sxs-lookup"><span data-stu-id="33840-159">AutoPlay launches the appropriate image application.</span></span>

<span data-ttu-id="33840-160">Analogamente, quando l'utente inserisce lo stesso supporto CompactFlash nel lettore quando il lettore è già collegato al sistema, l'evento media INSERT fa sì che AutoPlay avvii l'applicazione di presentazione dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="33840-160">Similarly, when the user inserts that same CompactFlash media into the reader when the reader is already attached to the system, the media insert event also causes AutoPlay to launch the image slide show application.</span></span> <span data-ttu-id="33840-161">L'utente ha la possibilità di passare alla pagina delle proprietà del dispositivo multimediale SanDisk per modificare il valore predefinito in un'altra applicazione di riproduzione automatica registrata, ad esempio la procedura guidata per lo scanner e la fotocamera o l'immagine.</span><span class="sxs-lookup"><span data-stu-id="33840-161">The user has the option of going to the Properties page of the SanDisk media device to change the default to another registered AutoPlay application, such as the Scanner and Camera Wizard or Picture It!.</span></span>

### <a name="autoplay-for-music-file-playback-devices-and-storage-devices-containing-music-media"></a><span data-ttu-id="33840-162">AutoPlay per la riproduzione di file musicali e dispositivi di archiviazione contenenti supporti musicali</span><span class="sxs-lookup"><span data-stu-id="33840-162">AutoPlay for Music File Playback Devices and Storage Devices Containing Music Media</span></span>

1.  <span data-ttu-id="33840-163">L'utente connette un lettore USB Diamond Rio MP3.</span><span class="sxs-lookup"><span data-stu-id="33840-163">The user attaches a USB Diamond Rio MP3 Player.</span></span>
2.  <span data-ttu-id="33840-164">Viene visualizzato un **nuovo lettore hardware Diamond Rio MP3**.</span><span class="sxs-lookup"><span data-stu-id="33840-164">Notification displays **Found New Hardware - Diamond Rio MP3 Player**.</span></span>
3.  <span data-ttu-id="33840-165">AutoPlay riproduce i file utilizzando il gestore predefinito registrato, ad esempio Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="33840-165">AutoPlay plays the files using its registered default handler—for instance, Windows Media Player.</span></span>

<span data-ttu-id="33840-166">Analogamente, se l'utente inserisce contenuti multimediali contenenti file con estensione MP3 (ad esempio, CompactFlash, SmartMedia, Memory Stick o CD-ROM) che rappresentano il 100% del contenuto supportato totale in un dispositivo di archiviazione, l'evento media INSERT genera anche la riproduzione automatica dei file con Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="33840-166">Similarly, if the user inserts any media containing .mp3 files (for example, CompactFlash, SmartMedia, Memory Stick, or CD-ROM) that account for 100 percent of the total supported content into a storage device, the media insert event would also cause AutoPlay to play the files using the Windows Media Player.</span></span> <span data-ttu-id="33840-167">L'utente può accedere alla finestra delle proprietà del dispositivo di archiviazione e modificare l'azione predefinita in un'altra applicazione AutoPlay registrata, ad esempio WinAmp o Real Player.</span><span class="sxs-lookup"><span data-stu-id="33840-167">The user can access the property sheet of the storage device and change the default action to another registered AutoPlay application, such as WinAmp or Real Player.</span></span>

### <a name="autoplay-for-video-playback-on-first-presentation"></a><span data-ttu-id="33840-168">AutoPlay per la riproduzione video nella prima presentazione</span><span class="sxs-lookup"><span data-stu-id="33840-168">AutoPlay for Video Playback on First Presentation</span></span>

1.  <span data-ttu-id="33840-169">L'utente inserisce una videocamera digitale 1394 per la prima volta.</span><span class="sxs-lookup"><span data-stu-id="33840-169">The user plugs in a 1394 digital video camera for the first time.</span></span>
2.  <span data-ttu-id="33840-170">All'utente viene visualizzata una semplice finestra di dialogo in cui viene chiesto quale applicazione eseguire.</span><span class="sxs-lookup"><span data-stu-id="33840-170">The user is presented with a simple dialog box that asks what application to run.</span></span> <span data-ttu-id="33840-171">È possibile scegliere di eseguire una delle applicazioni AutoPlay registrate o di aprire una cartella per visualizzare i file.</span><span class="sxs-lookup"><span data-stu-id="33840-171">The choices are to run one of the registered AutoPlay applications or to open a folder to view files.</span></span> <span data-ttu-id="33840-172">L'utente può impostare il comportamento selezionato in modo che venga salvato come azione predefinita per gli eventi di collegamento rapido della fotocamera video digitale successiva.</span><span class="sxs-lookup"><span data-stu-id="33840-172">The user may set the selected behavior to be saved as the default action for later digital video camera hot-plug events.</span></span>

## <a name="assigning-default-handler-applications"></a><span data-ttu-id="33840-173">Assegnazione di applicazioni gestore predefinite</span><span class="sxs-lookup"><span data-stu-id="33840-173">Assigning Default Handler Applications</span></span>

<span data-ttu-id="33840-174">Una nuova installazione di Windows trova AutoPlay con un set di applicazioni gestore registrate.</span><span class="sxs-lookup"><span data-stu-id="33840-174">A fresh installation of Windows finds AutoPlay with a set of registered handler applications.</span></span> <span data-ttu-id="33840-175">Le applicazioni registrate per impostazione predefinita durante un'installazione di Windows sono le seguenti.</span><span class="sxs-lookup"><span data-stu-id="33840-175">Applications registered by default during a Windows installation are as follows.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="33840-176">Tipo supporto</span><span class="sxs-lookup"><span data-stu-id="33840-176">Media Type</span></span></th>
<th><span data-ttu-id="33840-177">Applicazioni</span><span class="sxs-lookup"><span data-stu-id="33840-177">Applications</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33840-178">Immagini</span><span class="sxs-lookup"><span data-stu-id="33840-178">Pictures</span></span></td>
<td><ul>
<li><span data-ttu-id="33840-179">Slide Show (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="33840-179">Slide Show (default)</span></span></li>
<li><span data-ttu-id="33840-180">Creazione guidata fotocamera e scanner</span><span class="sxs-lookup"><span data-stu-id="33840-180">Camera and Scanner Wizard</span></span></li>
<li><span data-ttu-id="33840-181">Stampa guidata</span><span class="sxs-lookup"><span data-stu-id="33840-181">Printing Wizard</span></span></li>
<li><span data-ttu-id="33840-182">Aprire la cartella</span><span class="sxs-lookup"><span data-stu-id="33840-182">Open folder</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33840-183">Musica</span><span class="sxs-lookup"><span data-stu-id="33840-183">Music</span></span></td>
<td><ul>
<li><span data-ttu-id="33840-184">Windows Media Player (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="33840-184">Windows Media Player (default)</span></span></li>
<li><span data-ttu-id="33840-185">Aprire la cartella</span><span class="sxs-lookup"><span data-stu-id="33840-185">Open folder</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33840-186">Video</span><span class="sxs-lookup"><span data-stu-id="33840-186">Video</span></span></td>
<td><ul>
<li><span data-ttu-id="33840-187">Windows Media Player (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="33840-187">Windows Media Player (default)</span></span></li>
<li><span data-ttu-id="33840-188">Aprire la cartella</span><span class="sxs-lookup"><span data-stu-id="33840-188">Open folder</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="33840-189">Nel caso di tipi non supportati, agli utenti viene richiesto di assegnare l'impostazione predefinita per l'azione AutoPlay associata a ogni dispositivo di archiviazione alla prima introduzione al sistema.</span><span class="sxs-lookup"><span data-stu-id="33840-189">In the case of non-supported types, users are asked to assign the default setting for the AutoPlay action associated with each storage device on its first introduction to the system.</span></span> <span data-ttu-id="33840-190">A questo punto, all'utente viene richiesto di scegliere un'azione da un elenco fornito di applicazioni registrate o di visualizzare una visualizzazione di cartelle in cui è elencato il contenuto multimediale.</span><span class="sxs-lookup"><span data-stu-id="33840-190">At that time, the user is prompted to choose an action from a provided list of registered applications or to display a folder view listing the media content.</span></span> <span data-ttu-id="33840-191">L'utente ha anche la possibilità di scegliere di essere richiesto ogni volta che viene rilevato il tipo di supporto, anziché salvare un'applicazione specifica come predefinita.</span><span class="sxs-lookup"><span data-stu-id="33840-191">The user also has the option of choosing to be prompted each time the media type is detected rather than saving any particular application as a default.</span></span>

> [!Note]  
> <span data-ttu-id="33840-192">I produttori di dispositivi hanno la possibilità di registrare e assegnare applicazioni predefinite da usare con i prodotti specifici.</span><span class="sxs-lookup"><span data-stu-id="33840-192">Device manufacturers have the option of registering and assigning default applications to be used with their particular products.</span></span> <span data-ttu-id="33840-193">In questi casi, la finestra di dialogo che offre una scelta all'utente non viene visualizzata.</span><span class="sxs-lookup"><span data-stu-id="33840-193">In these cases, the dialog box offering a choice to the user is not displayed.</span></span>

 

<span data-ttu-id="33840-194">Per essere offerta come opzione del gestore da AutoPlay, le applicazioni appena installate devono registrarsi nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="33840-194">To be offered as a handler option by AutoPlay, newly installed applications must register themselves in the registry.</span></span> <span data-ttu-id="33840-195">Per informazioni dettagliate, vedere [preparazione dell'hardware e del software per l'uso con AutoPlay](#preparing-hardware-and-software-for-use-with-autoplay).</span><span class="sxs-lookup"><span data-stu-id="33840-195">For details, see [Preparing Hardware and Software for Use with AutoPlay](#preparing-hardware-and-software-for-use-with-autoplay).</span></span>

<span data-ttu-id="33840-196">Gli utenti possono sempre modificare il gestore AutoPlay predefinito per qualsiasi dispositivo di archiviazione o tipo di contenuto.</span><span class="sxs-lookup"><span data-stu-id="33840-196">Users can always change the default AutoPlay handler for any storage device or content type.</span></span> <span data-ttu-id="33840-197">La pagina delle proprietà AutoPlay è accessibile per le modifiche nella finestra delle proprietà del dispositivo di archiviazione in **computer locale**.</span><span class="sxs-lookup"><span data-stu-id="33840-197">The AutoPlay property page is accessible for change in the property sheet of the storage device in **My Computer**.</span></span>

<span data-ttu-id="33840-198">Per esempi di richieste utente e pagine delle proprietà, vedere [AutoPlay User Interfaces](#autoplay-user-interfaces).</span><span class="sxs-lookup"><span data-stu-id="33840-198">For examples of user prompts and property pages, see [AutoPlay User Interfaces](#autoplay-user-interfaces).</span></span>

## <a name="handling-media-containing-mixed-content-types"></a><span data-ttu-id="33840-199">Gestione di supporti contenenti tipi di contenuto misto</span><span class="sxs-lookup"><span data-stu-id="33840-199">Handling Media Containing Mixed Content Types</span></span>

<span data-ttu-id="33840-200">Quando AutoPlay viene visualizzato con un supporto misto per il contenuto, richiede l'input dell'utente prima di poter eseguire un'azione.</span><span class="sxs-lookup"><span data-stu-id="33840-200">When AutoPlay is presented with a mixed content medium, it requires user input before it can take action.</span></span> <span data-ttu-id="33840-201">In questo caso, all'utente viene visualizzata una finestra di dialogo contenente un elenco filtrato di tutte le applicazioni registrate appropriate disponibili per i tipi di contenuto presenti nei supporti.</span><span class="sxs-lookup"><span data-stu-id="33840-201">In this case, the user is presented with a dialog box containing a filtered list of all appropriate registered applications available for the content types present on the media.</span></span> <span data-ttu-id="33840-202">L'utente può scegliere una di queste applicazioni per AutoPlay quel particolare tipo di contenuto, mentre il resto rimane invariato.</span><span class="sxs-lookup"><span data-stu-id="33840-202">The user can choose one of these applications to AutoPlay that particular content type, while the rest remain untouched.</span></span> <span data-ttu-id="33840-203">Poiché la composizione di un supporto di contenuto misto varia a seconda del singolo disco, non è possibile salvare questa opzione come impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="33840-203">As the composition of mixed content media varies with each individual disc, there is no option to save this choice as a default.</span></span>

<span data-ttu-id="33840-204">Per esempi di prompt utente, vedere [interfacce utente AutoPlay](#autoplay-user-interfaces).</span><span class="sxs-lookup"><span data-stu-id="33840-204">For examples of user prompts, see [AutoPlay User Interfaces](#autoplay-user-interfaces).</span></span>

## <a name="autoplay-user-interfaces"></a><span data-ttu-id="33840-205">Interfacce utente AutoPlay</span><span class="sxs-lookup"><span data-stu-id="33840-205">AutoPlay User Interfaces</span></span>

<span data-ttu-id="33840-206">Sono disponibili tre interfacce utente possibili.</span><span class="sxs-lookup"><span data-stu-id="33840-206">There are three possible user interfaces.</span></span>

-   <span data-ttu-id="33840-207">Finestra di dialogo in cui viene richiesto all'utente di immettere un'azione per un singolo tipo di contenuto</span><span class="sxs-lookup"><span data-stu-id="33840-207">A dialog box that prompts the user to enter an action for a single content type</span></span>
-   <span data-ttu-id="33840-208">Finestra di dialogo in cui viene richiesto all'utente di immettere un'azione per i tipi di contenuto misto</span><span class="sxs-lookup"><span data-stu-id="33840-208">A dialog box that prompts the user to enter an action for mixed content types</span></span>
-   <span data-ttu-id="33840-209">Una pagina delle proprietà</span><span class="sxs-lookup"><span data-stu-id="33840-209">A property page</span></span>

### <a name="single-content-type-dialog-box"></a><span data-ttu-id="33840-210">Finestra di dialogo tipo di contenuto singolo</span><span class="sxs-lookup"><span data-stu-id="33840-210">Single Content Type Dialog Box</span></span>

<span data-ttu-id="33840-211">Una finestra di dialogo simile alla seguente viene visualizzata quando un supporto supportato non ancora assegnato a un'azione AutoPlay predefinita viene presentato al sistema.</span><span class="sxs-lookup"><span data-stu-id="33840-211">A dialog box similar to the following is displayed when any supported media not yet assigned a default AutoPlay action is presented to the system.</span></span>

![screenshot della finestra di dialogo tipo di contenuto singolo](images/pix.png)

<span data-ttu-id="33840-213">Gli utenti possono eseguire una delle operazioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="33840-213">Users can do one of the following.</span></span>

-   <span data-ttu-id="33840-214">Scegliere un'azione dall'elenco di applicazioni registrate.</span><span class="sxs-lookup"><span data-stu-id="33840-214">Choose an action from the list of registered applications.</span></span>
-   <span data-ttu-id="33840-215">Elencare i file sul supporto in una normale visualizzazione cartelle.</span><span class="sxs-lookup"><span data-stu-id="33840-215">List the files on the medium in a normal folder view.</span></span>
-   <span data-ttu-id="33840-216">Non eseguire alcuna azione.</span><span class="sxs-lookup"><span data-stu-id="33840-216">Take no action.</span></span>

<span data-ttu-id="33840-217">Un utente può anche salvare una scelta come azione predefinita per questo supporto facendo clic sulla casella **Esegui sempre l'azione selezionata** .</span><span class="sxs-lookup"><span data-stu-id="33840-217">A user can also save a choice as the default action for this medium by clicking the **Always do the selected action** box.</span></span> <span data-ttu-id="33840-218">Una volta effettuata questa scelta, la finestra di dialogo non viene visualizzata nuovamente.</span><span class="sxs-lookup"><span data-stu-id="33840-218">Once this choice is made, the dialog is not shown again.</span></span> <span data-ttu-id="33840-219">Tuttavia, in Windows XP Service Pack 1 (SP1), se al computer viene aggiunta una nuova applicazione in grado di gestire un particolare tipo di supporto, la finestra di dialogo viene nuovamente presentata all'utente, offrendo loro la possibilità di selezionare la nuova applicazione come azione AutoPlay predefinita.</span><span class="sxs-lookup"><span data-stu-id="33840-219">However, in Windows XP Service Pack 1 (SP1), if a new application that can handle a particular media type is added to the computer, the dialog is once again presented to the user, giving them the opportunity to select the new application as the default AutoPlay action.</span></span> <span data-ttu-id="33840-220">Le applicazioni possono inoltre impostare se stesse come selezione predefinita al momento dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="33840-220">Applications can also set themselves as the default selection when they are installed.</span></span>

<span data-ttu-id="33840-221">Windows XP SP1 aggiunge inoltre una funzionalità che mantiene la scelta dell'azione AutoPlay da parte dell'utente se non fa clic sulla casella **Esegui sempre l'azione selezionata** .</span><span class="sxs-lookup"><span data-stu-id="33840-221">Windows XP SP1 also adds a feature that retains the user's choice of AutoPlay action if they do not click the **Always do the selected action** box.</span></span> <span data-ttu-id="33840-222">Se un utente sceglie un'azione AutoPlay per una singola istanza, alla successiva visualizzazione della finestra di dialogo per quel tipo di supporto, la stessa azione è la selezione predefinita.</span><span class="sxs-lookup"><span data-stu-id="33840-222">If a user chooses an AutoPlay action for a single instance, the next time that dialog is presented for that media type, the same action is the default selection.</span></span>

<span data-ttu-id="33840-223">Per includere un'applicazione nell'elenco delle azioni possibili, è necessario registrarla con AutoPlay.</span><span class="sxs-lookup"><span data-stu-id="33840-223">For an application to be included in the list of possible actions, it must be registered with AutoPlay.</span></span> <span data-ttu-id="33840-224">Per altre informazioni, vedere [preparazione dell'hardware e del software per l'uso con AutoPlay](#preparing-hardware-and-software-for-use-with-autoplay).</span><span class="sxs-lookup"><span data-stu-id="33840-224">For more information, see [Preparing Hardware and Software for Use with AutoPlay](#preparing-hardware-and-software-for-use-with-autoplay).</span></span>

### <a name="mixed-media-dialog-box"></a><span data-ttu-id="33840-225">Finestra di dialogo supporto misto</span><span class="sxs-lookup"><span data-stu-id="33840-225">Mixed Media Dialog Box</span></span>

<span data-ttu-id="33840-226">La finestra di dialogo seguente viene visualizzata quando al sistema vengono presentati tutti i supporti che contengono una combinazione di tipi di file supportati.</span><span class="sxs-lookup"><span data-stu-id="33840-226">The following dialog box is displayed when any medium containing a mix of supported file types is presented to the system.</span></span> <span data-ttu-id="33840-227">Si tratta essenzialmente della finestra di dialogo Media contenuto singolo, ma con due differenze significative.</span><span class="sxs-lookup"><span data-stu-id="33840-227">This is essentially the same as the single content medium dialog box but with two significant differences.</span></span> <span data-ttu-id="33840-228">In primo luogo, le opzioni di azione disponibili sono costituite da un elenco filtrato di applicazioni rilevanti per tutti i tipi di contenuto presenti sul supporto.</span><span class="sxs-lookup"><span data-stu-id="33840-228">First, the available action options consist of a filtered list of applications relevant to all content types present on the medium.</span></span> <span data-ttu-id="33840-229">In secondo luogo, non è possibile scegliere un'azione predefinita permanente perché i tipi di contenuto e le percentuali di supporti di contenuto misto sono troppo imprevedibili.</span><span class="sxs-lookup"><span data-stu-id="33840-229">Second, there is no option to choose a permanent default action because the content types and percentages of mixed content media are too unpredictable.</span></span>

![screenshot della finestra di dialogo supporto misto](images/mix.png)

<span data-ttu-id="33840-231">Per includere un'applicazione nell'elenco delle azioni possibili, è necessario registrarla con AutoPlay.</span><span class="sxs-lookup"><span data-stu-id="33840-231">For an application to be included in the list of possible actions, it must be registered with AutoPlay.</span></span> <span data-ttu-id="33840-232">Per altre informazioni, vedere [preparazione dell'hardware e del software per l'uso con AutoPlay](#preparing-hardware-and-software-for-use-with-autoplay).</span><span class="sxs-lookup"><span data-stu-id="33840-232">For more information, see [Preparing Hardware and Software for Use with AutoPlay](#preparing-hardware-and-software-for-use-with-autoplay).</span></span>

### <a name="property-page"></a><span data-ttu-id="33840-233">Pagina Proprietà</span><span class="sxs-lookup"><span data-stu-id="33840-233">Property Page</span></span>

<span data-ttu-id="33840-234">Di seguito è riportato un esempio di pagina delle proprietà AutoPlay per un dispositivo DVD/CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="33840-234">The following is a sample AutoPlay property page for a DVD/CD-ROM device.</span></span>

![screenshot della pagina delle proprietà](images/apdlg.png)

<span data-ttu-id="33840-236">Ogni tipo di dispositivo offre un subset appropriato di tipi di contenuto per la configurazione AutoPlay.</span><span class="sxs-lookup"><span data-stu-id="33840-236">Each device type offers an appropriate subset of content types for AutoPlay configuration.</span></span> <span data-ttu-id="33840-237">A sua volta, ogni tipo di contenuto, se selezionato, offre un elenco appropriato di opzioni di azione nella casella di riepilogo.</span><span class="sxs-lookup"><span data-stu-id="33840-237">In turn, each content type, when selected, offers an appropriate list of action options in the list box.</span></span> <span data-ttu-id="33840-238">È possibile scegliere un'azione diversa per ogni tipo di contenuto.</span><span class="sxs-lookup"><span data-stu-id="33840-238">A different action can be chosen for each content type.</span></span>

 

 



