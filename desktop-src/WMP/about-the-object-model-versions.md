---
title: Informazioni sulle versioni del modello a oggetti
description: Informazioni sulle versioni del modello a oggetti
ms.assetid: 20bb1681-9079-4f8c-bb5e-5c98e3bdc76a
keywords:
- Windows Media Player, versioni
- Modello a oggetti di Windows Media Player, versioni
- modello a oggetti, versioni
- Controllo ActiveX di Windows Media Player, versioni per il modello a oggetti
- Controllo ActiveX, versioni per il modello a oggetti
- Controllo ActiveX Windows Media Player Mobile, versioni per il modello a oggetti
- Windows Media Player Mobile, versioni per il modello a oggetti
- versioni di Windows Media Player, modello a oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59886f5750b6fc42112f73d6bb6e05e8d013ffdc
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/21/2020
ms.locfileid: "104398751"
---
# <a name="about-the-object-model-versions"></a><span data-ttu-id="8113f-111">Informazioni sulle versioni del modello a oggetti</span><span class="sxs-lookup"><span data-stu-id="8113f-111">About the Object Model Versions</span></span>

<span data-ttu-id="8113f-112">In Windows Media Player 7,0 è stato introdotto un nuovo modello a oggetti.</span><span class="sxs-lookup"><span data-stu-id="8113f-112">Windows Media Player 7.0 introduced a new object model.</span></span> <span data-ttu-id="8113f-113">Questo modello a oggetti è stato esteso con Windows Media Player 7,1, Windows Media Player per Windows XP, Windows Media Player 9 Series, Windows Media Player 10, Windows Media Player 11 e Windows Media Player 12.</span><span class="sxs-lookup"><span data-stu-id="8113f-113">This object model has been extended with Windows Media Player 7.1, Windows Media Player for Windows XP, Windows Media Player 9 Series, Windows Media Player 10, Windows Media Player 11, and Windows Media Player 12.</span></span> <span data-ttu-id="8113f-114">Ogni argomento del riferimento del modello a oggetti include una sezione requisiti che descrive in dettaglio il requisito minimo per la singola proprietà, metodo o evento.</span><span class="sxs-lookup"><span data-stu-id="8113f-114">Each topic in the Object Model Reference includes a Requirements section that details the minimum requirement for the individual property, method, or event.</span></span> <span data-ttu-id="8113f-115">Negli elenchi seguenti vengono illustrati in dettaglio i nuovi oggetti, i metodi, le proprietà e gli eventi aggiunti per ogni versione a partire dalla versione 7,0.</span><span class="sxs-lookup"><span data-stu-id="8113f-115">The following lists detail the new objects, methods, properties, and events that have been added for each version since version 7.0.</span></span> <span data-ttu-id="8113f-116">Questi elenchi includono inoltre nuove interfacce, metodi ed eventi di C++.</span><span class="sxs-lookup"><span data-stu-id="8113f-116">These lists also include new C++ interfaces, methods, and events.</span></span>

<span data-ttu-id="8113f-117">Quando viene esposta anche un'interfaccia nuova o aggiornata come oggetto, viene elencato solo l'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8113f-117">Where a new or updated interface is also exposed as an object, only the object is listed.</span></span> <span data-ttu-id="8113f-118">Per individuare l'interfaccia, fare riferimento al [riferimento del modello a oggetti per C++](object-model-reference-for-c.md).</span><span class="sxs-lookup"><span data-stu-id="8113f-118">To locate the interface, refer to the [Object Model Reference for C++](object-model-reference-for-c.md).</span></span> <span data-ttu-id="8113f-119">In genere, sarà sufficiente aggiungere il prefisso IWMP al nome dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="8113f-119">Usually, you will simply need to add the IWMP prefix to the object name.</span></span> <span data-ttu-id="8113f-120">Se una nuova interfaccia ne estende una esistente, potrebbe essere necessario cercare il numero di versione più recente.</span><span class="sxs-lookup"><span data-stu-id="8113f-120">If a new interface extends an existing one, you may need to look for the latest version number.</span></span> <span data-ttu-id="8113f-121">Ad esempio, nella serie Windows Media Player 9 sono stati introdotti nuovi metodi e proprietà disponibili dall'oggetto [**Settings**](settings-object.md) .</span><span class="sxs-lookup"><span data-stu-id="8113f-121">For example, Windows Media Player 9 Series introduced new properties and methods available from the [**Settings**](settings-object.md) object.</span></span> <span data-ttu-id="8113f-122">In C++ sono disponibili tramite l'interfaccia [**IWMPSettings2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings2) , che estende [**IWMPSettings**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings).</span><span class="sxs-lookup"><span data-stu-id="8113f-122">In C++, these are available through the [**IWMPSettings2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings2) interface, which extends [**IWMPSettings**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings).</span></span>

## <a name="added-for-windows-media-player-71"></a><span data-ttu-id="8113f-123">Aggiunta per Windows Media Player 7,1</span><span class="sxs-lookup"><span data-stu-id="8113f-123">Added for Windows Media Player 7.1</span></span>

-   [<span data-ttu-id="8113f-124">**Proprietà Player. stretchToFit**</span><span class="sxs-lookup"><span data-stu-id="8113f-124">**Player.stretchToFit Property**</span></span>](player-stretchtofit.md)

## <a name="added-for-windows-media-player-for-windows-xp"></a><span data-ttu-id="8113f-125">Aggiunta per Windows Media Player per Windows XP</span><span class="sxs-lookup"><span data-stu-id="8113f-125">Added for Windows Media Player for Windows XP</span></span>

-   [<span data-ttu-id="8113f-126">**Metodo Controls. Step**</span><span class="sxs-lookup"><span data-stu-id="8113f-126">**Controls.step Method**</span></span>](controls-step.md)
-   [<span data-ttu-id="8113f-127">**Oggetto DVD**</span><span class="sxs-lookup"><span data-stu-id="8113f-127">**DVD Object**</span></span>](dvd-object.md)
-   [<span data-ttu-id="8113f-128">**Proprietà media. Error**</span><span class="sxs-lookup"><span data-stu-id="8113f-128">**Media.error Property**</span></span>](media-error.md)
-   [<span data-ttu-id="8113f-129">**Evento Player. DomainChange**</span><span class="sxs-lookup"><span data-stu-id="8113f-129">**Player.DomainChange Event**</span></span>](player-player-domainchange.md)
-   [<span data-ttu-id="8113f-130">**Evento Player. errore MediaError**</span><span class="sxs-lookup"><span data-stu-id="8113f-130">**Player.MediaError Event**</span></span>](player-player-mediaerror.md)
-   [<span data-ttu-id="8113f-131">**Evento Player. OpenPlaylistSwitch**</span><span class="sxs-lookup"><span data-stu-id="8113f-131">**Player.OpenPlaylistSwitch Event**</span></span>](player-player-openplaylistswitch.md)
-   [<span data-ttu-id="8113f-132">**Proprietà Player. windowlessVideo**</span><span class="sxs-lookup"><span data-stu-id="8113f-132">**Player.windowlessVideo Property**</span></span>](player-windowlessvideo.md)

## <a name="added-for-windows-media-player-9-series"></a><span data-ttu-id="8113f-133">Aggiunta per la serie Windows Media Player 9</span><span class="sxs-lookup"><span data-stu-id="8113f-133">Added for Windows Media Player 9 Series</span></span>

-   [<span data-ttu-id="8113f-134">**ClosedCaption. getSAMILangID, metodo**</span><span class="sxs-lookup"><span data-stu-id="8113f-134">**ClosedCaption.getSAMILangID Method**</span></span>](closedcaption-getsamilangid.md)
-   [<span data-ttu-id="8113f-135">**ClosedCaption. getSAMILangName, metodo**</span><span class="sxs-lookup"><span data-stu-id="8113f-135">**ClosedCaption.getSAMILangName Method**</span></span>](closedcaption-getsamilangname.md)
-   [<span data-ttu-id="8113f-136">**ClosedCaption. getSAMIStyleName, metodo**</span><span class="sxs-lookup"><span data-stu-id="8113f-136">**ClosedCaption.getSAMIStyleName Method**</span></span>](closedcaption-getsamistylename.md)
-   [<span data-ttu-id="8113f-137">**Proprietà ClosedCaption. SAMILangCount**</span><span class="sxs-lookup"><span data-stu-id="8113f-137">**ClosedCaption.SAMILangCount Property**</span></span>](closedcaption-samilangcount.md)
-   [<span data-ttu-id="8113f-138">**Proprietà ClosedCaption. SAMIStyleCount**</span><span class="sxs-lookup"><span data-stu-id="8113f-138">**ClosedCaption.SAMIStyleCount Property**</span></span>](closedcaption-samistylecount.md)
-   [<span data-ttu-id="8113f-139">**Proprietà Controls. audioLanguageCount**</span><span class="sxs-lookup"><span data-stu-id="8113f-139">**Controls.audioLanguageCount Property**</span></span>](controls-audiolanguagecount.md)
-   [<span data-ttu-id="8113f-140">**Proprietà Controls. currentAudioLanguage**</span><span class="sxs-lookup"><span data-stu-id="8113f-140">**Controls.currentAudioLanguage Property**</span></span>](controls-currentaudiolanguage.md)
-   [<span data-ttu-id="8113f-141">**Proprietà Controls. currentAudioLanguageIndex**</span><span class="sxs-lookup"><span data-stu-id="8113f-141">**Controls.currentAudioLanguageIndex Property**</span></span>](controls-currentaudiolanguageindex.md)
-   [<span data-ttu-id="8113f-142">**Proprietà Controls. currentPositionTimecode**</span><span class="sxs-lookup"><span data-stu-id="8113f-142">**Controls.currentPositionTimecode Property**</span></span>](controls-currentpositiontimecode.md)
-   [<span data-ttu-id="8113f-143">**Controls. getAudioLanguageDescription, metodo**</span><span class="sxs-lookup"><span data-stu-id="8113f-143">**Controls.getAudioLanguageDescription Method**</span></span>](controls-getaudiolanguagedescription.md)
-   [<span data-ttu-id="8113f-144">**Controls. getAudioLanguageID, metodo**</span><span class="sxs-lookup"><span data-stu-id="8113f-144">**Controls.getAudioLanguageID Method**</span></span>](controls-getaudiolanguageid.md)
-   [<span data-ttu-id="8113f-145">**Controls. getLanguageName, metodo**</span><span class="sxs-lookup"><span data-stu-id="8113f-145">**Controls.getLanguageName Method**</span></span>](controls-getlanguagename.md)
-   [<span data-ttu-id="8113f-146">**Proprietà ErrorItem. Condition**</span><span class="sxs-lookup"><span data-stu-id="8113f-146">**ErrorItem.condition Property**</span></span>](erroritem-condition.md)
-   [<span data-ttu-id="8113f-147">**Proprietà External. appColorLight**</span><span class="sxs-lookup"><span data-stu-id="8113f-147">**External.appColorLight Property**</span></span>](external-appcolorlight.md)
-   [<span data-ttu-id="8113f-148">**Evento External. OnColorChange**</span><span class="sxs-lookup"><span data-stu-id="8113f-148">**External.OnColorChange Event**</span></span>](external-oncolorchange-event.md)
-   [<span data-ttu-id="8113f-149">**Proprietà External. Version**</span><span class="sxs-lookup"><span data-stu-id="8113f-149">**External.version Property**</span></span>](external-version.md)
-   [<span data-ttu-id="8113f-150">**IWMPEvents::P evento layerDockedStateChange**</span><span class="sxs-lookup"><span data-stu-id="8113f-150">**IWMPEvents::PlayerDockedStateChange Event**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-playerdockedstatechange)
-   [<span data-ttu-id="8113f-151">**IWMPEvents::P evento layerReconnect**</span><span class="sxs-lookup"><span data-stu-id="8113f-151">**IWMPEvents::PlayerReconnect Event**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-playerreconnect)
-   [<span data-ttu-id="8113f-152">**Evento IWMPEvents:: SwitchedToControl**</span><span class="sxs-lookup"><span data-stu-id="8113f-152">**IWMPEvents::SwitchedToControl Event**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-switchedtocontrol)
-   [<span data-ttu-id="8113f-153">**Evento IWMPEvents:: SwitchedToPlayerApplication**</span><span class="sxs-lookup"><span data-stu-id="8113f-153">**IWMPEvents::SwitchedToPlayerApplication Event**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-switchedtoplayerapplication)
-   [<span data-ttu-id="8113f-154">**Interfaccia IWMPPlayerServices**</span><span class="sxs-lookup"><span data-stu-id="8113f-154">**IWMPPlayerServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices)
-   [<span data-ttu-id="8113f-155">**Interfaccia IWMPRemoteMediaServices**</span><span class="sxs-lookup"><span data-stu-id="8113f-155">**IWMPRemoteMediaServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices)
-   [<span data-ttu-id="8113f-156">**Interfaccia IWMPSkinManager**</span><span class="sxs-lookup"><span data-stu-id="8113f-156">**IWMPSkinManager Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpskinmanager)
-   [<span data-ttu-id="8113f-157">**Media. getAttributeCountByType, metodo**</span><span class="sxs-lookup"><span data-stu-id="8113f-157">**Media.getAttributeCountByType Method**</span></span>](media-getattributecountbytype.md)
-   [<span data-ttu-id="8113f-158">**Media. getItemInfoByType, metodo**</span><span class="sxs-lookup"><span data-stu-id="8113f-158">**Media.getItemInfoByType Method**</span></span>](media-getiteminfobytype.md)
-   [<span data-ttu-id="8113f-159">**Oggetto MetadataPicture**</span><span class="sxs-lookup"><span data-stu-id="8113f-159">**MetadataPicture Object**</span></span>](metadatapicture-object.md)
-   [<span data-ttu-id="8113f-160">**Oggetto MetadataText**</span><span class="sxs-lookup"><span data-stu-id="8113f-160">**MetadataText Object**</span></span>](metadatatext-object.md)
-   [<span data-ttu-id="8113f-161">**Evento Player. AudioLanguageChange**</span><span class="sxs-lookup"><span data-stu-id="8113f-161">**Player.AudioLanguageChange Event**</span></span>](player-player-audiolanguagechange.md)
-   [<span data-ttu-id="8113f-162">**Proprietà Player. Remote**</span><span class="sxs-lookup"><span data-stu-id="8113f-162">**Player.isRemote Property**</span></span>](player-isremote.md)
-   [<span data-ttu-id="8113f-163">**Evento Player. MediaCollectionAttributeStringChanged**</span><span class="sxs-lookup"><span data-stu-id="8113f-163">**Player.MediaCollectionAttributeStringChanged Event**</span></span>](player-player-mediacollectionattributestringchanged.md)
-   [<span data-ttu-id="8113f-164">**Player. newMedia, metodo**</span><span class="sxs-lookup"><span data-stu-id="8113f-164">**Player.newMedia Method**</span></span>](player-newmedia.md)
-   [<span data-ttu-id="8113f-165">**Player. nuova playlist, metodo**</span><span class="sxs-lookup"><span data-stu-id="8113f-165">**Player.newPlaylist Method**</span></span>](player-newplaylist.md)
-   [<span data-ttu-id="8113f-166">**Player. openPlayer, metodo**</span><span class="sxs-lookup"><span data-stu-id="8113f-166">**Player.openPlayer Method**</span></span>](player-openplayer.md)
-   [<span data-ttu-id="8113f-167">**Proprietà Player. playerApplication**</span><span class="sxs-lookup"><span data-stu-id="8113f-167">**Player.playerApplication Property**</span></span>](player-playerapplication.md)
-   [<span data-ttu-id="8113f-168">**Evento Player. StatusChange**</span><span class="sxs-lookup"><span data-stu-id="8113f-168">**Player.StatusChange Event**</span></span>](player-player-statuschange.md)
-   [<span data-ttu-id="8113f-169">**Oggetto PlayerApplication**</span><span class="sxs-lookup"><span data-stu-id="8113f-169">**PlayerApplication Object**</span></span>](playerapplication-object.md)
-   [<span data-ttu-id="8113f-170">**Proprietà Settings. defaultAudioLanguage**</span><span class="sxs-lookup"><span data-stu-id="8113f-170">**Settings.defaultAudioLanguage Property**</span></span>](settings-defaultaudiolanguage.md)
-   [<span data-ttu-id="8113f-171">**Proprietà Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="8113f-171">**Settings.mediaAccessRights Property**</span></span>](settings-mediaaccessrights.md)
-   [<span data-ttu-id="8113f-172">**Settings. requestMediaAccessRights, metodo**</span><span class="sxs-lookup"><span data-stu-id="8113f-172">**Settings.requestMediaAccessRights Method**</span></span>](settings-requestmediaaccessrights.md)

## <a name="added-for-windows-media-player-10"></a><span data-ttu-id="8113f-173">Aggiunta per Windows Media Player 10</span><span class="sxs-lookup"><span data-stu-id="8113f-173">Added for Windows Media Player 10</span></span>

-   [<span data-ttu-id="8113f-174">**Interfaccia IWMPGraphCreation**</span><span class="sxs-lookup"><span data-stu-id="8113f-174">**IWMPGraphCreation Interface**</span></span>](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpgraphcreation)
-   [<span data-ttu-id="8113f-175">**Interfaccia IWMPPlayerServices2**</span><span class="sxs-lookup"><span data-stu-id="8113f-175">**IWMPPlayerServices2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices2)
-   [<span data-ttu-id="8113f-176">**Interfaccia IWMPSyncDevice**</span><span class="sxs-lookup"><span data-stu-id="8113f-176">**IWMPSyncDevice Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
-   [<span data-ttu-id="8113f-177">**Interfaccia IWMPSyncServices**</span><span class="sxs-lookup"><span data-stu-id="8113f-177">**IWMPSyncServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncservices)
-   [<span data-ttu-id="8113f-178">**Enumerazione WMPDeviceStatus**</span><span class="sxs-lookup"><span data-stu-id="8113f-178">**WMPDeviceStatus Enumeration**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus)
-   [<span data-ttu-id="8113f-179">**Enumerazione WMPSyncState**</span><span class="sxs-lookup"><span data-stu-id="8113f-179">**WMPSyncState Enumeration**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpsyncstate)

## <a name="added-for-windows-media-player-11"></a><span data-ttu-id="8113f-180">Aggiunta per Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="8113f-180">Added for Windows Media Player 11</span></span>

-   [<span data-ttu-id="8113f-181">**Interfaccia IWMPCdromBurn**</span><span class="sxs-lookup"><span data-stu-id="8113f-181">**IWMPCdromBurn Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn)
-   [<span data-ttu-id="8113f-182">**Interfaccia IWMPCdromBurn (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="8113f-182">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
-   [<span data-ttu-id="8113f-183">**Interfaccia IWMPCdromRip**</span><span class="sxs-lookup"><span data-stu-id="8113f-183">**IWMPCdromRip Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip)
-   [<span data-ttu-id="8113f-184">**Interfaccia IWMPCdromRip (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="8113f-184">**IWMPCdromRip Interface (VB and C#)**</span></span>](iwmpcdromrip--vb-and-c.md)
-   [<span data-ttu-id="8113f-185">**Interfaccia IWMPEvents3**</span><span class="sxs-lookup"><span data-stu-id="8113f-185">**IWMPEvents3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents3)
-   [<span data-ttu-id="8113f-186">**Interfaccia IWMPFolderMonitorServices**</span><span class="sxs-lookup"><span data-stu-id="8113f-186">**IWMPFolderMonitorServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)
-   [<span data-ttu-id="8113f-187">**Interfaccia IWMPLibrary**</span><span class="sxs-lookup"><span data-stu-id="8113f-187">**IWMPLibrary Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary)
-   [<span data-ttu-id="8113f-188">**Interfaccia IWMPLibrary (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="8113f-188">**IWMPLibrary Interface (VB and C#)**</span></span>](iwmplibrary--vb-and-c.md)
-   [<span data-ttu-id="8113f-189">**Interfaccia IWMPLibraryServices**</span><span class="sxs-lookup"><span data-stu-id="8113f-189">**IWMPLibraryServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibraryservices)
-   [<span data-ttu-id="8113f-190">**Interfaccia IWMPLibraryServices (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="8113f-190">**IWMPLibraryServices Interface (VB and C#)**</span></span>](iwmplibraryservices--vb-and-c.md)
-   [<span data-ttu-id="8113f-191">**Interfaccia IWMPLibrarySharingServices**</span><span class="sxs-lookup"><span data-stu-id="8113f-191">**IWMPLibrarySharingServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrarysharingservices)
-   [<span data-ttu-id="8113f-192">**Interfaccia IWMPMediaCollection2**</span><span class="sxs-lookup"><span data-stu-id="8113f-192">**IWMPMediaCollection2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection2)
-   [<span data-ttu-id="8113f-193">**Interfaccia IWMPMediaCollection2 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="8113f-193">**IWMPMediaCollection2 Interface (VB and C#)**</span></span>](iwmpmediacollection2--vb-and-c.md)
-   [<span data-ttu-id="8113f-194">**Interfaccia IWMPQuery**</span><span class="sxs-lookup"><span data-stu-id="8113f-194">**IWMPQuery Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpquery)
-   [<span data-ttu-id="8113f-195">**Interfaccia IWMPQuery (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="8113f-195">**IWMPQuery Interface (VB and C#)**</span></span>](iwmpquery--vb-and-c.md)
-   [<span data-ttu-id="8113f-196">**Interfaccia IWMPRenderConfig**</span><span class="sxs-lookup"><span data-stu-id="8113f-196">**IWMPRenderConfig Interface**</span></span>](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmprenderconfig)
-   [<span data-ttu-id="8113f-197">**Interfaccia IWMPStringCollection2**</span><span class="sxs-lookup"><span data-stu-id="8113f-197">**IWMPStringCollection2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection2)
-   [<span data-ttu-id="8113f-198">**Interfaccia IWMPStringCollection2 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="8113f-198">**IWMPStringCollection2 Interface (VB and C#)**</span></span>](iwmpstringcollection2--vb-and-c.md)
-   [<span data-ttu-id="8113f-199">**Interfaccia IWMPSyncDevice2**</span><span class="sxs-lookup"><span data-stu-id="8113f-199">**IWMPSyncDevice2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice2)
-   [<span data-ttu-id="8113f-200">**Interfaccia IWMPVideoRenderConfig**</span><span class="sxs-lookup"><span data-stu-id="8113f-200">**IWMPVideoRenderConfig Interface**</span></span>](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpvideorenderconfig)
-   [<span data-ttu-id="8113f-201">**Oggetto query**</span><span class="sxs-lookup"><span data-stu-id="8113f-201">**Query Object**</span></span>](query-object.md)
-   [<span data-ttu-id="8113f-202">**Enumerazione WMPBurnFormat**</span><span class="sxs-lookup"><span data-stu-id="8113f-202">**WMPBurnFormat Enumeration**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnformat)
-   [<span data-ttu-id="8113f-203">**Enumerazione WMPBurnState**</span><span class="sxs-lookup"><span data-stu-id="8113f-203">**WMPBurnState Enumeration**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate)
-   [<span data-ttu-id="8113f-204">**Enumerazione WMPLibraryType**</span><span class="sxs-lookup"><span data-stu-id="8113f-204">**WMPLibraryType Enumeration**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype)
-   [<span data-ttu-id="8113f-205">**Enumerazione WMPRipState**</span><span class="sxs-lookup"><span data-stu-id="8113f-205">**WMPRipState Enumeration**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate)

## <a name="added-for-windows-media-player-12"></a><span data-ttu-id="8113f-206">Aggiunta per Windows Media Player 12</span><span class="sxs-lookup"><span data-stu-id="8113f-206">Added for Windows Media Player 12</span></span>

-   [<span data-ttu-id="8113f-207">**Interfaccia IWMPAudioRenderConfig**</span><span class="sxs-lookup"><span data-stu-id="8113f-207">**IWMPAudioRenderConfig Interface**</span></span>](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpaudiorenderconfig)
-   [<span data-ttu-id="8113f-208">**Interfaccia IWMPEvents4**</span><span class="sxs-lookup"><span data-stu-id="8113f-208">**IWMPEvents4 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents4)
-   [<span data-ttu-id="8113f-209">**Interfaccia IWMPLibrary2**</span><span class="sxs-lookup"><span data-stu-id="8113f-209">**IWMPLibrary2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary2)
-   [<span data-ttu-id="8113f-210">**Interfaccia IWMPSyncDevice3**</span><span class="sxs-lookup"><span data-stu-id="8113f-210">**IWMPSyncDevice3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice3)

## <a name="related-topics"></a><span data-ttu-id="8113f-211">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="8113f-211">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8113f-212">**Informazioni sul modello a oggetti del lettore**</span><span class="sxs-lookup"><span data-stu-id="8113f-212">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> <dt>

[<span data-ttu-id="8113f-213">**Riferimento del modello a oggetti per lo scripting**</span><span class="sxs-lookup"><span data-stu-id="8113f-213">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




