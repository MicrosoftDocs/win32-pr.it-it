---
title: Elemento MultipleInstancesPolicy (settingsType)
description: Specifica i criteri che definiscono il modo in cui il Utilità di pianificazione gestisce più istanze dell'attività.
ms.assetid: ec82d396-f83c-4684-98ab-f70e15ada075
keywords:
- Elemento MultipleInstancesPolicy Utilità di pianificazione
topic_type:
- apiref
api_name:
- MultipleInstancesPolicy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8d7728d2b39fbcbed060fce409f4d721b59ef5ca324cd141d7777a5ffed110a0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072451"
---
# <a name="multipleinstancespolicy-settingstype-element"></a>Elemento MultipleInstancesPolicy (settingsType)

Specifica i criteri che definiscono il modo in cui il Utilità di pianificazione gestisce più istanze dell'attività.

``` syntax
<xs:element name="MultipleInstancesPolicy"
    type="multipleInstancesPolicyType"
 />
```

**L'elemento MultipleInstancesPolicy** è definito dal tipo semplice [**multipleInstancesPolicyType.**](taskschedulerschema-multipleinstancespolicytype-simpletype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                           | Derivato da                                                         | Descrizione                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Impostazioni**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contiene le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo in C++, vedere [**Proprietà MultipleInstances di ITaskSettings.**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_multipleinstances)

Per lo sviluppo di script, [**vedere TaskSettings.MultipleInstances.**](tasksettings-multipleinstances.md)

### <a name="restricted-values"></a>Valori limitati

Questo elemento è limitato ai valori seguenti.

-   Parallelo: avvia una nuova istanza mentre è in esecuzione un'istanza esistente.
-   Coda: avvia una nuova istanza dell'attività dopo il completamento di tutte le altre istanze dell'attività.
-   IgnoreNew: impostazione predefinita. Non avvia una nuova istanza se è in esecuzione un'istanza esistente dell'attività.
-   StopExisting: arresta un'istanza esistente dell'attività prima di avviare una nuova istanza.

## <a name="examples"></a>Esempio

Nel codice XML seguente viene definito un elemento settings che consente l'esecuzione parallela di più istanze dell'attività.


```XML
<Settings>
    <MultipleInstancesPolicy>Parallel</MultipleInstancesPolicy>
</Settings>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione di schema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





