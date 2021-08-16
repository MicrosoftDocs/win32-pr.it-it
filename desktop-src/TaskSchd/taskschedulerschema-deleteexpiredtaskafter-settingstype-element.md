---
title: Elemento DeleteExpiredTaskAfter (settingsType)
description: Specifica la quantità di tempo di attesa del Utilità di pianificazione prima di eliminare l'attività dopo la scadenza.
ms.assetid: 947a2fec-ceda-4726-aa1a-26fd1b258c1f
keywords:
- Elemento DeleteExpiredTaskAfter Utilità di pianificazione
topic_type:
- apiref
api_name:
- DeleteExpiredTaskAfter
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e4f491d857eb4ca0fde629b780f22a7795b79f593f94332fb923003520cec706
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118357210"
---
# <a name="deleteexpiredtaskafter-settingstype-element"></a>Elemento DeleteExpiredTaskAfter (settingsType)

Specifica la quantità di tempo di attesa del Utilità di pianificazione prima di eliminare l'attività dopo la scadenza. Se non viene specificato alcun valore per questo elemento, il Utilità di pianificazione non eliminerà l'attività. Il formato di questa stringa è PnYnMnDTnHnMnS, dove nY è il numero di anni, nM è il numero di mesi, nD è il numero di giorni, 'T' è il separatore di data/ora, nH è il numero di ore, nM è il numero di minuti e nS è il numero di secondi (ad esempio, PT5M specifica 5 minuti e P1M4DT2H5M specifica un mese, quattro giorni, due ore e cinque minuti). Per altre informazioni sul tipo di durata, vedere <https://go.microsoft.com/fwlink/p/?linkid=106886> .

``` syntax
<xs:element name="DeleteExpiredTaskAfter"
    type="duration"
    minOccurs="0"
    default="PT0S"
 />
```

**L'elemento DeleteExpiredTaskAfter** è definito dal tipo [**complesso settingsType.**](taskschedulerschema-settingstype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                           | Derivato da                                                         | Descrizione                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Impostazioni**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contiene le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo in C++, [**vedere DeleteExpiredTaskAfter Property of ITaskSettings ( Proprietà DeleteExpiredTaskAfter di ITaskSettings).**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_deleteexpiredtaskafter)

Per lo sviluppo di script, [**vedere TaskSettings.DeleteExpiredTaskAfter.**](tasksettings-deleteexpiredtaskafter.md)

## <a name="examples"></a>Esempio

Nel codice XML seguente viene definito un elemento settings che elimina un'attività scaduta dopo una settimana.


```XML
<Settings>
    <DeleteExpiredTaskAfter>PT7D</DeleteExpiredTaskAfter>
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

 

 





