---
description: Contiene un puntatore all'interfaccia di callback delle applicazioni per il lettore di origine.
ms.assetid: de226a5a-03c0-4bfe-bb20-8969ce43cf53
title: MF_SOURCE_READER_ASYNC_CALLBACK attributo (Mfreadwrite.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af4dedfcdcb426eb62a0ae14bec3fd75232c9a871d0bad10194860305c687fa8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119605157"
---
# <a name="mf_source_reader_async_callback-attribute"></a>Attributo \_ MF SOURCE \_ READER \_ ASYNC \_ CALLBACK

Contiene un puntatore all'interfaccia di callback dell'applicazione per [il lettore di origine.](source-reader.md)

## <a name="data-type"></a>Tipo di dati

**IMFSourceReaderCallback \* *_ archiviato come _* IUnknown\***

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Per impostare questo attributo, chiamare [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Commenti

Il valore di questo attributo è un puntatore [**all'interfaccia IMFSourceReaderCallback**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereadercallback) dell'applicazione.

Usare questo attributo con le funzioni seguenti:

-   [**MFCreateSourceReaderFromByteStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource)
-   [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop app \| UWP\]<br/>                                        |
| Server minimo supportato<br/> | Windows App UWP per app desktop server 2008 R2 \[ \|\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Mfreadwrite.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Lettore di origine](source-reader.md)
</dt> <dt>

[Attributi del lettore di origine](source-reader-attributes.md)
</dt> </dl>

 

 




