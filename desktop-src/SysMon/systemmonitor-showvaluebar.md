---
title: Proprietà SystemMonitor. ShowValueBar
description: Recupera o imposta un valore che determina se la barra del valore (il set di valori statistici sotto il grafo) viene visualizzata nel controllo.
ms.assetid: 320fbbbb-c4ea-4772-9b10-1e123849c255
keywords:
- Proprietà ShowValueBar SysMon
- Proprietà ShowValueBar SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, proprietà ShowValueBar
topic_type:
- apiref
api_name:
- SystemMonitor.ShowValueBar
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f393b36162fae6aed996d2afaccd4749f22598f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740623"
---
# <a name="systemmonitorshowvaluebar-property"></a>Proprietà SystemMonitor. ShowValueBar

Recupera o imposta un valore che determina se la barra del valore (il set di valori statistici sotto il grafo) viene visualizzata nel controllo.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
Property ShowValueBar As Boolean
```



## <a name="property-value"></a>Valore proprietà

True indica che la barra dei valori è visualizzata sul controllo; in caso contrario, false. Il valore predefinito di questa proprietà è True.

## <a name="remarks"></a>Commenti

Le statistiche visualizzate includono l'ultimo valore, il valore medio e i valori minimo e massimo del contatore attualmente selezionato sull'intervallo di tempo visualizzato. Per selezionare i valori dei contatori da visualizzare, l'utente deve selezionare il contatore nel riquadro Legenda del controllo.

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

 

 





