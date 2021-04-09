---
title: Proprietà SystemMonitor. ChartScroll
description: Recupera o imposta un valore che determina se il grafico a linee scorre nella visualizzazione.
ms.assetid: df4806be-dfd3-4ff7-985d-b46c00bb19f8
keywords:
- Proprietà ChartScroll SysMon
- Proprietà ChartScroll SysMon, oggetto SystemMonitor
- Oggetto SystemMonitor SysMon, proprietà ChartScroll
topic_type:
- apiref
api_name:
- SystemMonitor.ChartScroll
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51288af710e5ae94baf46acf0d2ed91732a1d310
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964322"
---
# <a name="systemmonitorchartscroll-property"></a>Proprietà SystemMonitor. ChartScroll

Recupera o imposta un valore che determina se il grafico a linee scorre nella visualizzazione.

## <a name="syntax"></a>Sintassi


```VB
Property ChartScroll As Boolean
```



## <a name="property-value"></a>Valore proprietà

True se il grafico a linee scorre continuamente da destra a sinistra; in caso contrario, false se il grafico a linee viene disegnato da sinistra a destra e viene eseguito il wrapping su se stesso nella visualizzazione. False è l'impostazione predefinita.

## <a name="remarks"></a>Commenti

Questo valore viene ignorato se [**SystemMonitor. DisplayType**](systemmonitor-displaytype.md) non è [**DisplayTypeConstants.sysmonLineGraph**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



 

 





