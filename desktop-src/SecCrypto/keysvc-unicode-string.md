---
description: La \_ \_ struttura di stringhe Unicode KEYSVC definisce una stringa Unicode e una lunghezza massima per la stringa. Questa struttura viene utilizzata dalla funzione RKeyPFXInstall.
ms.assetid: 12142543-5c53-4638-9fd7-f523594142c8
title: Struttura KEYSVC_UNICODE_STRING (Rkeysvcc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KEYSVC_UNICODE_STRING
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 5424fa103b2bbbadd735dbda0bb92f9dea21787b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319352"
---
# <a name="keysvc_unicode_string-structure"></a>\_Struttura di \_ stringhe Unicode KEYSVC

La struttura di **\_ \_ stringhe Unicode KEYSVC** definisce una stringa [*Unicode*](../secgloss/u-gly.md) e una lunghezza massima per la stringa. Questa struttura viene utilizzata dalla funzione [**RKeyPFXInstall**](rkeypfxinstall.md) .

## <a name="syntax"></a>Sintassi


```C++
typedef struct _KEYSVC_UNICODE_STRING {
  USHORT Length;
  USHORT MaximumLength;
  USHORT *Buffer;
} KEYSVC_UNICODE_STRING, *PKEYSVC_UNICODE_STRING;
```



## <a name="members"></a>Members

<dl> <dt>

**Length**
</dt> <dd>

Valore **ushort** che specifica la lunghezza, in byte, utilizzata per il **buffer**.

</dd> <dt>

**MaximumLength**
</dt> <dd>

Valore **ushort** che specifica la lunghezza massima, in byte, consentita per il **buffer**.

</dd> <dt>

**Buffer**
</dt> <dd>

Puntatore a un **ushort** che rappresenta la stringa Unicode.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Rkeysvcc. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RKeyPFXInstall**](rkeypfxinstall.md)
</dt> <dt>

[**\_BLOB KEYSVC**](keysvc-blob.md)
</dt> </dl>

 

 
