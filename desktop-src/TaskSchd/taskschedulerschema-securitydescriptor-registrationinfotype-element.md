---
title: Elemento SecurityDescriptor (registrationInfoType)
description: Specifica il descrittore di sicurezza dell'attività.
ms.assetid: 79821b20-226a-4e7e-8ca1-6c9cf9f1b56e
keywords:
- Elemento SecurityDescriptor Utilità di pianificazione
topic_type:
- apiref
api_name:
- SecurityDescriptor
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 83742ebbbc6b8fb653610bf8e20c00094a3c8a3984123765adf6e953935c9011
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099861"
---
# <a name="securitydescriptor-registrationinfotype-element"></a>Elemento SecurityDescriptor (registrationInfoType)

Specifica il descrittore di sicurezza dell'attività.

``` syntax
<xs:element name="SecurityDescriptor"
    type="string"
 />
```

**L'elemento SecurityDescriptor** è definito dal tipo complesso [**registrationInfoType.**](taskschedulerschema-registrationinfotype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                           | Derivato da                                                                         | Descrizione                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | Specifica informazioni amministrative sull'attività, ad esempio l'autore dell'attività e la data di registrazione dell'attività.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo di script, il descrittore di sicurezza di un'attività viene specificato tramite la [**proprietà RegistrationInfo.SecurityDescriptor.**](registrationinfo-securitydescriptor.md)

Per lo sviluppo C++, il descrittore di sicurezza di un'attività viene specificato tramite la [**proprietà IRegistrationInfo::SecurityDescriptor.**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_securitydescriptor)

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

 

 





