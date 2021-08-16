---
title: SystemMonitor.MaximumScale - proprietà
description: Recupera o imposta il valore massimo dell'asse verticale (Y) del grafico.
ms.assetid: 305886e3-2586-47c7-a888-6e393580c456
keywords:
- Proprietà MaximumScale SysMon
- Proprietà MaximumScale SysMon , classe SystemMonitor
- Classe SystemMonitor SysMon , proprietà MaximumScale
topic_type:
- apiref
api_name:
- SystemMonitor.MaximumScale
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 176ebab3b2879b3d158310ec61fa9e65df45f8b502029ede1c58c2c1dd33f225
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882030"
---
# <a name="systemmonitormaximumscale-property"></a>SystemMonitor.MaximumScale - proprietà

Recupera o imposta il valore massimo dell'asse verticale (Y) del grafico.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
Property MaximumScale As Long
```



## <a name="property-value"></a>Valore proprietà

Valore massimo positivo dell'asse verticale del grafico. Il valore massimo predefinito della scala verticale è 100. Il valore minimo su cui è possibile impostare il valore massimo è maggiore di uno rispetto al [**valore MinimumScale.**](systemmonitor-minimumscale.md) Il valore massimo su cui è possibile impostare il valore massimo è 999.999.999.

## <a name="remarks"></a>Commenti

Il controllo regola automaticamente la posizione dei numeri di scala visualizzati sulla scala verticale in base alle dimensioni del controllo visualizzato.

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

[**SystemMonitor.MinimumScale**](systemmonitor-minimumscale.md)
</dt> <dt>

[**SystemMonitor.ShowScaleLabels**](systemmonitor-showscalelabels.md)
</dt> </dl>

 

 





