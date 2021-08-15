---
description: La struttura TRIGGER indica un'azione che il driver deve eseguire in un momento specificato.
ms.assetid: 63541796-b0d8-456c-8544-697fedbe05f7
title: Struttura TRIGGER (Netmon.h)
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
ms.openlocfilehash: 99404c8e9fc48e0ab85b956dd84af39b11eb87b22c87b4f9a232bd5b72d32143
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118363019"
---
# <a name="trigger-structure"></a>Struttura TRIGGER

La **struttura TRIGGER** indica un'azione che il driver deve eseguire in un momento specificato.

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

Codice operativo del trigger.

</dd> <dt>

**Triggeraction**
</dt> <dd>

Azione che il trigger deve eseguire se viene attivato.

</dd> <dt>

**TriggerFlags**
</dt> <dd>

Flag di trigger.

</dd> <dt>

**TriggerPatternMatch**
</dt> <dd>

Corrispondenza del modello di trigger.

</dd> <dt>

**TriggerBufferSize**
</dt> <dd>

Dimensioni del buffer del trigger.

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
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




