---
title: Proprietà SystemMonitor. ReportValueType
description: Recupera o imposta un valore che determina se l'istogramma e le visualizzazioni del rapporto disegnano l'ultimo valore campionato durante l'intervallo di campionamento o un valore calcolato dal campionamento, ad esempio il valore medio o minimo del contatore.
ms.assetid: add75744-c3ab-48ab-b567-28a072facfdd
keywords:
- Proprietà ReportValueType SysMon
- Proprietà ReportValueType SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, proprietà ReportValueType
topic_type:
- apiref
api_name:
- SystemMonitor.ReportValueType
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffc340516f1d99bb77dcc5a31c03eb189d2d70a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964178"
---
# <a name="systemmonitorreportvaluetype-property"></a>Proprietà SystemMonitor. ReportValueType

Recupera o imposta un valore che determina se l'istogramma e le visualizzazioni del rapporto disegnano l'ultimo valore campionato durante l'intervallo di campionamento o un valore calcolato dal campionamento, ad esempio il valore medio o minimo del contatore.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
Property ReportValueType As ReportValueTypeConstants
```



## <a name="property-value"></a>Valore proprietà

Determina se l'istogramma e le visualizzazioni del report disegnano l'ultimo valore campionato durante l'intervallo di campionamento o un valore calcolato dall'intervallo di campionamento. Per i valori possibili, vedere [**ReportValueTypeConstants**](/windows/win32/api/isysmon/ne-isysmon-reportvaluetypeconstants).

## <a name="remarks"></a>Commenti

SYSMON ignora questo valore e USA [**ReportValueTypeConstants.sysmonDefaultValue**](/windows/win32/api/isysmon/ne-isysmon-reportvaluetypeconstants) se [**SystemMonitor. DisplayType**](systemmonitor-displaytype.md) non è [**DisplayTypeConstants.sysmonHistogram**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants) o **DisplayTypeConstants.sysmonReport**.

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

 

 





