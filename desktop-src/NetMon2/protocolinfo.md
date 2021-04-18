---
description: La struttura PROTOCOLINFO descrive un protocollo.
ms.assetid: 7f936c93-a942-4591-9abc-59872df0964e
title: Struttura PROTOCOLINFO (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROTOCOLINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: ed1410148a72c57b860fdfdaee447dcca505d99c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315452"
---
# <a name="protocolinfo-structure"></a>Struttura PROTOCOLINFO

La struttura **PROTOCOLINFO** descrive un protocollo.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _PROTOCOLINFO {
  DWORD              ProtocolID;
  LPPROPERTYDATABASE PropertyDatabase;
  BYTE               ProtocolName[16];
  BYTE               HelpFile[16];
  BYTE               Comment[128];
} PROTOCOLINFO, *LPPROTOCOLINFO;
```



## <a name="members"></a>Members

<dl> <dt>

**ProtocolID**
</dt> <dd>

Identificatore di protocollo assegnato dal sistema della sessione di esecuzione specificata.

</dd> <dt>

**PropertyDatabase**
</dt> <dd>

Database di proprietà del protocollo specificato.

</dd> <dt>

**ProtocolName**
</dt> <dd>

Nome del protocollo abbreviato.

</dd> <dt>

**HelpFile**
</dt> <dd>

Nome del file della guida facoltativo associato al protocollo.

</dd> <dt>

**Commento**
</dt> <dd>

Commento che descrive il protocollo.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




