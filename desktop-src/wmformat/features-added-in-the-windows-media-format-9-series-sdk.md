---
title: Funzionalità aggiunte in Windows Media Format 9 Series SDK
description: Funzionalità aggiunte in Windows Media Format 9 Series SDK
ms.assetid: 73c4da27-a456-4845-a35b-edb75aa3f953
keywords:
- Windows Media Format SDK, funzionalità
- Windows Media Format SDK, nuove funzionalità
- Windows Media Format SDK, lettori sincroni
- Windows Media Format SDK, indicizzazione basata su frame
- Windows MEDIA Format SDK, codici ora SMPTE
- Windows Media Format SDK, DirectShow filtri
- Windows Media Format SDK, funzionalità di scrittura DRM
- Windows Media Format SDK, sink di file
- Windows Media Format SDK, Accelerazione video DirectX (DXVA)
- Windows MEDIA Format SDK, audio multicanale
- Windows Media Format SDK, watermarking
- Windows Media Format SDK, supporto per più lingue
- Windows MEDIA Format SDK, modelli di conformità dei dispositivi
- Windows MEDIA Format SDK, enumerazioni di codec
- Windows Media Format SDK, esclusione reciproca
- Windows Media Format SDK, velocità in bit multipla (MBR)
- Windows MEDIA Format SDK, transcoding con ricompressione intelligente
- Windows Media Format SDK, ricompressione intelligente
- Windows Media Format SDK, recompression
- Windows MEDIA Format SDK, metadati
- Windows Media Format SDK, proporzioni pixel dinamiche
- Windows MEDIA Format SDK, flussi video interlacciati
- Windows Media Format SDK, codifica a due passi
- Windows Media Format SDK,WMStub.lib
- lettori sincroni,informazioni
- indicizzazione basata su frame
- codici di ora SMPTE, informazioni
- DirectShow filtri
- sink di file, miglioramenti
- audio multicanale, informazioni
- filigrana, informazioni
- codec, enumerazioni
- esclusione reciproca, informazioni
- digital rights management (DRM), funzionalità di scrittura
- DRM (Digital Rights Management),funzionalità di scrittura
- Accelerazione video DirectX (DXVA), informazioni
- DXVA (Accelerazione video DirectX),informazioni
- Advanced Systems Format (ASF), supporto per più lingue
- ASF (Advanced Systems Format), supporto per più lingue
- velocità in bit multipla (MBR), informazioni
- MBR (velocità in bit multipla),about
- transcoding con ricompressione intelligente
- ricompressione intelligente
- Ricompressione
- metadata,Windows Media Format SDK
- proporzioni pixel dinamiche
- flussi video interlacciati
- codifica a due passi, informazioni
- codifica a 2 passi, informazioni
- WMStub.lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76dc0f4a8c0b23ba33409039ae7f1d46ada1b3299790ef82fb98b8714f616117
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119547451"
---
# <a name="features-added-in-the-windows-media-format-9-series-sdk"></a>Funzionalità aggiunte in Windows Media Format 9 Series SDK

L'SDK Windows Media Format 9 Series ha introdotto numerosi miglioramenti e funzionalità. Questa sezione offre una panoramica di queste funzionalità a vantaggio degli utenti che eseggono la migrazione da una versione precedente dell'SDK.

## <a name="synchronous-reading"></a>Lettura sincrona

È possibile leggere i file ASF con chiamate sincrone. Quando si legge un file in modo sincrono, è possibile modificare le impostazioni del lettore durante la lettura. Le operazioni di lettura sincrona dell'SDK non forniscono supporto per la lettura di file su Internet, ma è possibile usare l'interfaccia COM standard, **IStream,** per leggere da origini personalizzate.

## <a name="frame-based-indexing"></a>Indicizzazione basata su frame

È possibile indicizzare i file ASF in base ai fotogrammi video. Sia il lettore che il lettore sincrono possono cercare un frame di un flusso video e sincronizzare gli altri flussi con tale fotogramma.

## <a name="indexing-and-seeking-with-smpte-time-code"></a>Indicizzazione e ricerca con codice temporale SMPTE

L Windows Media Format SDK consente di archiviare i codici ora SMPTE nei file ASF. I file possono essere indicizzati da SMPTE time code e sia il lettore asincrono che il lettore sincrono possono cercare le voci di indice time code SMPTE.

## <a name="directshow-filters"></a>DirectShow Filtri

L Windows Media Format SDK include due filtri microsoft DirectShow® che consentono alle DirectShow basate su DirectShow di leggere e scrivere file ASF. DirectShow consente anche alle applicazioni di acquisire dati da dispositivi audio-video e di decomprimere i dati da un'ampia gamma di formati prima di ri-codificarlo come Windows contenuto basato su contenuti multimediali.

## <a name="enhanced-profiles"></a>Profili migliorati

I profili possono contenere informazioni sulla condivisione della larghezza di banda e informazioni sulla priorità del flusso. La condivisione della larghezza di banda consente di specificare che due o più flussi, indipendentemente dalle singole velocità in bit, non useranno mai una quantità di larghezza di banda superiore a quella specificata. La condivisione della larghezza di banda dei dati in un profilo è puramente informativo; non viene applicato da alcuna logica nell'SDK. La definizione delle priorità dei flussi consente di specificare un ordine di priorità per i flussi in un profilo. Se la larghezza di banda durante la riproduzione non è sufficiente per trasmettere correttamente il file, i flussi con priorità più bassa possono essere ignorati per migliorare le prestazioni.

## <a name="drm-writing-capability"></a>Funzionalità di scrittura DRM

Oltre al supporto per la lettura DRM esistente, Windows Media Format 9 Series SDK ha aggiunto il supporto per la scrittura di file ASF con protezione DRM versione 1 o DRM versione 7. Questa nuova funzionalità abilita scenari "Live DRM", ad esempio il webcast con pagamento in base alla visualizzazione di eventi live o conferenze.

## <a name="enhanced-file-sink"></a>Sink di file avanzato

Alla versione serie 9 dell'SDK sono state aggiunte diverse nuove funzionalità di sink di file. È possibile configurare il sink di file per disabilitare l'indicizzazione automatica dei file ASF appena creati. È anche possibile configurarlo per l'input e l'output senza buffer.

## <a name="directx-video-acceleration"></a>Accelerazione video DirectX

DirectX Video Acceleration (DXVA) è una tecnologia che consente la riproduzione di video ad alta velocità in bit (qualità DVD o superiore) in computer meno potenti con schede grafiche abilitate per DXVA. È possibile usare l'oggetto lettore di questo SDK per abilitare l'accelerazione video DirectX, se supportato dall'hardware, durante la riproduzione di file ASF.

## <a name="multichannel-audio"></a>Audio multicanale

È possibile codificare e riprodurre audio multicanale. Il codec Windows Media Audio 9 Professional supporta formati con 6 canali e 8 canali, nonché stereo ad alta definizione.

## <a name="watermarking"></a>Watermarking

È possibile codificare i file ASF con filigrane digitali per la sicurezza. Tutti i sistemi di filigrane sono diversi nell'approccio, ma tutti incorporano l'identificazione nel contenuto codificato. La filigrana viene eseguita usando oggetti multimediali ® DirectX di terze parti.

## <a name="support-for-multiple-languages-in-asf-files"></a>Supporto per più lingue nei file ASF

È possibile supportare più lingue nei file ASF, sia nei flussi che nei metadati. Ad esempio, è possibile creare un file video con flussi audio in diverse lingue. Durante la riproduzione, l'utente può selezionare la lingua da usare oppure l'applicazione può eseguire query sulle informazioni di sistema nel computer in riproduzione e selezionare automaticamente una lingua. Gli attributi dei metadati possono anche essere immessi più volte, con i valori in lingue diverse.

## <a name="device-conformance-templates"></a>Modelli di conformità dei dispositivi

Per supportare la destinazione del contenuto a dispositivi client specifici, i codec multimediali Windows ora supportano i modelli di conformità dei dispositivi. Ogni modello contiene una gamma definita di impostazioni e funzionalità di codec che devono essere usate per i supporti destinati a una particolare categoria di piattaforme. I profili di sistema non sono più supportati con le versioni più recenti Windows codec multimediali. Tutti i profili devono essere personalizzati in base alle esigenze. È possibile usare i modelli di conformità dei dispositivi per facilitare la progettazione dei profili.

## <a name="expanded-codec-enumeration"></a>Enumerazione codec espansa

L'oggetto profile manager può eseguire una query Windows codec audio e video multimediali per i formati supportati. È possibile impostare parametri per i formati recuperati. Ad esempio, è possibile recuperare tutti i formati di velocità in bit variabili basati sulla qualità supportati dal codec Windows Media Audio 9.

## <a name="improved-mutual-exclusion"></a>Esclusione reciproca migliorata

È possibile creare record denominati contenenti più flussi all'interno di un oggetto di esclusione reciproca. È anche possibile assegnare un nome agli oggetti di esclusione reciproca per facilitarne l'identificazione. In questo modo è possibile creare livelli di esclusione reciproca. Ad esempio, un file può contenere flussi che si escludono a vicenda per velocità in bit e per lingua. L'esclusione reciproca basata sul linguaggio comporterebbe gruppi di flussi, ognuno dei quali costituito da flussi nello stesso linguaggio, ma che si escludono a vicenda in base alla velocità in bit.

## <a name="expanded-multiple-bit-rate-support"></a>Supporto espanso per più velocità in bit

Il supporto dell'esclusione reciproca è incluso per l'audio MBR (Multiple Bit Rate) e per i video con flussi di dimensioni diverse delle immagini.

## <a name="attributes-for-streams"></a>Attributi per Flussi

È possibile assegnare attributi a singoli flussi nei file ASF. È comunque necessario usare gli attributi a livello di file per i file MP3. Questa funzionalità non aggiunge metodi all'SDK, ma i metodi esistenti accetteranno ora numeri di flusso diversi da zero.

## <a name="transcoding-with-smart-recompression"></a>Transcoding con smart recompression

La ricocompressione intelligente consente di transcodificare Windows file audio multimediali da una velocità in bit elevata a una velocità in bit inferiore con una qualità migliore rispetto a quella ottenibile in precedenza.

## <a name="expanded-metadata-support"></a>Supporto dei metadati espansi

L Windows Media Format SDK offre le nuove funzionalità di metadati seguenti:

-   Tag di metadati basati su indice, abilitando più tag con lo stesso nome.
-   Possibilità di leggere gli attributi dell'intestazione DRM senza un file WMStubDRM.lib.
-   Attributi con più di 64 kilobyte di dati associati.
-   Attributi in più lingue.
-   Decine di nuovi attributi predefiniti.

## <a name="dynamic-pixel-aspect-ratio"></a>Proporzioni pixel dinamiche

I flussi video costituiti da vari tipi di contenuto possono essere adattati identificando le proporzioni in pixel degli esempi diversi nel flusso. In questo modo l'applicazione in riproduzione può offrire una migliore riproduzione di tali contenuti.

## <a name="interlaced-video-streams"></a>Video interlacciato Flussi

Le versioni precedenti di Windows Media Format SDK hanno offerto la possibilità di codificare il contenuto [*interlacciato*](wmformat-glossary.md) in un flusso video a scansione progressiva. A partire da Windows Media Format 9 Series SDK, è possibile codificare video interlacciati mantenendone il formato interlacciato. Ciò può comportare una riproduzione migliorata, in particolare nei dispositivi interlacciati, ad esempio i set tv.

## <a name="two-pass-encoding"></a>Two-Pass codifica

Il nuovo Windows codec multimediali abilita la codifica a due passi. Il contenuto codificato in due passaggi può ottenere un output di qualità superiore.

## <a name="new-speech-codec"></a>Nuovo codec di riconoscimento vocale

Questo SDK include il nuovo codec Windows Media Audio 9 Voice, ottimizzato per la codifica della voce umana con una velocità in bit bassa. Questo codec offre anche prestazioni superiori per il contenuto di musica e voce mista.

## <a name="accessible-video-frame-duration"></a>Durata fotogramma video accessibile

È possibile fare in modo che l'oggetto writer di questo SDK fornissi la durata dei fotogrammi video al lettore.

## <a name="streaming-html"></a>Streaming HTML

Con la versione precedente di questo SDK è stato possibile usare un comando script per segnalare all'applicazione di aprire una pagina Web. A partire da Windows Media Format 9 Series SDK, è possibile archiviare i componenti delle pagine Web nei file ASF per assicurarsi che non ci siano ritardo nelle presentazioni.

## <a name="wmstublib-no-longer-required-for-build-environment"></a>WMStub.lib non è più necessario per l'ambiente di compilazione

Le impostazioni dell'ambiente di compilazione per Windows Media Format SDK sono cambiate a partire da Windows Media Format 9 Series SDK. Non è più necessario includere WMStub.lib per le applicazioni che usano questo SDK. Tuttavia, le applicazioni abilitate per DRM devono comunque ottenere e firmare un contratto di licenza separato e ottenere una libreria statica univoca da Microsoft. Per altre informazioni sulla libreria DRM e sul contratto di wmla@microsoft.com licenza, contattare . Per altre informazioni sulla compilazione di progetti con questo SDK, vedere [File di libreria e compilatore Impostazioni](library-files-and-compiler-settings.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni su Windows Media Format SDK**](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




