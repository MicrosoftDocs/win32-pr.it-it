---
title: Utilizzo di script in una pagina Web visualizzata da Firefox
description: Utilizzo di script in una pagina Web visualizzata da Firefox
ms.assetid: 0f1d21b1-1824-4ba9-9c0e-bd23ba847d9d
keywords:
- Windows Media Player, incorporamento del controllo ActiveX
- Modello a oggetti di Windows Media Player, incorporamento del controllo ActiveX
- modello a oggetti, incorporamento del controllo ActiveX
- Windows Media Player Mobile, incorporamento del controllo ActiveX
- Controllo ActiveX di Windows Media Player, incorporamento
- Controllo ActiveX Windows Media Player Mobile, incorporamento
- Controllo ActiveX, incorporamento
- Controllo ActiveX di Windows Media Player, pagine Web
- Controllo ActiveX Windows Media Player Mobile, pagine Web
- Controllo ActiveX, pagine Web
- Controllo ActiveX di Windows Media Player, esempio di scripting
- Controllo ActiveX Windows Media Player Mobile, esempio di scripting
- Controllo ActiveX, esempio di scripting
- incorporamento, pagine Web
- Incorporamento di pagine Web, esempio di scripting
- Windows Media Player, Firefox
- Modello a oggetti di Windows Media Player, Firefox
- modello a oggetti, Firefox
- Windows Media Player Mobile, Firefox
- Controllo ActiveX di Windows Media Player, Firefox
- Controllo ActiveX Windows Media Player Mobile, Firefox
- Controllo ActiveX, Firefox
- Firefox, esempio di scripting
- Incorporamento di pagine Web, Firefox
- esempio di script per l'incorporamento di pagine Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8629f87f954d12602999f76483fdd36ab279290
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/21/2019
ms.locfileid: "106299009"
---
# <a name="using-script-in-a-web-page-displayed-by-firefox"></a><span data-ttu-id="08c26-128">Utilizzo di script in una pagina Web visualizzata da Firefox</span><span class="sxs-lookup"><span data-stu-id="08c26-128">Using Script in a Web Page Displayed by Firefox</span></span>

<span data-ttu-id="08c26-129">Script in una pagina Web può usare il modello a oggetti del lettore per controllare il lettore quando l'utente interagisce con la pagina.</span><span class="sxs-lookup"><span data-stu-id="08c26-129">Script on a webpage can use the Player object model to control the Player as the user interacts with the page.</span></span> <span data-ttu-id="08c26-130">Ad esempio, l'elemento di INPUT seguente contiene uno script che imposta il volume del lettore.</span><span class="sxs-lookup"><span data-stu-id="08c26-130">For example, the following INPUT element has script that sets the Player volume.</span></span>


```HTML
<INPUT type="button" value="Vol" OnClick="ChangeVolume()"/>
 
<SCRIPT>
  function ChangeVolume()
  {
    Player.settings.volume = 90;
  }
</SCRIPT>

```



<span data-ttu-id="08c26-131">Molti degli oggetti nel modello a oggetti di Windows Media Player sono supportati da Internet Explorer e dal plug-in Firefox.</span><span class="sxs-lookup"><span data-stu-id="08c26-131">Many of the objects in the Windows Media Player object model are supported by Internet Explorer and by the Firefox plug-in.</span></span> <span data-ttu-id="08c26-132">Alcuni oggetti, tuttavia, non sono supportati dal plug-in di Firefox.</span><span class="sxs-lookup"><span data-stu-id="08c26-132">However, there are some objects that are not supported by the Firefox plug-in.</span></span> <span data-ttu-id="08c26-133">La tabella seguente elenca tutti gli oggetti nel modello a oggetti del lettore e Mostra gli oggetti supportati dal plug-in di Firefox.</span><span class="sxs-lookup"><span data-stu-id="08c26-133">The following table lists all of the objects in the Player object model and shows which objects are supported by the Firefox plug-in.</span></span>



| <span data-ttu-id="08c26-134">Oggetto</span><span class="sxs-lookup"><span data-stu-id="08c26-134">Object</span></span>                                              | <span data-ttu-id="08c26-135">Supporto di Firefox</span><span class="sxs-lookup"><span data-stu-id="08c26-135">Firefox support</span></span> |
|-----------------------------------------------------|-----------------|
| [<span data-ttu-id="08c26-136">Cdrom</span><span class="sxs-lookup"><span data-stu-id="08c26-136">Cdrom</span></span>](cdrom-object.md)                           | <span data-ttu-id="08c26-137">no</span><span class="sxs-lookup"><span data-stu-id="08c26-137">no</span></span>              |
| [<span data-ttu-id="08c26-138">Cdromcollection</span><span class="sxs-lookup"><span data-stu-id="08c26-138">CdromCollection</span></span>](cdromcollection-object.md)       | <span data-ttu-id="08c26-139">no</span><span class="sxs-lookup"><span data-stu-id="08c26-139">no</span></span>              |
| [<span data-ttu-id="08c26-140">ClosedCaption</span><span class="sxs-lookup"><span data-stu-id="08c26-140">ClosedCaption</span></span>](closedcaption-object.md)           | <span data-ttu-id="08c26-141">sì</span><span class="sxs-lookup"><span data-stu-id="08c26-141">yes</span></span>             |
| [<span data-ttu-id="08c26-142">Controlli</span><span class="sxs-lookup"><span data-stu-id="08c26-142">Controls</span></span>](controls-object.md)                     | <span data-ttu-id="08c26-143">no</span><span class="sxs-lookup"><span data-stu-id="08c26-143">no</span></span>              |
| [<span data-ttu-id="08c26-144">DVD</span><span class="sxs-lookup"><span data-stu-id="08c26-144">DVD</span></span>](dvd-object.md)                               | <span data-ttu-id="08c26-145">no</span><span class="sxs-lookup"><span data-stu-id="08c26-145">no</span></span>              |
| [<span data-ttu-id="08c26-146">Error (Errore) (Error (Errore)e)</span><span class="sxs-lookup"><span data-stu-id="08c26-146">Error</span></span>](error-object.md)                           | <span data-ttu-id="08c26-147">sì</span><span class="sxs-lookup"><span data-stu-id="08c26-147">yes</span></span>             |
| [<span data-ttu-id="08c26-148">ErrorItem</span><span class="sxs-lookup"><span data-stu-id="08c26-148">ErrorItem</span></span>](erroritem-object.md)                   | <span data-ttu-id="08c26-149">sì</span><span class="sxs-lookup"><span data-stu-id="08c26-149">yes</span></span>             |
| [<span data-ttu-id="08c26-150">Supporti</span><span class="sxs-lookup"><span data-stu-id="08c26-150">Media</span></span>](media-object.md)                           | <span data-ttu-id="08c26-151">sì</span><span class="sxs-lookup"><span data-stu-id="08c26-151">yes</span></span>             |
| [<span data-ttu-id="08c26-152">Mediacollection</span><span class="sxs-lookup"><span data-stu-id="08c26-152">MediaCollection</span></span>](mediacollection-object.md)       | <span data-ttu-id="08c26-153">no</span><span class="sxs-lookup"><span data-stu-id="08c26-153">no</span></span>              |
| [<span data-ttu-id="08c26-154">MetadataPicture</span><span class="sxs-lookup"><span data-stu-id="08c26-154">MetadataPicture</span></span>](metadatapicture-object.md)       | <span data-ttu-id="08c26-155">no</span><span class="sxs-lookup"><span data-stu-id="08c26-155">no</span></span>              |
| [<span data-ttu-id="08c26-156">MetadataText</span><span class="sxs-lookup"><span data-stu-id="08c26-156">MetadataText</span></span>](metadatatext-object.md)             | <span data-ttu-id="08c26-157">no</span><span class="sxs-lookup"><span data-stu-id="08c26-157">no</span></span>              |
| [<span data-ttu-id="08c26-158">Network</span><span class="sxs-lookup"><span data-stu-id="08c26-158">Network</span></span>](network-object.md)                       | <span data-ttu-id="08c26-159">sì</span><span class="sxs-lookup"><span data-stu-id="08c26-159">yes</span></span>             |
| [<span data-ttu-id="08c26-160">Player</span><span class="sxs-lookup"><span data-stu-id="08c26-160">Player</span></span>](player-object.md)                         | <span data-ttu-id="08c26-161">sì</span><span class="sxs-lookup"><span data-stu-id="08c26-161">yes</span></span>             |
| [<span data-ttu-id="08c26-162">PlayerApplication</span><span class="sxs-lookup"><span data-stu-id="08c26-162">PlayerApplication</span></span>](playerapplication-object.md)   | <span data-ttu-id="08c26-163">no</span><span class="sxs-lookup"><span data-stu-id="08c26-163">no</span></span>              |
| [<span data-ttu-id="08c26-164">Playlist</span><span class="sxs-lookup"><span data-stu-id="08c26-164">Playlist</span></span>](playlist-object.md)                     | <span data-ttu-id="08c26-165">sì</span><span class="sxs-lookup"><span data-stu-id="08c26-165">yes</span></span>             |
| [<span data-ttu-id="08c26-166">PlaylistArray</span><span class="sxs-lookup"><span data-stu-id="08c26-166">PlaylistArray</span></span>](playlistarray-object.md)           | <span data-ttu-id="08c26-167">no</span><span class="sxs-lookup"><span data-stu-id="08c26-167">no</span></span>              |
| [<span data-ttu-id="08c26-168">PlaylistCollection</span><span class="sxs-lookup"><span data-stu-id="08c26-168">PlaylistCollection</span></span>](playlistcollection-object.md) | <span data-ttu-id="08c26-169">no</span><span class="sxs-lookup"><span data-stu-id="08c26-169">no</span></span>              |
| [<span data-ttu-id="08c26-170">Query</span><span class="sxs-lookup"><span data-stu-id="08c26-170">Query</span></span>](query-object.md)                           | <span data-ttu-id="08c26-171">no</span><span class="sxs-lookup"><span data-stu-id="08c26-171">no</span></span>              |
| [<span data-ttu-id="08c26-172">Impostazioni</span><span class="sxs-lookup"><span data-stu-id="08c26-172">Settings</span></span>](settings-object.md)                     | <span data-ttu-id="08c26-173">sì</span><span class="sxs-lookup"><span data-stu-id="08c26-173">yes</span></span>             |
| [<span data-ttu-id="08c26-174">StringCollection</span><span class="sxs-lookup"><span data-stu-id="08c26-174">StringCollection</span></span>](stringcollection-object.md)     | <span data-ttu-id="08c26-175">no</span><span class="sxs-lookup"><span data-stu-id="08c26-175">no</span></span>              |



 

<span data-ttu-id="08c26-176">Il plug-in di Firefox supporta l'oggetto **Player** , ma alcune proprietà dell'oggetto **Player** restituiscono **null** in un browser Firefox.</span><span class="sxs-lookup"><span data-stu-id="08c26-176">The Firefox plug-in supports the **Player** object, but certain properties of the **Player** object return **NULL** in a Firefox browser.</span></span> <span data-ttu-id="08c26-177">Ad esempio, la proprietà [cdromcollection](player-cdromcollection.md) dell'oggetto **Player** restituisce **null** perché il plug-in di Firefox non supporta l'oggetto **CDROM** .</span><span class="sxs-lookup"><span data-stu-id="08c26-177">For example, the [cdromCollection](player-cdromcollection.md) property of the **Player** object returns **NULL** because the Firefox plug-in does not support the **Cdrom** object.</span></span> <span data-ttu-id="08c26-178">Analogamente, le proprietà [DVD](player-dvd.md), [mediacollection](player-mediacollection.md), [playerApplication](player-playerapplication.md)e [PlaylistCollection](player-playlistcollection.md) dell'oggetto **Player** restituiscono **null** in un browser Firefox.</span><span class="sxs-lookup"><span data-stu-id="08c26-178">Similarly, the [dvd](player-dvd.md), [mediaCollection](player-mediacollection.md), [playerApplication](player-playerapplication.md), and [playlistCollection](player-playlistcollection.md) properties of the **Player** object return **NULL** in a Firefox browser.</span></span>

<span data-ttu-id="08c26-179">La proprietà **Player. pluginVersionInfo** è supportata dal plug-in di Firefox ma non da Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="08c26-179">The **Player.pluginVersionInfo** property is supported by the Firefox plug-in but not by Internet Explorer.</span></span> <span data-ttu-id="08c26-180">Questa proprietà restituisce la versione del plug-in Firefox.</span><span class="sxs-lookup"><span data-stu-id="08c26-180">This property returns the version of the Firefox plug-in.</span></span>

<span data-ttu-id="08c26-181">Il plug-in di Firefox supporta l'oggetto **multimediale** , inclusa la proprietà [getItemInfoByType](media-getiteminfobytype.md) .</span><span class="sxs-lookup"><span data-stu-id="08c26-181">The Firefox plug-in supports the **Media** object, including the [getItemInfoByType](media-getiteminfobytype.md) property.</span></span> <span data-ttu-id="08c26-182">Tuttavia, in un browser Firefox, la proprietà **getItemInfoByType** non supporta i tipi restituiti **MetadataText** e **MetadataPicture** .</span><span class="sxs-lookup"><span data-stu-id="08c26-182">However, in a Firefox browser, the **getItemInfoByType** property does not support the **MetadataText** and **MetadataPicture** return types.</span></span>

<span data-ttu-id="08c26-183">Il plug-in di Firefox supporta l'oggetto [Settings](settings-object.md) , ad eccezione del metodo [semode](settings-setmode.md) e della proprietà [requestMediaAccessRights](settings-requestmediaaccessrights.md) .</span><span class="sxs-lookup"><span data-stu-id="08c26-183">The Firefox plug-in supports the [Settings](settings-object.md) object except for the [setMode](settings-setmode.md) method and the [requestMediaAccessRights](settings-requestmediaaccessrights.md) property.</span></span> <span data-ttu-id="08c26-184">In un browser Firefox, la proprietà **requestMediaAccessRight** restituisce sempre false.</span><span class="sxs-lookup"><span data-stu-id="08c26-184">In a Firefox browser, the **requestMediaAccessRight** property always returns false.</span></span>

## <a name="related-topics"></a><span data-ttu-id="08c26-185">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="08c26-185">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08c26-186">**Uso del controllo Media Player Windows con Firefox**</span><span class="sxs-lookup"><span data-stu-id="08c26-186">**Using the Windows Media Player Control with Firefox**</span></span>](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




