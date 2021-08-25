---
description: Attributi del descrittore di flusso
ms.assetid: 1364d7c5-67e8-49b6-8038-d6d4ea03fb7d
title: Attributi del descrittore di flusso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5db29ef0076415ff07e9ed25f7e6ca3e0588ec25257802fe0c7829ab3178c935
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953231"
---
# <a name="stream-descriptor-attributes"></a>Attributi del descrittore di flusso

## <a name="common-stream-descriptor-attributes"></a>Attributi comuni del descrittore di flusso

Gli attributi seguenti si applicano ai descrittori di flusso.



| Attributo                                                   | Descrizione                                                                           |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [**LINGUAGGIO \_ SD MF \_**](mf-sd-language-attribute.md)        | Specifica la lingua per un flusso.                                                  |
| [MF \_ SD SI \_ ESCLUDONO A \_ VICENDA](mf-sd-mutually-exclusive.md) | Specifica se un flusso si escludono a vicenda con altri flussi dello stesso tipo. |
| [**MF \_ SD \_ PROTECTED**](mf-sd-protected-attribute.md)      | Specifica se un flusso contiene contenuto protetto.                                |
| [MF SD STREAM NAME (NOME \_ FLUSSO SD \_ MF) \_](mf-sd-stream-name.md)               | Contiene il nome di un flusso.                                                        |



 

## <a name="asf-specific-stream-descriptor-attributes"></a>ASF-Specific attributi del descrittore di flusso

Gli attributi seguenti si applicano ai descrittori di flusso per i file ASF (Advanced Systems Format).



| Attributo                                                                                                                | Descrizione                                                                                |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ AVG \_ BUFFERSIZE**](mf-sd-asf-extstrmprop-avg-buffersize-attribute.md)                      | Specifica le dimensioni medie del buffer necessarie per un flusso in un file ASF, in byte.            |
| [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ AVG \_ DATA \_ BITRATE**](mf-sd-asf-extstrmprop-avg-data-bitrate-attribute.md)                 | Specifica la velocità in bit media dei dati di un flusso in un file ASF, in bit al secondo.        |
| [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ LANGUAGE \_ ID \_ INDEX**](mf-sd-asf-extstrmprop-language-id-index-attribute.md)               | Specifica la lingua utilizzata da un flusso in un file ASF.                                    |
| [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ MAX \_ BUFFERSIZE**](mf-sd-asf-extstrmprop-max-buffersize-attribute.md)                      | Specifica le dimensioni massime del buffer necessarie per un flusso in un file ASF, in byte.            |
| [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ VELOCITÀ IN BIT MASSIMA DEI \_ \_ DATI**](mf-sd-asf-extstrmprop-max-data-bitrate-attribute.md)                 | Specifica la velocità in bit massima dei dati di un flusso in un file ASF, in bit al secondo         |
| [**MODELLO DI CONFORMITÀ \_ DEL DISPOSITIVO MF SD \_ ASF \_ METADATA \_ \_ \_**](mf-sd-asf-metadata-device-conformance-template-attribute.md) | Specifica il modello di conformità del dispositivo per un flusso in un file ASF, in bit al secondo. |
| [**MF \_ SD \_ ASF \_ STREAMBITRATES \_ BITRATES**](mf-sd-asf-streambitrates-bitrate-attribute.md)                               | Specifica la velocità in bit media di un flusso in un file ASF, in bit al secondo.             |



 

## <a name="sami-media-source-stream-descriptor-attributes"></a>Attributi del descrittore del flusso di origine multimediale SAMI

L'attributo seguente si applica al descrittore di flusso per l'origine multimediale SAMI.



| Attributo                                                       | Descrizione                                                                                                 |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**MF \_ SD \_ SAMI \_ LANGUAGE**](mf-sd-sami-language-attribute.md) | Contiene il nome della lingua SAMI (Synchronized Accessible Media Interchange) definito per il flusso. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[Media Foundation attributi](media-foundation-attributes.md)
</dt> </dl>

 

 



