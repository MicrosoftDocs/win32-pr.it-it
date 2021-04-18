---
title: Elemento MultipleInstancesPolicy (settingsType)
description: Specifica i criteri che definiscono il modo in cui il Utilità di pianificazione gestisce più istanze dell'attività.
ms.assetid: ec82d396-f83c-4684-98ab-f70e15ada075
keywords:
- Utilità di pianificazione elemento MultipleInstancesPolicy
topic_type:
- apiref
api_name:
- MultipleInstancesPolicy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f5bcbbd26880f1ccced3e71b44dc93993d20f4a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301906"
---
# <a name="multipleinstancespolicy-settingstype-element"></a>Elemento MultipleInstancesPolicy (settingsType)

Specifica i criteri che definiscono il modo in cui il Utilità di pianificazione gestisce più istanze dell'attività.

``` syntax
<xs:element name="MultipleInstancesPolicy"
    type="multipleInstancesPolicyType"
 />
```

L'elemento **MultipleInstancesPolicy** è definito dal tipo semplice [**multipleInstancesPolicyType**](taskschedulerschema-multipleinstancespolicytype-simpletype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                           | Derivato da                                                         | Descrizione                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Impostazioni**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contiene le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo in C++, vedere [**la proprietà MultipleInstances di ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_multipleinstances).

Per lo sviluppo di script, vedere [**TaskSettings. MultipleInstances**](tasksettings-multipleinstances.md).

### <a name="restricted-values"></a>Valori con restrizioni

Questo elemento è limitato ai valori seguenti.

-   Parallel: avvia una nuova istanza mentre è in esecuzione un'istanza esistente.
-   Queue: avvia una nuova istanza dell'attività dopo il completamento di tutte le altre istanze dell'attività.
-   IgnoreNew: valore predefinito. Non avvia una nuova istanza di se è in esecuzione un'istanza esistente dell'attività.
-   StopExisting: arresta un'istanza esistente dell'attività prima di avviare una nuova istanza.

## <a name="examples"></a>Esempio

Nel codice XML seguente viene definito un elemento Settings che consente l'esecuzione in parallelo di più istanze dell'attività.


```XML
<Settings>
    <MultipleInstancesPolicy>Parallel</MultipleInstancesPolicy>
</Settings>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elementi dello schema Utilità di pianificazione](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





