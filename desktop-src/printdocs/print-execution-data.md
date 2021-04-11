---
description: Contiene il contesto di esecuzione del driver della stampante che chiama GetPrintExecutionData.
ms.assetid: 1fd25ed9-6f28-48f9-8132-d48fffc956ec
title: Struttura PRINT_EXECUTION_DATA (winspool. h)
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
ms.openlocfilehash: 0e33f77a3140c62a1f472fc27948ec26a7ecf3ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232895"
---
# <a name="print_execution_data-structure"></a>\_ \_ Struttura dei dati di esecuzione di stampa

Contiene il contesto di esecuzione del driver della stampante che chiama [**GetPrintExecutionData**](getprintexecutiondata.md).

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

Valore [**del \_ \_ contesto di esecuzione di stampa**](print-execution-context.md) che rappresenta il contesto di esecuzione corrente del driver della stampante.

</dd> <dt>

**clientAppPID**
</dt> <dd>

Se il valore di **context** è **il \_ contesto di esecuzione di stampa \_ \_ WOW64**, **clientAppPID** identifica l'applicazione client per conto del quale il splwow64.exe processo ha caricato il driver della stampante. Se il valore di **context** non è **il \_ contesto di esecuzione di stampa \_ \_ WOW64**, **clientAppPID** è zero.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                                |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                                   |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**GetPrintExecutionData**](getprintexecutiondata.md)
</dt> <dt>

[**\_contesto di esecuzione di stampa \_**](print-execution-context.md)
</dt> </dl>

 

 




