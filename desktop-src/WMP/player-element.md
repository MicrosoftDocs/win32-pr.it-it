---
title: Elemento PLAYER
description: Elemento PLAYER
ms.assetid: 009090b3-0055-4700-9078-0749da239674
keywords:
- Windows Media Player Skin, elemento PLAYER
- Skin, elemento PLAYER
- Elemento PLAYER
- riferimento per Skin, elemento PLAYER
- elementi, lettore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a50eb4383eab279c28b75467a9ed803501e7720b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116873"
---
# <a name="player-element"></a><span data-ttu-id="e7c15-108">Elemento PLAYER</span><span class="sxs-lookup"><span data-stu-id="e7c15-108">PLAYER Element</span></span>

<span data-ttu-id="e7c15-109">L'elemento **Player** consente di definire i gestori eventi e di specificare la proprietà **URL** dell'oggetto **Player** in fase di progettazione all'interno di un file di definizione dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="e7c15-109">The **PLAYER** element lets you define event handlers and specify the **URL** property of the **Player** object at design time within a skin definition file.</span></span> <span data-ttu-id="e7c15-110">All'interno del codice di script, l'oggetto **Player** è accessibile tramite l'attributo globale **Player** anziché tramite un nome specificato da un attributo **ID** , che non è supportato dall'elemento **Player** .</span><span class="sxs-lookup"><span data-stu-id="e7c15-110">Within script code, the **Player** object is accessed through the **player** global attribute rather than through a name specified by an **id** attribute, which is not supported by the **PLAYER** element.</span></span>

<span data-ttu-id="e7c15-111">L'elemento **Player** supporta l'attributo seguente.</span><span class="sxs-lookup"><span data-stu-id="e7c15-111">The **PLAYER** element supports the following attribute.</span></span>



| <span data-ttu-id="e7c15-112">Attributo</span><span class="sxs-lookup"><span data-stu-id="e7c15-112">Attribute</span></span>             | <span data-ttu-id="e7c15-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e7c15-113">Description</span></span>                                          |
|-----------------------|------------------------------------------------------|
| [<span data-ttu-id="e7c15-114">URL</span><span class="sxs-lookup"><span data-stu-id="e7c15-114">URL</span></span>](player-url.md) | <span data-ttu-id="e7c15-115">Specifica o Recupera il nome del file da riprodurre.</span><span class="sxs-lookup"><span data-stu-id="e7c15-115">Specifies or retrieves the name of the file to play.</span></span> |



 

<span data-ttu-id="e7c15-116">L'elemento **Player** può implementare i gestori eventi per gli eventi seguenti generati dall'oggetto **Player** .</span><span class="sxs-lookup"><span data-stu-id="e7c15-116">The **PLAYER** element can implement event handlers for the following events fired from the **Player** object.</span></span>



| <span data-ttu-id="e7c15-117">Event</span><span class="sxs-lookup"><span data-stu-id="e7c15-117">Event</span></span>                                                                                            | <span data-ttu-id="e7c15-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e7c15-118">Description</span></span>                                                                      |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="e7c15-119">AudioLanguageChange</span><span class="sxs-lookup"><span data-stu-id="e7c15-119">AudioLanguageChange</span></span>](player-player-audiolanguagechange.md)                                     | <span data-ttu-id="e7c15-120">Si verifica in seguito alla modifica della lingua audio corrente.</span><span class="sxs-lookup"><span data-stu-id="e7c15-120">Occurs when the current audio language changes.</span></span>                                  |
| [<span data-ttu-id="e7c15-121">responseBuffering</span><span class="sxs-lookup"><span data-stu-id="e7c15-121">Buffering</span></span>](player-player-buffering.md)                                                         | <span data-ttu-id="e7c15-122">Si verifica all'inizio o alla fine del buffering di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="e7c15-122">Occurs when Windows Media Player begins or ends buffering.</span></span>                       |
| [<span data-ttu-id="e7c15-123">CdromMediaChange</span><span class="sxs-lookup"><span data-stu-id="e7c15-123">CdromMediaChange</span></span>](player-player-cdrommediachange.md)                                           | <span data-ttu-id="e7c15-124">Si verifica in seguito alla modifica del supporto CD.</span><span class="sxs-lookup"><span data-stu-id="e7c15-124">Occurs when the CD media changes.</span></span>                                                |
| [<span data-ttu-id="e7c15-125">CurrentItemChange</span><span class="sxs-lookup"><span data-stu-id="e7c15-125">CurrentItemChange</span></span>](player-player-currentitemchange.md)                                         | <span data-ttu-id="e7c15-126">Si verifica quando l'elemento corrente viene modificato.</span><span class="sxs-lookup"><span data-stu-id="e7c15-126">Occurs when the current item changes.</span></span>                                            |
| [<span data-ttu-id="e7c15-127">CurrentMediaItemAvailable</span><span class="sxs-lookup"><span data-stu-id="e7c15-127">CurrentMediaItemAvailable</span></span>](player-player-currentmediaitemavailable.md)                         | <span data-ttu-id="e7c15-128">Si verifica quando l'elemento multimediale corrente diventa disponibile.</span><span class="sxs-lookup"><span data-stu-id="e7c15-128">Occurs when the current media item becomes available.</span></span>                            |
| [<span data-ttu-id="e7c15-129">CurrentPlaylistChange</span><span class="sxs-lookup"><span data-stu-id="e7c15-129">CurrentPlaylistChange</span></span>](player-player-currentplaylistchange.md)                                 | <span data-ttu-id="e7c15-130">Si verifica quando cambia la playlist corrente.</span><span class="sxs-lookup"><span data-stu-id="e7c15-130">Occurs when the current playlist changes.</span></span>                                        |
| [<span data-ttu-id="e7c15-131">CurrentPlaylistItemAvailable</span><span class="sxs-lookup"><span data-stu-id="e7c15-131">CurrentPlaylistItemAvailable</span></span>](player-player-currentplaylistitemavailable.md)                   | <span data-ttu-id="e7c15-132">Si verifica quando l'elemento della playlist corrente diventa disponibile.</span><span class="sxs-lookup"><span data-stu-id="e7c15-132">Occurs when the current playlist item becomes available.</span></span>                         |
| [<span data-ttu-id="e7c15-133">DomainChange</span><span class="sxs-lookup"><span data-stu-id="e7c15-133">DomainChange</span></span>](player-player-domainchange.md)                                                   | <span data-ttu-id="e7c15-134">Si verifica in seguito alla modifica del dominio DVD.</span><span class="sxs-lookup"><span data-stu-id="e7c15-134">Occurs when the DVD domain changes.</span></span>                                              |
| [<span data-ttu-id="e7c15-135">Error (Errore) (Error (Errore)e)</span><span class="sxs-lookup"><span data-stu-id="e7c15-135">Error</span></span>](player-player-error.md)                                                                 | <span data-ttu-id="e7c15-136">Si verifica quando il controllo Media Player Windows presenta una condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="e7c15-136">Occurs when the Windows Media Player control has an error condition.</span></span>             |
| [<span data-ttu-id="e7c15-137">MarkerHit</span><span class="sxs-lookup"><span data-stu-id="e7c15-137">MarkerHit</span></span>](player-player-markerhit.md)                                                         | <span data-ttu-id="e7c15-138">Si verifica quando Windows Media Player rileva un marcatore nella clip.</span><span class="sxs-lookup"><span data-stu-id="e7c15-138">Occurs when Windows Media Player encounters a marker in the clip.</span></span>                |
| [<span data-ttu-id="e7c15-139">MediaChange</span><span class="sxs-lookup"><span data-stu-id="e7c15-139">MediaChange</span></span>](player-player-mediachange.md)                                                     | <span data-ttu-id="e7c15-140">Si verifica quando un elemento multimediale viene modificato.</span><span class="sxs-lookup"><span data-stu-id="e7c15-140">Occurs when a media item changes.</span></span>                                                |
| [<span data-ttu-id="e7c15-141">MediaCollectionAttributeStringAdded</span><span class="sxs-lookup"><span data-stu-id="e7c15-141">MediaCollectionAttributeStringAdded</span></span>](player-player-mediacollectionattributestringadded.md)     | <span data-ttu-id="e7c15-142">Si verifica quando un valore di attributo viene aggiunto alla libreria.</span><span class="sxs-lookup"><span data-stu-id="e7c15-142">Occurs when an attribute value is added to the library.</span></span>                          |
| [<span data-ttu-id="e7c15-143">MediaCollectionAttributeStringChanged</span><span class="sxs-lookup"><span data-stu-id="e7c15-143">MediaCollectionAttributeStringChanged</span></span>](player-player-mediacollectionattributestringchanged.md) | <span data-ttu-id="e7c15-144">Si verifica quando viene modificato un valore di attributo nella libreria.</span><span class="sxs-lookup"><span data-stu-id="e7c15-144">Occurs when an attribute value in the library is changed.</span></span>                        |
| [<span data-ttu-id="e7c15-145">MediaCollectionAttributeStringRemoved</span><span class="sxs-lookup"><span data-stu-id="e7c15-145">MediaCollectionAttributeStringRemoved</span></span>](player-player-mediacollectionattributestringremoved.md) | <span data-ttu-id="e7c15-146">Si verifica quando un valore di attributo viene rimosso dalla libreria.</span><span class="sxs-lookup"><span data-stu-id="e7c15-146">Occurs when an attribute value is removed from the library.</span></span>                      |
| [<span data-ttu-id="e7c15-147">MediaCollectionChange</span><span class="sxs-lookup"><span data-stu-id="e7c15-147">MediaCollectionChange</span></span>](player-player-mediacollectionchange.md)                                 | <span data-ttu-id="e7c15-148">Si verifica quando l'oggetto **mediacollection** viene modificato.</span><span class="sxs-lookup"><span data-stu-id="e7c15-148">Occurs when the **MediaCollection** object changes.</span></span>                              |
| [<span data-ttu-id="e7c15-149">Errore MediaError</span><span class="sxs-lookup"><span data-stu-id="e7c15-149">MediaError</span></span>](player-player-mediaerror.md)                                                       | <span data-ttu-id="e7c15-150">Si verifica quando l'oggetto **multimediale** presenta una condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="e7c15-150">Occurs when the **Media** object has an error condition.</span></span>                         |
| [<span data-ttu-id="e7c15-151">ModeChange</span><span class="sxs-lookup"><span data-stu-id="e7c15-151">ModeChange</span></span>](player-player-modechange.md)                                                       | <span data-ttu-id="e7c15-152">Si verifica quando si passa dalla modalità casuale alla modalità normale.</span><span class="sxs-lookup"><span data-stu-id="e7c15-152">Occurs when switching between shuffle and normal mode.</span></span>                           |
| [<span data-ttu-id="e7c15-153">OpenPlaylistSwitch</span><span class="sxs-lookup"><span data-stu-id="e7c15-153">OpenPlaylistSwitch</span></span>](player-player-openplaylistswitch.md)                                       | <span data-ttu-id="e7c15-154">Si verifica quando viene avviata la riproduzione di un titolo in un DVD.</span><span class="sxs-lookup"><span data-stu-id="e7c15-154">Occurs when a title on a DVD begins playing.</span></span>                                     |
| [<span data-ttu-id="e7c15-155">OpenStateChange</span><span class="sxs-lookup"><span data-stu-id="e7c15-155">OpenStateChange</span></span>](player-player-openstatechange.md)                                             | <span data-ttu-id="e7c15-156">Si verifica quando il *lettore*. **openState** modifiche.</span><span class="sxs-lookup"><span data-stu-id="e7c15-156">Occurs when *player*.**openState** changes.</span></span>                                      |
| [<span data-ttu-id="e7c15-157">PlaylistChange</span><span class="sxs-lookup"><span data-stu-id="e7c15-157">PlaylistChange</span></span>](player-player-playlistchange.md)                                               | <span data-ttu-id="e7c15-158">Si verifica in seguito alla modifica di una playlist.</span><span class="sxs-lookup"><span data-stu-id="e7c15-158">Occurs when a playlist changes.</span></span>                                                  |
| [<span data-ttu-id="e7c15-159">PlaylistCollectionChange</span><span class="sxs-lookup"><span data-stu-id="e7c15-159">PlaylistCollectionChange</span></span>](player-player-playlistcollectionchange.md)                           | <span data-ttu-id="e7c15-160">Si verifica quando viene apportata una modifica alla raccolta di playlist.</span><span class="sxs-lookup"><span data-stu-id="e7c15-160">Occurs when something changes in the playlist collection.</span></span>                        |
| [<span data-ttu-id="e7c15-161">PlaylistCollectionPlaylistAdded</span><span class="sxs-lookup"><span data-stu-id="e7c15-161">PlaylistCollectionPlaylistAdded</span></span>](player-player-playlistcollectionplaylistadded.md)             | <span data-ttu-id="e7c15-162">Si verifica quando viene aggiunta una playlist alla raccolta di playlist.</span><span class="sxs-lookup"><span data-stu-id="e7c15-162">Occurs when a playlist is added to the playlist collection.</span></span>                      |
| [<span data-ttu-id="e7c15-163">PlaylistCollectionPlaylistRemoved</span><span class="sxs-lookup"><span data-stu-id="e7c15-163">PlaylistCollectionPlaylistRemoved</span></span>](player-player-playlistcollectionplaylistremoved.md)         | <span data-ttu-id="e7c15-164">Si verifica quando una playlist viene rimossa dalla raccolta di playlist.</span><span class="sxs-lookup"><span data-stu-id="e7c15-164">Occurs when a playlist is removed from the playlist collection.</span></span>                  |
| [<span data-ttu-id="e7c15-165">PlayStateChange</span><span class="sxs-lookup"><span data-stu-id="e7c15-165">PlayStateChange</span></span>](player-player-playstatechange.md)                                             | <span data-ttu-id="e7c15-166">Si verifica quando il *lettore*. **riproduzione** modifiche.</span><span class="sxs-lookup"><span data-stu-id="e7c15-166">Occurs when *player*.**playState** changes.</span></span>                                      |
| [<span data-ttu-id="e7c15-167">PositionChange</span><span class="sxs-lookup"><span data-stu-id="e7c15-167">PositionChange</span></span>](player-player-positionchange.md)                                               | <span data-ttu-id="e7c15-168">Si verifica quando il *lettore*. *controlli*. **currentPosition** modifiche.</span><span class="sxs-lookup"><span data-stu-id="e7c15-168">Occurs when *player*.*controls*.**currentPosition** changes.</span></span>                     |
| [<span data-ttu-id="e7c15-169">ScriptCommand</span><span class="sxs-lookup"><span data-stu-id="e7c15-169">ScriptCommand</span></span>](player-player-scriptcommand.md)                                                 | <span data-ttu-id="e7c15-170">Si verifica quando Windows Media Player rileva un comando script incorporato in un file.</span><span class="sxs-lookup"><span data-stu-id="e7c15-170">Occurs when Windows Media Player encounters a script command embedded in a file.</span></span> |
| [<span data-ttu-id="e7c15-171">StatusChange</span><span class="sxs-lookup"><span data-stu-id="e7c15-171">StatusChange</span></span>](player-player-statuschange.md)                                                   | <span data-ttu-id="e7c15-172">Si verifica in seguito alla modifica del valore della proprietà **status** .</span><span class="sxs-lookup"><span data-stu-id="e7c15-172">Occurs when the **status** property changes value.</span></span>                               |



 

## <a name="related-topics"></a><span data-ttu-id="e7c15-173">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="e7c15-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7c15-174">**Oggetto Player**</span><span class="sxs-lookup"><span data-stu-id="e7c15-174">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="e7c15-175">**Informazioni di riferimento sulla programmazione dell'interfaccia**</span><span class="sxs-lookup"><span data-stu-id="e7c15-175">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 




