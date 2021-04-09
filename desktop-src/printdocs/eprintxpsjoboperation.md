---
description: Specifica se un processo di stampa XPS si trova nella fase di spooling o di rendering.
ms.assetid: 14871d29-59e4-45a2-9697-12550c58396c
title: Enumerazione EPrintXPSJobOperation (winspool. h)
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
ms.openlocfilehash: 917993be2af6e7a78afaec1ad4749dadcaebecba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756392"
---
# <a name="eprintxpsjoboperation-enumeration"></a>Enumerazione EPrintXPSJobOperation

Specifica se un processo di stampa XPS si trova nella fase di spooling o di rendering.

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

Il processo XPS sta effettuando lo spooling.

</dd> <dt>

<span id="kJobConsumption"></span><span id="kjobconsumption"></span><span id="KJOBCONSUMPTION"></span>**kJobConsumption**
</dt> <dd>

Viene eseguito il rendering del processo XPS.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa enumerazione viene utilizzata principalmente come parametro per la funzione [**ReportJobProcessingProgress**](reportjobprocessingprogress.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                            |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winspool. h (include Windows. h)</dt> </dl> |



 

 




