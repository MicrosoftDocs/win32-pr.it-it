---
description: Specifica se un gestore del flusso di byte può utilizzare un flusso di byte aperto per la scrittura da parte di un altro thread.
ms.assetid: d9d97880-a563-420c-b598-c3ebd1ae8b74
title: MF_BYTESTREAMHANDLER_ACCEPTS_SHARE_WRITE attributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89ea9b6cf1d126fca44066e7d3292227ecf0ce01f3419b377b6d66b67845f990
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941031"
---
# <a name="mf_bytestreamhandler_accepts_share_write-attribute"></a>MF \_ BYTESTREAMHANDLER \_ ACCETTA \_ L'attributo SHARE \_ WRITE

Specifica se un gestore del flusso di byte può utilizzare un flusso di byte aperto per la scrittura da parte di un altro thread.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Commenti

I gestori di flussi di byte possono supportare questo attributo. Per ottenere o impostare l'attributo, eseguire prima una query sul gestore del flusso di byte per [**l'interfaccia IMFAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) Chiamare quindi [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) o [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

Se questo attributo è **TRUE,** significa che il gestore del flusso di byte può leggere da un flusso mentre un altro thread scrive nello stesso flusso. Quando un flusso viene aperto per la scrittura da un altro thread, il metodo [**IMFByteStream::GetCapabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities) restituisce il flag **MFBYTESTREAM \_ SHARE \_ WRITE.**

Questo attributo influisce sulla risoluzione dell'origine. Se per un flusso di byte è impostato il flag **MFBYTESTREAM \_ SHARE \_ WRITE,** il [resolver](source-resolver.md) di origine non passerà tale flusso a un gestore del flusso di byte, a meno che il gestore non abbia l'attributo MF \_ BYTESTREAMHANDLER ACCEPTS SHARE WRITE impostato \_ su \_ \_ **TRUE.**

Il flag **MFBYTESTREAM \_ SHARE \_ WRITE** è un hint che indica che la lunghezza del flusso potrebbe cambiare durante la lettura da parte del gestore.

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop app \| UWP\]<br/>                                  |
| Server minimo supportato<br/> | Windows App desktop di Server 2008 R2 \[ \| app UWP\]<br/>                     |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Gestori di schemi e Byte-Stream schema](scheme-handlers-and-byte-stream-handlers.md)
</dt> </dl>

 

 




