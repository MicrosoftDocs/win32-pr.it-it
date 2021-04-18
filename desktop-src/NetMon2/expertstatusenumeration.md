---
description: L'enumerazione EXPERTSTATUSENUMERATION contiene valori di stato. Viene usato dal membro di stato della struttura EXPERTSTATUS e dal parametro status in ExpertIndicateStatus.
ms.assetid: 217dce5a-3698-45a9-bb13-8379bcbdd762
title: Enumerazione EXPERTSTATUSENUMERATION (Netmon. h)
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
ms.openlocfilehash: b634d4dad2e024c3c995216b5af7de23b14b7da0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305942"
---
# <a name="expertstatusenumeration-enumeration"></a>Enumerazione EXPERTSTATUSENUMERATION

L'enumerazione **EXPERTSTATUSENUMERATION** contiene valori di stato. Viene usato dal membro di **stato** della struttura [EXPERTSTATUS](expertstatus.md) e dal parametro *status* in [ExpertIndicateStatus](expertindicatestatus.md).

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

<span id="EXPERTSTATUS_INACTIVE"></span><span id="expertstatus_inactive"></span>**EXPERTSTATUS \_ INattivo**
</dt> <dd>

L'esperto non è mai stato avviato.

</dd> <dt>

<span id="EXPERTSTATUS_STARTING"></span><span id="expertstatus_starting"></span>**avvio di EXPERTSTATUS \_**
</dt> <dd>

L'esperto si sta avviando.

</dd> <dt>

<span id="EXPERTSTATUS_RUNNING"></span><span id="expertstatus_running"></span>**EXPERTSTATUS \_ in esecuzione**
</dt> <dd>

L'esperto viene eseguito normalmente.

</dd> <dt>

<span id="EXPERTSTATUS_PROBLEM"></span><span id="expertstatus_problem"></span>**\_problema EXPERTSTATUS**
</dt> <dd>

Un problema specificato nello *stato secondario* ha interrotto l'esperto.

</dd> <dt>

<span id="EXPERTSTATUS_ABORTED"></span><span id="expertstatus_aborted"></span>**EXPERTSTATUS \_ interrotto**
</dt> <dd>

Network Monitor arrestato l'esperto.

</dd> <dt>

<span id="EXPERTSTATUS_DONE"></span><span id="expertstatus_done"></span>**EXPERTSTATUS \_ completato**
</dt> <dd>

L'esperto è stato completato correttamente.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                          |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



 

 




