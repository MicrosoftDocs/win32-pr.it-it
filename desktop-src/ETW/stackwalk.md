---
description: Questa classe è la classe padre per gli eventi di traccia dello stack.
ms.assetid: 3c0ff01b-fb37-4931-9484-ff8048abca66
title: Classe StackWalk
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StackWalk
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2ad873815cb5cea40c1a9d2f694eca8d0e90d11b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977623"
---
# <a name="stackwalk-class"></a>Classe StackWalk

Questa classe è la classe padre per gli eventi di traccia dello stack.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Guid("{def2fe46-7bd6-4b80-bd94-f57fe20d0ce3}")]
class StackWalk : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Members

La classe **StackWalk** non definisce membri.

## <a name="remarks"></a>Commenti

Per abilitare la traccia dello stack degli eventi del kernel, chiamare la funzione [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) e specificare gli eventi del kernel e i tipi per i quali si desidera acquisire la traccia dello stack. Per abilitare la traccia dello stack per altri eventi, impostare il membro **EnableProperty** di [**Abilita traccia \_ \_ parametri di traccia**](/windows/win32/api/evntrace/ns-evntrace-enable_trace_parameters) per abilitare la **\_ \_ \_ \_ traccia dello stack della proprietà**.

Usare il tipo di evento seguente per identificare l'evento effettivo quando si utilizzano gli eventi.



| Tipo di evento           | Descrizione                                                                                                           |
|----------------------|-----------------------------------------------------------------------------------------------------------------------|
| Valore del tipo di evento, 32 | Evento di traccia dello stack. La classe MOF dell' [**\_ evento StackWalk**](stackwalk-event.md) definisce i dati dell'evento per questo evento. |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>              |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/> |



 

 
