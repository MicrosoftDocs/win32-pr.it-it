---
title: SystemMonitor.ChartScroll - proprietà
description: Recupera o imposta un valore che determina se il grafico a linee scorre nella visualizzazione.
ms.assetid: df4806be-dfd3-4ff7-985d-b46c00bb19f8
keywords:
- Proprietà ChartScroll SysMon
- Proprietà ChartScroll SysMon , oggetto SystemMonitor
- Oggetto SystemMonitor SysMon , proprietà ChartScroll
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
ms.openlocfilehash: d64ec5ed2aae641fcc7525d2b547348ca4bdd756f89bb379da84ce224ce528d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117956120"
---
# <a name="systemmonitorchartscroll-property"></a>SystemMonitor.ChartScroll - proprietà

Recupera o imposta un valore che determina se il grafico a linee scorre nella visualizzazione.

## <a name="syntax"></a>Sintassi


```VB
Property ChartScroll As Boolean
```



## <a name="property-value"></a>Valore proprietà

True se il grafico a linee scorre continuamente da destra a sinistra; In caso contrario, False se il grafico a linee viene disegnato da sinistra a destra e viene disposto su se stesso nella visualizzazione. False è l'impostazione predefinita.

## <a name="remarks"></a>Commenti

Questo valore viene ignorato se [**SystemMonitor.DisplayType**](systemmonitor-displaytype.md) non è [**DisplayTypeConstants.sysmonLineGraph**](/windows/win32/api/isysmon/ne-isysmon-displaytypeconstants).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



 

 





