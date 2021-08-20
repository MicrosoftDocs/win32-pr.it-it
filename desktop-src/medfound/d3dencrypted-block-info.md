---
description: Specifica i byte crittografati in una superficie video protetta.
ms.assetid: 076f4f00-e86b-47e2-80dd-4d7434200138
title: D3DENCRYPTED_BLOCK_INFO struttura (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DENCRYPTED_BLOCK_INFO
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 94027dac3956376e32ad10cf7c1b600d9c65f3918e2781ab9da96d4d3891f43b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117879725"
---
# <a name="d3dencrypted_block_info-structure"></a>Struttura D3DENCRYPTED \_ BLOCK \_ INFO

Specifica i byte crittografati in una superficie video protetta.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _D3DENCRYPTED_BLOCK_INFO {
  UINT NumEncryptedBytesAtBeginning;
  UINT NumBytesInSkipPattern;
  UINT NumBytesInEncryptPattern;
} D3DENCRYPTED_BLOCK_INFO;
```



## <a name="members"></a>Members

<dl> <dt>

**NumEncryptedBytesAtBeginning**
</dt> <dd>

Numero di byte crittografati all'inizio del buffer.

</dd> <dt>

**NumBytesInSkipPattern**
</dt> <dd>

Numero di byte ignorati dopo i primi **byte NumEncryptedBytesAtBeginning** e quindi dopo ogni blocco di **byte NumBytesInEncryptPattern.** I byte ignorati non vengono crittografati.

</dd> <dt>

**NumBytesInEncryptPattern**
</dt> <dd>

Numero di byte crittografati dopo ogni blocco di byte ignorati.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                                 |
| Intestazione<br/>                   | <dl> <dt>D3d9types.h (includere D3d9.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture video Direct3D](direct3d-video-structures.md)
</dt> </dl>

 

 




