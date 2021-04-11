---
title: Proprietà SystemMonitor. Counters
description: Recupera i contatori che contengono una raccolta di oggetti CounterItem.
ms.assetid: eab21e1f-c8fb-474c-83e3-5ef56483d525
keywords:
- Proprietà dei contatori SysMon
- Proprietà Counters SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, Proprietà Counters
topic_type:
- apiref
api_name:
- SystemMonitor.Counters
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c4e09cc797c09033e90ba4d584ee63336a52cab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119978"
---
# <a name="systemmonitorcounters-property"></a>Proprietà SystemMonitor. Counters

Recupera i **contatori** che contengono una raccolta di oggetti [**CounterItem**](counteritem.md) .

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
Property Counters As ICounters
```



## <a name="property-value"></a>Valore proprietà

Oggetto **contatori** che contiene una raccolta di oggetti [**CounterItem**](counteritem.md) .

## <a name="remarks"></a>Commenti

Si tratta della proprietà predefinita dell'oggetto [**SystemMonitor**](systemmonitor.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> </dl>

 

 





