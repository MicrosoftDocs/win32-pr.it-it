---
title: Novità di Windows Media Player 12
description: In questo argomento vengono elencate le nuove funzionalità di Windows Media Player 12.
ms.assetid: 17f76963-c96d-46c9-82c0-3ed2d8a4e892
keywords:
- Windows Media Player, novità
- Windows Media Player, nuove funzionalità
- Software Development Kit (SDK), Windows Media Player 12
- SDK (Software Development Kit), Windows Media Player 12
- documentazione, Windows Media Player 12 SDK
- Novità, Windows Media Player 12
- nuove funzionalità, Windows Media Player 12
- interfacce, nuove funzionalità di Windows Media Player 12
- attributi, nuove funzionalità di Windows Media Player 12
- metadati, nuove funzionalità di Windows Media Player 12
- enumerazioni, nuove funzionalità di Windows Media Player 12
- flag, nuove funzionalità di Windows Media Player 12
- interfacce, deprecate in Windows Media Player 12
- metodi, deprecati in Windows Media Player 11 e non 12
- versioni di Windows Media Player, nuove funzionalità della versione 12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d16b21077df1f4a9c11edbfa20032ed473f872a0
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2020
ms.locfileid: "104117482"
---
# <a name="whats-new-in-windows-media-player-12"></a><span data-ttu-id="0ec33-118">Novità di Windows Media Player 12</span><span class="sxs-lookup"><span data-stu-id="0ec33-118">What's New in Windows Media Player 12</span></span>

<span data-ttu-id="0ec33-119">In questo argomento vengono elencate le nuove funzionalità di Windows Media Player 12.</span><span class="sxs-lookup"><span data-stu-id="0ec33-119">This topic lists features that are new in Windows Media Player 12.</span></span>

## <a name="new-interfaces"></a><span data-ttu-id="0ec33-120">Nuove interfacce</span><span class="sxs-lookup"><span data-stu-id="0ec33-120">New Interfaces</span></span>

-   [<span data-ttu-id="0ec33-121">**IWMPAudioRenderConfig**</span><span class="sxs-lookup"><span data-stu-id="0ec33-121">**IWMPAudioRenderConfig**</span></span>](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpaudiorenderconfig)
-   [<span data-ttu-id="0ec33-122">**IWMPEvents4**</span><span class="sxs-lookup"><span data-stu-id="0ec33-122">**IWMPEvents4**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents4)
-   [<span data-ttu-id="0ec33-123">**IWMPLibrary2**</span><span class="sxs-lookup"><span data-stu-id="0ec33-123">**IWMPLibrary2**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary2)
-   [<span data-ttu-id="0ec33-124">**IWMPSyncDevice3**</span><span class="sxs-lookup"><span data-stu-id="0ec33-124">**IWMPSyncDevice3**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice3)

## <a name="new-attributes"></a><span data-ttu-id="0ec33-125">Nuovi attributi</span><span class="sxs-lookup"><span data-stu-id="0ec33-125">New Attributes</span></span>

<span data-ttu-id="0ec33-126">I nuovi attributi seguenti per gli elementi multimediali sono disponibili tramite le interfacce [**IWMPMedia**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia) e [**IWMPMedia3**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia3) .</span><span class="sxs-lookup"><span data-stu-id="0ec33-126">The following new attributes for media items are available through the [**IWMPMedia**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia) and [**IWMPMedia3**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia3) interfaces.</span></span>

-   [<span data-ttu-id="0ec33-127">**AlbumCoverURL**</span><span class="sxs-lookup"><span data-stu-id="0ec33-127">**AlbumCoverURL**</span></span>](wm-albumcoverurl-attribute.md)
-   [<span data-ttu-id="0ec33-128">**AlternateSourceURL**</span><span class="sxs-lookup"><span data-stu-id="0ec33-128">**AlternateSourceURL**</span></span>](alternatesourceurl-attribute.md)
-   [<span data-ttu-id="0ec33-129">**DLNASourceURI**</span><span class="sxs-lookup"><span data-stu-id="0ec33-129">**DLNASourceURI**</span></span>](dlnasourceuri-attribute.md)
-   [<span data-ttu-id="0ec33-130">**DLNAServerUDN**</span><span class="sxs-lookup"><span data-stu-id="0ec33-130">**DLNAServerUDN**</span></span>](dlnaserverudn-attribute.md)
-   [<span data-ttu-id="0ec33-131">**DTCPIPHost**</span><span class="sxs-lookup"><span data-stu-id="0ec33-131">**DTCPIPHost**</span></span>](dtcpiphost-attribute.md)
-   [<span data-ttu-id="0ec33-132">**DTCPIPPort**</span><span class="sxs-lookup"><span data-stu-id="0ec33-132">**DTCPIPPort**</span></span>](dtcpipport-attribute.md)
-   [<span data-ttu-id="0ec33-133">**IDLibreria**</span><span class="sxs-lookup"><span data-stu-id="0ec33-133">**LibraryID**</span></span>](libraryid-attribute.md)
-   [<span data-ttu-id="0ec33-134">**LibraryName**</span><span class="sxs-lookup"><span data-stu-id="0ec33-134">**LibraryName**</span></span>](libraryname-attribute.md)

## <a name="new-device-metadata"></a><span data-ttu-id="0ec33-135">Nuovi metadati del dispositivo</span><span class="sxs-lookup"><span data-stu-id="0ec33-135">New Device Metadata</span></span>

<span data-ttu-id="0ec33-136">I nuovi elementi di metadati del dispositivo seguenti possono essere recuperati chiamando [**IWMPSyncDevice:: GetItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-getiteminfo).</span><span class="sxs-lookup"><span data-stu-id="0ec33-136">The following new device metadata items can be retrieved by calling [**IWMPSyncDevice::getItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-getiteminfo).</span></span>

-   <span data-ttu-id="0ec33-137">**BackgroundSyncState**</span><span class="sxs-lookup"><span data-stu-id="0ec33-137">**BackgroundSyncState**</span></span>
-   <span data-ttu-id="0ec33-138">**SkippedFiles**</span><span class="sxs-lookup"><span data-stu-id="0ec33-138">**SkippedFiles**</span></span>
-   <span data-ttu-id="0ec33-139">**SyncFilter**</span><span class="sxs-lookup"><span data-stu-id="0ec33-139">**SyncFilter**</span></span>

<span data-ttu-id="0ec33-140">I nuovi elementi di metadati del dispositivo seguenti possono essere impostati chiamando [**IWMPSyncDevice2:: setItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice2-setiteminfo).</span><span class="sxs-lookup"><span data-stu-id="0ec33-140">The following new device metadata items can be set by calling [**IWMPSyncDevice2::setItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice2-setiteminfo).</span></span>

-   <span data-ttu-id="0ec33-141">**AutoSyncDefaultRules**</span><span class="sxs-lookup"><span data-stu-id="0ec33-141">**AutoSyncDefaultRules**</span></span>
-   <span data-ttu-id="0ec33-142">**BackgroundSyncState**</span><span class="sxs-lookup"><span data-stu-id="0ec33-142">**BackgroundSyncState**</span></span>
-   <span data-ttu-id="0ec33-143">**IncludeSkippedFiles**</span><span class="sxs-lookup"><span data-stu-id="0ec33-143">**IncludeSkippedFiles**</span></span>
-   <span data-ttu-id="0ec33-144">**SyncFilter**</span><span class="sxs-lookup"><span data-stu-id="0ec33-144">**SyncFilter**</span></span>
-   <span data-ttu-id="0ec33-145">**SyncOnConnect**</span><span class="sxs-lookup"><span data-stu-id="0ec33-145">**SyncOnConnect**</span></span>

## <a name="new-enumeration-member"></a><span data-ttu-id="0ec33-146">Nuovo membro di enumerazione</span><span class="sxs-lookup"><span data-stu-id="0ec33-146">New Enumeration Member</span></span>

<span data-ttu-id="0ec33-147">L'enumerazione [**WMPSyncState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpsyncstate) dispone del nuovo membro seguente.</span><span class="sxs-lookup"><span data-stu-id="0ec33-147">The [**WMPSyncState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpsyncstate) enumeration has the following new member.</span></span>

-   <span data-ttu-id="0ec33-148">**wmpssEstimating**</span><span class="sxs-lookup"><span data-stu-id="0ec33-148">**wmpssEstimating**</span></span>

## <a name="new-flag"></a><span data-ttu-id="0ec33-149">Nuovo flag</span><span class="sxs-lookup"><span data-stu-id="0ec33-149">New Flag</span></span>

<span data-ttu-id="0ec33-150">Il metodo [**IWMPGraphCreation:: GetGraphCreationFlags**](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpgraphcreation-getgraphcreationflags) supporta il seguente nuovo flag.</span><span class="sxs-lookup"><span data-stu-id="0ec33-150">The [**IWMPGraphCreation::GetGraphCreationFlags**](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpgraphcreation-getgraphcreationflags) method supports the following new flag.</span></span>

-   <span data-ttu-id="0ec33-151">**\_flag WMPGC \_ usare \_ un \_ grafo personalizzato**</span><span class="sxs-lookup"><span data-stu-id="0ec33-151">**WMPGC\_FLAGS\_USE\_CUSTOM\_GRAPH**</span></span>

## <a name="deprecated-interface"></a><span data-ttu-id="0ec33-152">Interfaccia deprecata</span><span class="sxs-lookup"><span data-stu-id="0ec33-152">Deprecated Interface</span></span>

<span data-ttu-id="0ec33-153">L'interfaccia seguente è deprecata.</span><span class="sxs-lookup"><span data-stu-id="0ec33-153">The following interface is deprecated.</span></span>

-   [<span data-ttu-id="0ec33-154">**IWMPFolderMonitorServices**</span><span class="sxs-lookup"><span data-stu-id="0ec33-154">**IWMPFolderMonitorServices**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)

## <a name="methods-that-are-no-longer-deprecated"></a><span data-ttu-id="0ec33-155">Metodi che non sono più deprecati</span><span class="sxs-lookup"><span data-stu-id="0ec33-155">Methods That Are No Longer Deprecated</span></span>

<span data-ttu-id="0ec33-156">I metodi seguenti sono stati deprecati in Windows Media Player 11 SDK, ma non sono più deprecati.</span><span class="sxs-lookup"><span data-stu-id="0ec33-156">The following methods were deprecated in Windows Media Player 11 SDK, but are no longer deprecated.</span></span>

-   [<span data-ttu-id="0ec33-157">**IWMPGraphCreation::GraphCreationPreRender**</span><span class="sxs-lookup"><span data-stu-id="0ec33-157">**IWMPGraphCreation::GraphCreationPreRender**</span></span>](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpgraphcreation-graphcreationprerender)
-   [<span data-ttu-id="0ec33-158">**IWMPGraphCreation::GraphCreationPostRender**</span><span class="sxs-lookup"><span data-stu-id="0ec33-158">**IWMPGraphCreation::GraphCreationPostRender**</span></span>](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpgraphcreation-graphcreationpostrender)

## <a name="related-topics"></a><span data-ttu-id="0ec33-159">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0ec33-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ec33-160">Informazioni su Windows Media Player SDK</span><span class="sxs-lookup"><span data-stu-id="0ec33-160">About the Windows Media Player SDK</span></span>](about-the-windows-media-player-sdk.md)
</dt> </dl>

 

 




