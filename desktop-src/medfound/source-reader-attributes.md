---
description: Attributi lettore di origine
ms.assetid: 312a588a-848b-4563-893a-fac49a4ca465
title: Attributi lettore di origine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f425710139b2aebf23ff13a2593ba6931c78fe2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753863"
---
# <a name="source-reader-attributes"></a>Attributi lettore di origine

Per inizializzare il [lettore di origine](source-reader.md), è possibile usare gli attributi seguenti.



| Attributo                                                                                                            | Descrizione                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MF \_ bassa \_ latenza](mf-low-latency.md)                                                                               | Abilita l'elaborazione a bassa latenza.                                                                                                                                                                                                    |
| [MF \_ ReadWrite \_ Disabilita \_ convertitori](mf-readwrite-disable-converters.md)                                            | Abilita o Disabilita le conversioni di formato dal lettore di origine.                                                                                                                                                                       |
| [MF \_ ReadWrite \_ Abilita \_ le \_ trasformazioni hardware](mf-readwrite-enable-hardware-transforms.md)                           | Consente al lettore di origine di utilizzare le trasformazioni di Media Foundation basate su hardware (MFTs).                                                                                                                                                |
| [\_ \_ callback asincrono del lettore di origine MF \_ \_](mf-source-reader-async-callback.md)                                           | Contiene un puntatore all'interfaccia di callback dell'applicazione per il lettore di origine.                                                                                                                                                  |
| [\_ \_ Gestione D3D del lettore di origine MF \_ \_](mf-source-reader-d3d-manager.md)                                                 | Contiene un puntatore al Gestione dispositivi Microsoft [Direct3D](direct3d-device-manager.md).                                                                                                                                        |
| [MF \_ lettore di origine \_ \_ disabilitare \_ DXVA](mf-source-reader-disable-dxva.md)                                               | Specifica se il lettore di origine Abilita l'accelerazione video DirectX (DXVA) nel decodificatore video.                                                                                                                                |
| [MF \_ \_ lettore \_ di origine disconnettere \_ MEDIASOURCE \_ alla \_ chiusura](mf-source-reader-disconnect-mediasource-on-shutdown.md) | Specifica se il lettore di origine arresta l'origine del supporto.<br/> Si applica solo quando l'applicazione crea il lettore di origine da un oggetto di origine multimediale esistente.<br/>                                           |
| [MF \_ source \_ Reader \_ Abilita \_ \_ elaborazione video \_ avanzata](mf-source-reader-enable-advanced-video-processing.md)     | Abilita l'elaborazione video avanzata da parte del [lettore di origine](source-reader.md), tra cui conversione dello spazio colore, deinterlacciamento, ridimensionamento video e conversione della frequenza dei fotogrammi.                                                           |
| [MF \_ source \_ Reader \_ Abilita \_ l' \_ elaborazione video](mf-source-reader-enable-video-processing.md)                        | Abilita l'elaborazione video limitata da parte del lettore di origine.                                                                                                                                                                             |
| [\_configurazione del \_ lettore di origine \_ MF \_](mf-source-reader-mediasource-config.md)                                   | Contiene le proprietà di configurazione per l'origine del supporto.                                                                                                                                                                            |
| [\_Attributo di \_ sblocco \_ FIELDOFUSE MFT](mft-fieldofuse-unlock-attribute.md)                                            | Contiene un puntatore [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) , che viene usato per sbloccare un MFT con restrizioni di campo di utilizzo. Per ulteriori informazioni, vedere [restrizioni relative all'utilizzo dei campi](field-of-use-restrictions.md). |



 

Usare questi attributi con i metodi e le funzioni seguenti:

-   [**IMFReadWriteClassFactory::CreateInstanceFromObject**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromobject)
-   [**IMFReadWriteClassFactory::CreateInstanceFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromurl)
-   [**MFCreateSourceReaderFromByteStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)

Per usare uno di questi attributi, chiamare prima [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) per creare un nuovo archivio di attributi. Usare quindi l'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) per impostare gli attributi desiderati nell'archivio di attributi. Passare il puntatore **IMFAttributes** al parametro *pAttributes* di uno dei metodi o delle funzioni elencate in precedenza.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attributi di Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[Lettore di origine](source-reader.md)
</dt> <dt>

[**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)
</dt> </dl>

 

 




