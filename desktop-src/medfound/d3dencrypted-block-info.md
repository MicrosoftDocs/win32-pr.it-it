---
description: Specifica i byte crittografati in una superficie video protetta.
ms.assetid: 076f4f00-e86b-47e2-80dd-4d7434200138
title: Struttura D3DENCRYPTED_BLOCK_INFO (D3d9types. h)
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
ms.openlocfilehash: 21864dcc41ce86f139361af4357810137acf7f06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127918"
---
# <a name="d3dencrypted_block_info-structure"></a>Struttura delle informazioni sul \_ blocco D3DENCRYPTED \_

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

Il numero di byte che vengono ignorati dopo i primi **NumEncryptedBytesAtBeginning** byte e quindi dopo ogni blocco di **NumBytesInEncryptPattern** byte. I byte ignorati non sono crittografati.

</dd> <dt>

**NumBytesInEncryptPattern**
</dt> <dd>

Numero di byte crittografati dopo ogni blocco di byte ignorati.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                              |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                                 |
| Intestazione<br/>                   | <dl> <dt>D3d9types. h (include d3d9. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture video Direct3D](direct3d-video-structures.md)
</dt> </dl>

 

 




