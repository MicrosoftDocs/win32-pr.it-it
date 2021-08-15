---
title: Elemento Documentation (registrationInfoType)
description: Specifica qualsiasi documentazione aggiuntiva per l'attività.
ms.assetid: 5f0d2df3-4eef-430b-85a9-602bb29b85c7
keywords:
- Elemento Documentation Utilità di pianificazione
topic_type:
- apiref
api_name:
- Documentation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6cb8c2a78450fffa467ea659b55015f064310783ae21b067093de9473612fcc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118356869"
---
# <a name="documentation-registrationinfotype-element"></a>Elemento Documentation (registrationInfoType)

Specifica qualsiasi documentazione aggiuntiva per l'attività.

``` syntax
<xs:element name="Documentation"
    type="string"
    minOccurs="0"
 />
```

**L'elemento** Documentation è definito dal [**tipo complesso registrationInfoType.**](taskschedulerschema-registrationinfotype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                           | Derivato da                                                                         | Descrizione                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | Specifica le informazioni amministrative sull'attività, ad esempio l'autore dell'attività e la data di registrazione dell'attività.<br/> |



## <a name="remarks"></a>Commenti

Per le applicazioni di scripting, la documentazione aggiuntiva dell'attività viene specificata usando [**laRegistrationInfo.Doc**](registrationinfo-documentation.md) proprietà .

Per le applicazioni C++, la documentazione aggiuntiva delle attività viene specificata usando la proprietà [**IRegistrationInfo::D ocumentation.**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_documentation)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione di schema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





