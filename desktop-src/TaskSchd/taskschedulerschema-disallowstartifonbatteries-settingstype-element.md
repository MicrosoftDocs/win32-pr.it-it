---
title: Elemento DisallowStartIfOnBatteries (settingsType)
description: Specifica che l'attività non verrà avviata se il computer è in esecuzione sulle batterie.
ms.assetid: 48c0fd32-4441-4628-8090-c736f2945b4d
keywords:
- Utilità di pianificazione elemento DisallowStartIfOnBatteries
topic_type:
- apiref
api_name:
- DisallowStartIfOnBatteries
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8a8d93bcabd0e121c44f4a7212d11491624a08d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743775"
---
# <a name="disallowstartifonbatteries-settingstype-element"></a>Elemento DisallowStartIfOnBatteries (settingsType)

Specifica che l'attività non verrà avviata se il computer è in esecuzione sulle batterie.

``` syntax
<xs:element name="DisallowStartIfOnBatteries"
    type="boolean"
 />
```

L'elemento **DisallowStartIfOnBatteries** è definito dal tipo complesso [**settingsType**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                           | Derivato da                                                         | Descrizione                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Impostazioni**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contiene le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.<br/> |



## <a name="remarks"></a>Commenti

L'impostazione predefinita per questo elemento è true.

Per lo sviluppo di script, è possibile accedere a queste informazioni tramite la proprietà [**TaskSettings. DisallowStartIfOnBatteries**](tasksettings-disallowstartifonbatteries.md) .

Per lo sviluppo in C++, queste informazioni sono accessibili tramite la proprietà [**ITaskSettings::D isallowstartifonbatteries**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_disallowstartifonbatteries) .

## <a name="examples"></a>Esempio

Nel codice XML seguente viene definito un elemento Settings che non consente l'esecuzione dell'attività se il computer è in esecuzione sulle batterie.


```XML
<Settings>
    <DisallowStartIfOnBatteries>true</DisallowStartIfOnBatteries>
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

 

 





