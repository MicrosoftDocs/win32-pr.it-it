---
title: Elemento RequiredPrivileges (requiredPrivilegesType)
description: Specifica i privilegi richiesti dall'attività.
ms.assetid: 7b615af8-76f9-498c-aa2d-7da02d64992f
keywords:
- Elemento RequiredPrivileges Utilità di pianificazione
topic_type:
- apiref
api_name:
- RequiredPrivileges
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e395a61aace07dccb27eab04d9c0299115c25f16d84cd42e3d607435478f8060
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118611488"
---
# <a name="requiredprivileges-requiredprivilegestype-element"></a>Elemento RequiredPrivileges (requiredPrivilegesType)

Specifica i privilegi richiesti dall'attività.

``` syntax
<xs:element name="RequiredPrivileges"
    type="requiredPrivilegesType"
    minOccurs="0"
 />
```

**L'elemento RequiredPrivileges** è definito dal tipo complesso [**requiredPrivilegesType.**](taskschedulerschema-requiredprivilegestype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                                  | Derivato da                                                           | Descrizione                                                    |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Principal (principalType)**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Specifica le credenziali di sicurezza per un'entità.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo C++, queste informazioni sono accessibili tramite la [**proprietà IPrincipal2::RequiredPrivilege.**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_requiredprivilege)

## <a name="examples"></a>Esempio

Il codice XML seguente definisce l'uso di un identificatore di gruppo e dei privilegi necessari.


```XML
<Principal>
    <RequiredPrivileges>
        <Privilege>SeCreateTokenPrivilege</Privilege>
    </RequiredPrivileges>
</Principal>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





