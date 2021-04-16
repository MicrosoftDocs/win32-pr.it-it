---
title: Modello a oggetti del lettore per i linguaggi di scripting
description: Modello a oggetti del lettore per i linguaggi di scripting
ms.assetid: 785c1a3a-902a-4f30-8419-bbfb11b584a3
keywords:
- Windows Media Player, modello a oggetti
- Modello a oggetti di Windows Media Player, informazioni
- modello a oggetti, informazioni
- Controllo ActiveX di Windows Media Player, modello a oggetti
- Controllo ActiveX, modello a oggetti
- Controllo ActiveX Windows Media Player Mobile, modello a oggetti
- Windows Media Player Mobile, modello a oggetti
- Software Development Kit (SDK), modello a oggetti del controllo ActiveX di Windows Media Player
- SDK (Software Development Kit), modello a oggetti del controllo ActiveX di Windows Media Player
- documentazione, modello a oggetti del controllo ActiveX di Windows Media Player
- Windows Media Player, linguaggi di scripting
- Modello a oggetti di Windows Media Player, linguaggi di scripting
- modello a oggetti, linguaggi di scripting
- Controllo ActiveX di Windows Media Player, linguaggi di scripting
- Controllo ActiveX, linguaggi di scripting
- Controllo ActiveX Windows Media Player Mobile, linguaggi di scripting
- Windows Media Player Mobile, linguaggi di scripting
- linguaggi di scripting
- Windows Media Player, oggetto Player
- Modello a oggetti di Windows Media Player, oggetto Player
- modello a oggetti, oggetto Player
- Controllo ActiveX Windows Media Player, oggetto Player
- Controllo ActiveX, oggetto Player
- Controllo ActiveX Windows Media Player Mobile, oggetto Player
- Windows Media Player Mobile, oggetto lettore
- Oggetto Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 670bff03075fd98812dbee269115e297a137e92d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104551905"
---
# <a name="player-object-model-for-scripting-languages"></a><span data-ttu-id="572ed-129">Modello a oggetti del lettore per i linguaggi di scripting</span><span class="sxs-lookup"><span data-stu-id="572ed-129">Player Object Model for Scripting Languages</span></span>

<span data-ttu-id="572ed-130">ActiveX usa il concetto di oggetti per contenere la funzionalità di programmazione.</span><span class="sxs-lookup"><span data-stu-id="572ed-130">ActiveX uses the concept of objects to contain programming functionality.</span></span> <span data-ttu-id="572ed-131">Windows Media Player utilizza diversi oggetti per dividere la funzionalità fornita dal controllo.</span><span class="sxs-lookup"><span data-stu-id="572ed-131">Windows Media Player uses several objects to divide up the functionality the control provides.</span></span> <span data-ttu-id="572ed-132">L'oggetto radice è l'oggetto **Player** e gli altri oggetti sono collegati all'oggetto **Player** tramite proprietà specifiche.</span><span class="sxs-lookup"><span data-stu-id="572ed-132">The root object is the **Player** object, and the other objects are attached to the **Player** object through specific properties.</span></span>

<span data-ttu-id="572ed-133">Il diagramma seguente illustra il funzionamento del modello a oggetti del controllo ActiveX di Windows Media Player 11 per i linguaggi di scripting.</span><span class="sxs-lookup"><span data-stu-id="572ed-133">The following diagram shows how the Windows Media Player 11 ActiveX control object model works for scripting languages.</span></span>

![diagramma del modello a oggetti di Windows Media Player 11](images/playeromdiag.png)

<span data-ttu-id="572ed-135">In C++, e talvolta nei linguaggi .NET, gli oggetti sono rappresentati da interfacce COM.</span><span class="sxs-lookup"><span data-stu-id="572ed-135">In C++, and sometimes in .NET languages, objects are represented by COM interfaces.</span></span> <span data-ttu-id="572ed-136">Nel modello a oggetti di Windows Media Player, i nomi delle interfacce COM corrispondono al nome dell'oggetto, ma sono preceduti da "IWMP".</span><span class="sxs-lookup"><span data-stu-id="572ed-136">In the Windows Media Player object model, COM interface names are the same as the object name, but are prefixed with "IWMP".</span></span> <span data-ttu-id="572ed-137">Ad esempio, l'oggetto di **rete** viene esposto tramite l'interfaccia **IWMPNetwork** .</span><span class="sxs-lookup"><span data-stu-id="572ed-137">For example, the **Network** object is exposed through the **IWMPNetwork** interface.</span></span>

<span data-ttu-id="572ed-138">Nelle sezioni seguenti vengono fornite panoramiche concettuali per ogni oggetto:</span><span class="sxs-lookup"><span data-stu-id="572ed-138">The following sections provide conceptual overviews for each object:</span></span>

-   [<span data-ttu-id="572ed-139">Informazioni sugli oggetti cdrom e cdromcollection</span><span class="sxs-lookup"><span data-stu-id="572ed-139">About the Cdrom and CdromCollection Objects</span></span>](about-the-cdrom-and-cdromcollection-objects.md)
-   [<span data-ttu-id="572ed-140">Informazioni sull'oggetto ClosedCaption</span><span class="sxs-lookup"><span data-stu-id="572ed-140">About the ClosedCaption Object</span></span>](about-the-closedcaption-object.md)
-   [<span data-ttu-id="572ed-141">Informazioni sull'oggetto Controls</span><span class="sxs-lookup"><span data-stu-id="572ed-141">About the Controls Object</span></span>](about-the-controls-object.md)
-   [<span data-ttu-id="572ed-142">Informazioni sull'oggetto DVD</span><span class="sxs-lookup"><span data-stu-id="572ed-142">About the DVD Object</span></span>](about-the-dvd-object.md)
-   [<span data-ttu-id="572ed-143">Informazioni sugli oggetti Error e ErrorItem</span><span class="sxs-lookup"><span data-stu-id="572ed-143">About the Error and ErrorItem Objects</span></span>](about-the-error-and-erroritem-objects.md)
-   [<span data-ttu-id="572ed-144">Informazioni sugli oggetti Mediacollection e media</span><span class="sxs-lookup"><span data-stu-id="572ed-144">About the MediaCollection and Media Objects</span></span>](about-the-mediacollection-and-media-objects.md)
-   [<span data-ttu-id="572ed-145">Informazioni sull'oggetto MetadataPicture</span><span class="sxs-lookup"><span data-stu-id="572ed-145">About the MetadataPicture Object</span></span>](about-the-metadatapicture-object.md)
-   [<span data-ttu-id="572ed-146">Informazioni sull'oggetto MetadataText</span><span class="sxs-lookup"><span data-stu-id="572ed-146">About the MetadataText Object</span></span>](about-the-metadatatext-object.md)
-   [<span data-ttu-id="572ed-147">Informazioni sull'oggetto di rete</span><span class="sxs-lookup"><span data-stu-id="572ed-147">About the Network Object</span></span>](about-the-network-object.md)
-   [<span data-ttu-id="572ed-148">Informazioni sull'oggetto Player</span><span class="sxs-lookup"><span data-stu-id="572ed-148">About the Player Object</span></span>](about-the-player-object.md)
-   [<span data-ttu-id="572ed-149">Informazioni sull'oggetto PlayerApplication</span><span class="sxs-lookup"><span data-stu-id="572ed-149">About the PlayerApplication Object</span></span>](about-the-playerapplication-object.md)
-   [<span data-ttu-id="572ed-150">Informazioni sugli oggetti playlist, PlaylistCollection e PlaylistArray</span><span class="sxs-lookup"><span data-stu-id="572ed-150">About the Playlist, PlaylistCollection, and PlaylistArray Objects</span></span>](about-the-playlist--playlistcollection--and-playlistarray-objects.md)
-   [<span data-ttu-id="572ed-151">Informazioni sull'oggetto query</span><span class="sxs-lookup"><span data-stu-id="572ed-151">About the Query Object</span></span>](about-the-query-object.md)
-   [<span data-ttu-id="572ed-152">Informazioni sull'oggetto Settings</span><span class="sxs-lookup"><span data-stu-id="572ed-152">About the Settings Object</span></span>](about-the-settings-object.md)
-   [<span data-ttu-id="572ed-153">Informazioni sull'oggetto StringCollection</span><span class="sxs-lookup"><span data-stu-id="572ed-153">About the StringCollection Object</span></span>](about-the-stringcollection-object.md)

<span data-ttu-id="572ed-154">Funzionalità aggiuntive sono disponibili tramite determinate interfacce COM.</span><span class="sxs-lookup"><span data-stu-id="572ed-154">Additional functionality is available through certain COM interfaces.</span></span> <span data-ttu-id="572ed-155">La possibilità di accedere a tali interfacce può dipendere dal linguaggio utilizzato per la programmazione e da altri fattori, ad esempio la modalità utilizzata per creare l'istanza del controllo Media Player di Windows.</span><span class="sxs-lookup"><span data-stu-id="572ed-155">Whether you can access these interfaces may depend on the language you use for programming and other factors, such as the mode used to create the instance of the Windows Media Player control.</span></span> <span data-ttu-id="572ed-156">Per un elenco completo delle interfacce COM esposte dal controllo Media Player Windows, vedere [riferimento del modello a oggetti per C++](object-model-reference-for-c.md).</span><span class="sxs-lookup"><span data-stu-id="572ed-156">For a complete list of COM interfaces exposed by the Windows Media Player control, see the [Object Model Reference for C++](object-model-reference-for-c.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="572ed-157">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="572ed-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="572ed-158">**Informazioni sul modello a oggetti del lettore**</span><span class="sxs-lookup"><span data-stu-id="572ed-158">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> <dt>

[<span data-ttu-id="572ed-159">**Uso del controllo Media Player di Windows in una soluzione .NET Framework**</span><span class="sxs-lookup"><span data-stu-id="572ed-159">**Using the Windows Media Player Control in a .NET Framework Solution**</span></span>](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




