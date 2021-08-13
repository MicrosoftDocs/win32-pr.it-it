---
description: Attributi del lettore di origine
ms.assetid: 312a588a-848b-4563-893a-fac49a4ca465
title: Attributi del lettore di origine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a7bd9c5b3c5a71fb1b91515400fb0cf3670bd3b73b6635c811dcc79bd05e74f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118238329"
---
# <a name="source-reader-attributes"></a>Attributi del lettore di origine

Gli attributi seguenti possono essere usati per inizializzare il [lettore di origine](source-reader.md).



| Attributo                                                                                                            | Descrizione                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [BASSA \_ LATENZA MF \_](mf-low-latency.md)                                                                               | Abilita l'elaborazione a bassa latenza.                                                                                                                                                                                                    |
| [MF \_ READWRITE \_ DISABLE \_ CONVERTERS](mf-readwrite-disable-converters.md)                                            | Abilita o disabilita le conversioni di formato da parte del lettore di origine.                                                                                                                                                                       |
| [MF \_ READWRITE \_ ENABLE \_ HARDWARE \_ TRANSFORMS](mf-readwrite-enable-hardware-transforms.md)                           | Consente al lettore di origine di usare trasformazioni Media Foundation basate su hardware.                                                                                                                                                |
| [CALLBACK ASINCRONO \_ DEL \_ \_ LETTORE DI ORIGINE \_ MF](mf-source-reader-async-callback.md)                                           | Contiene un puntatore all'interfaccia di callback dell'applicazione per il lettore di origine.                                                                                                                                                  |
| [MF \_ SOURCE \_ READER \_ D3D \_ MANAGER](mf-source-reader-d3d-manager.md)                                                 | Contiene un puntatore a Gestione [dispositivi Direct3D di](direct3d-device-manager.md)Microsoft.                                                                                                                                        |
| [MF \_ SOURCE \_ READER \_ DISABLE \_ DXVA](mf-source-reader-disable-dxva.md)                                               | Specifica se il lettore di origine abilita l'accelerazione video DirectX (DXVA) nel decodificatore video.                                                                                                                                |
| [LETTORE DI ORIGINE MF \_ \_ DISCONNETTE \_ \_ MEDIASOURCE \_ \_ ALL'ARRESTO](mf-source-reader-disconnect-mediasource-on-shutdown.md) | Specifica se il lettore di origine arresta l'origine multimediale.<br/> Si applica solo quando l'applicazione crea il lettore di origine da un oggetto origine multimediale esistente.<br/>                                           |
| [IL LETTORE \_ DI ORIGINE MF \_ ABILITA \_ \_ \_ L'ELABORAZIONE VIDEO \_ AVANZATA](mf-source-reader-enable-advanced-video-processing.md)     | Abilita l'elaborazione video avanzata [da](source-reader.md)parte del lettore di origine, tra cui conversione dello spazio colore, delnterlacing, ridimensionamento video e conversione della frequenza dei fotogrammi.                                                           |
| [IL LETTORE \_ DI ORIGINE MF \_ ABILITA \_ \_ L'ELABORAZIONE \_ VIDEO](mf-source-reader-enable-video-processing.md)                        | Abilita l'elaborazione video limitata dal lettore di origine.                                                                                                                                                                             |
| [CONFIGURAZIONE DEL \_ LETTORE \_ DI ORIGINE \_ MF \_ MEDIASOURCE](mf-source-reader-mediasource-config.md)                                   | Contiene le proprietà di configurazione per l'origine multimediale.                                                                                                                                                                            |
| [Attributo \_ MFT FIELDOFUSE \_ UNLOCK \_](mft-fieldofuse-unlock-attribute.md)                                            | Contiene un [**puntatore IMFFieldOfUseMFTUnlock,**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) utilizzato per sbloccare un MFT con restrizioni sul campo di utilizzo. Per altre informazioni, vedere [Field of Use Restrictions](field-of-use-restrictions.md). |



 

Usare questi attributi con i metodi e le funzioni seguenti:

-   [**IMFReadWriteClassFactory::CreateInstanceFromObject**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromobject)
-   [**IMFReadWriteClassFactory::CreateInstanceFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromurl)
-   [**MFCreateSourceReaderFromByteStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)

Per usare uno di questi attributi, chiamare [**prima MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) per creare un nuovo archivio attributi. Usare quindi [**l'interfaccia IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) per impostare gli attributi desiderati nell'archivio attributi. Passare il **puntatore IMFAttributes** al *parametro pAttributes* di uno dei metodi o delle funzioni elencati in precedenza.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Media Foundation attributi](media-foundation-attributes.md)
</dt> <dt>

[Lettore di origine](source-reader.md)
</dt> <dt>

[**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)
</dt> </dl>

 

 




