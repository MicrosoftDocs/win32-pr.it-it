---
description: Specifica l'URL originale per un flusso di byte.
ms.assetid: 31d7de71-5bbb-4c29-8ce0-df3684c56916
title: MF_BYTESTREAM_ORIGIN_NAME attributo (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abc485beeaf2b3fb80b7dc231dedf4082b848e003d0128c0cf4c73e8c2c5cc3a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941061"
---
# <a name="mf_bytestream_origin_name-attribute"></a>Attributo MF \_ BYTESTREAM \_ ORIGIN \_ NAME

Specifica l'URL originale per un flusso di byte.

## <a name="data-type"></a>Tipo di dati

Stringa di caratteri wide

## <a name="remarks"></a>Commenti

I flussi di byte basati su file possono supportare questo attributo. Il valore dell'attributo viene impostato quando viene creato il flusso di byte. Per ottenere il valore dell'attributo, eseguire una query sull'oggetto flusso di byte per [**l'interfaccia IMFAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows App desktop vista \[ \| app UWP\]<br/>                                                    |
| Server minimo supportato<br/> | Windows App desktop di Server 2008 \[ \| app UWP\]<br/>                                              |
| Intestazione<br/>                   | <dl> <dt>Mfobjects.h (includere Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico degli Media Foundation personalizzati](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del flusso di byte](byte-stream-attributes.md)
</dt> <dt>

[**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 




