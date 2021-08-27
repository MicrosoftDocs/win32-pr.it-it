---
description: Specifica l'ultima modifica di un flusso di byte.
ms.assetid: dceff922-44eb-478f-842a-8ac0e73a02ee
title: MF_BYTESTREAM_LAST_MODIFIED_TIME attributo (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b476a78dba2bf757ed37b6029d67d5084804d1360dbc61e7c8861005b74a3bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113971"
---
# <a name="mf_bytestream_last_modified_time-attribute"></a>Attributo MF \_ BYTESTREAM \_ LAST MODIFIED \_ \_ TIME

Specifica l'ultima modifica di un flusso di byte.

## <a name="data-type"></a>Tipo di dati

Matrice di byte

## <a name="remarks"></a>Commenti

Questo attributo è facoltativo. Il valore dell'attributo è una [**struttura FILETIME.**](/windows/win32/api/minwinbase/ns-minwinbase-filetime)

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

[**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream)
</dt> </dl>

 

 
