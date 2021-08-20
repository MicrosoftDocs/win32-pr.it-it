---
description: Contiene le proprietà di configurazione per il lettore di origine.
ms.assetid: f7e5ef6a-5fc3-4f39-acc0-61ce79030211
title: MF_SOURCE_READER_MEDIASOURCE_CONFIG attributo (Mfreadwrite.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cae8ad787a794954004f7fcb3679a2a836279a7b9094ae170bafa14d848495d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118059065"
---
# <a name="mf_source_reader_mediasource_config-attribute"></a>Attributo \_ MF SOURCE \_ READER \_ MEDIASOURCE \_ CONFIG

Contiene le proprietà di configurazione per [il lettore di origine.](source-reader.md)

## <a name="data-type"></a>Tipo di dati

**IPropertyStore \* *_ archiviato come _* IUnknown\***

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Per impostare questo attributo, chiamare [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Commenti

Il valore di questo attributo è un puntatore **all'interfaccia IPropertyStore** di un archivio proprietà. È possibile usare questo attributo per passare le proprietà di configurazione all'origine multimediale.

Usare questo attributo con le funzioni seguenti:

-   [**MFCreateSourceReaderFromByteStream**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrombytestream)
-   [**MFCreateSourceReaderFromURL**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfromurl)

Internamente, il lettore di origine passa il **puntatore IPropertyStore** al sistema di risoluzione di origine. Per altre informazioni, vedere [Configurazione di un'origine multimediale](configuring-a-media-source.md).

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

 

 




