---
title: Proprietà CounterItem. Selected
description: Recupera o imposta un valore che indica se il contatore è selezionato.
ms.assetid: 293cc2ea-728c-4364-be2b-080bd188fe1c
keywords:
- Proprietà selezionata SysMon
- Proprietà selezionata SysMon, oggetto CounterItem
- Oggetto CounterItem SysMon, proprietà selezionata
topic_type:
- apiref
api_name:
- CounterItem.Selected
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac707dfaf2ed379884395a08128ddaeda771fa00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964323"
---
# <a name="counteritemselected-property"></a>Proprietà CounterItem. Selected

Recupera o imposta un valore che indica se il contatore è selezionato.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
Property Selected As Boolean
```



## <a name="property-value"></a>Valore proprietà

True se il contatore è selezionato; in caso contrario, false.

## <a name="remarks"></a>Commenti

È possibile selezionare uno o più contatori dalla raccolta di contatori. Selezionando un contatore, viene selezionato il contatore nella legenda, il contatore viene reso visibile nella legenda e viene generato un evento [**OnCounterSelected**](-systemmonitor-oncounterselected.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CounterItem**](counteritem.md)
</dt> </dl>

 

 





