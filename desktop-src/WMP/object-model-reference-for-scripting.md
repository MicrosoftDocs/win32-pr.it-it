---
title: Riferimento del modello a oggetti per lo scripting
description: Riferimento del modello a oggetti per lo scripting
ms.assetid: a900fd55-2213-46db-84ad-93f199c60182
keywords:
- Windows Media Player, modello a oggetti
- Windows Media Player Mobile, modello a oggetti
- Modello a oggetti di Windows Media Player, riferimento
- modello a oggetti, riferimento
- Controllo ActiveX, riferimento
- Controllo ActiveX di Windows Media Player, riferimento
- Controllo ActiveX Windows Media Player Mobile, riferimento
- riferimento per il modello a oggetti, Scripting
- Windows Media Player, informazioni di riferimento sugli script
- Windows Media Player Mobile, informazioni di riferimento sugli script
- Modello a oggetti di Windows Media Player, riferimento di scripting
- modello a oggetti, riferimento di scripting
- Controllo ActiveX di Windows Media Player, riferimento di scripting
- Controllo ActiveX Windows Media Player Mobile, riferimenti per script
- Controllo ActiveX, riferimento di scripting
- riferimento al modello a oggetti di scripting
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f20e5bacf6a1fd93579ce40e8957b7ce7aefae0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298701"
---
# <a name="object-model-reference-for-scripting"></a><span data-ttu-id="16796-119">Riferimento del modello a oggetti per lo scripting</span><span class="sxs-lookup"><span data-stu-id="16796-119">Object Model Reference for Scripting</span></span>

<span data-ttu-id="16796-120">Il riferimento del modello a oggetti per lo scripting contiene informazioni dettagliate sul modello a oggetti del controllo ActiveX di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="16796-120">The object model reference for scripting contains detailed information about the Windows Media Player ActiveX control object model.</span></span> <span data-ttu-id="16796-121">Le informazioni contenute in questa sezione sono illustrate in uno stile progettato per l'utilizzo con linguaggi di script come Microsoft JScript.</span><span class="sxs-lookup"><span data-stu-id="16796-121">The information in this section is presented in a style designed for use with script languages like Microsoft JScript.</span></span>

> [!Note]  
> <span data-ttu-id="16796-122">Tutti i metodi, le proprietà e gli eventi sono completamente supportati in Windows Media Player 10 mobile o versioni successive, a meno che non venga dichiarato in modo esplicito.</span><span class="sxs-lookup"><span data-stu-id="16796-122">All methods, properties, and events are fully supported in Windows Media Player 10 Mobile or later unless explicitly stated otherwise.</span></span>

 

<span data-ttu-id="16796-123">Il riferimento del modello a oggetti per lo scripting contiene la documentazione relativa agli oggetti seguenti e ai relativi metodi, proprietà ed eventi associati.</span><span class="sxs-lookup"><span data-stu-id="16796-123">The object model reference for scripting contains documentation for the following objects and their associated methods, properties, and events.</span></span>



| <span data-ttu-id="16796-124">Oggetto</span><span class="sxs-lookup"><span data-stu-id="16796-124">Object</span></span>                                              | <span data-ttu-id="16796-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16796-125">Description</span></span>                                                                                                                                                                                    |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="16796-126">Cdrom</span><span class="sxs-lookup"><span data-stu-id="16796-126">Cdrom</span></span>](cdrom-object.md)                           | <span data-ttu-id="16796-127">Metodi e proprietà per accedere a un CD o DVD nell'unità.</span><span class="sxs-lookup"><span data-stu-id="16796-127">Methods and properties for accessing a CD or DVD in its drive.</span></span>                                                                                                                                 |
| [<span data-ttu-id="16796-128">Cdromcollection</span><span class="sxs-lookup"><span data-stu-id="16796-128">CdromCollection</span></span>](cdromcollection-object.md)       | <span data-ttu-id="16796-129">Metodi e proprietà per accedere a una raccolta di unità CD o DVD.</span><span class="sxs-lookup"><span data-stu-id="16796-129">Methods and properties for accessing a collection of CD or DVD drives.</span></span>                                                                                                                         |
| [<span data-ttu-id="16796-130">ClosedCaption</span><span class="sxs-lookup"><span data-stu-id="16796-130">ClosedCaption</span></span>](closedcaption-object.md)           | <span data-ttu-id="16796-131">Proprietà per l'inclusione di didascalie con un elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="16796-131">Properties for including captions with a media item.</span></span>                                                                                                                                           |
| [<span data-ttu-id="16796-132">Controlli</span><span class="sxs-lookup"><span data-stu-id="16796-132">Controls</span></span>](controls-object.md)                     | <span data-ttu-id="16796-133">Metodi e proprietà che rappresentano i controlli di trasporto di Windows Media Player, ad esempio Play, stop e pause.</span><span class="sxs-lookup"><span data-stu-id="16796-133">Methods and properties representing the transport controls of Windows Media Player, such as Play, Stop, and Pause.</span></span>                                                                             |
| [<span data-ttu-id="16796-134">DVD</span><span class="sxs-lookup"><span data-stu-id="16796-134">DVD</span></span>](dvd-object.md)                               | <span data-ttu-id="16796-135">Proprietà, metodi ed eventi per l'utilizzo di DVD.</span><span class="sxs-lookup"><span data-stu-id="16796-135">A property, methods, and events for working with DVDs.</span></span>                                                                                                                                         |
| [<span data-ttu-id="16796-136">Error (Errore) (Error (Errore)e)</span><span class="sxs-lookup"><span data-stu-id="16796-136">Error</span></span>](error-object.md)                           | <span data-ttu-id="16796-137">Metodi e proprietà che consentono di accedere a una raccolta di oggetti **ErrorItem** .</span><span class="sxs-lookup"><span data-stu-id="16796-137">Methods and properties providing access to a collection of **ErrorItem** objects.</span></span>                                                                                                              |
| [<span data-ttu-id="16796-138">ErrorItem</span><span class="sxs-lookup"><span data-stu-id="16796-138">ErrorItem</span></span>](erroritem-object.md)                   | <span data-ttu-id="16796-139">Proprietà che forniscono informazioni sugli errori.</span><span class="sxs-lookup"><span data-stu-id="16796-139">Properties that provide information about errors.</span></span>                                                                                                                                              |
| [<span data-ttu-id="16796-140">Supporti</span><span class="sxs-lookup"><span data-stu-id="16796-140">Media</span></span>](media-object.md)                           | <span data-ttu-id="16796-141">Metodi e proprietà correlati agli elementi multimediali.</span><span class="sxs-lookup"><span data-stu-id="16796-141">Methods and properties relating to media items.</span></span>                                                                                                                                                |
| [<span data-ttu-id="16796-142">Mediacollection</span><span class="sxs-lookup"><span data-stu-id="16796-142">MediaCollection</span></span>](mediacollection-object.md)       | <span data-ttu-id="16796-143">Metodi che consentono di accedere a una raccolta di oggetti **multimediali** .</span><span class="sxs-lookup"><span data-stu-id="16796-143">Methods that provide access to a collection of **Media** objects.</span></span>                                                                                                                              |
| [<span data-ttu-id="16796-144">MetadataPicture</span><span class="sxs-lookup"><span data-stu-id="16796-144">MetadataPicture</span></span>](metadatapicture-object.md)       | <span data-ttu-id="16796-145">Proprietà per il recupero di informazioni sui valori di immagine dell'attributo dei metadati **WM/Picture** .</span><span class="sxs-lookup"><span data-stu-id="16796-145">Properties for retrieving information on the image values of the **WM/Picture** metadata attribute.</span></span>                                                                                            |
| [<span data-ttu-id="16796-146">MetadataText</span><span class="sxs-lookup"><span data-stu-id="16796-146">MetadataText</span></span>](metadatatext-object.md)             | <span data-ttu-id="16796-147">Proprietà per il recupero di metadati per attributi di metadati testuali complessi.</span><span class="sxs-lookup"><span data-stu-id="16796-147">Properties for retrieving metadata for complex textual metadata attributes.</span></span>                                                                                                                    |
| [<span data-ttu-id="16796-148">Network</span><span class="sxs-lookup"><span data-stu-id="16796-148">Network</span></span>](network-object.md)                       | <span data-ttu-id="16796-149">Proprietà relative alla connessione di rete di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="16796-149">Properties relating to the network connection of Windows Media Player.</span></span>                                                                                                                         |
| [<span data-ttu-id="16796-150">Player</span><span class="sxs-lookup"><span data-stu-id="16796-150">Player</span></span>](player-object.md)                         | <span data-ttu-id="16796-151">Metodi, proprietà ed eventi a cui è possibile programmare Windows Media Player per rispondere.</span><span class="sxs-lookup"><span data-stu-id="16796-151">Methods, properties, and events that Windows Media Player can be programmed to respond to.</span></span>                                                                                                     |
| [<span data-ttu-id="16796-152">PlayerApplication</span><span class="sxs-lookup"><span data-stu-id="16796-152">PlayerApplication</span></span>](playerapplication-object.md)   | <span data-ttu-id="16796-153">Metodi e proprietà per passare tra un controllo Media Player Windows remoto e la modalità completa del lettore.</span><span class="sxs-lookup"><span data-stu-id="16796-153">Methods and properties for switching between a remoted Windows Media Player control and the full mode of the Player.</span></span> <span data-ttu-id="16796-154">Può essere usato solo con programmi C++ che incorporano il controllo in modalità remota.</span><span class="sxs-lookup"><span data-stu-id="16796-154">Can only be used with C++ programs that embed the control in remote mode.</span></span> |
| [<span data-ttu-id="16796-155">Playlist</span><span class="sxs-lookup"><span data-stu-id="16796-155">Playlist</span></span>](playlist-object.md)                     | <span data-ttu-id="16796-156">Metodi e proprietà per la modifica degli elenchi di elementi multimediali.</span><span class="sxs-lookup"><span data-stu-id="16796-156">Methods and properties for manipulating lists of media items.</span></span>                                                                                                                                  |
| [<span data-ttu-id="16796-157">PlaylistArray</span><span class="sxs-lookup"><span data-stu-id="16796-157">PlaylistArray</span></span>](playlistarray-object.md)           | <span data-ttu-id="16796-158">Un metodo e una proprietà per accedere a una raccolta di oggetti **playlist** in base al numero di indice.</span><span class="sxs-lookup"><span data-stu-id="16796-158">A method and a property for accessing a collection of **Playlist** objects by index number.</span></span>                                                                                                    |
| [<span data-ttu-id="16796-159">PlaylistCollection</span><span class="sxs-lookup"><span data-stu-id="16796-159">PlaylistCollection</span></span>](playlistcollection-object.md) | <span data-ttu-id="16796-160">Metodi per organizzare una raccolta di oggetti **playlist** .</span><span class="sxs-lookup"><span data-stu-id="16796-160">Methods for organizing a collection of **Playlist** objects.</span></span>                                                                                                                                   |
| [<span data-ttu-id="16796-161">Query</span><span class="sxs-lookup"><span data-stu-id="16796-161">Query</span></span>](query-object.md)                           | <span data-ttu-id="16796-162">Metodi per la modifica di una query composta.</span><span class="sxs-lookup"><span data-stu-id="16796-162">Methods for modifying a compound query.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="16796-163">Impostazioni</span><span class="sxs-lookup"><span data-stu-id="16796-163">Settings</span></span>](settings-object.md)                     | <span data-ttu-id="16796-164">Proprietà che consentono la specifica o il recupero delle impostazioni di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="16796-164">Properties that allow the specification or retrieval of Windows Media Player settings.</span></span>                                                                                                         |
| [<span data-ttu-id="16796-165">StringCollection</span><span class="sxs-lookup"><span data-stu-id="16796-165">StringCollection</span></span>](stringcollection-object.md)     | <span data-ttu-id="16796-166">Metodo e proprietà per la modifica di raccolte di stringhe.</span><span class="sxs-lookup"><span data-stu-id="16796-166">A method and a property for manipulating collections of strings.</span></span>                                                                                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="16796-167">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="16796-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16796-168">**Riferimento al modello a oggetti di Windows Media Player**</span><span class="sxs-lookup"><span data-stu-id="16796-168">**Windows Media Player Object Model Reference**</span></span>](windows-media-player-object-model-reference.md)
</dt> </dl>

 

 




