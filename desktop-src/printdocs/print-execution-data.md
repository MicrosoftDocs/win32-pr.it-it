---
description: Contiene il contesto di esecuzione del driver della stampante che chiama GetPrintExecutionData.
ms.assetid: 1fd25ed9-6f28-48f9-8132-d48fffc956ec
title: PRINT_EXECUTION_DATA (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINT_EXECUTION_DATA
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: e67b43089c275baf59295f15e84d9bf38d1a3a5ff6e2adfaf2d270b02e2ad967
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119447141"
---
# <a name="print_execution_data-structure"></a>Struttura PRINT \_ EXECUTION \_ DATA

Contiene il contesto di esecuzione del driver della stampante che [**chiama GetPrintExecutionData.**](getprintexecutiondata.md)

## <a name="syntax"></a>Sintassi


```C++
typedef struct _PRINT_EXECUTION_DATA {
  PRINT_EXECUTION_CONTEXT  context;
  DWORD                    clientAppPID;
} PRINT_EXECUTION_DATA;
```



## <a name="members"></a>Members

<dl> <dt>

**context**
</dt> <dd>

Valore [**PRINT \_ EXECUTION \_ CONTEXT**](print-execution-context.md) che rappresenta il contesto di esecuzione corrente del driver della stampante.

</dd> <dt>

**clientAppPID**
</dt> <dd>

Se il valore di **context** è **PRINT EXECUTION CONTEXT \_ \_ \_ WOW64**, **clientAppPID** identifica l'applicazione client per conto del quale il processo splwow64.exe ha caricato il driver della stampante. Se il valore di **context** non è **PRINT EXECUTION CONTEXT \_ \_ \_ WOW64,** **clientAppPID** è zero.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                                |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                                   |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (includere Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GetPrintExecutionData**](getprintexecutiondata.md)
</dt> <dt>

[**STAMPARE IL \_ CONTESTO DI \_ ESECUZIONE**](print-execution-context.md)
</dt> </dl>

 

 




