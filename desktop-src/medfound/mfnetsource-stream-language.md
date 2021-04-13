---
description: Archivia la stringa inviata nell'intestazione del Accept-Language.
ms.assetid: b6ac613c-099b-4415-84ad-c0f8ad5f667b
title: Proprietà MFNETSOURCE_STREAM_LANGUAGE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 200c49d4a14146277c66fbb3389cf1ba6ab13fef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401526"
---
# <a name="mfnetsource_stream_language-property"></a>Proprietà della lingua del \_ flusso MFNETSOURCE \_

Archivia la stringa inviata nell'intestazione del Accept-Language.



Tipo di dati

Tipo PROPVARIANT (VT)

membro PROPVARIANT

**WCHAR \** _

\_LPWSTR VT

_ *pwszVal**



## <a name="remarks"></a>Commenti

La \_ costante del linguaggio del flusso MFNETSOURCE \_ definisce il GUID per la chiave della proprietà. L'identificatore di proprietà (PID) è zero. Per impostare questa proprietà nell'origine di rete, passare un puntatore **IPropertyStore** al resolver di origine. Per altre informazioni, vedere [configurazione di un'origine multimediale](configuring-a-media-source.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                         |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                            |
| Intestazione<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà Media Foundation](media-foundation-properties.md)
</dt> <dt>

[Rete in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




