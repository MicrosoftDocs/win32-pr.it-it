---
title: Proprietà SqlLogSetName di SystemMonitor
description: Recupera o imposta il nome descrittivo del set di log.
ms.assetid: a4593743-6b70-4f70-8e91-3324a808d97b
keywords:
- Proprietà SqlLogSetName SysMon
- Proprietà SqlLogSetName SysMon, interfaccia SystemMonitor
- Interfaccia SystemMonitor SysMon, proprietà SqlLogSetName
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
ms.openlocfilehash: be20ccc561eb3e9292b4a95dcc654ed7bac00ba7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104047819"
---
# <a name="systemmonitorsqllogsetname-property"></a>Proprietà SystemMonitor:: SqlLogSetName

Recupera o imposta il nome descrittivo del set di log.

## <a name="syntax"></a>Sintassi


```VB
Property SqlLogSetName As String
```



## <a name="property-value"></a>Valore proprietà

Nome descrittivo del set di log, che corrisponde a un singolo file di log contenente dati binari o di testo nel database SQL.

## <a name="remarks"></a>Commenti

**Prima di Windows Vista:** Non è possibile modificare questa proprietà se il valore di [**SystemMonitor. DataSourceType**](systemmonitor-datasourcetype.md) è impostato su sysmonSqlLog.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> <dt>

[**SystemMonitor. SqlDsnName**](systemmonitor-sqllogsetname.md)
</dt> </dl>

 

 





