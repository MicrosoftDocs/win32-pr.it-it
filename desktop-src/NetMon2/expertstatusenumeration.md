---
description: L'enumerazione EXPERTSTATUSENUMERATION contiene valori di stato. Viene usato dal membro Status della struttura EXPERTSTATUS e dal parametro Status in ExpertIndicateStatus.
ms.assetid: 217dce5a-3698-45a9-bb13-8379bcbdd762
title: Enumerazione EXPERTSTATUSENUMERATION (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERT_STATUS_ENUMERATION
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: ee0729deab566717457f03af27a7e31de8cdf8f1b78f9a5f97b3c3ff406641fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117795794"
---
# <a name="expertstatusenumeration-enumeration"></a>Enumerazione EXPERTSTATUSENUMERATION

**L'enumerazione EXPERTSTATUSENUMERATION** contiene valori di stato. Viene usato dal membro **Status della** struttura [EXPERTSTATUS](expertstatus.md) e dal *parametro Status* in [ExpertIndicateStatus.](expertindicatestatus.md)

## <a name="syntax"></a>Sintassi


```C++
typedef enum  { 
  EXPERTSTATUS_INACTIVE  = 0,
  EXPERTSTATUS_STARTING,
  EXPERTSTATUS_RUNNING,
  EXPERTSTATUS_PROBLEM,
  EXPERTSTATUS_ABORTED,
  EXPERTSTATUS_DONE
} EXPERT_STATUS_ENUMERATION;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="EXPERTSTATUS_INACTIVE"></span><span id="expertstatus_inactive"></span>**EXPERTSTATUS \_ INACTIVE**
</dt> <dd>

L'esperto non è mai iniziato.

</dd> <dt>

<span id="EXPERTSTATUS_STARTING"></span><span id="expertstatus_starting"></span>**AVVIO \_ DI EXPERTSTATUS**
</dt> <dd>

L'esperto sta iniziando.

</dd> <dt>

<span id="EXPERTSTATUS_RUNNING"></span><span id="expertstatus_running"></span>**EXPERTSTATUS \_ IN ESECUZIONE**
</dt> <dd>

L'esperto funziona normalmente.

</dd> <dt>

<span id="EXPERTSTATUS_PROBLEM"></span><span id="expertstatus_problem"></span>**PROBLEMA DI STATO \_ ESPERTO**
</dt> <dd>

Un problema specificato in *SubStatus ha arrestato* l'esperto.

</dd> <dt>

<span id="EXPERTSTATUS_ABORTED"></span><span id="expertstatus_aborted"></span>**EXPERTSTATUS \_ ABORTED**
</dt> <dd>

Network Monitor ha arrestato l'esperto.

</dd> <dt>

<span id="EXPERTSTATUS_DONE"></span><span id="expertstatus_done"></span>**EXPERTSTATUS \_ DONE**
</dt> <dd>

L'esperto è stato completato correttamente.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



 

 




