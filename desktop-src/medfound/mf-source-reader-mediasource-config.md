---
description: Contiene le proprietà di configurazione per il lettore di origine.
ms.assetid: f7e5ef6a-5fc3-4f39-acc0-61ce79030211
title: Attributo MF_SOURCE_READER_MEDIASOURCE_CONFIG (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31f36b2a09810dd1c2563033ea65643f1dabcb3f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320814"
---
# <a name="mf_source_reader_mediasource_config-attribute"></a>Attributo di configurazione di MF \_ source \_ Reader \_ MEDIASOURCE \_

Contiene le proprietà di configurazione per il [lettore di origine](source-reader.md).

## <a name="data-type"></a>Tipo di dati

**IPropertyStore \* *_ archiviato come _* IUnknown\***

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: getunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Per impostare questo attributo, chiamare [**IMFAttributes:: seunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Commenti

Il valore di questo attributo è un puntatore all'interfaccia **IPropertyStore** di un archivio delle proprietà. È possibile usare questo attributo per passare le proprietà di configurazione all'origine multimediale.

Utilizzare questo attributo con le funzioni seguenti:

-   [**MFCreateSourceReaderFromByteStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)

Internamente, il lettore di origine passa il puntatore **IPropertyStore** al resolver di origine. Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 7 \[ \| UWP\]<br/>                                        |
| Server minimo supportato<br/> | App desktop di Windows Server 2008 R2 \[ \| UWP\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Mfreadwrite. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Lettore di origine](source-reader.md)
</dt> <dt>

[Attributi lettore di origine](source-reader-attributes.md)
</dt> </dl>

 

 




