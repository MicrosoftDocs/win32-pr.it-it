---
title: Proprietà SystemMonitor. DisplayType
description: Recupera o imposta il tipo di grafico utilizzato per rappresentare i dati del contatore delle prestazioni.
ms.assetid: a04545b1-920e-4fb3-909b-dc47e1374629
keywords:
- Proprietà DisplayType SysMon
- Proprietà DisplayType SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, proprietà DisplayType
topic_type:
- apiref
api_name:
- SystemMonitor.DisplayType
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99c0e96ff0da57ef9e5f580063dc4f693d672e15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119874"
---
# <a name="systemmonitordisplaytype-property"></a>Proprietà SystemMonitor. DisplayType

Recupera o imposta il tipo di grafico utilizzato per rappresentare i dati del contatore delle prestazioni.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
Property DisplayType As DisplayTypeConstants
```



## <a name="property-value"></a>Valore proprietà

Tipo di grafico utilizzato per rappresentare i dati del contatore delle prestazioni. Per i valori possibili, vedere [**DisplayTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants).

## <a name="exceptions"></a>Eccezioni



| Tipo di eccezione               | Condizione                                         |
|------------------------------|---------------------------------------------------|
| **System. ArgumentException** | Il valore del grafico o del report specificato non è valido. |



 

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

 

 





