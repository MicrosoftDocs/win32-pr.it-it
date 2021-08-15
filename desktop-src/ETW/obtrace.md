---
description: Rappresenta la classe padre da cui vengono derivate tutte le classi di traccia eventi di gestione oggetti.
ms.assetid: 07cfc4a2-c665-4080-bc4b-fe9ec7191fdc
title: Classe ObTrace
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObTrace
api_type:
- NA
api_location: ''
ms.openlocfilehash: 8cf30fe0c7b028c819477bcf0c66c2b674fc588286916be1cd1fd1a6b207770d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119328751"
---
# <a name="obtrace-class"></a>Classe ObTrace

Rappresenta la classe padre da cui vengono derivate tutte le classi di traccia eventi di gestione oggetti.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[DisplayName("Object"), Dynamic, EventVersion(2), Guid("{89497f50-effe-4440-8cf2-ce6b1cdcaca7}")]
class ObTrace : MSNT_SystemTrace
{
};
```

## <a name="members"></a>Members

La **classe ObTrace** non definisce membri.

## <a name="remarks"></a>Commenti

Per abilitare la traccia degli eventi di Gestione oggetti, chiamare la funzione [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) con il parametro *InformationClass* uguale al valore di enumerazione [**TRACE INFO \_ \_ CLASS**](/windows/win32/api/evntrace/ne-evntrace-trace_query_info_class) **TraceSystemTraceEnableFlagsInfo** e al membro **EnableFlags** della struttura EVENT [**TRACE \_ \_ PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) uguale a **PERF OB \_ \_ HANDLE** (0x80000040).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                             |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                   |
| MOF<br/>                      | <dl> <dt>Wmicore.mof</dt> </dl> |



 

 
