---
description: La struttura del TRIGGER indica un'azione che deve essere eseguita dal driver a un'ora specificata.
ms.assetid: 63541796-b0d8-456c-8544-697fedbe05f7
title: Struttura TRIGGER (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TRIGGER
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: d9b385557e3c34bdf75f2bf959d4e5e3e47e0750
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315886"
---
# <a name="trigger-structure"></a>Struttura TRIGGER

La struttura del **trigger** indica un'azione che deve essere eseguita dal driver a un'ora specificata.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _TRIGGER {
  BOOL         TriggerActive;
  BYTE         TriggerType;
  BYTE         TriggerAction;
  DWORD        TriggerFlags;
  PATTERNMATCH TriggerPatternMatch;
  DWORD        TriggerBufferSize;
  DWORD        Reserved;
} TRIGGER, *LPTRIGGER;
```



## <a name="members"></a>Members

<dl> <dt>

**TriggerActive**
</dt> <dd>

Valore booleano che determina se il trigger deve prestare attenzione al driver.

</dd> <dt>

**TriggerType**
</dt> <dd>

Codice op del trigger.

</dd> <dt>

**TriggerAction**
</dt> <dd>

Azione che il trigger deve eseguire se viene attivato.

</dd> <dt>

**TriggerFlags**
</dt> <dd>

Flag del trigger.

</dd> <dt>

**TriggerPatternMatch**
</dt> <dd>

Modello di trigger corrispondente.

</dd> <dt>

**TriggerBufferSize**
</dt> <dd>

Dimensioni del buffer di trigger.

</dd> <dt>

**Reserved**
</dt> <dd>

Riservato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




