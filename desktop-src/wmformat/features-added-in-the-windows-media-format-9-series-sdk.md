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
# <a name="features-added-in-the-windows-media-format-9-series-sdk"></a>Funzionalità aggiunte in Windows Media Format 9 Series SDK

In Windows Media Format 9 Series SDK sono stati introdotti numerosi miglioramenti e funzionalità. In questa sezione viene fornita una panoramica di queste funzionalità per i vantaggi offerti dagli utenti che eseguono la migrazione da una versione precedente dell'SDK.

## <a name="synchronous-reading"></a>Lettura sincrona

È possibile leggere i file ASF con chiamate sincrone. Quando si legge un file in modo sincrono, è possibile modificare le impostazioni del lettore durante la lettura. Le operazioni di lettura sincrona dell'SDK non forniscono supporto per la lettura di file su Internet, ma è possibile usare l'interfaccia COM standard, **IStream**, per leggere da origini personalizzate.

## <a name="frame-based-indexing"></a>Indicizzazione basata su frame

È possibile indicizzare i file ASF in base ai fotogrammi video. Sia il Reader che il lettore sincrono possono cercare un frame di un flusso video e sincronizzare gli altri flussi a tale frame.

## <a name="indexing-and-seeking-with-smpte-time-code"></a>Indicizzazione e ricerca con codice ora SMPTE

Windows Media Format SDK consente di archiviare i codici temporali SMPTE nei file ASF. I file possono essere indicizzati in base al codice ora SMPTE e il lettore asincrono e il lettore sincrono possono cercare le voci di indice del codice ora SMPTE.

## <a name="directshow-filters"></a>Filtri DirectShow

Windows Media Format SDK include due filtri Microsoft DirectShow® che consentono alle applicazioni basate su DirectShow di leggere e scrivere file ASF. DirectShow consente inoltre alle applicazioni di acquisire dati da dispositivi audio-video e decomprimere i dati da una varietà di formati prima di ricodificarli come contenuto basato su Windows Media.

## <a name="enhanced-profiles"></a>Profili avanzati

I profili possono contenere informazioni di condivisione della larghezza di banda e informazioni relative alla priorità dei flussi. La condivisione della larghezza di banda consente di specificare che due o più flussi, indipendentemente dalle singole frequenze di bit, non utilizzeranno mai più di una quantità di larghezza di banda specificata. I dati di condivisione della larghezza di banda in un profilo sono puramente informativi; non viene applicato da alcuna logica nell'SDK. La definizione delle priorità del flusso consente di specificare un ordine di priorità per i flussi in un profilo. Se la larghezza di banda della riproduzione non è sufficiente per trasmettere correttamente il file, è possibile ignorare i flussi con priorità più bassa per migliorare le prestazioni.

## <a name="drm-writing-capability"></a>Funzionalità di scrittura DRM

Oltre al supporto di lettura DRM esistente, Windows Media Format 9 Series SDK ha aggiunto il supporto per la scrittura di file ASF con la protezione DRM versione 1 o DRM versione 7. Questa nuova funzionalità consente di eseguire scenari "DRM Live", come il webcast in base alla visualizzazione di eventi sportivi o concerti live.

## <a name="enhanced-file-sink"></a>Sink di file avanzato

Diverse nuove funzionalità di sink di file sono state aggiunte alla versione 9 della serie dell'SDK. È possibile configurare il sink di file per disabilitare l'indicizzazione automatica dei file ASF appena creati. È anche possibile configurare la configurazione per l'input e l'output non memorizzati nel buffer.

## <a name="directx-video-acceleration"></a>Accelerazione video DirectX

DirectX Video Acceleration (DXVA) è una tecnologia che consente la riproduzione di video a velocità elevata (qualità DVD o superiore) in computer meno potenti con schede grafiche abilitate per DXVA. È possibile usare l'oggetto Reader di questo SDK per abilitare l'accelerazione video DirectX, se l'hardware lo supporta, durante la riproduzione di file ASF.

## <a name="multichannel-audio"></a>Audio multicanale

È possibile codificare e riprodurre l'audio multicanale. Il codec Windows Media Audio 9 Professional supporta formati con 6 canali e 8 canali, oltre a stereo ad alta definizione.

## <a name="watermarking"></a>Soglie

È possibile codificare i file ASF con filigrane digitali per la sicurezza. Tutti i sistemi di filigrana sono diversi nel loro approccio, ma tutte le identificazioni incorporano nel contenuto codificato. La filigrana viene eseguita utilizzando speciali DMOs (® DirectX di terze parti).

## <a name="support-for-multiple-languages-in-asf-files"></a>Supporto per più lingue nei file ASF

È possibile supportare più lingue nei file ASF, sia nei flussi che nei metadati. Ad esempio, è possibile creare un file video con flussi audio in diverse lingue. Al momento della riproduzione, l'utente può selezionare la lingua da usare oppure l'applicazione può eseguire query sulle informazioni di sistema nel computer di riproduzione e selezionare una lingua automaticamente. Gli attributi dei metadati possono anche essere immessi più volte, con i valori in lingue diverse.

## <a name="device-conformance-templates"></a>Modelli di conformità del dispositivo

Per semplificare il targeting del contenuto a dispositivi client specifici, i codec Windows Media supportano ora i modelli di conformità dei dispositivi. Ogni modello contiene un intervallo definito di impostazioni e funzionalità di codec da usare per i supporti destinati a una categoria specifica di piattaforme. I profili di sistema non sono più supportati con le versioni più recenti dei codec Windows Media. Tutti i profili devono essere personalizzati in base alle proprie esigenze. È possibile usare i modelli di conformità del dispositivo per semplificare la progettazione dei profili.

## <a name="expanded-codec-enumeration"></a>Enumerazione codec espansa

L'oggetto Gestione profili può eseguire una query sui codec Windows Media Audio e video per i formati supportati. È possibile impostare i parametri per i formati recuperati. È ad esempio possibile recuperare tutti i formati di velocità in bit della variabile basata sulla qualità supportati dal codec Windows Media Audio 9.

## <a name="improved-mutual-exclusion"></a>Esclusione reciproca migliorata

È possibile creare record denominati contenenti più flussi all'interno di un oggetto di esclusione reciproca. È anche possibile denominare oggetti di esclusione reciproca per facilitarne l'identificazione. In questo modo è possibile creare livelli di esclusione reciproca. Un file, ad esempio, può contenere flussi che si escludono a vicenda in base alla velocità in bit e alla lingua. L'esclusione reciproca basata sul linguaggio implica gruppi di flussi, ognuno dei quali è costituito da flussi nella stessa lingua, ma che si escludono a vicenda in base alla velocità in bit.

## <a name="expanded-multiple-bit-rate-support"></a>Supporto per più velocità in bit espansa

Il supporto per l'esclusione reciproca è incluso per l'audio con velocità in bit multipli (MBR) e per i video con flussi di dimensioni di immagine variabili.

## <a name="attributes-for-streams"></a>Attributi per i flussi

È possibile assegnare attributi a singoli flussi nei file ASF. È comunque necessario usare gli attributi a livello di file per i file MP3. Questa funzionalità non aggiunge alcun metodo all'SDK, ma i metodi esistenti accetteranno ora numeri di flusso diversi da zero.

## <a name="transcoding-with-smart-recompression"></a>Transcodifica con ricompressione intelligente

La ricompressione intelligente consente di transcodificare i file audio di Windows Media da una velocità in bit elevata a una velocità in bit più bassa con una qualità superiore a quella consentita in precedenza.

## <a name="expanded-metadata-support"></a>Supporto dei metadati espanso

Windows Media Format SDK fornisce le seguenti nuove funzionalità dei metadati:

-   Tag di metadati basati su indice, abilitando più tag con lo stesso nome.
-   Possibilità di leggere gli attributi di intestazione DRM senza un file WMStubDRM. lib.
-   Attributi con più di 64 kilobyte di dati associati.
-   Attributi in più lingue.
-   Dozzine di nuovi attributi predefiniti.

## <a name="dynamic-pixel-aspect-ratio"></a>Proporzioni dinamiche in pixel

I flussi video composti da vari tipi di contenuto possono essere configurati identificando le proporzioni in pixel degli esempi diversi nel flusso. In questo modo, l'applicazione di riproduzione garantisce una migliore riproduzione di tale contenuto.

## <a name="interlaced-video-streams"></a>Flussi video interlacciati

Le versioni precedenti di Windows Media Format SDK hanno consentito di codificare il contenuto [*interlacciato*](wmformat-glossary.md) in un flusso video con analisi progressiva. A partire da Windows Media Format 9 Series SDK, è possibile codificare video interlacciato mantenendo il formato interlacciato. Questo può comportare una migliore riproduzione, in particolare sui dispositivi interlacciati, ad esempio i set di televisione.

## <a name="two-pass-encoding"></a>Codifica Two-Pass

I nuovi codec Windows Media abilitano la codifica a due passaggi. Il contenuto codificato in due passaggi può ottenere un output di qualità superiore.

## <a name="new-speech-codec"></a>Nuovo codec vocale

Questo SDK include il nuovo codec Windows Media Audio 9 Voice, ottimizzato per la codifica della voce umana con una velocità in bit bassa. Questo codec fornisce anche prestazioni superiori per contenuto audio misto.

## <a name="accessible-video-frame-duration"></a>Durata fotogramma video accessibile

È possibile fare in modo che l'oggetto writer di questo SDK fornisca la durata dei fotogrammi video al lettore.

## <a name="streaming-html"></a>Flusso HTML

Con la versione precedente di questo SDK, era possibile usare un comando script per segnalare all'applicazione di aprire una pagina Web. A partire da Windows Media Format 9 Series SDK, è possibile archiviare i componenti di pagine Web nei file ASF, per assicurarsi che non vi siano ritardi nelle presentazioni.

## <a name="wmstublib-no-longer-required-for-build-environment"></a>WMStub. lib non è più necessario per l'ambiente di compilazione

Le impostazioni dell'ambiente di compilazione per Windows Media Format SDK sono state modificate a partire da Windows Media Format 9 Series SDK. Non è più necessario includere WMStub. lib per le applicazioni che usano questo SDK. Tuttavia, le applicazioni abilitate per DRM devono comunque ottenere e firmare un contratto di licenza separato e ottenere una libreria statica univoca da Microsoft. wmla@microsoft.comPer ulteriori informazioni sulla libreria DRM e sul contratto di licenza, contattare. Per altre informazioni sulla creazione di progetti con questo SDK, vedere [file di libreria e impostazioni del compilatore](library-files-and-compiler-settings.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni su Windows Media Format SDK**](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




