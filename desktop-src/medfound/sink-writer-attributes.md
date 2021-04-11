---
description: Attributi del writer di sink
ms.assetid: f27b9beb-f35f-400e-a337-50d9de21e91e
title: Attributi del writer di sink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e23dbca06c3ff1a4ac80b8e68413fdd0816d71a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130470"
---
# <a name="sink-writer-attributes"></a>Attributi del writer di sink

Gli attributi seguenti possono essere utilizzati per inizializzare il writer del sink.



| Attributo                                                                                  | Descrizione                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MF \_ bassa \_ latenza](mf-low-latency.md)                                                     | Abilita l'elaborazione a bassa latenza.                                                                                                                                                                                                    |
| [MF \_ ReadWrite \_ Disabilita \_ convertitori](mf-readwrite-disable-converters.md)                  | Abilita o Disabilita le conversioni di formato dal writer del sink.                                                                                                                                                                         |
| [MF \_ ReadWrite \_ Abilita \_ le \_ trasformazioni hardware](mf-readwrite-enable-hardware-transforms.md) | Consente al writer di sink di utilizzare le trasformazioni di Media Foundation basate su hardware (MFTs).                                                                                                                                                  |
| [\_ \_ callback asincrono del writer di sink MF \_ \_](mf-sink-writer-async-callback.md)                     | Contiene un puntatore all'interfaccia di callback dell'applicazione per il writer del sink.                                                                                                                                                    |
| [\_disabilitare la \_ limitazione del writer di sink MF \_ \_](mf-sink-writer-disable-throttling.md)             | Specifica se il writer di sink limita la frequenza dei dati in arrivo.                                                                                                                                                                |
| [MF \_ transcode \_ CONTAINERTYPE](mf-transcode-containertype.md)                             | Specifica il tipo di contenitore del file di output.                                                                                                                                                                                   |
| [\_Attributo di \_ sblocco \_ FIELDOFUSE MFT](mft-fieldofuse-unlock-attribute.md)                  | Contiene un puntatore [**IMFFieldOfUseMFTUnlock**](/windows/desktop/api/mfidl/nn-mfidl-imffieldofusemftunlock) , che viene usato per sbloccare un MFT con restrizioni di campo di utilizzo. Per ulteriori informazioni, vedere [restrizioni relative all'utilizzo dei campi](field-of-use-restrictions.md). |
| [\_ \_ \_ Gestione D3D sink writer \_ MF](mf-sink-writer-d3d-manager.md)                           | Usare questo attributo per fornire un dispositivo Direct3D per tutti i codificatori video o i sink di supporto caricati dal writer del sink.                                                                                                                   |



 

Usare questi attributi con i metodi e le funzioni seguenti:

-   [**IMFReadWriteClassFactory::CreateInstanceFromObject**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromobject)
-   [**IMFReadWriteClassFactory::CreateInstanceFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromurl)
-   [**MFCreateSinkWriterFromMediaSink**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfrommediasink)
-   [**MFCreateSinkWriterFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl)

Per usare uno di questi attributi, chiamare prima [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) per creare un nuovo archivio di attributi. Usare quindi l'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) per impostare gli attributi desiderati nell'archivio di attributi. Passare il puntatore **IMFAttributes** al parametro *pAttributes* di uno dei metodi o delle funzioni elencate in precedenza.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IMFSinkWriter**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsinkwriter)
</dt> <dt>

[Attributi di Media Foundation](media-foundation-attributes.md)
</dt> </dl>

 

 



