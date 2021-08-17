---
title: SystemMonitor.ReportValueType - proprietà
description: Recupera o imposta un valore che determina se le visualizzazioni Istogramma e Report tracciano l'ultimo valore campionato durante l'intervallo di campionamento o un valore calcolato dal campionamento, ad esempio il valore medio o minimo del contatore.
ms.assetid: add75744-c3ab-48ab-b567-28a072facfdd
keywords:
- Proprietà ReportValueType SysMon
- Proprietà ReportValueType SysMon , classe SystemMonitor
- Classe SystemMonitor SysMon , proprietà ReportValueType
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
ms.openlocfilehash: 95282c48ac30b13af07c124ea21f36f91c7ae658b10d290a109fdd1dcc7a5ee5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117955009"
---
# <a name="systemmonitorreportvaluetype-property"></a>SystemMonitor.ReportValueType - proprietà

Recupera o imposta un valore che determina se le visualizzazioni Istogramma e Report tracciano l'ultimo valore campionato durante l'intervallo di campionamento o un valore calcolato dal campionamento, ad esempio il valore medio o minimo del contatore.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
Property ReportValueType As ReportValueTypeConstants
```



## <a name="property-value"></a>Valore proprietà

Determina se le visualizzazioni Istogramma e Report tracciano l'ultimo valore campionato durante l'intervallo di campionamento o un valore calcolato dall'intervallo di campionamento. Per i valori possibili, [**vedere ReportValueTypeConstants.**](/windows/win32/api/isysmon/ne-isysmon-reportvaluetypeconstants)

## <a name="remarks"></a>Commenti

SYSMON ignora questo valore e usa [**ReportValueTypeConstants.sysmonDefaultValue**](/windows/win32/api/isysmon/ne-isysmon-reportvaluetypeconstants) se [**SystemMonitor.DisplayType**](systemmonitor-displaytype.md) non èDisplayTypeConstants.sys [**monHistogram**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants) **oDisplayTypeConstants.sysmonReport**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SystemMonitor**](systemmonitor.md)
</dt> </dl>

 

 





