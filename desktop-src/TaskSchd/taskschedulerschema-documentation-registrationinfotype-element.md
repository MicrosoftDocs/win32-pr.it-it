---
title: Elemento Documentation (registrationInfoType)
description: Specifica qualsiasi documentazione aggiuntiva per l'attività.
ms.assetid: 5f0d2df3-4eef-430b-85a9-602bb29b85c7
keywords:
- Utilità di pianificazione elemento della documentazione
topic_type:
- apiref
api_name:
- Documentation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3407a6611886f867734dc7f32cd867a2930d3d2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302691"
---
# <a name="documentation-registrationinfotype-element"></a>Elemento Documentation (registrationInfoType)

Specifica qualsiasi documentazione aggiuntiva per l'attività.

``` syntax
<xs:element name="Documentation"
    type="string"
    minOccurs="0"
 />
```

L'elemento **Documentation** è definito dal tipo complesso [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                           | Derivato da                                                                         | Descrizione                                                                                                                         |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) | [**registrationInfoType**](taskschedulerschema-registrationinfotype-complextype.md) | Specifica le informazioni amministrative sull'attività, ad esempio l'autore dell'attività e la data di registrazione dell'attività.<br/> |



## <a name="remarks"></a>Commenti

Per le applicazioni di scripting, è stata specificata una documentazione aggiuntiva sulle attività usando la proprietà [**RegistrationInfo.Documentation**](registrationinfo-documentation.md) .

Per le applicazioni C++, è stata specificata una documentazione aggiuntiva sulle attività usando la proprietà [**IRegistrationInfo::D kumentace**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationinfo-get_documentation) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elementi dello schema Utilità di pianificazione](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





