---
title: CounterItem.Selected - proprietà
description: Recupera o imposta un valore che indica se il contatore è selezionato.
ms.assetid: 293cc2ea-728c-4364-be2b-080bd188fe1c
keywords:
- Proprietà selezionata SysMon
- Proprietà selezionata SysMon , oggetto CounterItem
- Oggetto CounterItem SysMon , proprietà Selected
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
ms.openlocfilehash: 41e5cfcc65c54f882f10e87a0f2aaebad0e1a55c94b6581031b034799987bc6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117956960"
---
# <a name="counteritemselected-property"></a>CounterItem.Selected - proprietà

Recupera o imposta un valore che indica se il contatore è selezionato.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
Property Selected As Boolean
```



## <a name="property-value"></a>Valore proprietà

True se il contatore è selezionato; in caso contrario, false.

## <a name="remarks"></a>Commenti

È possibile selezionare uno o più contatori dalla raccolta di contatori. La selezione di un contatore, la selezione del contatore nella legenda, la visibilità del contatore nella legenda e la generazione di [**un evento OnCounterSelected.**](-systemmonitor-oncounterselected.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon.ocx</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CounterItem**](counteritem.md)
</dt> </dl>

 

 





