---
description: Specifica se il lettore di origine arresta l'origine multimediale.
ms.assetid: c85f5994-8005-48c9-8a05-0316f48f4142
title: MF_SOURCE_READER_DISCONNECT_MEDIASOURCE_ON_SHUTDOWN attributo (Mfreadwrite.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 323340a0b95fd6f52d4ac7e8db2e9ff53bf70edb30442369f1ffd8f2f2c55fa1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663891"
---
# <a name="mf_source_reader_disconnect_mediasource_on_shutdown-attribute"></a>ATTRIBUTO ON SHUTDOWN DEL LETTORE DI ORIGINE MF \_ \_ DISCONNECT \_ \_ MEDIASOURCE \_ \_

Specifica se il [lettore di origine](source-reader.md) arresta l'origine multimediale.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Commenti

Questo attributo si applica solo quando l'applicazione crea il lettore di origine da un oggetto di origine multimediale esistente, chiamando [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource) o [**chiamando IMFReadWriteClassFactory::CreateInstanceFromObject**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromobject).

Per impostazione predefinita, quando l'applicazione rilascia il lettore di origine, il lettore di origine arresta l'origine multimediale chiamando [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) sull'origine multimediale. A questo punto, l'applicazione non può più usare l'origine multimediale.

Tuttavia, se l'attributo MF SOURCE READER DISCONNECT MEDIASOURCE ON SHUTDOWN è TRUE, il lettore di origine non \_ \_ \_ \_ \_ \_ arresta l'origine multimediale.  Ciò significa che l'applicazione può comunque usare l'origine multimediale dopo che l'applicazione ha rilasciato il lettore di origine. Significa anche che l'applicazione è responsabile della chiamata [**di IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) sull'origine multimediale.

Se l'applicazione crea il lettore di origine da un URL o da un flusso di byte, il lettore di origine arresta sempre l'origine multimediale. In \_ questo caso, \_ l'attributo MF SOURCE READER DISCONNECT \_ \_ MEDIASOURCE ON SHUTDOWN viene \_ \_ ignorato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop app \| UWP\]<br/>                                        |
| Server minimo supportato<br/> | Windows App desktop di Server 2008 R2 \[ \| app UWP\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>Mfreadwrite.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Lettore di origine](source-reader.md)
</dt> <dt>

[Attributi del lettore di origine](source-reader-attributes.md)
</dt> </dl>

 

 




