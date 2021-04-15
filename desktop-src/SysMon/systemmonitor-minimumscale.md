---
title: Proprietà SystemMonitor. MinimumScale
description: Recupera o imposta il valore minimo dell'asse verticale (Y) del grafico.
ms.assetid: 22dacfbf-27bb-48fe-b646-4cf17645a131
keywords:
- Proprietà MinimumScale SysMon
- Proprietà MinimumScale SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, proprietà MinimumScale
topic_type:
- apiref
api_name:
- SystemMonitor.MinimumScale
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24f675e96ecdd4e547ca4a93b248556fd8c0539a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476576"
---
# <a name="systemmonitorminimumscale-property"></a>Proprietà SystemMonitor. MinimumScale

Recupera o imposta il valore minimo dell'asse verticale (Y) del grafico.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
Property MinimumScale As Long
```



## <a name="property-value"></a>Valore proprietà

Valore minimo positivo dell'asse verticale del grafico. Il valore minimo predefinito della scala verticale è 0. Il valore massimo in cui è possibile impostare il valore minimo è uno minore del valore [**MaximumScale**](systemmonitor-maximumscale.md) .

## <a name="remarks"></a>Commenti

Il controllo regola automaticamente la posizione dei numeri di scala visualizzati sulla scala verticale in base alle dimensioni del controllo visualizzato.

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

[**SystemMonitor. MaximumScale**](systemmonitor-maximumscale.md)
</dt> <dt>

[**SystemMonitor. ShowScaleLabels**](systemmonitor-showscalelabels.md)
</dt> </dl>

 

 





