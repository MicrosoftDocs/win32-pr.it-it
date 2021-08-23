---
description: La struttura KEYSVC \_ UNICODE STRING definisce una stringa Unicode e una lunghezza massima per la \_ stringa. Questa struttura viene usata dalla funzione RKeyPFXInstall.
ms.assetid: 12142543-5c53-4638-9fd7-f523594142c8
title: KEYSVC_UNICODE_STRING struttura (Rkeysvcc.h)
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
ms.openlocfilehash: ac1e82ab481b9844e8a21940112c6014a19f111cab53db2974c488dff0982027
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119622331"
---
# <a name="keysvc_unicode_string-structure"></a>Struttura STRINGA UNICODE KEYSVC \_ \_

La **struttura KEYSVC \_ UNICODE \_ STRING** definisce una stringa [*Unicode*](../secgloss/u-gly.md) e una lunghezza massima per la stringa. Questa struttura viene usata dalla [**funzione RKeyPFXInstall.**](rkeypfxinstall.md)

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

Valore **USHORT** che specifica la lunghezza, in byte, utilizzata per **buffer**.

</dd> <dt>

**MaximumLength**
</dt> <dd>

Valore **USHORT** che specifica la lunghezza massima, in byte, consentita per **Buffer**.

</dd> <dt>

**Buffer**
</dt> <dd>

Puntatore a un **USHORT che** rappresenta la stringa Unicode.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Rkeysvcc.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RKeyPFXInstall**](rkeypfxinstall.md)
</dt> <dt>

[**KEYSVC \_ BLOB**](keysvc-blob.md)
</dt> </dl>

 

 
