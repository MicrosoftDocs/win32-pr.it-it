---
description: Specifica se un gestore del flusso di byte può utilizzare un flusso di byte aperto per la scrittura da un altro thread.
ms.assetid: d9d97880-a563-420c-b598-c3ebd1ae8b74
title: Attributo MF_BYTESTREAMHANDLER_ACCEPTS_SHARE_WRITE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b46a3402585cbce9c1d1464ceb9fb161527673c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309586"
---
# <a name="mf_bytestreamhandler_accepts_share_write-attribute"></a>MF \_ BYTESTREAMHANDLER \_ accetta \_ l' \_ attributo Share Write

Specifica se un gestore del flusso di byte può utilizzare un flusso di byte aperto per la scrittura da un altro thread.

## <a name="data-type"></a>Tipo di dati

**UINT32**

## <a name="getset"></a>Ottenere/impostare

Per ottenere questo attributo, chiamare [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Per impostare questo attributo, chiamare [**IMFAttributes::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)SetAttribute.

## <a name="remarks"></a>Commenti

I gestori del flusso di byte possono supportare questo attributo. Per ottenere o impostare l'attributo, eseguire prima una query sul gestore del flusso di byte per l'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) . Chiamare quindi [**IMFAttributes:: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32) o [**IMFAttributes:: seuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

Se questo attributo è **true**, significa che il gestore del flusso di byte può leggere da un flusso mentre un altro thread scrive nello stesso flusso. Quando un flusso viene aperto per la scrittura da parte di un altro thread, il metodo [**IMFByteStream:: GetCapabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities) restituisce il flag di **\_ \_ scrittura della condivisione MFBYTESTREAM** .

Questo attributo influiscono sulla risoluzione dell'origine. Se per un flusso di byte è impostato il flag di **\_ \_ scrittura della condivisione MFBYTESTREAM** , il [resolver di origine](source-resolver.md) non passerà il flusso a un gestore del flusso di byte, a meno che il gestore non abbia l' \_ attributo MF BYTESTREAMHANDLER \_ accepts \_ per la scrittura della condivisione \_ impostata su **true**.

Il flag di **\_ \_ scrittura della condivisione MFBYTESTREAM** è un suggerimento che la lunghezza del flusso potrebbe cambiare durante la lettura da parte del gestore.

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows 7 \[ \| UWP\]<br/>                                  |
| Server minimo supportato<br/> | App desktop di Windows Server 2008 R2 \[ \| UWP\]<br/>                     |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Gestori di schemi e gestori di Byte-Stream](scheme-handlers-and-byte-stream-handlers.md)
</dt> </dl>

 

 




