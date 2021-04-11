---
title: Funzionalità aggiunte in Windows Media 9,5 SDK
description: Funzionalità aggiunte in Windows Media 9,5 SDK
ms.assetid: 1525132c-8aa1-42bb-9552-41531fb83055
keywords:
- Windows Media Format SDK, funzionalità
- Windows Media Format SDK, nuove funzionalità
- Windows Media Format SDK, interfaccia per l'elaborazione specifica dell'applicazione
- Windows Media Format SDK, accelerazione video DirectX (DXVA)
- Windows Media Format SDK, interfaccia IWMPlayerHook
- IWMPlayerHook
- Windows Media Format SDK, versioni basate su x64 di Windows
- Windows Media Format SDK, Windows Media Video image codec
- Windows Media Format SDK, codec audio
- Windows Media Format SDK, DRM 10 per i dispositivi di rete
- Windows Media Format SDK, licenze DRM
- Windows Media Format SDK, Advanced Profile codec
- Windows Media Format SDK, formato di interconnessione digitale Sony/Philips (S/PDIF)
- Windows Media Format SDK, formati a basso ritardo
- Windows Media Format SDK, modalità di ricerca approssimativa
- Windows Media Format SDK, Burning delle playlist
- Windows Media Format SDK, supporto per più lingue
- Windows Media Format SDK, Windows Media Gestione dispositivi SDK
- Windows Media Format SDK, interfacce codec
- codec, immagine Windows Media Video
- Digital Rights Management (DRM), dispositivi di rete Secure Transfer Protocol
- DRM (Digital Rights Management), dispositivi di rete Secure Transfer Protocol
- Digital Rights Management (DRM), licenze
- DRM (Digital Rights Management), licenze
- codec, Advanced Profile codec
- Formato di interconnessione digitale Sony/Philips (S/PDIF), trasferimento o trasmissione tramite
- S/PDIF (formato di interconnessione digitale Sony/Philips), trasferimento o trasmissione tramite
- modalità di ricerca approssimativa
- metadati, supporto per più linguaggi
- Windows Media Gestione dispositivi SDK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e58c9816ef80325422ee365b952842727b5004e
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/20/2020
ms.locfileid: "104117411"
---
# <a name="features-added-in-the-windows-media-95-sdk"></a><span data-ttu-id="4f08e-133">Funzionalità aggiunte in Windows Media 9,5 SDK</span><span class="sxs-lookup"><span data-stu-id="4f08e-133">Features Added in the Windows Media 9.5 SDK</span></span>

<span data-ttu-id="4f08e-134">Windows Media Format 9,5 SDK ha introdotto nuove funzionalità per offrire maggiore flessibilità e sicurezza del contenuto.</span><span class="sxs-lookup"><span data-stu-id="4f08e-134">The Windows Media Format 9.5 SDK introduced new features to provide enhanced content security and flexibility.</span></span> <span data-ttu-id="4f08e-135">Le modifiche seguenti sono state apportate all'SDK dalla versione 9 della serie.</span><span class="sxs-lookup"><span data-stu-id="4f08e-135">The following changes were made to the SDK since the 9 Series release.</span></span>

## <a name="new-interface-for-application-specific-processing-during-directx-video-acceleration"></a><span data-ttu-id="4f08e-136">Nuova interfaccia per l'elaborazione specifica dell'applicazione durante l'accelerazione video DirectX</span><span class="sxs-lookup"><span data-stu-id="4f08e-136">New Interface for Application-specific Processing During DirectX Video Acceleration</span></span>

<span data-ttu-id="4f08e-137">Le applicazioni lettore che supportano l'accelerazione video DirectX ora possono implementare l'interfaccia [**IWMPlayerHook**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmplayerhook) per eseguire l'elaborazione specifica dell'applicazione durante la decodifica di DirectX va.</span><span class="sxs-lookup"><span data-stu-id="4f08e-137">Player applications that support DirectX Video Acceleration can now implement the [**IWMPlayerHook**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmplayerhook) interface to perform application-specific processing during DirectX VA decoding.</span></span> <span data-ttu-id="4f08e-138">Il lettore chiama il metodo di callback [**IWMPLayerHook::P redecode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmplayerhook-predecode) prima di passare gli esempi video compressi al processore video per la decodifica.</span><span class="sxs-lookup"><span data-stu-id="4f08e-138">The reader calls the [**IWMPLayerHook::PreDecode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmplayerhook-predecode) callback method before passing compressed video samples to the video processor for decoding.</span></span>

> [!Note]  
> <span data-ttu-id="4f08e-139">Per usare l'interfaccia **IWMPlayerHook** e l'interfaccia [**IWMReaderAdvanced5**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced5) associata, è necessario aver installato l'aggiornamento numero 888656 in Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="4f08e-139">To use the **IWMPlayerHook** interface and the associated [**IWMReaderAdvanced5**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced5) interface, you must have update number 888656 installed in the Windows Media Format SDK.</span></span> <span data-ttu-id="4f08e-140">È possibile scaricare l'aggiornamento dal [sito Web Microsoft](https://support.microsoft.com/?id=888656).</span><span class="sxs-lookup"><span data-stu-id="4f08e-140">You can download the update from the [Microsoft Web site](https://support.microsoft.com/?id=888656).</span></span>

 

## <a name="windows-media-format-sdk-version-for-x64-based-versions-of-windows"></a><span data-ttu-id="4f08e-141">Windows Media Format SDK versione per versioni basate su x64 di Windows</span><span class="sxs-lookup"><span data-stu-id="4f08e-141">Windows Media Format SDK version for x64-based versions of Windows</span></span>

<span data-ttu-id="4f08e-142">È disponibile una versione basata su x64 di Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="4f08e-142">An x64-based version of the Windows Media Format SDK is available.</span></span> <span data-ttu-id="4f08e-143">Questa documentazione si applica sia alle versioni a 32 bit che alla versione basata su x64 dell'SDK.</span><span class="sxs-lookup"><span data-stu-id="4f08e-143">This documentation applies to both the 32-bit versions and the x64-based version of the SDK.</span></span> <span data-ttu-id="4f08e-144">Tuttavia, Digital Rights Management (DRM) non è supportato in Windows Media Format SDK basato su x64.</span><span class="sxs-lookup"><span data-stu-id="4f08e-144">However, digital rights management (DRM) is not supported in the x64-based Windows Media Format SDK.</span></span>

## <a name="new-version-of-the-windows-media-video-image-codec"></a><span data-ttu-id="4f08e-145">Nuova versione del codec di immagine Windows Media Video</span><span class="sxs-lookup"><span data-stu-id="4f08e-145">New Version of the Windows Media Video Image Codec</span></span>

<span data-ttu-id="4f08e-146">Il codec Windows Media Video 9 image V2 semplifica i calcoli Geometry di esempio per la panoramica e lo zoom.</span><span class="sxs-lookup"><span data-stu-id="4f08e-146">The Windows Media Video 9 Image v2 codec simplifies the sample geometry calculations for panning and zooming.</span></span> <span data-ttu-id="4f08e-147">Il nuovo codec supporta inoltre diverse transizioni complesse tra le immagini.</span><span class="sxs-lookup"><span data-stu-id="4f08e-147">The new codec also supports several complex transitions between images.</span></span>

## <a name="new-version-of-the-windows-media-audio-codecs"></a><span data-ttu-id="4f08e-148">Nuova versione dei codec Windows Media Audio</span><span class="sxs-lookup"><span data-stu-id="4f08e-148">New Version of the Windows Media Audio Codecs</span></span>

<span data-ttu-id="4f08e-149">Windows Media Format 9,5 SDK include i codec audio aggiornati seguenti:</span><span class="sxs-lookup"><span data-stu-id="4f08e-149">The Windows Media Format 9.5 SDK includes the following updated audio codecs:</span></span>

-   <span data-ttu-id="4f08e-150">Windows Media Audio 9,1</span><span class="sxs-lookup"><span data-stu-id="4f08e-150">Windows Media Audio 9.1</span></span>
-   <span data-ttu-id="4f08e-151">Windows Media Audio 9,1 Professional</span><span class="sxs-lookup"><span data-stu-id="4f08e-151">Windows Media Audio 9.1 Professional</span></span>
-   <span data-ttu-id="4f08e-152">Windows Media Audio 9,1 senza perdita di perdite</span><span class="sxs-lookup"><span data-stu-id="4f08e-152">Windows Media Audio 9.1 Lossless</span></span>

## <a name="windows-media-drm-10-for-network-devices-protocol-support"></a><span data-ttu-id="4f08e-153">Supporto del protocollo Windows Media DRM 10 per dispositivi di rete</span><span class="sxs-lookup"><span data-stu-id="4f08e-153">Windows Media DRM 10 for Network Devices Protocol Support</span></span>

<span data-ttu-id="4f08e-154">Windows Media Format 9,5 SDK supporta il nuovo protocollo Windows Media DRM 10 per i dispositivi di rete Secure Transfer Protocol.</span><span class="sxs-lookup"><span data-stu-id="4f08e-154">The Windows Media Format 9.5 SDK supports the new Windows Media DRM 10 for Network Devices secure transfer protocol.</span></span> <span data-ttu-id="4f08e-155">Questo protocollo può essere usato per trasmettere il contenuto crittografato in una rete locale a un dispositivo di riproduzione, ad esempio un ricevitore video di set-top.</span><span class="sxs-lookup"><span data-stu-id="4f08e-155">This protocol can be used to stream encrypted content over a local network to a playback device, such as a set-top video receiver.</span></span>

<span data-ttu-id="4f08e-156">La maggior parte delle procedure utilizzate per implementare il supporto per Windows Media DRM 10 per i dispositivi di rete deve essere eseguita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4f08e-156">Most of the procedures used to implement support for Windows Media DRM 10 for Network Devices must be performed by the application.</span></span> <span data-ttu-id="4f08e-157">Tuttavia, è possibile usare i metodi di Windows Media Format SDK per fornire le funzionalità seguenti:</span><span class="sxs-lookup"><span data-stu-id="4f08e-157">However, you can use methods of the Windows Media Format SDK to provide the following functionality:</span></span>

-   <span data-ttu-id="4f08e-158">Gestire un database di dispositivi, inclusi quelli abilitati per Windows Media DRM 10 per i dispositivi di rete.</span><span class="sxs-lookup"><span data-stu-id="4f08e-158">Maintain a database of devices, including those that are enabled for Windows Media DRM 10 for Network Devices.</span></span>
-   <span data-ttu-id="4f08e-159">Convalidare i dispositivi per assicurarsi che siano sufficientemente vicini al client in rete per lo streaming protetto.</span><span class="sxs-lookup"><span data-stu-id="4f08e-159">Validate devices to ensure that they are "near" enough to the client on the network for secure streaming.</span></span>
-   <span data-ttu-id="4f08e-160">Convertire i file protetti da DRM in Windows Media DRM 10 per i flussi di dispositivi di rete.</span><span class="sxs-lookup"><span data-stu-id="4f08e-160">Convert DRM-protected files to Windows Media DRM 10 for Network Devices streams.</span></span>
-   <span data-ttu-id="4f08e-161">Scrivere file usando dati precedentemente crittografati.</span><span class="sxs-lookup"><span data-stu-id="4f08e-161">Write files using previously encrypted data.</span></span>

## <a name="support-for-new-drm-licenses"></a><span data-ttu-id="4f08e-162">Supporto per le nuove licenze DRM</span><span class="sxs-lookup"><span data-stu-id="4f08e-162">Support for New DRM Licenses</span></span>

<span data-ttu-id="4f08e-163">Le nuove licenze create mediante Windows Media Rights Manager SDK utilizzano i livelli di protezione dell'output (OPLs) per specificare i diritti e le restrizioni per la riproduzione e la copia del contenuto.</span><span class="sxs-lookup"><span data-stu-id="4f08e-163">New licenses created by using the Windows Media Rights Manager SDK use Output Protection Levels (OPLs) to specify rights and restrictions for playing and copying content.</span></span> <span data-ttu-id="4f08e-164">Windows Media Format SDK fornisce il supporto per la lettura di OPLs da una licenza.</span><span class="sxs-lookup"><span data-stu-id="4f08e-164">The Windows Media Format SDK provides support for reading the OPLs from a license.</span></span>

## <a name="new-video-codec"></a><span data-ttu-id="4f08e-165">Nuovo codec video</span><span class="sxs-lookup"><span data-stu-id="4f08e-165">New Video Codec</span></span>

<span data-ttu-id="4f08e-166">Il Windows Media Video 9 Advanced Profile codec si basa sull'elevata qualità del codec Windows Media Video 9, mentre aggiunge il supporto per la codifica interlacciata.</span><span class="sxs-lookup"><span data-stu-id="4f08e-166">The Windows Media Video 9 Advanced Profile codec builds on the high quality of the Windows Media Video 9 codec while adding support for interlaced encoding.</span></span>

## <a name="spdif-output"></a><span data-ttu-id="4f08e-167">Output S/PDIF</span><span class="sxs-lookup"><span data-stu-id="4f08e-167">S/PDIF Output</span></span>

<span data-ttu-id="4f08e-168">Il contenuto codificato con uno dei codec professionali Windows Media Audio ora può essere trasferito o trasmesso usando il formato di interconnessione digitale (S/PDIF) di Sony/Philips.</span><span class="sxs-lookup"><span data-stu-id="4f08e-168">Content encoded with one of the Windows Media Audio Professional codecs can now be transferred or transmitted using the Sony/Philips Digital Interconnect Format (S/PDIF).</span></span>

## <a name="low-delay-audio"></a><span data-ttu-id="4f08e-169">Audio Low-Delay</span><span class="sxs-lookup"><span data-stu-id="4f08e-169">Low-Delay Audio</span></span>

<span data-ttu-id="4f08e-170">I codec Windows Media Audio 9,1 e Windows Media Audio 9,1 Professional supportano ora diversi formati a basso ritardo.</span><span class="sxs-lookup"><span data-stu-id="4f08e-170">The Windows Media Audio 9.1 and Windows Media Audio 9.1 Professional codecs now each support several low-delay formats.</span></span> <span data-ttu-id="4f08e-171">Questi formati producono flussi audio che possono essere avviati più rapidamente, riducendo la latenza negli scenari di cambio di flusso.</span><span class="sxs-lookup"><span data-stu-id="4f08e-171">These formats produce audio streams that can be started more quickly, reducing latency in stream-switching scenarios.</span></span> <span data-ttu-id="4f08e-172">La latenza complessiva nelle trasmissioni live viene anche migliorata usando formati a ritardo ridotto.</span><span class="sxs-lookup"><span data-stu-id="4f08e-172">Overall latency in live broadcasts is also improved by using low-delay formats.</span></span>

## <a name="approximate-seeking-mode"></a><span data-ttu-id="4f08e-173">Modalità di ricerca approssimativa</span><span class="sxs-lookup"><span data-stu-id="4f08e-173">Approximate Seeking Mode</span></span>

<span data-ttu-id="4f08e-174">È ora possibile cercare un'ora approssimativa in un file ASF con il lettore.</span><span class="sxs-lookup"><span data-stu-id="4f08e-174">You can now seek to an approximate time in an ASF file with the reader.</span></span> <span data-ttu-id="4f08e-175">Questa modalità migliora le prestazioni quando si esegue una ricerca imprecisa, ad esempio quando un utente fa clic sulla barra di ricerca in Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="4f08e-175">This mode improves performance when performing an imprecise seek, such as when a user clicks the seek bar in Windows Media Player.</span></span> <span data-ttu-id="4f08e-176">La ricerca approssimativa restituisce l'esempio di supporto per il cleanpoint precedente invece di ricostruire l'esempio per il tempo esatto ricercato.</span><span class="sxs-lookup"><span data-stu-id="4f08e-176">Approximate seeking returns the media sample for the previous cleanpoint instead of reconstructing the sample for the precise time sought.</span></span>

## <a name="playlist-burning"></a><span data-ttu-id="4f08e-177">Masterizzazione playlist</span><span class="sxs-lookup"><span data-stu-id="4f08e-177">Playlist Burning</span></span>

<span data-ttu-id="4f08e-178">Windows Media DRM 10 supporta i diritti per la copia dei file audio nel CD di Red Book come parte di una playlist.</span><span class="sxs-lookup"><span data-stu-id="4f08e-178">Windows Media DRM 10 supports rights for copying audio files to Red Book CD as part of a playlist.</span></span> <span data-ttu-id="4f08e-179">Windows Media Format SDK fornisce i metodi per verificare se i file in una playlist possono essere copiati.</span><span class="sxs-lookup"><span data-stu-id="4f08e-179">The Windows Media Format SDK provides methods for verifying whether the files in a playlist are allowed to be copied.</span></span>

## <a name="improved-multiple-language-support-for-metadata"></a><span data-ttu-id="4f08e-180">Supporto Multiple-Language migliorato per i metadati</span><span class="sxs-lookup"><span data-stu-id="4f08e-180">Improved Multiple-Language Support for Metadata</span></span>

<span data-ttu-id="4f08e-181">In Windows Media Format 9 Series SDK tutti i metadati aggiunti a un file sono stati assegnati a un elenco di lingue a cui è stato assegnato l'identificatore della lingua predefinita.</span><span class="sxs-lookup"><span data-stu-id="4f08e-181">In the Windows Media Format 9 Series SDK, all metadata added to a file was assigned to a language list that was given the language identifier of the default language.</span></span> <span data-ttu-id="4f08e-182">Ciò ha causato problemi quando i distributori di contenuti in impostazioni locali diverse hanno aggiunto alcuni metadati, perché gli utenti nelle impostazioni locali del server di distribuzione visualizzano solo i pochi attributi aggiunti per la lingua.</span><span class="sxs-lookup"><span data-stu-id="4f08e-182">This caused problems when content distributors in different locales added some metadata, because users in the distributor's locale only see the few attributes added for their language.</span></span> <span data-ttu-id="4f08e-183">Il Windows Media Format 9,5 SDK risolve questo problema non creando un elenco di lingue fino a quando non sono presenti attributi di due lingue presenti nel file.</span><span class="sxs-lookup"><span data-stu-id="4f08e-183">The Windows Media Format 9.5 SDK solves this problem by not creating a language list until there are attributes from two languages present in the file.</span></span> <span data-ttu-id="4f08e-184">A questo punto, tutti i metadati sono associati alle impostazioni locali della seconda lingua, che diventa quindi il valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="4f08e-184">At that point, all of the metadata is associated with the locale of the second language, which then becomes the default.</span></span> <span data-ttu-id="4f08e-185">In questo modo, un server di distribuzione del contenuto può mantenere tutti i metadati originali per un file, ad esempio titolo e autore, intatti durante l'aggiunta di alcuni attributi pertinenti alle rispettive impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="4f08e-185">In this way, a content distributor can keep all of the original metadata for a file, such as title and author, intact while adding some attributes pertinent to their locale.</span></span>

## <a name="windows-media-device-manager-sdk-included-in-installation"></a><span data-ttu-id="4f08e-186">Windows Media Gestione dispositivi SDK incluso nell'installazione</span><span class="sxs-lookup"><span data-stu-id="4f08e-186">Windows Media Device Manager SDK Included in Installation</span></span>

<span data-ttu-id="4f08e-187">Il pacchetto di installazione per Windows Media Format 9,5 SDK installa Windows Media Gestione dispositivi SDK.</span><span class="sxs-lookup"><span data-stu-id="4f08e-187">The installation package for the Windows Media Format 9.5 SDK installs the Windows Media Device Manager SDK.</span></span> <span data-ttu-id="4f08e-188">La documentazione relativa a Windows Media Gestione dispositivi SDK si trova nella cartella C: \\ WMSDK \\ WMFSDK95 \\ WMDM \\ docs (la cartella sarà diversa se non si installa Windows Media Format SDK nella cartella predefinita).</span><span class="sxs-lookup"><span data-stu-id="4f08e-188">The documentation for the Windows Media Device Manager SDK can be found in the C:\\WMSDK\\WMFSDK95\\WMDM\\docs folder (your folder will be different if you do not install the Windows Media Format SDK in the default folder.)</span></span>

## <a name="codec-interface-documentation"></a><span data-ttu-id="4f08e-189">Documentazione dell'interfaccia codec</span><span class="sxs-lookup"><span data-stu-id="4f08e-189">Codec Interface Documentation</span></span>

<span data-ttu-id="4f08e-190">Questa documentazione include informazioni sull'uso dei codec Windows Media Audio e video al di fuori di Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="4f08e-190">This documentation includes information about using the Windows Media Audio and Video codecs outside of the Windows Media Format SDK.</span></span> <span data-ttu-id="4f08e-191">Questa documentazione è stata originariamente rilasciata come parte di un download da Microsoft Developer Network.</span><span class="sxs-lookup"><span data-stu-id="4f08e-191">This documentation was originally released as part of a download from the Microsoft Developer Network.</span></span> <span data-ttu-id="4f08e-192">Le applicazioni di esempio che illustrano l'uso diretto del codec DMOs sono incluse nell'installazione di Windows Media Format SDK con le intestazioni.</span><span class="sxs-lookup"><span data-stu-id="4f08e-192">The sample applications that demonstrate using the codec DMOs directly are included in the Windows Media Format SDK installation along with headers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4f08e-193">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="4f08e-193">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4f08e-194">**Informazioni su Windows Media Format SDK**</span><span class="sxs-lookup"><span data-stu-id="4f08e-194">**About the Windows Media Format SDK**</span></span>](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




