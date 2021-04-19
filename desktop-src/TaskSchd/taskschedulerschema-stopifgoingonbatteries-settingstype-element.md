---
title: Elemento StopIfGoingOnBatteries (settingsType)
description: Specifica che l'attività verrà arrestata se il computer sta per accedere alle batterie.
ms.assetid: 0d772dbb-a552-45ed-9dc0-7159f6ef12ed
keywords:
- Utilità di pianificazione elemento StopIfGoingOnBatteries
topic_type:
- apiref
api_name:
- StopIfGoingOnBatteries
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2e7de57cde928760c15dd671010880e824c8979f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301329"
---
# <a name="stopifgoingonbatteries-settingstype-element"></a>Elemento StopIfGoingOnBatteries (settingsType)

Specifica che l'attività verrà arrestata se il computer sta per accedere alle batterie.

``` syntax
<xs:element name="StopIfGoingOnBatteries"
    type="boolean"
    default="true"
    minOccurs="0"
 />
```

L'elemento **StopIfGoingOnBatteries** è definito dal tipo complesso [**settingsType**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                           | Derivato da                                                         | Descrizione                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Impostazioni**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contiene le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.<br/> |



## <a name="remarks"></a>Commenti

L'impostazione predefinita per questo elemento è false. Si noti che il valore predefinito è stato modificato rispetto alle versioni precedenti di Utilità di pianificazione.

Per lo sviluppo di script, questa impostazione viene specificata tramite la proprietà [**TaskSettings. StopIfGoingOnBatteries**](tasksettings-stopifgoingonbatteries.md) .

Per lo sviluppo in C++, questa impostazione viene specificata tramite la proprietà [**ITaskSettings:: StopIfGoingOnBatteries**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_stopifgoingonbatteries) .

## <a name="examples"></a>Esempio

Nel codice XML seguente viene definito un elemento Settings che consente la terminazione rigida dell'attività.


```XML
<Settings>
    <StopIfGoingOnBatteries>true</StopIfGoingOnBatteries>
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

 

 





