---
title: Proprietà SystemMonitor. ManualUpdate
description: Recupera o imposta un valore che indica se il contenuto del monitor di sistema verrà aggiornato manualmente o automaticamente a intervalli specificati.
ms.assetid: e068a955-ec1d-4f93-9261-25ba87773913
keywords:
- Proprietà ManualUpdate SysMon
- Proprietà ManualUpdate SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, proprietà ManualUpdate
topic_type:
- apiref
api_name:
- SystemMonitor.ManualUpdate
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d1ecb426b47ba9cb7ec50b737f4f32d5ce274eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301576"
---
# <a name="systemmonitormanualupdate-property"></a>Proprietà SystemMonitor. ManualUpdate

Recupera o imposta un valore che indica se il contenuto del monitor di sistema verrà aggiornato manualmente o automaticamente a intervalli specificati.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
Property ManualUpdate As Boolean
```



## <a name="property-value"></a>Valore proprietà

True indica che il grafo è stato aggiornato manualmente. False indica che il grafico viene aggiornato automaticamente in base all'intervallo di aggiornamento specificato in [**SystemMonitor. UpdateInterval**](systemmonitor-updateinterval.md).

## <a name="remarks"></a>Commenti

Per impostazione predefinita, il grafico viene aggiornato automaticamente.

Per aggiornare il grafo manualmente, chiamare il metodo [**SystemMonitor. CollectSample**](systemmonitor-collectsample.md) .

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

[**SystemMonitor. CollectSample**](systemmonitor-collectsample.md)
</dt> <dt>

[**SystemMonitor. UpdateGraph**](systemmonitor-updategraph.md)
</dt> </dl>

 

 





