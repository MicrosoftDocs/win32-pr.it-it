---
title: Proprietà SystemMonitor.EnableDigitGrouping
description: Recupera o imposta un valore che determina se SYSMON usa il raggruppamento di cifre durante la visualizzazione di valori numerici.
ms.assetid: 6a277960-fd01-423c-af2a-b35ed46c6d9a
keywords:
- Proprietà EnableDigitGrouping SysMon
- Proprietà EnableDigitGrouping SysMon , oggetto SystemMonitor
- Oggetto SystemMonitor SysMon , proprietà EnableDigitGrouping
topic_type:
- apiref
api_name:
- SystemMonitor.EnableDigitGrouping
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d910e479cc0a957ea5f1332d7fead0f93badd797bfe2d90b26f9914f0c3d863a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118882606"
---
# <a name="systemmonitorenabledigitgrouping-property"></a>Proprietà SystemMonitor.EnableDigitGrouping

Recupera o imposta un valore che determina se SYSMON usa il raggruppamento di cifre durante la visualizzazione di valori numerici.

## <a name="syntax"></a>Sintassi


```VB
Property EnableDigitGrouping As Boolean
```



## <a name="property-value"></a>Valore proprietà

Se True, SYSMON raggruppa le cifre quando visualizza valori numerici, ad esempio 1.214. Se False, i valori numerici non vengono raggruppati, ad esempio 1214. True è l'impostazione predefinita.

## <a name="remarks"></a>Commenti

Il simbolo di raggruppamento delle cifre è localizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



 

 





