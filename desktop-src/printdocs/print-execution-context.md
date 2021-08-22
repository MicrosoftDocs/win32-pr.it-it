---
description: Rappresenta il contesto di esecuzione quando viene chiamato GetPrintExecutionData.
ms.assetid: b6c026b2-8519-45d3-9614-b502eec23cde
title: PRINT_EXECUTION_CONTEXT enumerazione (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINT_EXECUTION_CONTEXT
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 78e4afb29b75c0a73799302ddb76e270b18ca2c38cb6325b59ebae5041d5f99e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119033959"
---
# <a name="print_execution_context-enumeration"></a>Enumerazione PRINT \_ EXECUTION \_ CONTEXT

Rappresenta il contesto di esecuzione [**quando viene chiamato GetPrintExecutionData.**](getprintexecutiondata.md)

## <a name="syntax"></a>Sintassi


```C++
typedef enum  { 
  PRINT_EXECUTION_CONTEXT_APPLICATION             = 0,
  PRINT_EXECUTION_CONTEXT_SPOOLER_SERVICE         = 1,
  PRINT_EXECUTION_CONTEXT_SPOOLER_ISOLATION_HOST  = 2,
  PRINT_EXECUTION_CONTEXT_FILTER_PIPELINE         = 3,
  PRINT_EXECUTION_CONTEXT_WOW64                   = 4
} PRINT_EXECUTION_CONTEXT;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="PRINT_EXECUTION_CONTEXT_APPLICATION"></span><span id="print_execution_context_application"></span>**APPLICAZIONE DEL \_ CONTESTO DI ESECUZIONE DELLA \_ \_ STAMPA**
</dt> <dd>

Il chiamante è in esecuzione in un'applicazione.

</dd> <dt>

<span id="PRINT_EXECUTION_CONTEXT_SPOOLER_SERVICE"></span><span id="print_execution_context_spooler_service"></span>**SERVIZIO \_ \_ \_ SPOOLER DEL CONTESTO DI ESECUZIONE DELLA \_ STAMPA**
</dt> <dd>

Il chiamante è in esecuzione nel servizio spooler (spoolsv.exe).

</dd> <dt>

<span id="PRINT_EXECUTION_CONTEXT_SPOOLER_ISOLATION_HOST"></span><span id="print_execution_context_spooler_isolation_host"></span>**\_STAMPARE L'HOST DI \_ ISOLAMENTO DELLO \_ SPOOLER DEL \_ CONTESTO DI \_ ESECUZIONE**
</dt> <dd>

Il chiamante è in esecuzione nell'host di isolamento della stampa (PrintIsolationHost.exe)

</dd> <dt>

<span id="PRINT_EXECUTION_CONTEXT_FILTER_PIPELINE"></span><span id="print_execution_context_filter_pipeline"></span>**STAMPARE LA \_ PIPELINE DI FILTRO DEL CONTESTO DI \_ \_ \_ ESECUZIONE**
</dt> <dd>

Il chiamante è in esecuzione nella pipeline del filtro di stampa (printfilterpipelinesvc.exe)

</dd> <dt>

<span id="PRINT_EXECUTION_CONTEXT_WOW64"></span><span id="print_execution_context_wow64"></span>**CONTESTO \_ DI ESECUZIONE DI STAMPA \_ \_ WOW64**
</dt> <dd>

Il chiamante è in esecuzione in splwow64.exe

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

[**STAMPARE I \_ DATI DI \_ ESECUZIONE**](print-execution-data.md)
</dt> </dl>

 

 




