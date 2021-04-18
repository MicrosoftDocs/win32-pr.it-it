---
description: La \_ struttura PF HANDOFFSET definisce i protocolli che vengono consegnati al parser o i protocolli a cui il parser passa.
ms.assetid: 2fda399d-a09e-47b4-bb2e-95996de9f950
title: Struttura PF_HANDOFFSET (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_HANDOFFSET
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 1b5dc9620f3b1860b27af973432aa4218c05b63b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314751"
---
# <a name="pf_handoffset-structure"></a>\_Struttura PF HANDOFFSET

La struttura **PF \_ HANDOFFSET** definisce i protocolli che vengono consegnati al parser o i protocolli a cui il parser passa.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _PF_HANDOFFSET {
  DWORD           nEntries;
  PF_HANDOFFENTRY Entry[];
} PF_HANDOFFSET, *PPF_HANDOFFSET;
```



## <a name="members"></a>Members

<dl> <dt>

**nEntries**
</dt> <dd>

Numero di protocolli.

</dd> <dt>

**Voce**
</dt> <dd>

Matrice di strutture [PF \_ HANDOFFENTRY](pf-handoffentry.md) che definiscono ogni protocollo.

</dd> </dl>

## <a name="remarks"></a>Commenti

La struttura [PF \_ PARSERINFO](pf-parserinfo.md) usa la struttura **PF \_ HANDOFFSET** per elencare quanto segue:

-   Protocolli passati al parser.
-   Protocolli a cui il parser passa.

È necessario allocare la struttura **PF \_ HANDOFFSET** usando **HeapAlloc**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[PF \_ PARSERINFO](pf-parserinfo.md)
</dt> <dt>

[PF \_ HANDOFFENTRY](pf-handoffentry.md)
</dt> </dl>

 

 




