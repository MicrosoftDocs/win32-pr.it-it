---
description: Specifica se il lettore di origine arresta l'origine del supporto.
ms.assetid: c85f5994-8005-48c9-8a05-0316f48f4142
title: Attributo MF_SOURCE_READER_DISCONNECT_MEDIASOURCE_ON_SHUTDOWN (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7a9474e7fb19bb6531baf31a97238bbe6b10e46
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351716"
---
# <a name="mf_source_reader_disconnect_mediasource_on_shutdown-attribute"></a>MF \_ source \_ Reader \_ disconnettere \_ MEDIASOURCE \_ sull' \_ attributo Shutdown

Specifica se il [lettore di origine](source-reader.md) arresta l'origine del supporto.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.

## <a name="remarks"></a>Commenti

Questo attributo si applica solo quando l'applicazione crea il lettore di origine da un oggetto di origine multimediale esistente, chiamando [**MFCreateSourceReaderFromMediaSource**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesourcereaderfrommediasource) o chiamando [**IMFReadWriteClassFactory:: CreateInstanceFromObject**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfreadwriteclassfactory-createinstancefromobject).

Per impostazione predefinita, quando l'applicazione rilascia il lettore di origine, il lettore di origine arresta l'origine multimediale chiamando [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) nell'origine del supporto. A questo punto, l'applicazione non può più usare l'origine multimediale.

Tuttavia, se il \_ \_ lettore di origine MF \_ Disconnect \_ MEDIASOURCE \_ on \_ Shutdown attribute è **true**, il lettore di origine non arresta l'origine del supporto. Ciò significa che l'applicazione può comunque utilizzare l'origine multimediale dopo che l'applicazione rilascia il lettore di origine. Significa anche che l'applicazione è responsabile della chiamata di [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) nell'origine multimediale.

Se l'applicazione crea il lettore di origine da un URL o da un flusso di byte, il lettore di origine arresta sempre l'origine del supporto. \_ \_ \_ In questo caso, l'attributo per la disconnessione di un lettore di origine MF all' \_ \_ \_ arresto viene ignorato.

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

 

 




