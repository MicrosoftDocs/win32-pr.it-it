---
title: Proprietà SystemMonitor. UpdateInterval
description: Recupera o imposta il periodo di attesa di SYSMON prima della successiva raccolta dei dati del contatore e l'aggiornamento del grafico o del report.
ms.assetid: 297931e4-23ae-4384-a04a-9c1fa8aa1239
keywords:
- Proprietà UpdateInterval SysMon
- Proprietà UpdateInterval SysMon, classe SystemMonitor
- Classe SystemMonitor SysMon, proprietà UpdateInterval
topic_type:
- apiref
api_name:
- SystemMonitor.UpdateInterval
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5872f870e831896ff37157a4a0f47584e77d93c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964143"
---
# <a name="systemmonitorupdateinterval-property"></a>Proprietà SystemMonitor. UpdateInterval

Recupera o imposta il periodo di attesa di SYSMON prima della successiva raccolta dei dati del contatore e l'aggiornamento del grafico o del report.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```VB
Property UpdateInterval As Single
```



## <a name="property-value"></a>Valore proprietà

Tempo di attesa, in secondi, di SYSMON prima della successiva raccolta dei dati del contatore e aggiornamento del grafico o del report. L'intervallo minimo è di 1 secondo (questo è anche il valore predefinito). Il valore massimo è 1 milione.

## <a name="remarks"></a>Commenti

Questa proprietà è pertinente solo quando [**SystemMonitor. ManualUpdate**](systemmonitor-manualupdate.md) è impostato su false.

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

 

 





