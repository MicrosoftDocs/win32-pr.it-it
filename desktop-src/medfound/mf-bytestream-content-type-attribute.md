---
description: Specifica il tipo MIME di un flusso di byte.
ms.assetid: bcf86ece-2673-4ed8-98fd-cd0e2154b4a8
title: MF_BYTESTREAM_CONTENT_TYPE attributo (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 901f3d9d2b46e503bcf8f66127eb94383710a7c1055c04fccb97f6d935d463b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974010"
---
# <a name="mf_bytestream_content_type-attribute"></a>Attributo MF \_ BYTESTREAM \_ CONTENT \_ TYPE

Specifica il tipo MIME di un flusso di byte.

## <a name="data-type"></a>Tipo di dati

Stringa di caratteri wide

## <a name="remarks"></a>Commenti

Per ottenere il valore dell'attributo, eseguire una query sull'oggetto flusso di byte per [**l'interfaccia IMFAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)

La costante GUID per questo attributo viene esportata da mfuuid.lib.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows App desktop Di Vista \[ \| app UWP\]<br/>                                                    |
| Server minimo supportato<br/> | Windows App UWP per app desktop server 2008 \[ \|\]<br/>                                              |
| Intestazione<br/>                   | <dl> <dt>Mfobjects.h (includere Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elenco alfabetico di Media Foundation attributi](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributi del flusso di byte](byte-stream-attributes.md)
</dt> <dt>

[**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 




