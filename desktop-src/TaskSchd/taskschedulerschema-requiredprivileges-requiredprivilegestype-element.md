---
title: Elemento RequiredPrivileges (requiredPrivilegesType)
description: Specifica i privilegi richiesti dall'attività.
ms.assetid: 7b615af8-76f9-498c-aa2d-7da02d64992f
keywords:
- Utilità di pianificazione elemento RequiredPrivileges
topic_type:
- apiref
api_name:
- RequiredPrivileges
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 70476cff01113dcf612f890e8a6aa5538d0ca38e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121554"
---
# <a name="requiredprivileges-requiredprivilegestype-element"></a>Elemento RequiredPrivileges (requiredPrivilegesType)

Specifica i privilegi richiesti dall'attività.

``` syntax
<xs:element name="RequiredPrivileges"
    type="requiredPrivilegesType"
    minOccurs="0"
 />
```

L'elemento **RequiredPrivileges** è definito dal tipo complesso [**requiredPrivilegesType**](taskschedulerschema-requiredprivilegestype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                                  | Derivato da                                                           | Descrizione                                                    |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Entità (principalType)**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Specifica le credenziali di sicurezza per un'entità.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo in C++, queste informazioni sono accessibili tramite la proprietà [**IPrincipal2:: RequiredPrivilege**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_requiredprivilege) .

## <a name="examples"></a>Esempio

Nel codice XML seguente viene definito utilizzando un identificatore di gruppo e i privilegi necessari.


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
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>              |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





