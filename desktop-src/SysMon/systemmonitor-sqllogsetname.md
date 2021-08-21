---
title: Proprietà SystemMonitor SqlLogSetName
description: Recupera o imposta il nome descrittivo del set di log.
ms.assetid: a4593743-6b70-4f70-8e91-3324a808d97b
keywords:
- Proprietà SqlLogSetName SysMon
- Proprietà SqlLogSetName SysMon , interfaccia SystemMonitor
- Interfaccia SystemMonitor SysMon , proprietà SqlLogSetName
topic_type:
- apiref
api_name:
- SystemMonitor.SqlLogSetName
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce06e396b6a90a46de88d915a0191258da723bef31dfe82f67a20c9507b2939d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118881308"
---
# <a name="systemmonitorsqllogsetname-property"></a>Proprietà SystemMonitor::SqlLogSetName

Recupera o imposta il nome descrittivo del set di log.

## <a name="syntax"></a>Sintassi


```VB
Property SqlLogSetName As String
```



## <a name="property-value"></a>Valore proprietà

Nome descrittivo del set di log, che corrisponde a un singolo file di log contenente dati binari o di testo nel database SQL dati.

## <a name="remarks"></a>Commenti

**Prima di Windows Vista:** Non è possibile modificare questa proprietà se il valore di [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) è impostato su sysmonSqlLog.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**SystemMonitor.SqlDsnName**](systemmonitor-sqllogsetname.md)
</dt> </dl>

 

 





