---
title: Elemento Version (registrationInfoType)
description: Specifica il numero di versione dell'attività.
ms.assetid: 0a7223ae-dfc7-4356-aea4-88ff3b3b9148
keywords:
- Elemento Version Utilità di pianificazione
topic_type:
- apiref
api_name:
- Version
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 63d69b501b12890939f3bd0b146c959278eeaa0d5eb596851a488cef87f0770a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118610426"
---
# <a name="version-registrationinfotype-element"></a>Elemento Version (registrationInfoType)

Specifica il numero di versione dell'attività.

``` syntax
<xs:element name="Version"
    type="string"
    minOccurs="0"
 />
```

**L'elemento** Version è definito dal tipo complesso [**registrationInfoType.**](taskschedulerschema-registrationinfotype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                           | Derivato da                                                                         | Descrizione                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | Specifica informazioni amministrative sull'attività, ad esempio l'autore dell'attività e la data di registrazione dell'attività.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo di script, la versione di un'attività viene specificata tramite [**la proprietà RegistrationInfo.Version.**](registrationinfo-version.md)

Per lo sviluppo C++, la versione di un'attività viene specificata tramite [**la proprietà IRegistrationInfo::Version.**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_version)

## <a name="examples"></a>Esempio

Il codice XML seguente definisce la versione di un'attività.


```XML
<RegistrationInfo>
    <Version></Version>
 </RegistrationInfo>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione elementi dello schema](task-scheduler-schema-elements.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





