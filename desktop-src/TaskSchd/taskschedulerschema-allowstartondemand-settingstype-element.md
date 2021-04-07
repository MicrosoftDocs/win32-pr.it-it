---
title: Elemento AllowStartOnDemand (settingsType)
description: Specifica che l'attività può essere avviata utilizzando il comando Esegui o il menu di scelta rapida.
ms.assetid: 5a0f0842-9f09-4d52-bed2-45740945d9a5
keywords:
- Utilità di pianificazione elemento AllowStartOnDemand
topic_type:
- apiref
api_name:
- AllowStartOnDemand
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ec396bf10efbd11024fe39e57bdf05025db0e610
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963917"
---
# <a name="allowstartondemand-settingstype-element"></a>Elemento AllowStartOnDemand (settingsType)

Specifica che l'attività può essere avviata utilizzando il comando Esegui o il menu di scelta rapida.

``` syntax
<xs:element name="AllowStartOnDemand"
    type="boolean"
    minOccurs="0"
    default="true"
 />
```

L'elemento **AllowStartOnDemand** è definito dal tipo complesso [**settingsType**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                           | Derivato da                                                         | Descrizione                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Impostazioni**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contiene le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.<br/> |



## <a name="remarks"></a>Commenti

Quando questo elemento è impostato su true, l'attività può essere avviata indipendentemente dall'avvio dell'attività da parte dei trigger.

Per lo sviluppo in C++, vedere la [**Proprietà AllowDemandStart di ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_allowdemandstart).

Per lo sviluppo di script, vedere [**TaskSettings. AllowDemandStart**](tasksettings-allowdemandstart.md).

## <a name="examples"></a>Esempio

Per un esempio completo del codice XML per un'attività che consente l'avvio della richiesta, vedere l' [esempio di trigger di ora (XML)](time-trigger-example--xml-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elementi dello schema Utilità di pianificazione](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





