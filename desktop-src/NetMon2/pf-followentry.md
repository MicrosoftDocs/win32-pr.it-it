---
description: La \_ struttura PF FOLLOWENTRY definisce un protocollo che Network Monitor aggiunge al set seguente di un parser.
ms.assetid: 931ae70f-8c5e-4b7a-aae6-64a33dac3b23
title: Struttura PF_FOLLOWENTRY (Netmon. h)
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
ms.openlocfilehash: f93ec4784fc8d0f92f68fdff3914e230ffd3cdce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882906"
---
# <a name="pf_followentry-structure"></a>\_Struttura PF FOLLOWENTRY

La struttura **PF \_ FOLLOWENTRY** definisce un protocollo che Network Monitor aggiunge al set seguente di un parser.

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

La struttura [PF \_ follower](pf-followset.md) usa una matrice di strutture **PF \_ FOLLOWENTRY** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[PF \_](pf-followset.md)
</dt> </dl>

 

 




