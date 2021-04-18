---
description: Specifica l'URL originale per un flusso di byte.
ms.assetid: 31d7de71-5bbb-4c29-8ce0-df3684c56916
title: Attributo MF_BYTESTREAM_ORIGIN_NAME (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe32602501b3750f709135cf7ca458b6eb6a572f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307981"
---
# <a name="mf_bytestream_origin_name-attribute"></a>\_Attributo del \_ nome di origine MF BYTESTREAM \_

Specifica l'URL originale per un flusso di byte.

## <a name="data-type"></a>Tipo di dati

Stringa di caratteri wide

## <a name="remarks"></a>Commenti

I flussi di byte basati su file possono supportare questo attributo. Il valore dell'attributo viene impostato quando viene creato il flusso di byte. Per ottenere il valore dell'attributo, eseguire una query sull'oggetto flusso di byte per l'interfaccia [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .

La costante GUID per questo attributo viene esportata da mfuuid. lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | App desktop di Windows Vista app \[ \| UWP\]<br/>                                                    |
| Server minimo supportato<br/> | App UWP per \[ app desktop di Windows Server 2008 \|\]<br/>                                              |
| Intestazione<br/>                   | <dl> <dt>Mfobjects. h (include Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli attributi di Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del flusso di byte](byte-stream-attributes.md)
</dt> <dt>

[**IMFAttributes:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[**IMFAttributes:: sestring**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 




