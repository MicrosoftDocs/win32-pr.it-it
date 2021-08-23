---
description: La struttura PF FOLLOWENTRY definisce un protocollo \_ che Network Monitor aggiunge al set seguente di un parser.
ms.assetid: 931ae70f-8c5e-4b7a-aae6-64a33dac3b23
title: PF_FOLLOWENTRY struttura (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_FOLLOWENTRY
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 8fd7452a4db6318df0d4c23ea405d2cd4afcf6575c7abac34749a66bc88c2084
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063731"
---
# <a name="pf_followentry-structure"></a>Struttura PF \_ FOLLOWENTRY

La **struttura PF \_ FOLLOWENTRY** definisce un protocollo che Network Monitor aggiunge al set seguente di un parser.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _PF_FOLLOWENTRY {
  char szProtocol[MAX_PROTOCOL_NAME_LEN];
} PF_FOLLOWENTRY, *PPF_FOLLOWENTRY;
```



## <a name="members"></a>Members

<dl> <dt>

**szProtocol**
</dt> <dd>

Nome del protocollo.

</dd> </dl>

## <a name="remarks"></a>Commenti

La [struttura PF \_ FOLLOWSET](pf-followset.md) usa una matrice **di strutture PF \_ FOLLOWENTRY.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[PF \_ FOLLOWSET](pf-followset.md)
</dt> </dl>

 

 




