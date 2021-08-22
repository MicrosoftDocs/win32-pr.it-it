---
description: Specifica se un processo di stampa XPS si trova nello spooling o nella fase di rendering.
ms.assetid: 14871d29-59e4-45a2-9697-12550c58396c
title: Enumerazione EPrintXPSJobOperation (Winspool.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EPrintXPSJobOperation
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 44f1f7ed80cd1de071633de37c5f0e91e913841388754a65c0194665bd3084de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971540"
---
# <a name="eprintxpsjoboperation-enumeration"></a>Enumerazione EPrintXPSJobOperation

Specifica se un processo di stampa XPS si trova nello spooling o nella fase di rendering.

## <a name="syntax"></a>Sintassi


```C++
typedef enum tagEPrintXPSJobOperation { 
  kJobProduction,
  kJobConsumption
} EPrintXPSJobOperation;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="kJobProduction"></span><span id="kjobproduction"></span><span id="KJOBPRODUCTION"></span>**kJobProduction**
</dt> <dd>

Lo spooling del processo XPS è in esecuzione.

</dd> <dt>

<span id="kJobConsumption"></span><span id="kjobconsumption"></span><span id="KJOBCONSUMPTION"></span>**kJobConsumption**
</dt> <dd>

Il processo XPS esegue il rendering.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa enumerazione viene usata principalmente come parametro per la [**funzione ReportJobProcessingProgress.**](reportjobprocessingprogress.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                            |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool.h (include Windows.h)</dt> </dl> |



 

 




