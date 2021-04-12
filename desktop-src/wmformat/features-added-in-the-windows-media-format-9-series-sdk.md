---
title: Funzionalità aggiunte in Windows Media Format 9 Series SDK
description: Funzionalità aggiunte in Windows Media Format 9 Series SDK
ms.assetid: 73c4da27-a456-4845-a35b-edb75aa3f953
keywords:
- Windows Media Format SDK, funzionalità
- Windows Media Format SDK, nuove funzionalità
- Windows Media Format SDK, lettori sincroni
- Windows Media Format SDK, indicizzazione basata su frame
- Windows Media Format SDK, codici temporali SMPTE
- Windows Media Format SDK, filtri DirectShow
- Windows Media Format SDK, funzionalità di scrittura DRM
- Windows Media Format SDK, sink di file
- Windows Media Format SDK, accelerazione video DirectX (DXVA)
- Windows Media Format SDK, audio multicanale
- Windows Media Format SDK, filigrana
- Windows Media Format SDK, supporto per più lingue
- Windows Media Format SDK, modelli di conformità del dispositivo
- Windows Media Format SDK, enumerazioni codec
- Windows Media Format SDK, esclusione reciproca
- Windows Media Format SDK, frequenza a più bit (MBR)
- Windows Media Format SDK, transcodifica con la ricompressione intelligente
- Windows Media Format SDK, ricompressione intelligente
- Windows Media Format SDK, ricompressione
- Windows Media Format SDK, metadati
- Windows Media Format SDK, proporzioni pixel dinamiche
- Windows Media Format SDK, flussi video interlacciati
- Windows Media Format SDK, codifica a due passaggi
- Windows Media Format SDK, WMStub. lib
- lettori sincroni, informazioni
- indicizzazione basata su frame
- Codici temporali SMPTE, informazioni
- Filtri DirectShow
- sink di file, miglioramenti
- audio multicanale, informazioni
- watermarking, informazioni
- codec, enumerazioni
- esclusione reciproca, informazioni
- Digital Rights Management (DRM), funzionalità di scrittura
- DRM (Digital Rights Management), funzionalità di scrittura
- Accelerazione video DirectX (DXVA), informazioni
- DXVA (accelerazione video DirectX), informazioni
- Advanced Systems Format (ASF), supporto per più lingue
- ASF (Advanced Systems Format), supporto per più lingue
- velocità in bit multipla (MBR), informazioni
- MBR (velocità in bit multipla), informazioni
- transcodifica con ricompressione intelligente
- ricompressione intelligente
- ricompressione
- metadati, Windows Media Format SDK
- proporzioni dinamiche in pixel
- flussi video interlacciati
- codifica a due passaggi, informazioni
- codifica a 2 passaggi, informazioni
- WMStub. lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adca7e39c89220c2c8c4cac6af354eefb77257aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221491"
---
# <a name="features-added-in-the-windows-media-format-9-series-sdk"></a><span data-ttu-id="d0e24-153">Funzionalità aggiunte in Windows Media Format 9 Series SDK</span><span class="sxs-lookup"><span data-stu-id="d0e24-153">Features Added in the Windows Media Format 9 Series SDK</span></span>

<span data-ttu-id="d0e24-154">In Windows Media Format 9 Series SDK sono stati introdotti numerosi miglioramenti e funzionalità.</span><span class="sxs-lookup"><span data-stu-id="d0e24-154">The Windows Media Format 9 Series SDK introduced many improvements and features.</span></span> <span data-ttu-id="d0e24-155">In questa sezione viene fornita una panoramica di queste funzionalità per i vantaggi offerti dagli utenti che eseguono la migrazione da una versione precedente dell'SDK.</span><span class="sxs-lookup"><span data-stu-id="d0e24-155">This section provides an overview of those features for the benefit of users migrating from an earlier version of the SDK.</span></span>

## <a name="synchronous-reading"></a><span data-ttu-id="d0e24-156">Lettura sincrona</span><span class="sxs-lookup"><span data-stu-id="d0e24-156">Synchronous Reading</span></span>

<span data-ttu-id="d0e24-157">È possibile leggere i file ASF con chiamate sincrone.</span><span class="sxs-lookup"><span data-stu-id="d0e24-157">You can read ASF files with synchronous calls.</span></span> <span data-ttu-id="d0e24-158">Quando si legge un file in modo sincrono, è possibile modificare le impostazioni del lettore durante la lettura.</span><span class="sxs-lookup"><span data-stu-id="d0e24-158">When reading a file synchronously, you can change the settings of the reader while it is reading.</span></span> <span data-ttu-id="d0e24-159">Le operazioni di lettura sincrona dell'SDK non forniscono supporto per la lettura di file su Internet, ma è possibile usare l'interfaccia COM standard, **IStream**, per leggere da origini personalizzate.</span><span class="sxs-lookup"><span data-stu-id="d0e24-159">The synchronous reading operations of the SDK do not provide support for reading files over the Internet, but you can use the standard COM interface, **IStream**, to read from custom sources.</span></span>

## <a name="frame-based-indexing"></a><span data-ttu-id="d0e24-160">Indicizzazione basata su frame</span><span class="sxs-lookup"><span data-stu-id="d0e24-160">Frame-based Indexing</span></span>

<span data-ttu-id="d0e24-161">È possibile indicizzare i file ASF in base ai fotogrammi video.</span><span class="sxs-lookup"><span data-stu-id="d0e24-161">You can index ASF files based on video frames.</span></span> <span data-ttu-id="d0e24-162">Sia il Reader che il lettore sincrono possono cercare un frame di un flusso video e sincronizzare gli altri flussi a tale frame.</span><span class="sxs-lookup"><span data-stu-id="d0e24-162">Both the reader and the synchronous reader can seek to a frame of a video stream and synchronize the other streams to that frame.</span></span>

## <a name="indexing-and-seeking-with-smpte-time-code"></a><span data-ttu-id="d0e24-163">Indicizzazione e ricerca con codice ora SMPTE</span><span class="sxs-lookup"><span data-stu-id="d0e24-163">Indexing and Seeking with SMPTE Time Code</span></span>

<span data-ttu-id="d0e24-164">Windows Media Format SDK consente di archiviare i codici temporali SMPTE nei file ASF.</span><span class="sxs-lookup"><span data-stu-id="d0e24-164">The Windows Media Format SDK enables you to store SMPTE time codes in ASF files.</span></span> <span data-ttu-id="d0e24-165">I file possono essere indicizzati in base al codice ora SMPTE e il lettore asincrono e il lettore sincrono possono cercare le voci di indice del codice ora SMPTE.</span><span class="sxs-lookup"><span data-stu-id="d0e24-165">Files can be indexed by SMPTE time code, and both the asynchronous reader and synchronous reader can seek to SMPTE time code index entries.</span></span>

## <a name="directshow-filters"></a><span data-ttu-id="d0e24-166">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="d0e24-166">DirectShow Filters</span></span>

<span data-ttu-id="d0e24-167">Windows Media Format SDK include due filtri Microsoft DirectShow® che consentono alle applicazioni basate su DirectShow di leggere e scrivere file ASF.</span><span class="sxs-lookup"><span data-stu-id="d0e24-167">The Windows Media Format SDK includes two Microsoft DirectShow® filters that enable DirectShow-based applications to read and write ASF files.</span></span> <span data-ttu-id="d0e24-168">DirectShow consente inoltre alle applicazioni di acquisire dati da dispositivi audio-video e decomprimere i dati da una varietà di formati prima di ricodificarli come contenuto basato su Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d0e24-168">DirectShow also enables applications to capture data from audio-video devices and decompress data from a variety of formats before re-encoding it as Windows Media-based content.</span></span>

## <a name="enhanced-profiles"></a><span data-ttu-id="d0e24-169">Profili avanzati</span><span class="sxs-lookup"><span data-stu-id="d0e24-169">Enhanced Profiles</span></span>

<span data-ttu-id="d0e24-170">I profili possono contenere informazioni di condivisione della larghezza di banda e informazioni relative alla priorità dei flussi.</span><span class="sxs-lookup"><span data-stu-id="d0e24-170">Profiles can contain bandwidth sharing information and stream prioritization information.</span></span> <span data-ttu-id="d0e24-171">La condivisione della larghezza di banda consente di specificare che due o più flussi, indipendentemente dalle singole frequenze di bit, non utilizzeranno mai più di una quantità di larghezza di banda specificata.</span><span class="sxs-lookup"><span data-stu-id="d0e24-171">Bandwidth sharing enables you to specify that two or more streams, regardless of their individual bit rates, will never use more than a specified amount of bandwidth.</span></span> <span data-ttu-id="d0e24-172">I dati di condivisione della larghezza di banda in un profilo sono puramente informativi; non viene applicato da alcuna logica nell'SDK.</span><span class="sxs-lookup"><span data-stu-id="d0e24-172">The bandwidth sharing data in a profile is purely informational; it is not enforced by any logic in the SDK.</span></span> <span data-ttu-id="d0e24-173">La definizione delle priorità del flusso consente di specificare un ordine di priorità per i flussi in un profilo.</span><span class="sxs-lookup"><span data-stu-id="d0e24-173">Stream prioritization enables you to specify an order of priority for the streams in a profile.</span></span> <span data-ttu-id="d0e24-174">Se la larghezza di banda della riproduzione non è sufficiente per trasmettere correttamente il file, è possibile ignorare i flussi con priorità più bassa per migliorare le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="d0e24-174">If there is not enough bandwidth at playback to stream the file properly, the lowest priority streams can be ignored in order to improve performance.</span></span>

## <a name="drm-writing-capability"></a><span data-ttu-id="d0e24-175">Funzionalità di scrittura DRM</span><span class="sxs-lookup"><span data-stu-id="d0e24-175">DRM Writing Capability</span></span>

<span data-ttu-id="d0e24-176">Oltre al supporto di lettura DRM esistente, Windows Media Format 9 Series SDK ha aggiunto il supporto per la scrittura di file ASF con la protezione DRM versione 1 o DRM versione 7.</span><span class="sxs-lookup"><span data-stu-id="d0e24-176">In addition to the existing DRM-reading support, the Windows Media Format 9 Series SDK added support for writing ASF files with either DRM version 1 or DRM version 7 protection.</span></span> <span data-ttu-id="d0e24-177">Questa nuova funzionalità consente di eseguire scenari "DRM Live", come il webcast in base alla visualizzazione di eventi sportivi o concerti live.</span><span class="sxs-lookup"><span data-stu-id="d0e24-177">This new capability enables "Live DRM" scenarios such as pay-per-view webcasting of live sporting events or concerts.</span></span>

## <a name="enhanced-file-sink"></a><span data-ttu-id="d0e24-178">Sink di file avanzato</span><span class="sxs-lookup"><span data-stu-id="d0e24-178">Enhanced File Sink</span></span>

<span data-ttu-id="d0e24-179">Diverse nuove funzionalità di sink di file sono state aggiunte alla versione 9 della serie dell'SDK.</span><span class="sxs-lookup"><span data-stu-id="d0e24-179">Several new file sink capabilities were added to the 9 Series version of the SDK.</span></span> <span data-ttu-id="d0e24-180">È possibile configurare il sink di file per disabilitare l'indicizzazione automatica dei file ASF appena creati.</span><span class="sxs-lookup"><span data-stu-id="d0e24-180">You can configure the file sink to disable automatic indexing of newly created ASF files.</span></span> <span data-ttu-id="d0e24-181">È anche possibile configurare la configurazione per l'input e l'output non memorizzati nel buffer.</span><span class="sxs-lookup"><span data-stu-id="d0e24-181">You also have the option to configure it for unbuffered input and output.</span></span>

## <a name="directx-video-acceleration"></a><span data-ttu-id="d0e24-182">Accelerazione video DirectX</span><span class="sxs-lookup"><span data-stu-id="d0e24-182">DirectX Video Acceleration</span></span>

<span data-ttu-id="d0e24-183">DirectX Video Acceleration (DXVA) è una tecnologia che consente la riproduzione di video a velocità elevata (qualità DVD o superiore) in computer meno potenti con schede grafiche abilitate per DXVA.</span><span class="sxs-lookup"><span data-stu-id="d0e24-183">DirectX Video Acceleration (DXVA) is a technology that enables playback of high-bit-rate video (DVD quality or better) on less powerful machines with DXVA-enabled graphics cards.</span></span> <span data-ttu-id="d0e24-184">È possibile usare l'oggetto Reader di questo SDK per abilitare l'accelerazione video DirectX, se l'hardware lo supporta, durante la riproduzione di file ASF.</span><span class="sxs-lookup"><span data-stu-id="d0e24-184">You can use the reader object of this SDK to enable DirectX Video Acceleration, if the hardware supports it, when playing ASF files.</span></span>

## <a name="multichannel-audio"></a><span data-ttu-id="d0e24-185">Audio multicanale</span><span class="sxs-lookup"><span data-stu-id="d0e24-185">Multichannel Audio</span></span>

<span data-ttu-id="d0e24-186">È possibile codificare e riprodurre l'audio multicanale.</span><span class="sxs-lookup"><span data-stu-id="d0e24-186">You can encode and play multichannel audio.</span></span> <span data-ttu-id="d0e24-187">Il codec Windows Media Audio 9 Professional supporta formati con 6 canali e 8 canali, oltre a stereo ad alta definizione.</span><span class="sxs-lookup"><span data-stu-id="d0e24-187">The Windows Media Audio 9 Professional codec supports formats with 6 channels and 8 channels as well as high definition stereo.</span></span>

## <a name="watermarking"></a><span data-ttu-id="d0e24-188">Soglie</span><span class="sxs-lookup"><span data-stu-id="d0e24-188">Watermarking</span></span>

<span data-ttu-id="d0e24-189">È possibile codificare i file ASF con filigrane digitali per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="d0e24-189">You can encode ASF files with digital watermarks for security.</span></span> <span data-ttu-id="d0e24-190">Tutti i sistemi di filigrana sono diversi nel loro approccio, ma tutte le identificazioni incorporano nel contenuto codificato.</span><span class="sxs-lookup"><span data-stu-id="d0e24-190">All watermarking systems are different in their approach, but all embed identification into encoded content.</span></span> <span data-ttu-id="d0e24-191">La filigrana viene eseguita utilizzando speciali DMOs (® DirectX di terze parti).</span><span class="sxs-lookup"><span data-stu-id="d0e24-191">Watermarking is performed using special third-party DirectX® media objects (DMOs).</span></span>

## <a name="support-for-multiple-languages-in-asf-files"></a><span data-ttu-id="d0e24-192">Supporto per più lingue nei file ASF</span><span class="sxs-lookup"><span data-stu-id="d0e24-192">Support for Multiple Languages in ASF files</span></span>

<span data-ttu-id="d0e24-193">È possibile supportare più lingue nei file ASF, sia nei flussi che nei metadati.</span><span class="sxs-lookup"><span data-stu-id="d0e24-193">You can support multiple languages in ASF files, both in streams and in metadata.</span></span> <span data-ttu-id="d0e24-194">Ad esempio, è possibile creare un file video con flussi audio in diverse lingue.</span><span class="sxs-lookup"><span data-stu-id="d0e24-194">For example, you can create a video file with audio streams in several languages.</span></span> <span data-ttu-id="d0e24-195">Al momento della riproduzione, l'utente può selezionare la lingua da usare oppure l'applicazione può eseguire query sulle informazioni di sistema nel computer di riproduzione e selezionare una lingua automaticamente.</span><span class="sxs-lookup"><span data-stu-id="d0e24-195">At playback, the user can select which language to use, or your application can query the system information on the playing computer and select a language automatically.</span></span> <span data-ttu-id="d0e24-196">Gli attributi dei metadati possono anche essere immessi più volte, con i valori in lingue diverse.</span><span class="sxs-lookup"><span data-stu-id="d0e24-196">Metadata attributes can also be entered multiple times, with the values in different languages.</span></span>

## <a name="device-conformance-templates"></a><span data-ttu-id="d0e24-197">Modelli di conformità del dispositivo</span><span class="sxs-lookup"><span data-stu-id="d0e24-197">Device Conformance Templates</span></span>

<span data-ttu-id="d0e24-198">Per semplificare il targeting del contenuto a dispositivi client specifici, i codec Windows Media supportano ora i modelli di conformità dei dispositivi.</span><span class="sxs-lookup"><span data-stu-id="d0e24-198">To assist in targeting content to specific client devices, the Windows Media codecs now support device conformance templates.</span></span> <span data-ttu-id="d0e24-199">Ogni modello contiene un intervallo definito di impostazioni e funzionalità di codec da usare per i supporti destinati a una categoria specifica di piattaforme.</span><span class="sxs-lookup"><span data-stu-id="d0e24-199">Each template contains a defined range of settings and codec features that should be used for media intended for a particular category of platforms.</span></span> <span data-ttu-id="d0e24-200">I profili di sistema non sono più supportati con le versioni più recenti dei codec Windows Media.</span><span class="sxs-lookup"><span data-stu-id="d0e24-200">System profiles are no longer supported with the latest versions of the Windows Media codecs.</span></span> <span data-ttu-id="d0e24-201">Tutti i profili devono essere personalizzati in base alle proprie esigenze.</span><span class="sxs-lookup"><span data-stu-id="d0e24-201">All profiles must be customized to suit your needs.</span></span> <span data-ttu-id="d0e24-202">È possibile usare i modelli di conformità del dispositivo per semplificare la progettazione dei profili.</span><span class="sxs-lookup"><span data-stu-id="d0e24-202">You can use device conformance templates to assist you in designing your profiles.</span></span>

## <a name="expanded-codec-enumeration"></a><span data-ttu-id="d0e24-203">Enumerazione codec espansa</span><span class="sxs-lookup"><span data-stu-id="d0e24-203">Expanded Codec Enumeration</span></span>

<span data-ttu-id="d0e24-204">L'oggetto Gestione profili può eseguire una query sui codec Windows Media Audio e video per i formati supportati.</span><span class="sxs-lookup"><span data-stu-id="d0e24-204">The profile manager object can query the Windows Media Audio and Video codecs for supported formats.</span></span> <span data-ttu-id="d0e24-205">È possibile impostare i parametri per i formati recuperati.</span><span class="sxs-lookup"><span data-stu-id="d0e24-205">You can set parameters for the formats retrieved.</span></span> <span data-ttu-id="d0e24-206">È ad esempio possibile recuperare tutti i formati di velocità in bit della variabile basata sulla qualità supportati dal codec Windows Media Audio 9.</span><span class="sxs-lookup"><span data-stu-id="d0e24-206">For example, you can retrieve all the quality-based variable bit rate formats supported by the Windows Media Audio 9 codec.</span></span>

## <a name="improved-mutual-exclusion"></a><span data-ttu-id="d0e24-207">Esclusione reciproca migliorata</span><span class="sxs-lookup"><span data-stu-id="d0e24-207">Improved Mutual Exclusion</span></span>

<span data-ttu-id="d0e24-208">È possibile creare record denominati contenenti più flussi all'interno di un oggetto di esclusione reciproca.</span><span class="sxs-lookup"><span data-stu-id="d0e24-208">You can create named records containing multiple streams within a mutual exclusion object.</span></span> <span data-ttu-id="d0e24-209">È anche possibile denominare oggetti di esclusione reciproca per facilitarne l'identificazione.</span><span class="sxs-lookup"><span data-stu-id="d0e24-209">You can also name mutual exclusion objects to make them easier to identify.</span></span> <span data-ttu-id="d0e24-210">In questo modo è possibile creare livelli di esclusione reciproca.</span><span class="sxs-lookup"><span data-stu-id="d0e24-210">This enables you to create layers of mutual exclusion.</span></span> <span data-ttu-id="d0e24-211">Un file, ad esempio, può contenere flussi che si escludono a vicenda in base alla velocità in bit e alla lingua.</span><span class="sxs-lookup"><span data-stu-id="d0e24-211">For example, a file can contain streams that are mutually exclusive by bit rate and by language.</span></span> <span data-ttu-id="d0e24-212">L'esclusione reciproca basata sul linguaggio implica gruppi di flussi, ognuno dei quali è costituito da flussi nella stessa lingua, ma che si escludono a vicenda in base alla velocità in bit.</span><span class="sxs-lookup"><span data-stu-id="d0e24-212">The language-based mutual exclusion would involve groups of streams, each group consisting of streams in the same language but mutually exclusive by bit rate.</span></span>

## <a name="expanded-multiple-bit-rate-support"></a><span data-ttu-id="d0e24-213">Supporto per più velocità in bit espansa</span><span class="sxs-lookup"><span data-stu-id="d0e24-213">Expanded Multiple Bit Rate Support</span></span>

<span data-ttu-id="d0e24-214">Il supporto per l'esclusione reciproca è incluso per l'audio con velocità in bit multipli (MBR) e per i video con flussi di dimensioni di immagine variabili.</span><span class="sxs-lookup"><span data-stu-id="d0e24-214">Mutual exclusion support is included for multiple bit rate (MBR) audio and for video with streams of varying image sizes.</span></span>

## <a name="attributes-for-streams"></a><span data-ttu-id="d0e24-215">Attributi per i flussi</span><span class="sxs-lookup"><span data-stu-id="d0e24-215">Attributes for Streams</span></span>

<span data-ttu-id="d0e24-216">È possibile assegnare attributi a singoli flussi nei file ASF.</span><span class="sxs-lookup"><span data-stu-id="d0e24-216">You can assign attributes to individual streams in ASF files.</span></span> <span data-ttu-id="d0e24-217">È comunque necessario usare gli attributi a livello di file per i file MP3.</span><span class="sxs-lookup"><span data-stu-id="d0e24-217">You must still use file-level attributes for MP3 files.</span></span> <span data-ttu-id="d0e24-218">Questa funzionalità non aggiunge alcun metodo all'SDK, ma i metodi esistenti accetteranno ora numeri di flusso diversi da zero.</span><span class="sxs-lookup"><span data-stu-id="d0e24-218">This feature does not add any methods to the SDK, but the existing methods will now accept stream numbers other than zero.</span></span>

## <a name="transcoding-with-smart-recompression"></a><span data-ttu-id="d0e24-219">Transcodifica con ricompressione intelligente</span><span class="sxs-lookup"><span data-stu-id="d0e24-219">Transcoding with Smart Recompression</span></span>

<span data-ttu-id="d0e24-220">La ricompressione intelligente consente di transcodificare i file audio di Windows Media da una velocità in bit elevata a una velocità in bit più bassa con una qualità superiore a quella consentita in precedenza.</span><span class="sxs-lookup"><span data-stu-id="d0e24-220">Smart recompression allows you to transcode Windows Media audio files from a high bit rate to a lower bit rate with better quality than previously achievable.</span></span>

## <a name="expanded-metadata-support"></a><span data-ttu-id="d0e24-221">Supporto dei metadati espanso</span><span class="sxs-lookup"><span data-stu-id="d0e24-221">Expanded Metadata Support</span></span>

<span data-ttu-id="d0e24-222">Windows Media Format SDK fornisce le seguenti nuove funzionalità dei metadati:</span><span class="sxs-lookup"><span data-stu-id="d0e24-222">The Windows Media Format SDK provides the following new metadata features:</span></span>

-   <span data-ttu-id="d0e24-223">Tag di metadati basati su indice, abilitando più tag con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="d0e24-223">Index-based metadata tags, enabling multiple tags with the same name.</span></span>
-   <span data-ttu-id="d0e24-224">Possibilità di leggere gli attributi di intestazione DRM senza un file WMStubDRM. lib.</span><span class="sxs-lookup"><span data-stu-id="d0e24-224">Ability to read DRM header attributes without a WMStubDRM.lib file.</span></span>
-   <span data-ttu-id="d0e24-225">Attributi con più di 64 kilobyte di dati associati.</span><span class="sxs-lookup"><span data-stu-id="d0e24-225">Attributes with more than 64 kilobytes of associated data.</span></span>
-   <span data-ttu-id="d0e24-226">Attributi in più lingue.</span><span class="sxs-lookup"><span data-stu-id="d0e24-226">Attributes in multiple languages.</span></span>
-   <span data-ttu-id="d0e24-227">Dozzine di nuovi attributi predefiniti.</span><span class="sxs-lookup"><span data-stu-id="d0e24-227">Dozens of new predefined attributes.</span></span>

## <a name="dynamic-pixel-aspect-ratio"></a><span data-ttu-id="d0e24-228">Proporzioni dinamiche in pixel</span><span class="sxs-lookup"><span data-stu-id="d0e24-228">Dynamic Pixel Aspect Ratio</span></span>

<span data-ttu-id="d0e24-229">I flussi video composti da vari tipi di contenuto possono essere configurati identificando le proporzioni in pixel degli esempi diversi nel flusso.</span><span class="sxs-lookup"><span data-stu-id="d0e24-229">Video streams that are composed of various types of content can be accommodated by identifying the pixel aspect ratio of the disparate samples in the stream.</span></span> <span data-ttu-id="d0e24-230">In questo modo, l'applicazione di riproduzione garantisce una migliore riproduzione di tale contenuto.</span><span class="sxs-lookup"><span data-stu-id="d0e24-230">This enables the playing application to provide better playback of such content.</span></span>

## <a name="interlaced-video-streams"></a><span data-ttu-id="d0e24-231">Flussi video interlacciati</span><span class="sxs-lookup"><span data-stu-id="d0e24-231">Interlaced Video Streams</span></span>

<span data-ttu-id="d0e24-232">Le versioni precedenti di Windows Media Format SDK hanno consentito di codificare il contenuto [*interlacciato*](wmformat-glossary.md) in un flusso video con analisi progressiva.</span><span class="sxs-lookup"><span data-stu-id="d0e24-232">Previous versions of the Windows Media Format SDK have provided the ability to encode [*interlaced*](wmformat-glossary.md) content into a progressive-scan video stream.</span></span> <span data-ttu-id="d0e24-233">A partire da Windows Media Format 9 Series SDK, è possibile codificare video interlacciato mantenendo il formato interlacciato.</span><span class="sxs-lookup"><span data-stu-id="d0e24-233">Starting with the Windows Media Format 9 Series SDK, you can encode interlaced video while preserving its interlaced format.</span></span> <span data-ttu-id="d0e24-234">Questo può comportare una migliore riproduzione, in particolare sui dispositivi interlacciati, ad esempio i set di televisione.</span><span class="sxs-lookup"><span data-stu-id="d0e24-234">This can result in improved playback, particularly on interlaced devices, such as television sets.</span></span>

## <a name="two-pass-encoding"></a><span data-ttu-id="d0e24-235">Codifica Two-Pass</span><span class="sxs-lookup"><span data-stu-id="d0e24-235">Two-Pass Encoding</span></span>

<span data-ttu-id="d0e24-236">I nuovi codec Windows Media abilitano la codifica a due passaggi.</span><span class="sxs-lookup"><span data-stu-id="d0e24-236">The new Windows Media codecs enable two-pass encoding.</span></span> <span data-ttu-id="d0e24-237">Il contenuto codificato in due passaggi può ottenere un output di qualità superiore.</span><span class="sxs-lookup"><span data-stu-id="d0e24-237">Content encoded in two passes can achieve higher quality output.</span></span>

## <a name="new-speech-codec"></a><span data-ttu-id="d0e24-238">Nuovo codec vocale</span><span class="sxs-lookup"><span data-stu-id="d0e24-238">New Speech Codec</span></span>

<span data-ttu-id="d0e24-239">Questo SDK include il nuovo codec Windows Media Audio 9 Voice, ottimizzato per la codifica della voce umana con una velocità in bit bassa.</span><span class="sxs-lookup"><span data-stu-id="d0e24-239">This SDK includes the new Windows Media Audio 9 Voice codec which is optimized for encoding the human voice while using a low bit rate.</span></span> <span data-ttu-id="d0e24-240">Questo codec fornisce anche prestazioni superiori per contenuto audio misto.</span><span class="sxs-lookup"><span data-stu-id="d0e24-240">This codec also provides superior performance for mixed music-voice content.</span></span>

## <a name="accessible-video-frame-duration"></a><span data-ttu-id="d0e24-241">Durata fotogramma video accessibile</span><span class="sxs-lookup"><span data-stu-id="d0e24-241">Accessible Video Frame Duration</span></span>

<span data-ttu-id="d0e24-242">È possibile fare in modo che l'oggetto writer di questo SDK fornisca la durata dei fotogrammi video al lettore.</span><span class="sxs-lookup"><span data-stu-id="d0e24-242">You can have the writer object of this SDK provide the duration of video frames to the reader.</span></span>

## <a name="streaming-html"></a><span data-ttu-id="d0e24-243">Flusso HTML</span><span class="sxs-lookup"><span data-stu-id="d0e24-243">Streaming HTML</span></span>

<span data-ttu-id="d0e24-244">Con la versione precedente di questo SDK, era possibile usare un comando script per segnalare all'applicazione di aprire una pagina Web.</span><span class="sxs-lookup"><span data-stu-id="d0e24-244">With previous version of this SDK, you were able to use a script command to signal your application to open a Web page.</span></span> <span data-ttu-id="d0e24-245">A partire da Windows Media Format 9 Series SDK, è possibile archiviare i componenti di pagine Web nei file ASF, per assicurarsi che non vi siano ritardi nelle presentazioni.</span><span class="sxs-lookup"><span data-stu-id="d0e24-245">Starting with the Windows Media Format 9 Series SDK, you can store the components of Web pages in your ASF files, to ensure that there is no lag in presentations.</span></span>

## <a name="wmstublib-no-longer-required-for-build-environment"></a><span data-ttu-id="d0e24-246">WMStub. lib non è più necessario per l'ambiente di compilazione</span><span class="sxs-lookup"><span data-stu-id="d0e24-246">WMStub.lib no longer required for build environment</span></span>

<span data-ttu-id="d0e24-247">Le impostazioni dell'ambiente di compilazione per Windows Media Format SDK sono state modificate a partire da Windows Media Format 9 Series SDK.</span><span class="sxs-lookup"><span data-stu-id="d0e24-247">The build-environment settings for the Windows Media Format SDK changed starting with the Windows Media Format 9 Series SDK.</span></span> <span data-ttu-id="d0e24-248">Non è più necessario includere WMStub. lib per le applicazioni che usano questo SDK.</span><span class="sxs-lookup"><span data-stu-id="d0e24-248">You no longer need to include WMStub.lib for applications using this SDK.</span></span> <span data-ttu-id="d0e24-249">Tuttavia, le applicazioni abilitate per DRM devono comunque ottenere e firmare un contratto di licenza separato e ottenere una libreria statica univoca da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d0e24-249">However, DRM-enabled applications still must obtain and sign a separate license agreement, and obtain a unique static library from Microsoft.</span></span> <span data-ttu-id="d0e24-250">wmla@microsoft.comPer ulteriori informazioni sulla libreria DRM e sul contratto di licenza, contattare.</span><span class="sxs-lookup"><span data-stu-id="d0e24-250">Contact wmla@microsoft.com for more information about the DRM library and license agreement.</span></span> <span data-ttu-id="d0e24-251">Per altre informazioni sulla creazione di progetti con questo SDK, vedere [file di libreria e impostazioni del compilatore](library-files-and-compiler-settings.md).</span><span class="sxs-lookup"><span data-stu-id="d0e24-251">For more information about building projects with this SDK, see [Library Files and Compiler Settings](library-files-and-compiler-settings.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d0e24-252">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="d0e24-252">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0e24-253">**Informazioni su Windows Media Format SDK**</span><span class="sxs-lookup"><span data-stu-id="d0e24-253">**About the Windows Media Format SDK**</span></span>](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




