---
description: La struttura BLOB KEYSVC \_ definisce un BLOB del servizio chiave. Questa struttura viene usata dalla funzione RKeyPFXInstall.
ms.assetid: 255b5fab-6271-4d3f-9c56-a63278b8b104
title: KEYSVC_BLOB (Rkeysvcc.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KEYSVC_BLOB
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 7e71a090558b31444c550146a2cb99f062080db9b80e7d69561ff891b93262b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992971"
---
# <a name="keysvc_blob-structure"></a>Struttura BLOB \_ KEYSVC

La **struttura \_ BLOB KEYSVC** definisce un BLOB del servizio chiave. Questa struttura viene usata dalla [**funzione RKeyPFXInstall.**](rkeypfxinstall.md)

## <a name="syntax"></a>Sintassi


```C++
typedef struct _KEYSVC_BLOB {
  ULONG cb;
  BYTE  *pb;
} KEYSVC_BLOB, *PKEYSVC_BLOB;
```



## <a name="members"></a>Members

<dl> <dt>

**Cb**
</dt> <dd>

Valore **ULONG** che specifica la dimensione, in byte, di **pb**.

</dd> <dt>

**Pb**
</dt> <dd>

Puntatore a un **byte** che contiene il BLOB, in [*formato PKCS \# 12.*](../secgloss/p-gly.md)

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                             |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Rkeysvcc.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RKeyPFXInstall**](rkeypfxinstall.md)
</dt> <dt>

[**STRINGA UNICODE KEYSVC \_ \_**](keysvc-unicode-string.md)
</dt> </dl>

 

 
