---
description: Archivia la stringa inviata nell'intestazione Accept-Language personalizzata.
ms.assetid: b6ac613c-099b-4415-84ad-c0f8ad5f667b
title: MFNETSOURCE_STREAM_LANGUAGE proprietà (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c44b6f55fd2f5652a41d9aa5eed76e60e73152343d2baf6c577be56bc462c94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119344541"
---
# <a name="mfnetsource_stream_language-property"></a>MFNETSOURCE \_ STREAM LANGUAGE - \_ proprietà

Archivia la stringa inviata nell'intestazione Accept-Language personalizzata.



Tipo di dati

Tipo PROPVARIANT (vt)

membro PROPVARIANT

**Wchar\***

VT \_ LPWSTR

**pwszVal**



## <a name="remarks"></a>Commenti

La costante MFNETSOURCE \_ STREAM LANGUAGE definisce il GUID per la chiave di \_ proprietà. L'identificatore di proprietà (PID) è zero. Per impostare questa proprietà nell'origine di rete, passare un **puntatore IPropertyStore** al resolver di origine. Per altre informazioni, vedere [Configurazione di un'origine multimediale.](configuring-a-media-source.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Media Foundation proprietà](media-foundation-properties.md)
</dt> <dt>

[Rete in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




