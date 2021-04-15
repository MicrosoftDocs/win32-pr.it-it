---
title: Elemento Privilege (requiredPrivilegesType)
description: Specifica il diritto di un'attività di eseguire varie operazioni correlate al sistema, ad esempio l'arresto del sistema, il caricamento dei driver di dispositivo o la modifica dell'ora di sistema.
ms.assetid: d5585d1c-e121-4770-a13e-108158bc703e
keywords:
- Elemento Privilege Utilità di pianificazione
topic_type:
- apiref
api_name:
- Privilege
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 55e9263ae9d02bb384bfbe56101ea82f98c2e076
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478388"
---
# <a name="privilege-requiredprivilegestype-element"></a>Elemento Privilege (requiredPrivilegesType)

Specifica il diritto di un'attività di eseguire varie operazioni correlate al sistema, ad esempio l'arresto del sistema, il caricamento dei driver di dispositivo o la modifica dell'ora di sistema.

``` syntax
<xs:element name="Privilege"
    type="privilegeType"
    maxOccurs="64"
    minOccurs="1"
 />
```

L'elemento **Privilege** è definito dal tipo complesso [**requiredPrivilegesType**](taskschedulerschema-requiredprivilegestype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                                             | Derivato da                                                                             | Descrizione                                                                        |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**RequiredPrivileges**](taskschedulerschema-requiredprivileges-requiredprivilegestype-element.md) | [**requiredPrivilegesType**](taskschedulerschema-requiredprivilegestype-complextype.md) | Contiene le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo in C++, queste informazioni sono accessibili tramite la proprietà [**IPrincipal2:: RequiredPrivilege**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_requiredprivilege) .

## <a name="examples"></a>Esempio

Nel codice XML seguente viene definito un elemento Settings che specifica il diritto di un'attività di eseguire varie operazioni correlate al sistema, ad esempio l'arresto del sistema, il caricamento dei driver di dispositivo o la modifica dell'ora di sistema.


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

[Elementi dello schema Utilità di pianificazione](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





