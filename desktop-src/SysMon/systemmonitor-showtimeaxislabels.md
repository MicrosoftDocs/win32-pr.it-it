---
title: Proprietà SystemMonitor. ShowTimeAxisLabels
description: Recupera o imposta un valore che determina se l'asse orizzontale (X) della visualizzazione grafico contiene etichette.
ms.assetid: 9e9d2d2c-f053-4afe-85de-25242842498f
keywords:
- Proprietà ShowTimeAxisLabels SysMon
- Proprietà ShowTimeAxisLabels SysMon, oggetto SystemMonitor
- Oggetto SystemMonitor SysMon, proprietà ShowTimeAxisLabels
topic_type:
- apiref
api_name:
- SystemMonitor.ShowTimeAxisLabels
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06569dcd4702ae687b09bfae88c84482a49afb71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301254"
---
# <a name="systemmonitorshowtimeaxislabels-property"></a>Proprietà SystemMonitor. ShowTimeAxisLabels

Recupera o imposta un valore che determina se l'asse orizzontale (X) della visualizzazione grafico contiene etichette.

## <a name="syntax"></a>Sintassi


```VB
Property ShowTimeAxisLabels As Boolean
```



## <a name="property-value"></a>Valore proprietà

Se il valore è true, le etichette verranno applicate all'asse x. Il valore false non lo è. Il valore predefinito è False.

## <a name="remarks"></a>Commenti

SYSMON ignora questa proprietà per grafici a barre, report e istogrammi.

Per i grafici a linee, SYSMON usa l'ora in cui è stato campionato il valore del contatore come etichetta.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



 

 





