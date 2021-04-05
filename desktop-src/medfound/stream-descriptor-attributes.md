---
description: Attributi del descrittore di flusso
ms.assetid: 1364d7c5-67e8-49b6-8038-d6d4ea03fb7d
title: Attributi del descrittore di flusso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cc7b49b8da74bacc84151148047ccdeaffc364a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753842"
---
# <a name="stream-descriptor-attributes"></a>Attributi del descrittore di flusso

## <a name="common-stream-descriptor-attributes"></a>Attributi del descrittore di flusso comuni

Gli attributi seguenti si applicano ai descrittori di flusso.



| Attributo                                                   | Descrizione                                                                           |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [**\_lingua MF SD \_**](mf-sd-language-attribute.md)        | Specifica la lingua per un flusso.                                                  |
| [MF \_ SD si \_ escludono a vicenda \_](mf-sd-mutually-exclusive.md) | Specifica se un flusso si escludono a vicenda con altri flussi dello stesso tipo. |
| [**MF \_ SD \_ protetto**](mf-sd-protected-attribute.md)      | Specifica se un flusso contiene contenuto protetto.                                |
| [\_ \_ Nome flusso MF \_ SD](mf-sd-stream-name.md)               | Contiene il nome di un flusso.                                                        |



 

## <a name="asf-specific-stream-descriptor-attributes"></a>Attributi del descrittore di flusso ASF-Specific

Gli attributi seguenti si applicano ai descrittori di flusso per i file di formato Advanced Systems (ASF).



| Attributo                                                                                                                | Descrizione                                                                                |
|--------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ Avg \_ bufferSize**](mf-sd-asf-extstrmprop-avg-buffersize-attribute.md)                      | Specifica la dimensione media del buffer necessaria per un flusso in un file ASF, in byte.            |
| [**\_velocità in \_ \_ \_ \_ bit dei dati media \_ di MF SD ASF EXTSTRMPROP**](mf-sd-asf-extstrmprop-avg-data-bitrate-attribute.md)                 | Specifica la velocità media dei bit di dati di un flusso in un file ASF, in bit al secondo.        |
| [**\_ \_ \_ \_ \_ indice ID lingua \_ MF SD ASF EXTSTRMPROP**](mf-sd-asf-extstrmprop-language-id-index-attribute.md)               | Specifica la lingua utilizzata da un flusso in un file ASF.                                    |
| [**MF \_ SD \_ ASF \_ EXTSTRMPROP \_ Max \_ bufferSize**](mf-sd-asf-extstrmprop-max-buffersize-attribute.md)                      | Specifica la dimensione massima del buffer necessaria per un flusso in un file ASF, in byte.            |
| [**\_velocità in \_ \_ \_ \_ bit massima dei dati di EXTSTRMPROP \_ MF SD ASF**](mf-sd-asf-extstrmprop-max-data-bitrate-attribute.md)                 | Specifica la velocità in bit massima dei dati di un flusso in un file ASF, in bit al secondo         |
| [**\_modello di \_ \_ conformità del \_ dispositivo di metadati \_ \_ MF SD ASF**](mf-sd-asf-metadata-device-conformance-template-attribute.md) | Specifica il modello di conformità del dispositivo per un flusso in un file ASF, in bit al secondo. |
| [**\_velocità in bit MF SD \_ ASF \_ STREAMBITRATES \_**](mf-sd-asf-streambitrates-bitrate-attribute.md)                               | Specifica la velocità in bit media di un flusso in un file ASF, in bit al secondo.             |



 

## <a name="sami-media-source-stream-descriptor-attributes"></a>Attributi del descrittore del flusso di origine dei supporti SAMI

Il seguente attributo si applica al descrittore di flusso per l'origine dei supporti SAMI.



| Attributo                                                       | Descrizione                                                                                                 |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**\_lingua MF SD \_ Sami \_**](mf-sd-sami-language-attribute.md) | Contiene il nome del linguaggio SAMI (Synchronized Accessible Media Interchange) definito per il flusso. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
</dt> <dt>

[Attributi di Media Foundation](media-foundation-attributes.md)
</dt> </dl>

 

 



