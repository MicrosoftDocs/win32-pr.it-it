---
description: La \_ struttura BLOB KEYSVC definisce un BLOB del servizio Key. Questa struttura viene utilizzata dalla funzione RKeyPFXInstall.
ms.assetid: 255b5fab-6271-4d3f-9c56-a63278b8b104
title: Struttura KEYSVC_BLOB (Rkeysvcc. h)
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
ms.openlocfilehash: 801be5f5a0d431f488da6e13e1f3082d147c5974
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319353"
---
# <a name="keysvc_blob-structure"></a>\_Struttura BLOB KEYSVC

La **struttura \_ BLOB KEYSVC** definisce un BLOB del servizio Key. Questa struttura viene utilizzata dalla funzione [**RKeyPFXInstall**](rkeypfxinstall.md) .

## <a name="syntax"></a>Sintassi


```C++
typedef struct _KEYSVC_BLOB {
  ULONG cb;
  BYTE  *pb;
} KEYSVC_BLOB, *PKEYSVC_BLOB;
```



## <a name="members"></a>Members

<dl> <dt>

**CB**
</dt> <dd>

Valore **ULONG** che specifica la dimensione, in byte, del **PB**.

</dd> <dt>

**PB**
</dt> <dd>

Puntatore a un **byte** che contiene il BLOB, in formato [*PKCS \# 12*](../secgloss/p-gly.md) .

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

[**\_stringa Unicode \_ KEYSVC**](keysvc-unicode-string.md)
</dt> </dl>

 

 
