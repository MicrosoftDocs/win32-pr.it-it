---
title: Elemento Date (registrationInfoType)
description: Specifica la data e l'ora di registrazione dell'attività.
ms.assetid: 0b226786-152d-4231-afa6-db5a630525f3
keywords:
- Elemento Date Utilità di pianificazione
topic_type:
- apiref
api_name:
- Date
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f191d6181e450deff8ffdb7bda0bf97cd0b27901fe454c25599d17b8edb30628
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866641"
---
# <a name="date-registrationinfotype-element"></a>Elemento Date (registrationInfoType)

Specifica la data e l'ora di registrazione dell'attività.

``` syntax
<xs:element name="Date"
    type="dateTime"
    minOccurs="0"
 />
```

**L'elemento Date** è definito dal tipo complesso [**registrationInfoType.**](taskschedulerschema-registrationinfotype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                           | Derivato da                                                                         | Descrizione                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | Specifica informazioni amministrative sull'attività, ad esempio l'autore dell'attività e la data di registrazione dell'attività.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo di script, la data di registrazione di un'attività viene specificata tramite la [**proprietà RegistrationInfo.Date.**](registrationinfo-date.md)

Per lo sviluppo C++, la data di registrazione di un'attività viene specificata usando la proprietà [**IRegistrationInfo::D ate.**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_date)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione schema](task-scheduler-schema-elements.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





