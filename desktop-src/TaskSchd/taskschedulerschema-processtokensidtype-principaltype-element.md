---
title: Elemento ProcessTokenSidType (principalType)
description: Specifica il tipo di identificazione di sicurezza del processo (SID) dell'attività.
ms.assetid: d9bffa92-c0dc-4332-a29c-7f2710ec34e3
keywords:
- Utilità di pianificazione elemento ProcessTokenSidType
topic_type:
- apiref
api_name:
- ProcessTokenSidType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1875da055f2719afca454d225c3bebd13b404b3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120406"
---
# <a name="processtokensidtype-principaltype-element"></a>Elemento ProcessTokenSidType (principalType)

Specifica il tipo di identificazione di sicurezza del processo (SID) dell'attività.

``` syntax
<xs:element name="ProcessTokenSidType"
    type="processTokenSidType"
    maxOccurs="1"
    minOccurs="0"
 />
```

L'elemento **ProcessTokenSidType** è definito dal tipo complesso [**PrincipalType**](taskschedulerschema-principaltype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                  | Derivato da                                                           | Descrizione                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Principale**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Specifica le credenziali di sicurezza per un'entità.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo in C++, il tipo di SID del processo viene specificato tramite la proprietà [**IPrincipal2::P rocesstokensidtype**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal2-get_processtokensidtype) .

## <a name="examples"></a>Esempio

Nel codice XML seguente viene definito il tipo di SID di processo dell'attività.


```XML
<Principal>
    <GroupId>NT AUTHORITY\LOCAL SERVICE</GroupId>
    <ProcessTokenSidType>None</ProcessTokenSidType>
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

 

 





