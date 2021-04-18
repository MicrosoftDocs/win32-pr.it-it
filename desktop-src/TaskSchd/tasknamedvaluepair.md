---
title: Oggetto TaskNamedValuePair
description: Oggetto di scripting utilizzato per creare una coppia nome-valore in cui il nome è associato al valore.
ms.assetid: def679b1-28d5-4c52-9dca-42a6de06a1ec
keywords:
- Utilità di pianificazione oggetto TaskNamedValuePair
- Oggetto TaskNamedValuePair Utilità di pianificazione, descritto
topic_type:
- apiref
api_name:
- TaskNamedValuePair
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b95229b5714d2cdcc43a071f2e51a50e04706429
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301154"
---
# <a name="tasknamedvaluepair-object"></a>Oggetto TaskNamedValuePair

Oggetto di scripting utilizzato per creare una coppia nome-valore in cui il nome è associato al valore.

## <a name="members"></a>Membri

L'oggetto **TaskNamedValuePair** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'oggetto **TaskNamedValuePair** dispone di queste proprietà.



| Proprietà                                             | Descrizione                                                                            |
|:-----------------------------------------------------|:---------------------------------------------------------------------------------------|
| [**Nome**](tasknamedvaluepair-name.md)<br/>   | Ottiene o imposta il nome associato a un valore in una coppia nome-valore.<br/> |
| [**Valore**](tasknamedvaluepair-value.md)<br/> | Ottiene o imposta il valore associato a un nome in una coppia nome-valore.<br/> |



 

## <a name="remarks"></a>Commenti

Durante la lettura o la scrittura di un codice XML personalizzato per un'attività, viene specificata una coppia nome-valore utilizzando l'elemento [**ValueQueries**](taskschedulerschema-valuequeries-eventtriggertype-element.md) dello schema utilità di pianificazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TaskNamedValueCollection**](tasknamedvaluecollection.md)
</dt> </dl>

 

 





