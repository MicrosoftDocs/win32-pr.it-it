---
description: Associa un nome di gruppo e il relativo handle.
ms.assetid: 76f3fe37-cf85-42ab-8f9e-3ab2c6053dcd
title: Struttura GROUPINFO (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GROUPINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 5152b0a621a34e49d6f1024a81b7e91aed94a06b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305891"
---
# <a name="groupinfo-structure"></a>Struttura GROUPINFO

La struttura **GROUPINFO** associa un nome di gruppo e il relativo handle.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  char   szGroupName[EXPERTGROUPNAMELENGTH+1];
  HGROUP hGroup;
} GROUPINFO, *PGROUPINFO;
```



## <a name="members"></a>Members

<dl> <dt>

**szGroupName**
</dt> <dd>

Valore incrementato di una matrice nella struttura **GroupName** .

</dd> <dt>

**hGroup**
</dt> <dd>

Handle per un gruppo.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




