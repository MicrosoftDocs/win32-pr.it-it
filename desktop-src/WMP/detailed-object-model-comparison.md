---
title: Confronto dettagliato del modello a oggetti
description: Confronto dettagliato del modello a oggetti
ms.assetid: 8f08e2a6-1944-4814-b3b7-680a3722e1a0
keywords:
- Windows Media Player, modello a oggetti
- Modello a oggetti di Windows Media Player, differenze di versione
- modello a oggetti, differenze di versione
- Controllo ActiveX di Windows Media Player, differenze di versione
- Controllo ActiveX, differenze di versione
- Controllo ActiveX Windows Media Player Mobile, differenze di versione
- Windows Media Player Mobile, modello a oggetti
- Guida alla migrazione, differenze di versione
- versioni di Windows Media Player, modello a oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 086607a9d367f42479e155e3273c30d88425a457
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/11/2020
ms.locfileid: "104046253"
---
# <a name="detailed-object-model-comparison"></a><span data-ttu-id="a4d46-112">Confronto dettagliato del modello a oggetti</span><span class="sxs-lookup"><span data-stu-id="a4d46-112">Detailed Object Model Comparison</span></span>

<span data-ttu-id="a4d46-113">Nella tabella seguente vengono confrontate le proprietà del modello a oggetti di Windows Media Player 6,4 con il modello a oggetti di Windows Media Player 7 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="a4d46-113">The following table compares the Windows Media Player 6.4 object model properties with the Windows Media Player 7 or later object model.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a4d46-114">Proprietà di Windows Media Player 6,4</span><span class="sxs-lookup"><span data-stu-id="a4d46-114">Windows Media Player 6.4 property</span></span></th>
<th><span data-ttu-id="a4d46-115">Equivalente a Windows Media Player 7 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="a4d46-115">Windows Media Player 7 or later equivalent</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a4d46-116"><em>Player6</em>. <strong>AllowChangeDisplaySize</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-116"><em>Player6</em>.<strong>AllowChangeDisplaySize</strong></span></span></td>
<td><span data-ttu-id="a4d46-117">La visualizzazione di Windows Media Player 7 o versioni successive viene ridimensionata automaticamente per adattarsi ai supporti.</span><span class="sxs-lookup"><span data-stu-id="a4d46-117">The display of Windows Media Player 7 or later automatically resizes to fit the media.</span></span> <span data-ttu-id="a4d46-118">È possibile impostare le proprietà Height e Width nel <OBJECT> tag o nello script.</span><span class="sxs-lookup"><span data-stu-id="a4d46-118">You can set the height and width properties in the <OBJECT> tag or in script.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-119"><em>Player6</em>. <strong>AllowScan</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-119"><em>Player6</em>.<strong>AllowScan</strong></span></span></td>
<td><span data-ttu-id="a4d46-120"><em>Controlli</em>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-120"><em>Controls</em>.</span></span> <span data-ttu-id="a4d46-121"><strong>fastForward</strong> e <em>controlli</em>. <strong>fastReverse</strong> sono abilitati automaticamente per i tipi di file che supportano questi metodi.</span><span class="sxs-lookup"><span data-stu-id="a4d46-121"><strong>fastForward</strong> and <em>Controls</em>.<strong>fastReverse</strong> are automatically enabled for file types that support these methods.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-122"><em>Player6</em>. <strong>AnglesAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-122"><em>Player6</em>.<strong>AnglesAvailable</strong></span></span></td>
<td><span data-ttu-id="a4d46-123">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-123">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-124"><em>Player6</em>. <strong>AnimationAtStart</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-124"><em>Player6</em>.<strong>AnimationAtStart</strong></span></span></td>
<td><span data-ttu-id="a4d46-125">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-125">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-126"><em>Player6</em>. <strong>AudioStream</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-126"><em>Player6</em>.<strong>AudioStream</strong></span></span></td>
<td><span data-ttu-id="a4d46-127">Usare i <em>controlli</em>. <strong>currentAudioLanguageIndex</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-127">Use <em>Controls</em>.<strong>currentAudioLanguageIndex</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-128"><em>Player6</em>. <strong>AudioStreamsAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-128"><em>Player6</em>.<strong>AudioStreamsAvailable</strong></span></span></td>
<td><span data-ttu-id="a4d46-129">Usare i <em>controlli</em>. <strong>audioLanguageCount</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-129">Use <em>Controls</em>.<strong>audioLanguageCount</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-130"><em>Player6</em>. <strong>Riavvolgimento rapido</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-130"><em>Player6</em>.<strong>AutoRewind</strong></span></span></td>
<td><span data-ttu-id="a4d46-131">Usare i <em>controlli</em>. <strong>currentPosition</strong> nello script per specificare o recuperare la posizione corrente.</span><span class="sxs-lookup"><span data-stu-id="a4d46-131">Use <em>Controls</em>.<strong>currentPosition</strong> in script to specify or retrieve the current position.</span></span> <span data-ttu-id="a4d46-132">In alternativa, usare i marcatori e il <em>lettore</em>. evento <strong>markerHit</strong> .</span><span class="sxs-lookup"><span data-stu-id="a4d46-132">Alternatively, use markers and the <em>Player</em>.<strong>markerHit</strong> event.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-133"><em>Player6</em>. <strong>Ridimensiona automaticamente</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-133"><em>Player6</em>.<strong>AutoSize</strong></span></span></td>
<td><span data-ttu-id="a4d46-134">Il ridimensionamento automatico è il comportamento predefinito.</span><span class="sxs-lookup"><span data-stu-id="a4d46-134">Automatic sizing is the default behavior.</span></span> <span data-ttu-id="a4d46-135">Per eseguire l'override del ridimensionamento automatico, impostare le proprietà Height e Width nel <OBJECT> tag o nello script.</span><span class="sxs-lookup"><span data-stu-id="a4d46-135">To override automatic sizing, set the height and width properties in the <OBJECT> tag or in script.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-136"><em>Player6</em>. <strong>Avvio automatico</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-136"><em>Player6</em>.<strong>AutoStart</strong></span></span></td>
<td><span data-ttu-id="a4d46-137">Usare <em>Impostazioni</em>. <strong>avvio automatico</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-137">Use <em>Settings</em>.<strong>autoStart</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-138"><em>Player6</em>. <strong>Bilancia</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-138"><em>Player6</em>.<strong>Balance</strong></span></span></td>
<td><span data-ttu-id="a4d46-139">Usare <em>Impostazioni</em>. <strong>saldo</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-139">Use <em>Settings</em>.<strong>balance</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-140"><em>Player6</em>. <strong>Larghezza di banda</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-140"><em>Player6</em>.<strong>Bandwidth</strong></span></span></td>
<td><span data-ttu-id="a4d46-141">Utilizzare la <em>rete</em>. <strong>larghezza di banda</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-141">Use <em>Network</em>.<strong>bandWidth</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-142"><em>Player6</em>. <strong>BaseUrl</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-142"><em>Player6</em>.<strong>BaseURL</strong></span></span></td>
<td><span data-ttu-id="a4d46-143">Usare <em>Impostazioni</em>. <strong>BaseUrl</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-143">Use <em>Settings</em>.<strong>baseURL</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-144"><em>Player6</em>. <strong>BufferingCount</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-144"><em>Player6</em>.<strong>BufferingCount</strong></span></span></td>
<td><span data-ttu-id="a4d46-145">Utilizzare la <em>rete.</em> <strong>bufferingCount</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-145">Use <em>Network.</em><strong>bufferingCount</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-146"><em>Player6</em>. <strong>BufferingProgress</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-146"><em>Player6</em>.<strong>BufferingProgress</strong></span></span></td>
<td><span data-ttu-id="a4d46-147">Utilizzare la <em>rete</em>. <strong>bufferingProgress</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-147">Use <em>Network</em>.<strong>bufferingProgress</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-148"><em>Player6</em>. <strong>BufferingTime</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-148"><em>Player6</em>.<strong>BufferingTime</strong></span></span></td>
<td><span data-ttu-id="a4d46-149">Utilizzare la <em>rete</em>. <strong>bufferingTime</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-149">Use <em>Network</em>.<strong>bufferingTime</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-150"><em>Player6</em>. <strong>ButtonsAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-150"><em>Player6</em>.<strong>ButtonsAvailable</strong></span></span></td>
<td><span data-ttu-id="a4d46-151">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-151">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-152"><em>Player6</em>. <strong>CanPreview</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-152"><em>Player6</em>.<strong>CanPreview</strong></span></span></td>
<td><span data-ttu-id="a4d46-153">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-153">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-154"><em>Player6</em>. <strong>CANSCAN</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-154"><em>Player6</em>.<strong>CanScan</strong></span></span></td>
<td><span data-ttu-id="a4d46-155">Usare i <em>controlli</em>. i controlli e sono <strong>disponibili</strong>( &quot; FastForward &quot; ). <em></em><strong> Disponibile</strong>( &quot; FastReverse &quot; ).</span><span class="sxs-lookup"><span data-stu-id="a4d46-155">Use <em>Controls</em>.<strong>isAvailable</strong>(&quot;FastForward&quot;) and <em>Controls</em>.<strong>isAvailable</strong>(&quot;FastReverse&quot;).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-156"><em>Player6</em>. <strong>CanSeek</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-156"><em>Player6</em>.<strong>CanSeek</strong></span></span></td>
<td><span data-ttu-id="a4d46-157">Usare i <em>controlli</em>. è <strong>disponibile</strong> per verificare se è possibile eseguire un particolare metodo Seek.</span><span class="sxs-lookup"><span data-stu-id="a4d46-157">Use <em>Controls</em>.<strong>isAvailable</strong> to test whether a particular seek method can be performed.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-158"><em>Player6</em>. <strong>CanSeekToMarkers</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-158"><em>Player6</em>.<strong>CanSeekToMarkers</strong></span></span></td>
<td><span data-ttu-id="a4d46-159">Usare i <em>controlli</em>. <strong>disponibile</strong>( &quot; CurrentMarker &quot; ).</span><span class="sxs-lookup"><span data-stu-id="a4d46-159">Use <em>Controls</em>.<strong>isAvailable</strong>(&quot;CurrentMarker&quot;).</span></span> <span data-ttu-id="a4d46-160">Utilizzare <em>supporti</em>. <strong>markerCount</strong> per recuperare il numero di marcatori in un particolare elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="a4d46-160">Use <em>Media</em>.<strong>markerCount</strong> to retrieve the count of markers in a particular media item.</span></span> <span data-ttu-id="a4d46-161">Usare i <em>controlli</em>. <strong>currentMarker</strong> per specificare o recuperare il numero di marcatore corrente.</span><span class="sxs-lookup"><span data-stu-id="a4d46-161">Use <em>Controls</em>.<strong>currentMarker</strong> to specify or retrieve the current marker number.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-162"><em>Player6</em>. <strong>CaptioningID</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-162"><em>Player6</em>.<strong>CaptioningID</strong></span></span></td>
<td><span data-ttu-id="a4d46-163">Usare <em>ClosedCaption</em>. <strong>captioningID</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-163">Use <em>ClosedCaption</em>.<strong>captioningID</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-164"><em>Player6</em>. <strong>CCActive</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-164"><em>Player6</em>.<strong>CCActive</strong></span></span></td>
<td><span data-ttu-id="a4d46-165">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-165">Not available.</span></span> <span data-ttu-id="a4d46-166">Per informazioni sul modo in cui la didascalia chiusa è cambiata in Windows Media Player, vedere <a href="closed-captioning.md">sottotitoli codificati</a> .</span><span class="sxs-lookup"><span data-stu-id="a4d46-166">See <a href="closed-captioning.md">Closed Captioning</a> for information about how closed captioning has changed in Windows Media Player.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-167"><em>Player6</em>. <strong>ChannelDescription</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-167"><em>Player6</em>.<strong>ChannelDescription</strong></span></span></td>
<td><span data-ttu-id="a4d46-168">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-168">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-169"><em>Player6</em>. <strong>Canalename</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-169"><em>Player6</em>.<strong>ChannelName</strong></span></span></td>
<td><span data-ttu-id="a4d46-170">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-170">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-171"><em>Player6</em>. <strong>ChannelURL</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-171"><em>Player6</em>.<strong>ChannelURL</strong></span></span></td>
<td><span data-ttu-id="a4d46-172">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-172">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-173"><em>Player6</em>. <strong>ClickToPlay</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-173"><em>Player6</em>.<strong>ClickToPlay</strong></span></span></td>
<td><span data-ttu-id="a4d46-174">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-174">Not available.</span></span> <span data-ttu-id="a4d46-175">È necessario fornire i controlli nell'interfaccia utente per avviare la riproduzione.</span><span class="sxs-lookup"><span data-stu-id="a4d46-175">You should provide controls in your user interface to start playback.</span></span> <span data-ttu-id="a4d46-176">In alternativa, l'utente può fare clic con il pulsante destro del mouse sull'immagine del video per aprire un menu a comparsa che contiene una selezione <strong>riproduzione/sospensione</strong> se <em>Player</em>. <strong>enableContextMenu</strong> è uguale a true.</span><span class="sxs-lookup"><span data-stu-id="a4d46-176">Alternatively, the user can right-click the video image to open a pop-up menu that contains a <strong>Play/Pause</strong> selection if <em>Player</em>.<strong>enableContextMenu</strong> equals true.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-177"><em>Player6</em>. <strong>ClientID</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-177"><em>Player6</em>.<strong>ClientID</strong></span></span></td>
<td><span data-ttu-id="a4d46-178">Non disponibile. Windows Media Player 9 Series o versioni successive consente all'utente di selezionare se un ID giocatore univoco viene trasmesso ai provider di contenuti.</span><span class="sxs-lookup"><span data-stu-id="a4d46-178">Not available.Windows Media Player 9 Series or later allows the user to select whether a unique Player ID is transmitted to content providers.</span></span><br/> <span data-ttu-id="a4d46-179">Se l'utente seleziona questa opzione, il lettore invia un ID univoco al server Windows Media.</span><span class="sxs-lookup"><span data-stu-id="a4d46-179">If the user selects this option, the Player sends a unique ID to the Windows Media server.</span></span> <span data-ttu-id="a4d46-180">L'ID viene registrato nel file di log del server, che si trova in. cartella <em>system32\logfiles</em> per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="a4d46-180">The ID is logged in the server's log file, located in the ..<em>system32\logfiles</em> folder by default.</span></span> <span data-ttu-id="a4d46-181">Il nome del campo di log è &quot; c-playerid &quot; .</span><span class="sxs-lookup"><span data-stu-id="a4d46-181">The log field name is &quot;c-playerid&quot;.</span></span> <span data-ttu-id="a4d46-182">La registrazione del server non è abilitata per impostazione predefinita in Servizi Windows Media.</span><span class="sxs-lookup"><span data-stu-id="a4d46-182">Server logging is not enabled by default in Windows Media Services.</span></span><br/> <span data-ttu-id="a4d46-183">Se l'utente non seleziona questa opzione, il server genera un ID di sessione casuale, che è univoco per ogni client per una determinata sessione.</span><span class="sxs-lookup"><span data-stu-id="a4d46-183">If the user does not select this option, the server generates a random session ID, which is unique for each client for a given session.</span></span><br/> <span data-ttu-id="a4d46-184">Per ulteriori informazioni, vedere la documentazione della serie Windows Media Services 9.</span><span class="sxs-lookup"><span data-stu-id="a4d46-184">For more information, see the Windows Media Services 9 Series documentation.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-185"><em>Player6</em>. <strong>CodecCount</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-185"><em>Player6</em>.<strong>CodecCount</strong></span></span></td>
<td><span data-ttu-id="a4d46-186">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-186">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-187"><em>Player6</em>. <strong>ColorKey</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-187"><em>Player6</em>.<strong>ColorKey</strong></span></span></td>
<td><span data-ttu-id="a4d46-188">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-188">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-189"><em>Player6</em>. <strong>ConnectionSpeed</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-189"><em>Player6</em>.<strong>ConnectionSpeed</strong></span></span></td>
<td><span data-ttu-id="a4d46-190">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-190">Not available.</span></span> <span data-ttu-id="a4d46-191">Utilizzare la <em>rete</em>. <strong>bitrate</strong> per determinare la velocità in bit corrente.</span><span class="sxs-lookup"><span data-stu-id="a4d46-191">Use <em>Network</em>.<strong>bitRate</strong> to determine the current bit rate.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-192"><em>Player6</em>. <strong>ContactAddress</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-192"><em>Player6</em>.<strong>ContactAddress</strong></span></span></td>
<td><span data-ttu-id="a4d46-193">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-193">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-194"><em>Player6</em>. <strong>ContactEmail</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-194"><em>Player6</em>.<strong>ContactEmail</strong></span></span></td>
<td><span data-ttu-id="a4d46-195">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-195">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-196"><em>Player6</em>. <strong>ContactPhone</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-196"><em>Player6</em>.<strong>ContactPhone</strong></span></span></td>
<td><span data-ttu-id="a4d46-197">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-197">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-198"><em>Player6</em>. <strong>CreationDate</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-198"><em>Player6</em>.<strong>CreationDate</strong></span></span></td>
<td><span data-ttu-id="a4d46-199">Usare <em>mediacollection</em>. <strong>getMediaAtom</strong>( &quot; CreationDate &quot; ) per recuperare l'indice della data Atom di creazione.</span><span class="sxs-lookup"><span data-stu-id="a4d46-199">Use <em>MediaCollection</em>.<strong>getMediaAtom</strong>(&quot;CreationDate&quot;) to retrieve the index of the creation date atom.</span></span> <span data-ttu-id="a4d46-200">Utilizzare <em>supporti</em>. <strong>getItemInfoByAtom</strong> per recuperare i metadati.</span><span class="sxs-lookup"><span data-stu-id="a4d46-200">Use <em>Media</em>.<strong>getItemInfoByAtom</strong> to retrieve the metadata.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-201"><em>Player6</em>. <strong>CurrentAngle</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-201"><em>Player6</em>.<strong>CurrentAngle</strong></span></span></td>
<td><span data-ttu-id="a4d46-202">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-202">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-203"><em>Player6</em>. <strong>CurrentAudioStream</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-203"><em>Player6</em>.<strong>CurrentAudioStream</strong></span></span></td>
<td><span data-ttu-id="a4d46-204">Usare i <em>controlli</em>. <strong>currentAudioLanguageIndex</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-204">Use <em>Controls</em>.<strong>currentAudioLanguageIndex</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-205"><em>Player6</em>. <strong>CurrentButton</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-205"><em>Player6</em>.<strong>CurrentButton</strong></span></span></td>
<td><span data-ttu-id="a4d46-206">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-206">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-207"><em>Player6</em>. <strong>CurrentCCService</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-207"><em>Player6</em>.<strong>CurrentCCService</strong></span></span></td>
<td><span data-ttu-id="a4d46-208">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-208">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-209"><em>Player6</em>. <strong>CurrentChapter</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-209"><em>Player6</em>.<strong>CurrentChapter</strong></span></span></td>
<td><span data-ttu-id="a4d46-210">Recuperare la playlist corrente.</span><span class="sxs-lookup"><span data-stu-id="a4d46-210">Retrieve the current playlist.</span></span> <span data-ttu-id="a4d46-211">Se la playlist corrente non è uguale a quella restituita da <em>CDROM</em>. <strong>playlist</strong>, quindi non esiste alcun capitolo corrente.</span><span class="sxs-lookup"><span data-stu-id="a4d46-211">If the current playlist is not the same one as the playlist returned by <em>Cdrom</em>.<strong>playlist</strong>, then there is no current chapter.</span></span> <span data-ttu-id="a4d46-212">In caso contrario, il numero del capitolo corrente è l'indice del supporto corrente nella playlist corrente.</span><span class="sxs-lookup"><span data-stu-id="a4d46-212">Otherwise, the current chapter number is the index of the current media in the current playlist.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-213"><em>Player6</em>. <strong>CurrentDiscSide</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-213"><em>Player6</em>.<strong>CurrentDiscSide</strong></span></span></td>
<td><span data-ttu-id="a4d46-214">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-214">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-215"><em>Player6</em>. <strong>CurrentDomain</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-215"><em>Player6</em>.<strong>CurrentDomain</strong></span></span></td>
<td><span data-ttu-id="a4d46-216">Usare il <em>DVD</em>. <strong>dominio</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-216">Use <em>DVD</em>.<strong>domain</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-217"><em>Player6</em>. <strong>CurrentMarker</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-217"><em>Player6</em>.<strong>CurrentMarker</strong></span></span></td>
<td><span data-ttu-id="a4d46-218">Usare i <em>controlli</em>. <strong>currentMarker</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-218">Use <em>Controls</em>.<strong>currentMarker</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-219"><em>Player6</em>. <strong>CurrentPosition</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-219"><em>Player6</em>.<strong>CurrentPosition</strong></span></span></td>
<td><span data-ttu-id="a4d46-220">Usare i <em>controlli</em>. <strong>currentPosition</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-220">Use <em>Controls</em>.<strong>currentPosition</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-221"><em>Player6</em>. <strong>CurrentSubpictureStream</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-221"><em>Player6</em>.<strong>CurrentSubpictureStream</strong></span></span></td>
<td><span data-ttu-id="a4d46-222">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-222">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-223"><em>Player6</em>. <strong>CurrentTime</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-223"><em>Player6</em>.<strong>CurrentTime</strong></span></span></td>
<td><span data-ttu-id="a4d46-224">Usare i <em>controlli</em>. <strong>currentPositionTimeCode</strong>, <em>controlli</em>. <strong>currentPositionString</strong>o <em>controlli</em>. <strong>CurrentPosition.</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-224">Use <em>Controls</em>.<strong>currentPositionTimeCode</strong>, <em>Controls</em>.<strong>currentPositionString</strong>, or <em>Controls</em>.<strong>currentPosition.</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-225"><em>Player6</em>. <strong>CurrentTitle</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-225"><em>Player6</em>.<strong>CurrentTitle</strong></span></span></td>
<td><span data-ttu-id="a4d46-226">Recuperare la playlist corrente.</span><span class="sxs-lookup"><span data-stu-id="a4d46-226">Retrieve the current playlist.</span></span> <span data-ttu-id="a4d46-227">Se la playlist corrente corrisponde alla playlist restituita dal <em>CDROM</em>. <strong>playlist</strong>, il numero del titolo è l'indice del supporto corrente nella playlist corrente.</span><span class="sxs-lookup"><span data-stu-id="a4d46-227">If the current playlist is the same one as the playlist returned by <em>Cdrom</em>.<strong>playlist</strong>, then the title number is the index of the current media in the current playlist.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-228"><em>Player6</em>. <strong>CurrentVolume</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-228"><em>Player6</em>.<strong>CurrentVolume</strong></span></span></td>
<td><span data-ttu-id="a4d46-229">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-229">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-230"><em>Player6</em>. <strong>CursorType</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-230"><em>Player6</em>.<strong>CursorType</strong></span></span></td>
<td><span data-ttu-id="a4d46-231">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-231">Not available.</span></span> <span data-ttu-id="a4d46-232">Usare invece gli stili di Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="a4d46-232">Use Internet Explorer styles instead.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-233"><em>Player6</em>. <strong>DefaultFrame</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-233"><em>Player6</em>.<strong>DefaultFrame</strong></span></span></td>
<td><span data-ttu-id="a4d46-234">Usare <em>Impostazioni</em>. <strong>DefaultFrame</strong>oppure usare un</span><span class="sxs-lookup"><span data-stu-id="a4d46-234">Use <em>Settings</em>.<strong>defaultFrame</strong>, or use a</span></span> <PARAM> <span data-ttu-id="a4d46-235">attributo nell' <OBJECT> elemento: <pre data-space="preserve"><code><PARAM NAME=&quot;defaultFrame&quot; VALUE=&quot;right&quot;></code></pre></span><span class="sxs-lookup"><span data-stu-id="a4d46-235">attribute in the <OBJECT> element: <pre data-space="preserve"><code><PARAM NAME=&quot;defaultFrame&quot; VALUE=&quot;right&quot;></code></pre></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-236"><em>Player6</em>. <strong>DisplayBackColor</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-236"><em>Player6</em>.<strong>DisplayBackColor</strong></span></span></td>
<td><span data-ttu-id="a4d46-237">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-237">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-238"><em>Player6</em>. <strong>DisplayForeColor</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-238"><em>Player6</em>.<strong>DisplayForeColor</strong></span></span></td>
<td><span data-ttu-id="a4d46-239">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-239">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-240"><em>Player6</em>. <strong>DisplayMode</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-240"><em>Player6</em>.<strong>DisplayMode</strong></span></span></td>
<td><span data-ttu-id="a4d46-241">La posizione corrente può essere recuperata in pochi secondi dall'inizio come <strong>numero</strong> usando i <em>controlli</em>. <strong>currentPosition</strong>, sotto forma di <strong>stringa</strong> in formato HH: mm: SS (hours, minutes, seconds) utilizzando i <em>controlli</em>. <strong>currentPositionString</strong>o nel formato del codice temporale utilizzando i <em>controlli</em>. <strong>currentPositionTimeCode</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-241">The current position can be retrieved in seconds from the beginning as a <strong>Number</strong> using <em>Controls</em>.<strong>currentPosition</strong>, as a <strong>String</strong> formatted as HH:MM:SS (hours, minutes, seconds) using <em>Controls</em>.<strong>currentPositionString</strong>, or in time code format using <em>Controls</em>.<strong>currentPositionTimeCode</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-242"><em>Player6</em>. <strong>DisplaySize</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-242"><em>Player6</em>.<strong>DisplaySize</strong></span></span></td>
<td><span data-ttu-id="a4d46-243">La visualizzazione predefinita viene ridimensionata automaticamente per adattarsi ai supporti.</span><span class="sxs-lookup"><span data-stu-id="a4d46-243">The default display automatically resizes to fit the media.</span></span> <span data-ttu-id="a4d46-244">È possibile impostare le proprietà Height e Width nel <OBJECT> tag o nello script.</span><span class="sxs-lookup"><span data-stu-id="a4d46-244">You can set the height and width properties in the <OBJECT> tag, or in script.</span></span> <span data-ttu-id="a4d46-245">Usare <em>Player</em>. <strong>schermo</strong> intero per passare alla modalità schermo intero.</span><span class="sxs-lookup"><span data-stu-id="a4d46-245">Use <em>Player</em>.<strong>fullScreen</strong> to switch to full-screen mode.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-246"><em>Player6</em>. <strong>Durata</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-246"><em>Player6</em>.<strong>Duration</strong></span></span></td>
<td><span data-ttu-id="a4d46-247">Utilizzare <em>supporti</em>. <strong>durata</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-247">Use <em>Media</em>.<strong>duration</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-248"><em>Player6</em>. <strong>DVD</strong> di</span><span class="sxs-lookup"><span data-stu-id="a4d46-248"><em>Player6</em>.<strong>DVD</strong></span></span></td>
<td><span data-ttu-id="a4d46-249">Usare <em>Player</em>. <strong>DVD</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-249">Use <em>Player</em>.<strong>DVD</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-250"><em>Player6</em>. <strong>EnableContextMenu</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-250"><em>Player6</em>.<strong>EnableContextMenu</strong></span></span></td>
<td><span data-ttu-id="a4d46-251">Usare <em>Player</em>. <strong>enableContextMenu</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-251">Use <em>Player</em>.<strong>enableContextMenu</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-252"><em>Player6</em>. <strong>Abilitato</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-252"><em>Player6</em>.<strong>Enabled</strong></span></span></td>
<td><span data-ttu-id="a4d46-253">Usare <em>Player</em>. <strong>abilitata</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-253">Use <em>Player</em>.<strong>enabled</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-254"><em>Player6</em>. <strong>EnableFullScreenControls</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-254"><em>Player6</em>.<strong>EnableFullScreenControls</strong></span></span></td>
<td><span data-ttu-id="a4d46-255">Quando si usa Windows Media Player 9 Series o versioni successive, i controlli a schermo intero vengono abilitati automaticamente a meno che non sia il <em>lettore</em>. <strong></strong>  =  uiMode &quot; nessuno &quot; .</span><span class="sxs-lookup"><span data-stu-id="a4d46-255">When using Windows Media Player 9 Series or later, full-screen controls are enabled automatically unless <em>Player</em>.<strong>uiMode</strong> = &quot;none&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-256"><em>Player6</em>. <strong>EnablePositionControls</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-256"><em>Player6</em>.<strong>EnablePositionControls</strong></span></span></td>
<td><span data-ttu-id="a4d46-257">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-257">Not available.</span></span> <span data-ttu-id="a4d46-258">È possibile fornire controlli personalizzati o utilizzare <em>Player</em>. <strong>uiMode</strong> per scegliere una configurazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="a4d46-258">You can provide custom controls or use <em>Player</em>.<strong>uimode</strong> to choose a default configuration.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-259"><em>Player6</em>. <strong>EnableTracker</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-259"><em>Player6</em>.<strong>EnableTracker</strong></span></span></td>
<td><span data-ttu-id="a4d46-260">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-260">Not available.</span></span> <span data-ttu-id="a4d46-261">È possibile fornire un controllo personalizzato o usare un <em>lettore</em>. <strong>uiMode</strong> per scegliere una configurazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="a4d46-261">You can provide a custom control or use <em>Player</em>.<strong>uimode</strong> to choose a default configuration.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-262"><em>Player6</em>. <strong>EntryCount</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-262"><em>Player6</em>.<strong>EntryCount</strong></span></span></td>
<td><span data-ttu-id="a4d46-263">Usare <em>playlist</em>. <strong>numero</strong> di</span><span class="sxs-lookup"><span data-stu-id="a4d46-263">Use <em>Playlist</em>.<strong>count</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-264"><em>Player6</em>. <strong></strong> Codice errore</span><span class="sxs-lookup"><span data-stu-id="a4d46-264"><em>Player6</em>.<strong>ErrorCode</strong></span></span></td>
<td><span data-ttu-id="a4d46-265">Usare <em>ErrorItem</em>. <strong>ErrorCode</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-265">Use <em>ErrorItem</em>.<strong>errorCode</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-266"><em>Player6</em>. <strong>ErrorCorrection</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-266"><em>Player6</em>.<strong>ErrorCorrection</strong></span></span></td>
<td><span data-ttu-id="a4d46-267">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-267">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-268"><em>Player6</em>. <strong>ErrorDescription</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-268"><em>Player6</em>.<strong>ErrorDescription</strong></span></span></td>
<td><span data-ttu-id="a4d46-269">Usare <em>ErrorItem</em>. <strong>errorDescription</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-269">Use <em>ErrorItem</em>.<strong>errorDescription</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-270"><em>Player6</em>. <strong>Nome file</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-270"><em>Player6</em>.<strong>FileName</strong></span></span></td>
<td><span data-ttu-id="a4d46-271">Usare <em>Player</em>. <strong>URL</strong> o <em>lettore</em>. <strong>currentMedia</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-271">Use <em>Player</em>.<strong>URL</strong> or <em>Player</em>.<strong>currentMedia</strong>.</span></span> <span data-ttu-id="a4d46-272">Usare i <em>controlli</em>. <strong>CurrentItem</strong> quando si lavora all'interno di una playlist.</span><span class="sxs-lookup"><span data-stu-id="a4d46-272">Use <em>Controls</em>.<strong>currentItem</strong> when working within a playlist.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-273"><em>Player6</em>. <strong>FramesPerSecond</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-273"><em>Player6</em>.<strong>FramesPerSecond</strong></span></span></td>
<td><span data-ttu-id="a4d46-274">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-274">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-275"><em>Player6</em>. <strong>HasError</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-275"><em>Player6</em>.<strong>HasError</strong></span></span></td>
<td><span data-ttu-id="a4d46-276">Usare l' <em>errore</em>. <strong>ErrorCount</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-276">Use <em>Error</em>.<strong>errorCount</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-277"><em>Player6</em>. <strong>HasMultipleItems</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-277"><em>Player6</em>.<strong>HasMultipleItems</strong></span></span></td>
<td><span data-ttu-id="a4d46-278">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-278">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-279"><em>Player6</em>. <strong>ImageSourceHeight</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-279"><em>Player6</em>.<strong>ImageSourceHeight</strong></span></span></td>
<td><span data-ttu-id="a4d46-280">Utilizzare <em>supporti</em>. <strong>imageSourceHeight</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-280">Use <em>Media</em>.<strong>imageSourceHeight</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-281"><em>Player6</em>. <strong>ImageSourceWidth</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-281"><em>Player6</em>.<strong>ImageSourceWidth</strong></span></span></td>
<td><span data-ttu-id="a4d46-282">Utilizzare <em>supporti</em>. <strong>imageSourceWidth</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-282">Use <em>Media</em>.<strong>imageSourceWidth</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-283"><em>Player6</em>. <strong>InvokeURLs</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-283"><em>Player6</em>.<strong>InvokeURLs</strong></span></span></td>
<td><span data-ttu-id="a4d46-284">Usare <em>Impostazioni</em>. <strong>invokeURLs</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-284">Use <em>Settings</em>.<strong>invokeURLs</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-285"><em>Player6</em>. <strong>Trasmissione</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-285"><em>Player6</em>.<strong>IsBroadcast</strong></span></span></td>
<td><span data-ttu-id="a4d46-286">Utilizzare la <em>rete</em>. <strong>sourceProtocol</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-286">Use <em>Network</em>.<strong>sourceProtocol</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-287"><em>Player6</em>. <strong>IsDurationValid</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-287"><em>Player6</em>.<strong>IsDurationValid</strong></span></span></td>
<td><span data-ttu-id="a4d46-288">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-288">Not available.</span></span> <span data-ttu-id="a4d46-289"><em>Supporti</em>. <strong>Duration</strong> contiene un valore valido se utilizzato con l'oggetto multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="a4d46-289"><em>Media</em>.<strong>duration</strong> contains a valid value when used with the current media object.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-290"><em>Player6</em>. <strong>Lingua</strong> di</span><span class="sxs-lookup"><span data-stu-id="a4d46-290"><em>Player6</em>.<strong>Language</strong></span></span></td>
<td><span data-ttu-id="a4d46-291">Usare i <em>controlli</em>. <strong>currentAudioLanguage</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-291">Use <em>Controls</em>.<strong>currentAudioLanguage</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-292"><em>Player6</em>. <strong>LostPackets</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-292"><em>Player6</em>.<strong>LostPackets</strong></span></span></td>
<td><span data-ttu-id="a4d46-293">Utilizzare la <em>rete</em>. <strong>lostPackets</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-293">Use <em>Network</em>.<strong>lostPackets</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-294"><em>Player6</em>. <strong>MarkerCount</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-294"><em>Player6</em>.<strong>MarkerCount</strong></span></span></td>
<td><span data-ttu-id="a4d46-295">Utilizzare <em>supporti</em>. <strong>markerCount</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-295">Use <em>Media</em>.<strong>markerCount</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-296"><em>Player6</em>. <strong>Disattiva</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-296"><em>Player6</em>.<strong>Mute</strong></span></span></td>
<td><span data-ttu-id="a4d46-297">Usare <em>Impostazioni</em>. <strong>Disattiva</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-297">Use <em>Settings</em>.<strong>mute</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-298"><em>Player6</em>. <strong>OpenState</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-298"><em>Player6</em>.<strong>OpenState</strong></span></span></td>
<td><span data-ttu-id="a4d46-299">Usare <em>Player</em>. <strong>openState</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-299">Use <em>Player</em>.<strong>openState</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-300"><em>Player6</em>. <strong>PlayCount</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-300"><em>Player6</em>.<strong>PlayCount</strong></span></span></td>
<td><span data-ttu-id="a4d46-301">Usare <em>Impostazioni</em>. <strong>playCount</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-301">Use <em>Settings</em>.<strong>playCount</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-302"><em>Player6</em>. <strong>Riproduzione</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-302"><em>Player6</em>.<strong>PlayState</strong></span></span></td>
<td><span data-ttu-id="a4d46-303">Usare <em>Player</em>. <strong>riproduzione</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-303">Use <em>Player</em>.<strong>playState</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-304"><em>Player6</em>. <strong>PreviewMode</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-304"><em>Player6</em>.<strong>PreviewMode</strong></span></span></td>
<td><span data-ttu-id="a4d46-305">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-305">Not available.</span></span> <span data-ttu-id="a4d46-306">Usare una struttura del ciclo di script con un timer HTML per duplicare questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="a4d46-306">Use a script loop structure with an HTML timer to duplicate this functionality.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-307"><em>Player6</em>. <strong>Frequenza</strong> di</span><span class="sxs-lookup"><span data-stu-id="a4d46-307"><em>Player6</em>.<strong>Rate</strong></span></span></td>
<td><span data-ttu-id="a4d46-308">Usare <em>Impostazioni</em>. <strong>frequenza</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-308">Use <em>Settings</em>.<strong>rate</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-309"><em>Player6</em>. <strong>ReadyState</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-309"><em>Player6</em>.<strong>ReadyState</strong></span></span></td>
<td><span data-ttu-id="a4d46-310">Usare <em>Player</em>. <strong>openState</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-310">Use <em>Player</em>.<strong>openState</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-311"><em>Player6</em>. <strong>ReceivedPackets</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-311"><em>Player6</em>.<strong>ReceivedPackets</strong></span></span></td>
<td><span data-ttu-id="a4d46-312">Utilizzare la <em>rete</em>. <strong>receivedPackets</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-312">Use <em>Network</em>.<strong>receivedPackets</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-313"><em>Player6</em>. <strong>ReceptionQuality</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-313"><em>Player6</em>.<strong>ReceptionQuality</strong></span></span></td>
<td><span data-ttu-id="a4d46-314">Utilizzare la <em>rete</em>. <strong>receptionQuality</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-314">Use <em>Network</em>.<strong>receptionQuality</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-315"><em>Player6</em>. <strong>RecoveredPackets</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-315"><em>Player6</em>.<strong>RecoveredPackets</strong></span></span></td>
<td><span data-ttu-id="a4d46-316">Utilizzare la <em>rete</em>. <strong>recoveredPackets</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-316">Use <em>Network</em>.<strong>recoveredPackets</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-317"><em>Player6</em>. <strong>Radice</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-317"><em>Player6</em>.<strong>Root</strong></span></span></td>
<td><span data-ttu-id="a4d46-318">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-318">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-319"><em>Player6</em>. <strong>SAMIFileName</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-319"><em>Player6</em>.<strong>SAMIFileName</strong></span></span></td>
<td><span data-ttu-id="a4d46-320">Usare <em>ClosedCaption</em>. <strong>SAMIFileName</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-320">Use <em>ClosedCaption</em>.<strong>SAMIFileName</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-321"><em>Player6</em>. <strong>SAMILang</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-321"><em>Player6</em>.<strong>SAMILang</strong></span></span></td>
<td><span data-ttu-id="a4d46-322">Usare <em>ClosedCaption</em>. <strong>SAMILang</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-322">Use <em>ClosedCaption</em>.<strong>SAMILang</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-323"><em>Player6</em>. <strong>SAMIStyle</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-323"><em>Player6</em>.<strong>SAMIStyle</strong></span></span></td>
<td><span data-ttu-id="a4d46-324">Usare <em>ClosedCaption</em>. <strong>SAMIStyle</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-324">Use <em>ClosedCaption</em>.<strong>SAMIStyle</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-325"><em>Player6</em>. <strong>SelectionEnd</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-325"><em>Player6</em>.<strong>SelectionEnd</strong></span></span></td>
<td><span data-ttu-id="a4d46-326">Utilizzare <em>supporti</em>. <strong>durata</strong> per determinare la lunghezza di un oggetto <strong>multimediale</strong> .</span><span class="sxs-lookup"><span data-stu-id="a4d46-326">Use <em>Media</em>.<strong>duration</strong> to determine the length of a <strong>Media</strong> object.</span></span> <span data-ttu-id="a4d46-327">Usare un marcatore con i <em>controlli</em>. <strong>currentMarker</strong> per specificare una posizione finale personalizzata.</span><span class="sxs-lookup"><span data-stu-id="a4d46-327">Use a marker with <em>Controls</em>.<strong>currentMarker</strong> to specify a custom end position.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-328"><em>Player6</em>. <strong>SelectionStart</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-328"><em>Player6</em>.<strong>SelectionStart</strong></span></span></td>
<td><span data-ttu-id="a4d46-329">Usare i <em>controlli</em>. <strong>currentPosition</strong> avviare la riproduzione da una posizione specifica o utilizzare un marcatore con i <em>controlli</em>. <strong>currentMarker</strong> per specificare una posizione iniziale personalizzata.</span><span class="sxs-lookup"><span data-stu-id="a4d46-329">Use <em>Controls</em>.<strong>currentPosition</strong> to start playback from a particular position or use a marker with <em>Controls</em>.<strong>currentMarker</strong> to specify a custom start position.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-330"><em>Player6</em>. <strong>SendErrorEvents</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-330"><em>Player6</em>.<strong>SendErrorEvents</strong></span></span></td>
<td><span data-ttu-id="a4d46-331">Gli errori vengono accodati.</span><span class="sxs-lookup"><span data-stu-id="a4d46-331">Errors are queued.</span></span> <span data-ttu-id="a4d46-332">Usare l'oggetto <strong>Error</strong> e l'oggetto <strong>ErrorItem</strong> per recuperare le informazioni sull'errore.</span><span class="sxs-lookup"><span data-stu-id="a4d46-332">Use the <strong>Error</strong> object and the <strong>ErrorItem</strong> object to retrieve error information.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-333"><em>Player6</em>. <strong>SendKeyboardEvents</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-333"><em>Player6</em>.<strong>SendKeyboardEvents</strong></span></span></td>
<td><span data-ttu-id="a4d46-334">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-334">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-335"><em>Player6</em>. <strong>SendMouseClickEvents</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-335"><em>Player6</em>.<strong>SendMouseClickEvents</strong></span></span></td>
<td><span data-ttu-id="a4d46-336">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-336">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-337"><em>Player6</em>. <strong>SendMouseMoveEvents</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-337"><em>Player6</em>.<strong>SendMouseMoveEvents</strong></span></span></td>
<td><span data-ttu-id="a4d46-338">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-338">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-339"><em>Player6</em>. <strong>SendOpenStateChangeEvents</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-339"><em>Player6</em>.<strong>SendOpenStateChangeEvents</strong></span></span></td>
<td><span data-ttu-id="a4d46-340">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-340">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-341"><em>Player6</em>. <strong>SendPlayStateChangeEvents</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-341"><em>Player6</em>.<strong>SendPlayStateChangeEvents</strong></span></span></td>
<td><span data-ttu-id="a4d46-342">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-342">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-343"><em>Player6</em>. <strong>SendWarningEvents</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-343"><em>Player6</em>.<strong>SendWarningEvents</strong></span></span></td>
<td><span data-ttu-id="a4d46-344">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-344">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-345"><em>Player6</em>. <strong>ShowAudioControls</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-345"><em>Player6</em>.<strong>ShowAudioControls</strong></span></span></td>
<td><span data-ttu-id="a4d46-346">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-346">Not available.</span></span> <span data-ttu-id="a4d46-347">È possibile fornire controlli personalizzati o utilizzare <em>Player</em>. <strong>uiMode</strong> per scegliere una configurazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="a4d46-347">You can provide custom controls or use <em>Player</em>.<strong>uimode</strong> to choose a default configuration.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-348"><em>Player6</em>. <strong>ShowCaptioning</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-348"><em>Player6</em>.<strong>ShowCaptioning</strong></span></span></td>
<td><span data-ttu-id="a4d46-349">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-349">Not available.</span></span> <span data-ttu-id="a4d46-350">È possibile fornire una visualizzazione didascalia personalizzata chiusa.</span><span class="sxs-lookup"><span data-stu-id="a4d46-350">You can provide a custom closed caption display.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-351"><em>Player6</em>. <strong>ShowControls</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-351"><em>Player6</em>.<strong>ShowControls</strong></span></span></td>
<td><span data-ttu-id="a4d46-352">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-352">Not available.</span></span> <span data-ttu-id="a4d46-353">È possibile fornire controlli personalizzati o utilizzare <em>Player</em>. <strong>uiMode</strong> per scegliere una configurazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="a4d46-353">You can provide custom controls or use <em>Player</em>.<strong>uimode</strong> to choose a default configuration.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-354"><em>Player6</em>. <strong>ShowDisplay</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-354"><em>Player6</em>.<strong>ShowDisplay</strong></span></span></td>
<td><span data-ttu-id="a4d46-355">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-355">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-356"><em>Player6</em>. <strong>ShowGotoBar</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-356"><em>Player6</em>.<strong>ShowGotoBar</strong></span></span></td>
<td><span data-ttu-id="a4d46-357">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-357">Not available.</span></span> <span data-ttu-id="a4d46-358">È possibile fornire funzionalità personalizzate utilizzando l'oggetto multimediale</span><span class="sxs-lookup"><span data-stu-id="a4d46-358">You can provide custom functionality using the Media object</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-359"><em>Player6</em>. <strong>ShowPositionControls</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-359"><em>Player6</em>.<strong>ShowPositionControls</strong></span></span></td>
<td><span data-ttu-id="a4d46-360">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-360">Not available.</span></span> <span data-ttu-id="a4d46-361">È possibile fornire controlli personalizzati o utilizzare <em>Player</em>. <strong>uiMode</strong> per scegliere una configurazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="a4d46-361">You can provide custom controls or use <em>Player</em>.<strong>uimode</strong> to choose a default configuration.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-362"><em>Player6</em>. <strong>ShowStatusBar</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-362"><em>Player6</em>.<strong>ShowStatusBar</strong></span></span></td>
<td><span data-ttu-id="a4d46-363">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-363">Not available.</span></span> <span data-ttu-id="a4d46-364">È possibile fornire controlli personalizzati o utilizzare <em>Player</em>. <strong>uiMode</strong> per scegliere una configurazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="a4d46-364">You can provide custom controls or use <em>Player</em>.<strong>uimode</strong> to choose a default configuration.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-365"><em>Player6</em>. <strong>ShowTracker</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-365"><em>Player6</em>.<strong>ShowTracker</strong></span></span></td>
<td><span data-ttu-id="a4d46-366">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-366">Not available.</span></span> <span data-ttu-id="a4d46-367">È possibile fornire controlli personalizzati o utilizzare <em>Player</em>. <strong>uiMode</strong> per scegliere una configurazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="a4d46-367">You can provide custom controls or use <em>Player</em>.<strong>uimode</strong> to choose a default configuration.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-368"><em>Player6</em>. <strong>SourceLink</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-368"><em>Player6</em>.<strong>SourceLink</strong></span></span></td>
<td><span data-ttu-id="a4d46-369">Utilizzare <em>supporti</em>. <strong>sourceURL</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-369">Use <em>Media</em>.<strong>sourceURL</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-370"><em>Player6</em>. <strong>SourceProtocol</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-370"><em>Player6</em>.<strong>SourceProtocol</strong></span></span></td>
<td><span data-ttu-id="a4d46-371">Utilizzare la <em>rete</em>. <strong>sourceProtocol</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-371">Use <em>Network</em>.<strong>sourceProtocol</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-372"><em>Player6</em>. <strong>StreamCount</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-372"><em>Player6</em>.<strong>StreamCount</strong></span></span></td>
<td><span data-ttu-id="a4d46-373">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-373">Not available.</span></span> <span data-ttu-id="a4d46-374">Usare i <em>controlli</em>. <strong>audioLanguageCount</strong> per recuperare il numero di flussi di lingua audio.</span><span class="sxs-lookup"><span data-stu-id="a4d46-374">Use <em>Controls</em>.<strong>audioLanguageCount</strong> to retrieve the number of audio language streams.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-375"><em>Player6</em>. <strong>SubpictureOn</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-375"><em>Player6</em>.<strong>SubpictureOn</strong></span></span></td>
<td><span data-ttu-id="a4d46-376">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-376">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-377"><em>Player6</em>. <strong>SubpictureStreamsAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-377"><em>Player6</em>.<strong>SubpictureStreamsAvailable</strong></span></span></td>
<td><span data-ttu-id="a4d46-378">Non disponibile</span><span class="sxs-lookup"><span data-stu-id="a4d46-378">Not available</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-379"><em>Player6</em>. <strong>TitlesAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-379"><em>Player6</em>.<strong>TitlesAvailable</strong></span></span></td>
<td><span data-ttu-id="a4d46-380">Usare il codice seguente:<code>Player.Cdrom.playlist.count - 1</code></span><span class="sxs-lookup"><span data-stu-id="a4d46-380">Use the following:<code>Player.Cdrom.playlist.count - 1</code></span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-381"><em>Player6</em>. <strong>TotalTitleTime</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-381"><em>Player6</em>.<strong>TotalTitleTime</strong></span></span></td>
<td><span data-ttu-id="a4d46-382">Usare <em>currentMedia</em>. <strong>Duration</strong> o <em>currentMedia</em>. <strong>durationstring</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-382">Use <em>currentMedia</em>.<strong>duration</strong> or <em>currentMedia</em>.<strong>durationString</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-383"><em>Player6</em>. <strong>TransparentAtStart</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-383"><em>Player6</em>.<strong>TransparentAtStart</strong></span></span></td>
<td><span data-ttu-id="a4d46-384">Usare lo script per specificare i valori di altezza e larghezza per rendere il lettore visibile o invisibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-384">Use script to specify the height and width values to make the player visible or invisible.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-385"><em>Player6</em>. <strong>UniqueId</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-385"><em>Player6</em>.<strong>UniqueID</strong></span></span></td>
<td><span data-ttu-id="a4d46-386">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-386">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-387"><em>Player6</em>. <strong>VideoBorder3D</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-387"><em>Player6</em>.<strong>VideoBorder3D</strong></span></span></td>
<td><span data-ttu-id="a4d46-388">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-388">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-389"><em>Player6</em>. <strong>VideoBorderColor</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-389"><em>Player6</em>.<strong>VideoBorderColor</strong></span></span></td>
<td><span data-ttu-id="a4d46-390">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-390">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-391"><em>Player6</em>. <strong>VideoBorderWidth</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-391"><em>Player6</em>.<strong>VideoBorderWidth</strong></span></span></td>
<td><span data-ttu-id="a4d46-392">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-392">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-393"><em>Player6</em>. <strong>Volume</strong> di</span><span class="sxs-lookup"><span data-stu-id="a4d46-393"><em>Player6</em>.<strong>Volume</strong></span></span></td>
<td><span data-ttu-id="a4d46-394">Usare <em>Impostazioni</em>. <strong>Volume</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-394">Use <em>Settings</em>.<strong>Volume</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-395"><em>Player6</em>. <strong>VolumesAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-395"><em>Player6</em>.<strong>VolumesAvailable</strong></span></span></td>
<td><span data-ttu-id="a4d46-396">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-396">Not available.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="a4d46-397">Nella tabella seguente vengono confrontati i metodi del modello a oggetti di Windows Media Player versione 6,4 con il modello a oggetti di Windows Media Player 7 o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="a4d46-397">The following table compares the Windows Media Player version 6.4 object model methods with the Windows Media Player 7 or later object model.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a4d46-398">Metodo Windows Media Player 6,4</span><span class="sxs-lookup"><span data-stu-id="a4d46-398">Windows Media Player 6.4 method</span></span></th>
<th><span data-ttu-id="a4d46-399">Equivalente a Windows Media Player 7 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="a4d46-399">Windows Media Player 7 or later equivalent</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a4d46-400"><em>Player6</em>. <strong>AboutBox</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-400"><em>Player6</em>.<strong>AboutBox</strong></span></span></td>
<td><span data-ttu-id="a4d46-401">Usare <em>Player</em>. <strong>VERSIONINFO</strong> per recuperare la versione di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="a4d46-401">Use <em>Player</em>.<strong>versionInfo</strong> to retrieve the version of Windows Media Player.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-402"><em>Player6</em>. <strong>BackwardScan</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-402"><em>Player6</em>.<strong>BackwardScan</strong></span></span></td>
<td><span data-ttu-id="a4d46-403">Usare <em>Impostazioni</em>. <strong>frequenza</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-403">Use <em>Settings</em>.<strong>rate</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-404"><em>Player6</em>. <strong>ButtonActivate</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-404"><em>Player6</em>.<strong>ButtonActivate</strong></span></span></td>
<td><span data-ttu-id="a4d46-405">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-405">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-406"><em>Player6</em>. <strong>ButtonSelectAndActivate</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-406"><em>Player6</em>.<strong>ButtonSelectAndActivate</strong></span></span></td>
<td><span data-ttu-id="a4d46-407">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-407">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-408"><em>Player6</em>. <strong>Annulla</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-408"><em>Player6</em>.<strong>Cancel</strong></span></span></td>
<td><span data-ttu-id="a4d46-409">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-409">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-410"><em>Player6</em>. <strong>ChapterPlay</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-410"><em>Player6</em>.<strong>ChapterPlay</strong></span></span></td>
<td><span data-ttu-id="a4d46-411">Se si sta già eseguendo la playlist del titolo specificata, recuperare il capitolo desiderato come oggetto multimediale usando la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="a4d46-411">If already playing the specified title playlist, retrieve the desired chapter as a media object using the following syntax:</span></span>
<pre data-space="preserve"><code>var media = Player.currentPlaylist.item(index);</code></pre>
<span data-ttu-id="a4d46-412">Quindi, specificare <em>Player</em>. <strong>currentMedia</strong> utilizzando l'oggetto multimediale restituito.</span><span class="sxs-lookup"><span data-stu-id="a4d46-412">Then, specify <em>Player</em>.<strong>currentMedia</strong> using the media object returned.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-413"><em>Player6</em>. <strong>ChapterPlayAutoStop</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-413"><em>Player6</em>.<strong>ChapterPlayAutoStop</strong></span></span></td>
<td><span data-ttu-id="a4d46-414">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-414">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-415"><em>Player6</em>. <strong>ChapterSearch</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-415"><em>Player6</em>.<strong>ChapterSearch</strong></span></span></td>
<td><span data-ttu-id="a4d46-416">Se si sta già eseguendo la playlist del titolo specificata, recuperare il capitolo desiderato come oggetto multimediale usando la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="a4d46-416">If already playing the specified title playlist, retrieve the desired chapter as a media object using the following syntax:</span></span>
<pre data-space="preserve"><code>var media = Player.currentPlaylist.item(index);</code></pre>
<span data-ttu-id="a4d46-417">Quindi, specificare <em>Player</em>. <strong>currentMedia</strong> utilizzando l'oggetto multimediale restituito.</span><span class="sxs-lookup"><span data-stu-id="a4d46-417">Then, specify <em>Player</em>.<strong>currentMedia</strong> using the media object returned.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-418"><em>Player6</em>. <strong>FastForward</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-418"><em>Player6</em>.<strong>FastForward</strong></span></span></td>
<td><span data-ttu-id="a4d46-419">Usare i <em>controlli</em>. <strong>fastForward</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-419">Use <em>Controls</em>.<strong>fastForward</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-420"><em>Player6</em>. <strong>FastReverse</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-420"><em>Player6</em>.<strong>FastReverse</strong></span></span></td>
<td><span data-ttu-id="a4d46-421">Usare i <em>controlli</em>. <strong>fastReverse</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-421">Use <em>Controls</em>.<strong>fastReverse</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-422"><em>Player6</em>. <strong>ForwardScan</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-422"><em>Player6</em>.<strong>ForwardScan</strong></span></span></td>
<td><span data-ttu-id="a4d46-423">Usare <em>Impostazioni</em>. <strong>frequenza</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-423">Use <em>Settings</em>.<strong>rate</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-424"><em>Player6</em>. <strong>GetAllGPRMs</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-424"><em>Player6</em>.<strong>GetAllGPRMs</strong></span></span></td>
<td><span data-ttu-id="a4d46-425">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-425">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-426"><em>Player6</em>. <strong>GetAllSPRMs</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-426"><em>Player6</em>.<strong>GetAllSPRMs</strong></span></span></td>
<td><span data-ttu-id="a4d46-427">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-427">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-428"><em>Player6</em>. <strong>GetAudioLanguage</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-428"><em>Player6</em>.<strong>GetAudioLanguage</strong></span></span></td>
<td><span data-ttu-id="a4d46-429">Usare i <em>controlli</em>. <strong>currentAudioLanguage</strong> per recuperare l'LCID della lingua audio corrente.</span><span class="sxs-lookup"><span data-stu-id="a4d46-429">Use <em>Controls</em>.<strong>currentAudioLanguage</strong> to retrieve the LCID of the current audio language.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-430"><em>Player6</em>. <strong>GetCodecDescription</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-430"><em>Player6</em>.<strong>GetCodecDescription</strong></span></span></td>
<td><span data-ttu-id="a4d46-431">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-431">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-432"><em>Player6</em>. <strong>GetCodecInstalled</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-432"><em>Player6</em>.<strong>GetCodecInstalled</strong></span></span></td>
<td><span data-ttu-id="a4d46-433">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-433">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-434"><em>Player6</em>. <strong>GetCodecURL</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-434"><em>Player6</em>.<strong>GetCodecURL</strong></span></span></td>
<td><span data-ttu-id="a4d46-435">Usare <em>ErrorItem</em>. <strong>customUrl</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-435">Use <em>ErrorItem</em>.<strong>customUrl</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-436"><em>Player6</em>. <strong>GetCurrentEntry</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-436"><em>Player6</em>.<strong>GetCurrentEntry</strong></span></span></td>
<td><span data-ttu-id="a4d46-437">Usare script per scorrere in ciclo la playlist corrente.</span><span class="sxs-lookup"><span data-stu-id="a4d46-437">Use script to loop through the current playlist.</span></span> <span data-ttu-id="a4d46-438">Utilizzare <em>supporti</em>. è <strong>identico</strong> per confrontare ogni voce della playlist con il <em>lettore</em>. oggetto <strong>currentMedia</strong> .</span><span class="sxs-lookup"><span data-stu-id="a4d46-438">Use <em>Media</em>.<strong>isIdentical</strong> to compare each entry in the playlist to the <em>Player</em>.<strong>currentMedia</strong> object.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-439"><em>Player6</em>. <strong>Getmarcatore</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-439"><em>Player6</em>.<strong>GetMarkerName</strong></span></span></td>
<td><span data-ttu-id="a4d46-440">Utilizzare <em>supporti</em>. <strong>Getmarkname</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-440">Use <em>Media</em>.<strong>getMarkerName</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-441"><em>Player6</em>. <strong>GetMarkerTime</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-441"><em>Player6</em>.<strong>GetMarkerTime</strong></span></span></td>
<td><span data-ttu-id="a4d46-442">Utilizzare <em>supporti</em>. <strong>getMarkerTime</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-442">Use <em>Media</em>.<strong>getMarkerTime</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-443"><em>Player6</em>. <strong>GetMediaInfoString</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-443"><em>Player6</em>.<strong>GetMediaInfoString</strong></span></span></td>
<td><span data-ttu-id="a4d46-444">Utilizzare <em>supporti</em>. <strong>GetItemInfo</strong>, <em>supporto</em>. <strong>getItemInfoByAtom</strong>e i metodi associati per recuperare i metadati.</span><span class="sxs-lookup"><span data-stu-id="a4d46-444">Use <em>Media</em>.<strong>getItemInfo</strong>, <em>Media</em>.<strong>getItemInfoByAtom</strong>, and their associated methods to retrieve metadata.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-445"><em>Player6</em>. <strong>GetMediaParameter</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-445"><em>Player6</em>.<strong>GetMediaParameter</strong></span></span></td>
<td><span data-ttu-id="a4d46-446">Usare <em>playlist</em>. <strong>elemento</strong> per recuperare un elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="a4d46-446">Use <em>Playlist</em>.<strong>item</strong> to retrieve a media item.</span></span> <span data-ttu-id="a4d46-447">Usare quindi i <em>supporti</em>. <strong>GetItemInfo</strong> per recuperare la stringa di parametro.</span><span class="sxs-lookup"><span data-stu-id="a4d46-447">Then use <em>Media</em>.<strong>getItemInfo</strong> to retrieve the parameter string.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-448"><em>Player6</em>. <strong>GetMediaParameterName</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-448"><em>Player6</em>.<strong>GetMediaParameterName</strong></span></span></td>
<td><span data-ttu-id="a4d46-449">Usare <em>playlist</em>. <strong>elemento</strong> per recuperare un elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="a4d46-449">Use <em>Playlist</em>.<strong>item</strong> to retrieve a media item.</span></span> <span data-ttu-id="a4d46-450">Usare quindi i <em>supporti</em>. <strong>GetAttribute</strong> per recuperare la stringa di parametro.</span><span class="sxs-lookup"><span data-stu-id="a4d46-450">Then use <em>Media</em>.<strong>getAttributeName</strong> to retrieve the parameter string.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-451"><em>Player6</em>. <strong>GetMoreInfoURL</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-451"><em>Player6</em>.<strong>GetMoreInfoURL</strong></span></span></td>
<td><span data-ttu-id="a4d46-452">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-452">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-453"><em>Player6</em>. <strong>GetNumberOfChapters</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-453"><em>Player6</em>.<strong>GetNumberOfChapters</strong></span></span></td>
<td><span data-ttu-id="a4d46-454">Se un titolo è attualmente in riproduzione, usare <em>currentPlaylist</em>. <strong>conteggio</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-454">If a title is currently playing, use <em>currentPlaylist</em>.<strong>count</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-455"><em>Player6</em>. <strong>GetStreamGroup</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-455"><em>Player6</em>.<strong>GetStreamGroup</strong></span></span></td>
<td><span data-ttu-id="a4d46-456">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-456">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-457"><em>Player6</em>. <strong>GetStreamName</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-457"><em>Player6</em>.<strong>GetStreamName</strong></span></span></td>
<td><span data-ttu-id="a4d46-458">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-458">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-459"><em>Player6</em>. <strong>GetStreamSelected</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-459"><em>Player6</em>.<strong>GetStreamSelected</strong></span></span></td>
<td><span data-ttu-id="a4d46-460">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-460">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-461"><em>Player6</em>. <strong>GetSubpictureLanguage</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-461"><em>Player6</em>.<strong>GetSubpictureLanguage</strong></span></span></td>
<td><span data-ttu-id="a4d46-462">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-462">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-463"><em>Player6</em>. <strong>Goup</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-463"><em>Player6</em>.<strong>GoUp</strong></span></span></td>
<td><span data-ttu-id="a4d46-464">Usare il <em>DVD</em>. <strong>indietro</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-464">Use <em>DVD</em>.<strong>back</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-465"><em>Player6</em>. <strong>IsSoundCardEnabled</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-465"><em>Player6</em>.<strong>IsSoundCardEnabled</strong></span></span></td>
<td><span data-ttu-id="a4d46-466">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-466">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-467"><em>Player6</em>. <strong>LeftButtonSelect</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-467"><em>Player6</em>.<strong>LeftButtonSelect</strong></span></span></td>
<td><span data-ttu-id="a4d46-468">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-468">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-469"><em>Player6</em>. <strong>LowerButtonSelect</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-469"><em>Player6</em>.<strong>LowerButtonSelect</strong></span></span></td>
<td><span data-ttu-id="a4d46-470">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-470">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-471"><em>Player6</em>. <strong>MenuCall</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-471"><em>Player6</em>.<strong>MenuCall</strong></span></span></td>
<td><span data-ttu-id="a4d46-472">Usare il <em>DVD</em>. <strong>titleMenu</strong> o <em>DVD</em>. <strong>menu di scelta rapida</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-472">Use <em>DVD</em>.<strong>titleMenu</strong> or <em>DVD</em>.<strong>topMenu</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-473"><em>Player6</em>. <strong>Avanti</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-473"><em>Player6</em>.<strong>Next</strong></span></span></td>
<td><span data-ttu-id="a4d46-474">Usare i <em>controlli</em>. <strong>quindi</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-474">Use <em>Controls</em>.<strong>next</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-475"><em>Player6</em>. <strong>NextPGSearch</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-475"><em>Player6</em>.<strong>NextPGSearch</strong></span></span></td>
<td><span data-ttu-id="a4d46-476">Usare i <em>controlli</em>. <strong>quindi</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-476">Use <em>Controls</em>.<strong>next</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-477"><em>Player6</em>. <strong>Apri</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-477"><em>Player6</em>.<strong>Open</strong></span></span></td>
<td><span data-ttu-id="a4d46-478">Usare <em>Player</em>. <strong>URL</strong> o <em>lettore</em>. <strong>currentMedia</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-478">Use <em>Player</em>.<strong>URL</strong> or <em>Player</em>.<strong>currentMedia</strong>.</span></span> <span data-ttu-id="a4d46-479">I file vengono sempre aperti in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="a4d46-479">Files always open asynchronously.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-480"><em>Player6</em>. <strong>Sospendi</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-480"><em>Player6</em>.<strong>Pause</strong></span></span></td>
<td><span data-ttu-id="a4d46-481">Usare i <em>controlli</em>. <strong>Sospendi</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-481">Use <em>Controls</em>.<strong>pause</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-482"><em>Player6</em>. <strong>Esegui la riproduzione</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-482"><em>Player6</em>.<strong>Play</strong></span></span></td>
<td><span data-ttu-id="a4d46-483">Usare i <em>controlli</em>. <strong>Riproduci</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-483">Use <em>Controls</em>.<strong>play</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-484"><em>Player6</em>. <strong>Precedente</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-484"><em>Player6</em>.<strong>Previous</strong></span></span></td>
<td><span data-ttu-id="a4d46-485">Usare i <em>controlli</em>. <strong>precedente</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-485">Use <em>Controls</em>.<strong>previous</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-486"><em>Player6</em>. <strong>PrevPGSearch</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-486"><em>Player6</em>.<strong>PrevPGSearch</strong></span></span></td>
<td><span data-ttu-id="a4d46-487">Usare i <em>controlli</em>. <strong>precedente</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-487">Use <em>Controls</em>.<strong>previous</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-488"><em>Player6</em>. <strong>ResumeFromMenu</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-488"><em>Player6</em>.<strong>ResumeFromMenu</strong></span></span></td>
<td><span data-ttu-id="a4d46-489">Usare il <em>DVD</em>. <strong>riprendere</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-489">Use <em>DVD</em>.<strong>resume</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-490"><em>Player6</em>. <strong>RightButtonSelect</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-490"><em>Player6</em>.<strong>RightButtonSelect</strong></span></span></td>
<td><span data-ttu-id="a4d46-491">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-491">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-492"><em>Player6</em>. <strong>SetCurrentEntry</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-492"><em>Player6</em>.<strong>SetCurrentEntry</strong></span></span></td>
<td><span data-ttu-id="a4d46-493">Recuperare un oggetto multimediale utilizzando <em>currentPlaylist</em>. <strong>elemento</strong>(<em>entryNumber</em>).</span><span class="sxs-lookup"><span data-stu-id="a4d46-493">Retrieve a media object using <em>currentPlaylist</em>.<strong>item</strong>(<em>entryNumber</em>).</span></span> <span data-ttu-id="a4d46-494">Specificare quindi l'oggetto supporto recuperato utilizzando i <em>controlli</em>. <strong>CurrentItem</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-494">Then, specify the retrieved media object using <em>Controls</em>.<strong>currentItem</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-495"><em>Player6</em>. <strong>ShowDialog</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-495"><em>Player6</em>.<strong>ShowDialog</strong></span></span></td>
<td><span data-ttu-id="a4d46-496">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-496">Not available.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-497"><em>Player6</em>. <strong>StillOff</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-497"><em>Player6</em>.<strong>StillOff</strong></span></span></td>
<td><span data-ttu-id="a4d46-498">Usare i <em>controlli</em>. <strong>Riproduci</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-498">Use <em>Controls</em>.<strong>play</strong>.</span></span> <span data-ttu-id="a4d46-499">In alternativa, usare i <em>controlli</em>. A questo punto <strong>, se attualmente</strong> si trova in modalità continua.</span><span class="sxs-lookup"><span data-stu-id="a4d46-499">Alternatively, use <em>Controls</em>.<strong>Next</strong> if currently in still mode.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-500"><em>Player6</em>. <strong>Arresta</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-500"><em>Player6</em>.<strong>Stop</strong></span></span></td>
<td><span data-ttu-id="a4d46-501">Usare i <em>controlli</em>. <strong>arrestare</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-501">Use <em>Controls</em>.<strong>stop</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-502"><em>Player6</em>. <strong>StreamSelect</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-502"><em>Player6</em>.<strong>StreamSelect</strong></span></span></td>
<td><span data-ttu-id="a4d46-503">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-503">Not available.</span></span> <span data-ttu-id="a4d46-504">Usare i <em>controlli</em>. <strong>currentAudioLanguage</strong> per specificare un flusso di lingua audio.</span><span class="sxs-lookup"><span data-stu-id="a4d46-504">Use <em>Controls</em>.<strong>currentAudioLanguage</strong> to specify an audio language stream.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-505"><em>Player6</em>. <strong>TimePlay</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-505"><em>Player6</em>.<strong>TimePlay</strong></span></span></td>
<td><span data-ttu-id="a4d46-506">Dalla playlist radice usare <em>currentPlaylist</em>. <strong>elemento</strong>(<em>Indice</em>) per recuperare un oggetto multimediale.</span><span class="sxs-lookup"><span data-stu-id="a4d46-506">From the root playlist, use <em>currentPlaylist</em>.<strong>item</strong>(<em>index</em>) to retrieve a media object.</span></span> <span data-ttu-id="a4d46-507">Impostare quindi l'oggetto supporto come quello corrente usando i <em>controlli</em>. <strong>CurrentItem</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-507">Then, set the media object as the current one using <em>Controls</em>.<strong>currentItem</strong>.</span></span> <span data-ttu-id="a4d46-508">Specificare quindi i <em>controlli</em>. <strong>currentPosition</strong> che utilizza un valore di ora in secondi.</span><span class="sxs-lookup"><span data-stu-id="a4d46-508">Then, specify <em>Controls</em>.<strong>currentPosition</strong> using a time value in seconds.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-509"><em>Player6</em>. <strong>TimeSearch</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-509"><em>Player6</em>.<strong>TimeSearch</strong></span></span></td>
<td><span data-ttu-id="a4d46-510">Usare i <em>controlli</em>. <strong>currentPosition</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-510">Use <em>Controls</em>.<strong>currentPosition</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-511"><em>Player6</em>. <strong>TitlePlay</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-511"><em>Player6</em>.<strong>TitlePlay</strong></span></span></td>
<td><span data-ttu-id="a4d46-512">Se si sta già eseguendo la playlist del titolo specificata, recuperare il capitolo desiderato come oggetto multimediale usando la sintassi seguente:</span><span class="sxs-lookup"><span data-stu-id="a4d46-512">If already playing the specified title playlist, retrieve the desired chapter as a media object using the following syntax:</span></span>
<pre data-space="preserve"><code>var media = Player.currentPlaylist.item(index);</code></pre>
<span data-ttu-id="a4d46-513">Quindi, specificare <em>Player</em>. <strong>currentMedia</strong> utilizzando l'oggetto multimediale restituito.</span><span class="sxs-lookup"><span data-stu-id="a4d46-513">Then, specify <em>Player</em>.<strong>currentMedia</strong> using the media object returned.</span></span><br/> <span data-ttu-id="a4d46-514">In alternativa, usare <em>currentPlaylist</em>. <strong>elemento</strong> per recuperare un oggetto multimediale, quindi utilizzare l'oggetto multimediale restituito per specificare i <em>controlli</em>. <strong>CurrentItem</strong>.</span><span class="sxs-lookup"><span data-stu-id="a4d46-514">Alternatively, use <em>currentPlaylist</em>.<strong>item</strong> to retrieve a media object, and then use the media object returned to specify <em>Controls</em>.<strong>currentItem</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-515"><em>Player6</em>. <strong>TopPGSearch</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-515"><em>Player6</em>.<strong>TopPGSearch</strong></span></span></td>
<td><span data-ttu-id="a4d46-516">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-516">Not available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4d46-517"><em>Player6</em>. <strong>UOPValid</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-517"><em>Player6</em>.<strong>UOPValid</strong></span></span></td>
<td><span data-ttu-id="a4d46-518">Non disponibile</span><span class="sxs-lookup"><span data-stu-id="a4d46-518">Not available</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4d46-519"><em>Player6</em>. <strong>UpperButtonSelect</strong></span><span class="sxs-lookup"><span data-stu-id="a4d46-519"><em>Player6</em>.<strong>UpperButtonSelect</strong></span></span></td>
<td><span data-ttu-id="a4d46-520">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-520">Not available.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="a4d46-521">Nella tabella seguente vengono confrontati gli eventi del modello a oggetti di Windows Media Player versione 6,4 con il modello a oggetti di Windows Media Player 7 o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="a4d46-521">The following table compares the Windows Media Player version 6.4 object model events with the Windows Media Player 7 or later object model.</span></span>



| <span data-ttu-id="a4d46-522">Evento Windows Media Player 6,4</span><span class="sxs-lookup"><span data-stu-id="a4d46-522">Windows Media Player 6.4 event</span></span>  | <span data-ttu-id="a4d46-523">Equivalente a Windows Media Player 7 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="a4d46-523">Windows Media Player 7 or later equivalent</span></span>                                                                                                                                                                               |
|---------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4d46-524">*Player6*. **Memorizzazione nel buffer**</span><span class="sxs-lookup"><span data-stu-id="a4d46-524">*Player6*.**Buffering**</span></span>         | <span data-ttu-id="a4d46-525">Usare *Player*. **Memorizzazione nel buffer**.</span><span class="sxs-lookup"><span data-stu-id="a4d46-525">Use *Player*.**Buffering**.</span></span>                                                                                                                                                                                              |
| <span data-ttu-id="a4d46-526">*Player6*. **Fare clic su**</span><span class="sxs-lookup"><span data-stu-id="a4d46-526">*Player6*.**Click**</span></span>             | <span data-ttu-id="a4d46-527">Usare *Player*. **Fare clic su**</span><span class="sxs-lookup"><span data-stu-id="a4d46-527">Use *Player*.**Click**</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="a4d46-528">*Player6*. **DblClick**</span><span class="sxs-lookup"><span data-stu-id="a4d46-528">*Player6*.**DblClick**</span></span>          | <span data-ttu-id="a4d46-529">Usare *Player*. **DoubleClick**</span><span class="sxs-lookup"><span data-stu-id="a4d46-529">Use *Player*.**DoubleClick**</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="a4d46-530">*Player6*. **Disconnetti**</span><span class="sxs-lookup"><span data-stu-id="a4d46-530">*Player6*.**Disconnect**</span></span>        | <span data-ttu-id="a4d46-531">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-531">Not available.</span></span>                                                                                                                                                                                                           |
| <span data-ttu-id="a4d46-532">*Player6*. **DisplayModeChange**</span><span class="sxs-lookup"><span data-stu-id="a4d46-532">*Player6*.**DisplayModeChange**</span></span> | <span data-ttu-id="a4d46-533">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-533">Not available.</span></span>                                                                                                                                                                                                           |
| <span data-ttu-id="a4d46-534">*Player6*. **DVDNotify**</span><span class="sxs-lookup"><span data-stu-id="a4d46-534">*Player6*.**DVDNotify**</span></span>         | <span data-ttu-id="a4d46-535">*Player*. **DomainChange** e *Player*. **OpenPlaylistSwitch** sono eventi specifici del DVD.</span><span class="sxs-lookup"><span data-stu-id="a4d46-535">*Player*.**DomainChange** and *Player*.**OpenPlaylistSwitch** are DVD-specific events.</span></span> <span data-ttu-id="a4d46-536">Potrebbero essere applicati anche altri eventi relativi a playlist, supporti multimediali e CD-ROM, a seconda dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="a4d46-536">Other events related to playlists, media, and CD-ROM media may apply as well depending on the application.</span></span>                        |
| <span data-ttu-id="a4d46-537">*Player6*. **EndOfStream**</span><span class="sxs-lookup"><span data-stu-id="a4d46-537">*Player6*.**EndOfStream**</span></span>       | <span data-ttu-id="a4d46-538">Usare *Player*. **Riproduzione**.</span><span class="sxs-lookup"><span data-stu-id="a4d46-538">Use *Player*.**PlayState**.</span></span>                                                                                                                                                                                              |
| <span data-ttu-id="a4d46-539">*Player6*. **Errore**</span><span class="sxs-lookup"><span data-stu-id="a4d46-539">*Player6*.**Error**</span></span>             | <span data-ttu-id="a4d46-540">L'evento è invariato.</span><span class="sxs-lookup"><span data-stu-id="a4d46-540">The event is unchanged.</span></span> <span data-ttu-id="a4d46-541">Gli errori, tuttavia, vengono accodati.</span><span class="sxs-lookup"><span data-stu-id="a4d46-541">Errors, however, are queued.</span></span> <span data-ttu-id="a4d46-542">Usare l'oggetto **Error** con l'oggetto **ErrorItem** per recuperare le informazioni sull'errore dalla coda.</span><span class="sxs-lookup"><span data-stu-id="a4d46-542">Use the **Error** object with the **ErrorItem** object to retrieve error information from the queue.</span></span> <span data-ttu-id="a4d46-543">Vedere il codice di esempio nella sezione precedente, gestione degli errori.</span><span class="sxs-lookup"><span data-stu-id="a4d46-543">See the example code in the preceding section, Error handling.</span></span> |
| <span data-ttu-id="a4d46-544">*Player6*. **KeyDown**</span><span class="sxs-lookup"><span data-stu-id="a4d46-544">*Player6*.**KeyDown**</span></span>           | <span data-ttu-id="a4d46-545">Usare *Player*. **KeyDown**</span><span class="sxs-lookup"><span data-stu-id="a4d46-545">Use *Player*.**Keydown**</span></span>                                                                                                                                                                                                 |
| <span data-ttu-id="a4d46-546">*Player6*. **Pressione** del tasto</span><span class="sxs-lookup"><span data-stu-id="a4d46-546">*Player6*.**KeyPress**</span></span>          | <span data-ttu-id="a4d46-547">Usare *Player*. **Pressione** del tasto</span><span class="sxs-lookup"><span data-stu-id="a4d46-547">Use *Player*.**KeyPress**</span></span>                                                                                                                                                                                                |
| <span data-ttu-id="a4d46-548">*Player6*. **Evento KeyUp**</span><span class="sxs-lookup"><span data-stu-id="a4d46-548">*Player6*.**KeyUp**</span></span>             | <span data-ttu-id="a4d46-549">Usare *Player*. **Evento KeyUp**</span><span class="sxs-lookup"><span data-stu-id="a4d46-549">Use *Player*.**KeyUp**</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="a4d46-550">*Player6*. **MarkerHit**</span><span class="sxs-lookup"><span data-stu-id="a4d46-550">*Player6*.**MarkerHit**</span></span>         | <span data-ttu-id="a4d46-551">Usare *Player*. **MarkerHit**.</span><span class="sxs-lookup"><span data-stu-id="a4d46-551">Use *Player*.**MarkerHit**.</span></span>                                                                                                                                                                                              |
| <span data-ttu-id="a4d46-552">*Player6*. **MouseDown**</span><span class="sxs-lookup"><span data-stu-id="a4d46-552">*Player6*.**MouseDown**</span></span>         | <span data-ttu-id="a4d46-553">Usare *Player*. **MouseDown**</span><span class="sxs-lookup"><span data-stu-id="a4d46-553">Use *Player*.**MouseDown**</span></span>                                                                                                                                                                                               |
| <span data-ttu-id="a4d46-554">*Player6*. **MouseMove**</span><span class="sxs-lookup"><span data-stu-id="a4d46-554">*Player6*.**MouseMove**</span></span>         | <span data-ttu-id="a4d46-555">Usare *Player*. **MouseMove**</span><span class="sxs-lookup"><span data-stu-id="a4d46-555">Use *Player*.**MouseMove**</span></span>                                                                                                                                                                                               |
| <span data-ttu-id="a4d46-556">*Player6*. **MouseUp**</span><span class="sxs-lookup"><span data-stu-id="a4d46-556">*Player6*.**MouseUp**</span></span>           | <span data-ttu-id="a4d46-557">Usare *Player*. **MouseUp**</span><span class="sxs-lookup"><span data-stu-id="a4d46-557">Use *Player*.**MouseUp**</span></span>                                                                                                                                                                                                 |
| <span data-ttu-id="a4d46-558">*Player6*. **NewStream**</span><span class="sxs-lookup"><span data-stu-id="a4d46-558">*Player6*.**NewStream**</span></span>         | <span data-ttu-id="a4d46-559">Usare *Player*. **OpenStateChange**</span><span class="sxs-lookup"><span data-stu-id="a4d46-559">Use *Player*.**OpenStateChange**</span></span>                                                                                                                                                                                         |
| <span data-ttu-id="a4d46-560">*Player6*. **OpenStateChange**</span><span class="sxs-lookup"><span data-stu-id="a4d46-560">*Player6*.**OpenStateChange**</span></span>   | <span data-ttu-id="a4d46-561">Usare *Player*. **OpenStateChange**.</span><span class="sxs-lookup"><span data-stu-id="a4d46-561">Use *Player*.**OpenStateChange**.</span></span>                                                                                                                                                                                        |
| <span data-ttu-id="a4d46-562">*Player6*. **PlayStateChange**</span><span class="sxs-lookup"><span data-stu-id="a4d46-562">*Player6*.**PlayStateChange**</span></span>   | <span data-ttu-id="a4d46-563">Usare *Player*. **PlayStateChange**.</span><span class="sxs-lookup"><span data-stu-id="a4d46-563">Use *Player*.**PlayStateChange**.</span></span>                                                                                                                                                                                        |
| <span data-ttu-id="a4d46-564">*Player6*. **PositionChange**</span><span class="sxs-lookup"><span data-stu-id="a4d46-564">*Player6*.**PositionChange**</span></span>    | <span data-ttu-id="a4d46-565">Usare *Player*. **PositionChange**.</span><span class="sxs-lookup"><span data-stu-id="a4d46-565">Use *Player*.**PositionChange**.</span></span>                                                                                                                                                                                         |
| <span data-ttu-id="a4d46-566">*Player6*. **ReadyStateChange**</span><span class="sxs-lookup"><span data-stu-id="a4d46-566">*Player6*.**ReadyStateChange**</span></span>  | <span data-ttu-id="a4d46-567">Usare *Player*. **PlayStateChange**.</span><span class="sxs-lookup"><span data-stu-id="a4d46-567">Use *Player*.**PlayStateChange**.</span></span>                                                                                                                                                                                        |
| <span data-ttu-id="a4d46-568">*Player6*. **ScriptCommand**</span><span class="sxs-lookup"><span data-stu-id="a4d46-568">*Player6*.**ScriptCommand**</span></span>     | <span data-ttu-id="a4d46-569">Usare *Player*. **ScriptCommand**.</span><span class="sxs-lookup"><span data-stu-id="a4d46-569">Use *Player*.**ScriptCommand**.</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="a4d46-570">*Player6*. **Avviso** di</span><span class="sxs-lookup"><span data-stu-id="a4d46-570">*Player6*.**Warning**</span></span>           | <span data-ttu-id="a4d46-571">Non disponibile.</span><span class="sxs-lookup"><span data-stu-id="a4d46-571">Not available.</span></span>                                                                                                                                                                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="a4d46-572">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a4d46-572">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4d46-573">**Guida alla migrazione del modello a oggetti**</span><span class="sxs-lookup"><span data-stu-id="a4d46-573">**Object Model Migration Guide**</span></span>](object-model-migration-guide.md)
</dt> <dt>

[<span data-ttu-id="a4d46-574">**Riferimento del modello a oggetti per lo scripting**</span><span class="sxs-lookup"><span data-stu-id="a4d46-574">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 





