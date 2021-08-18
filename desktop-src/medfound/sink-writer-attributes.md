---
description: Attributi del writer di sink
ms.assetid: f27b9beb-f35f-400e-a337-50d9de21e91e
title: Attributi del writer di sink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18bf64dd4279ef2e35ed86f50c4444412b3cc70205f6aad52adac8a41895af11
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012369"
---
# <a name="sink-writer-attributes"></a>Attributi del writer di sink

Gli attributi seguenti possono essere usati per inizializzare il writer di sink.



| Attributo                                                                                  | Descrizione                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [BASSA \_ LATENZA MF \_](mf-low-latency.md)                                                     | Abilita l'elaborazione a bassa latenza.                                                                                                                                                                                                    |
| [MF \_ READWRITE \_ \_ DISABILITARE I CONVERTITORI](mf-readwrite-disable-converters.md)                  | Abilita o disabilita le conversioni di formato da parte del writer di sink.                                                                                                                                                                         |
| [MF \_ READWRITE \_ ENABLE \_ HARDWARE \_ TRANSFORMS](mf-readwrite-enable-hardware-transforms.md) | Consente al writer di sink di usare trasformazioni Media Foundation hardware( MFT).                                                                                                                                                  |
| [CALLBACK ASINCRONO DEL \_ \_ WRITER \_ DI SINK MF \_](mf-sink-writer-async-callback.md)                     | Contiene un puntatore all'interfaccia di callback dell'applicazione per il writer di sink.                                                                                                                                                    |
| [MF \_ SINK \_ WRITER \_ DISABLE \_ THROTTLING](mf-sink-writer-disable-throttling.md)             | Specifica se il writer di sink limita la velocità dei dati in ingresso.                                                                                                                                                                |
| [MF \_ TRANSCODE \_ CONTAINERTYPE](mf-transcode-containertype.md)                             | Specifica il tipo di contenitore del file di output.                                                                                                                                                                                   |
| [Attributo \_ MFT FIELDOFUSE \_ UNLOCK \_](mft-fieldofuse-unlock-attribute.md)                  | Contiene un [**puntatore IMFFieldOfUseMFTUnlock,**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) usato per sbloccare un MFT con restrizioni sul campo di utilizzo. Per altre informazioni, vedere [Field of Use Restrictions](field-of-use-restrictions.md). |
| [MF \_ SINK \_ WRITER \_ D3D \_ MANAGER](mf-sink-writer-d3d-manager.md)                           | Usare questo attributo per fornire un dispositivo Direct3D per qualsiasi codificatore video o sink multimediale caricato dal writer di sink.                                                                                                                   |



 

Usare questi attributi con i metodi e le funzioni seguenti:

-   [**IMFReadWriteClassFactory::CreateInstanceFromObject**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromobject)
-   [**IMFReadWriteClassFactory::CreateInstanceFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromurl)
-   [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

Per usare uno di questi attributi, chiamare [**prima MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) per creare un nuovo archivio attributi. Usare quindi [**l'interfaccia IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) per impostare gli attributi desiderati nell'archivio attributi. Passare il **puntatore IMFAttributes** al *parametro pAttributes* di uno dei metodi o delle funzioni elencati in precedenza.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IMFSinkWriter**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter)
</dt> <dt>

[Media Foundation attributi](media-foundation-attributes.md)
</dt> </dl>

 

 



