---
description: Indica lo stato corrente di un esperto in esecuzione.
ms.assetid: 49107459-599c-4710-8935-4b2c789081de
title: Struttura EXPERTSTATUS (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTSTATUS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: a9e201b692bb82c78f88a35f22f2688d096f1771
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525158"
---
# <a name="expertstatus-structure"></a>Struttura EXPERTSTATUS

La struttura **EXPERTSTATUS** indica lo stato corrente di un esperto in esecuzione.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  EXPERTSTATUSENUMERATION Status;
  DWORD                   SubStatus;
  DWORD                   PercentDone;
  DWORD                   Frame;
  char                    szStatusText[EXPERTSTRINGLENGTH];
} EXPERTSTATUS, *PEXPERTSTATUS;
```



## <a name="members"></a>Members

<dl> <dt>

**Status**
</dt> <dd>

Valore di stato esperto corrente definito dall'enumerazione [**EXPERTSTATUSENUMERATION**](expertstatusenumeration.md) .

</dd> <dt>

**Stato secondario**
</dt> <dd>

Valore di stato secondario.

</dd> <dt>

**PercentDone**
</dt> <dd>

Percentuale di completamento dell'analisi di esperti dei dati di rete.

</dd> <dt>

**Frame**
</dt> <dd>

Numero di frame.

</dd> <dt>

**szStatusText**
</dt> <dd>

Testo che descrive lo stato dell'esperto.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




