---
description: Attributi del flusso di byte
ms.assetid: d57a57e9-87e4-4f7f-943a-63fd2ad1d1a6
title: Attributi del flusso di byte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0471905925b397f4f83ad457384b5e9b4790b54c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305511"
---
# <a name="byte-stream-attributes"></a>Attributi del flusso di byte

Gli attributi seguenti si applicano ad alcuni flussi di byte. Per determinare se un flusso di byte supporta gli attributi, eseguire una query sull'oggetto flusso di byte per l'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .



| Attributo                                                                                  | Descrizione                                                       |
|--------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| [**\_tipo di \_ contenuto MF BYTESTREAM \_**](mf-bytestream-content-type-attribute.md)              | Specifica il tipo MIME di un flusso di byte.                         |
| [**\_durata MF BYTESTREAM \_**](mf-bytestream-duration-attribute.md)                       | Specifica la durata di un flusso di byte, in unità di 100 nanosecondi. |
| [\_URI del file MF BYTESTREAM \_ IFO \_ \_](mf-bytestream-ifo-file-uri.md)                           | Specifica l'URL di un file IFO associato.                      |
| [**\_ora dell' \_ Ultima \_ modifica MF BYTESTREAM \_**](mf-bytestream-last-modified-time-attribute.md) | Specifica la data dell'Ultima modifica di un flusso di byte.                   |
| [**\_nome dell' \_ origine MF BYTESTREAM \_**](mf-bytestream-origin-name-attribute.md)                | Specifica l'URL originale per un flusso di byte.                     |



 

Gli attributi seguenti si applicano ai gestori del flusso di byte.



| Attributo                                                                                    | Descrizione                                                                                                |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [MF \_ BYTESTREAMHANDLER \_ accetta \_ la \_ scrittura condivisa](mf-bytestreamhandler-accepts-share-write.md) | Specifica se un gestore del flusso di byte può utilizzare un flusso di byte aperto per la scrittura da un altro thread |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> <dt>

[Attributi di Media Foundation](media-foundation-attributes.md)
</dt> </dl>

 

 



