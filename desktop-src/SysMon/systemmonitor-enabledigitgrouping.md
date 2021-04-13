---
title: Proprietà SystemMonitor. EnableDigitGrouping
description: Recupera o imposta un valore che determina se SYSMON utilizza il raggruppamento di cifre durante la visualizzazione dei valori numerici.
ms.assetid: 6a277960-fd01-423c-af2a-b35ed46c6d9a
keywords:
- Proprietà EnableDigitGrouping SysMon
- Proprietà EnableDigitGrouping SysMon, oggetto SystemMonitor
- Oggetto SystemMonitor SysMon, proprietà EnableDigitGrouping
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
ms.openlocfilehash: 66da0ad5ade7f3e01f58ef29bbd1094634c01b37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400653"
---
# <a name="systemmonitorenabledigitgrouping-property"></a>Proprietà SystemMonitor. EnableDigitGrouping

Recupera o imposta un valore che determina se SYSMON utilizza il raggruppamento di cifre durante la visualizzazione dei valori numerici.

## <a name="syntax"></a>Sintassi


```VB
Property EnableDigitGrouping As Boolean
```



## <a name="property-value"></a>Valore proprietà

Se è true, SYSMON raggruppa le cifre quando si visualizzano i valori numerici, ad esempio 1.214. Se false, i valori numerici non sono raggruppati, ad esempio 1214. Il valore predefinito è true.

## <a name="remarks"></a>Commenti

Il simbolo di raggruppamento digit è localizzato.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



 

 





