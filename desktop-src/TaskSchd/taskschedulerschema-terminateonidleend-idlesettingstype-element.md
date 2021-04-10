---
title: Elemento StopOnIdleEnd (idleSettingsType)
description: Specifica che il Utilità di pianificazione arresterà l'attività se la condizione di inattività termina prima del completamento dell'attività.
ms.assetid: 5e8e4fd9-bba1-4ede-a0b3-9f50feb1b6f3
keywords:
- Utilità di pianificazione elemento StopOnIdleEnd
topic_type:
- apiref
api_name:
- TerminateOnIdleEnd
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a47a01d7d77f3dd20f055bce8e4bb12fad82c771
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964821"
---
# <a name="stoponidleend-idlesettingstype-element"></a>Elemento StopOnIdleEnd (idleSettingsType)

Specifica che il Utilità di pianificazione arresterà l'attività se la condizione di inattività termina prima del completamento dell'attività.

``` syntax
<xs:element name="StopOnIdleEnd"
    type="boolean"
    minOccurs="0"
    default="true"
 />
```

L'elemento **StopOnIdleEnd** è definito dal tipo complesso [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                       | Derivato da                                                                 | Descrizione                                                                                       |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**IdleSettings**](taskschedulerschema-idlesettings-settingstype-element.md) | [**idleSettingsType**](taskschedulerschema-idlesettingstype-complextype.md) | Specifica il modo in cui il Utilità di pianificazione esegue le attività quando il computer si trova in uno stato inattivo.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo in C++, vedere [**la proprietà StopOnIdleEnd di IIdleSettings**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_stoponidleend).

Per lo sviluppo di script, vedere [**IdleSettings. StopOnIdleEnd**](idlesettings-stoponidleend.md).

## <a name="examples"></a>Esempio

Il codice XML seguente definisce un'impostazione inattiva che indica che l'attività non deve essere eseguita al termine della condizione di inattività.


```XML
<IdleSettings>
    <StopOnIdleEnd>false</StopOnIdleEnd>
</IdleSettings>
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

 

 





