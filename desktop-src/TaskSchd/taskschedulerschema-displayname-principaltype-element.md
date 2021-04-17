---
title: Elemento DisplayName (principalType)
description: Specifica il nome dell'entità visualizzata nell'interfaccia utente di Utilità di pianificazione.
ms.assetid: a8640cc9-fc16-4e73-9f0c-1ebff338fb84
keywords:
- Elemento DisplayName Utilità di pianificazione
topic_type:
- apiref
api_name:
- DisplayName
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e8ef310869ea8558bca231e866ddeefc0dc35944
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519134"
---
# <a name="displayname-principaltype-element"></a>Elemento DisplayName (principalType)

Specifica il nome dell'entità visualizzata nell'interfaccia utente di Utilità di pianificazione.

``` syntax
<xs:element name="DisplayName"
    type="string"
 />
```

L'elemento **DisplayName** è definito dal tipo complesso [**PrincipalType**](taskschedulerschema-principaltype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                  | Derivato da                                                           | Descrizione                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Principale**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Specifica le credenziali di sicurezza per un'entità.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo di script, il nome visualizzato dell'entità viene specificato utilizzando la proprietà [**Principal. DisplayName**](principal-displayname.md) .

Per lo sviluppo in C++, il nome visualizzato dell'entità viene specificato tramite la proprietà [**IPrincipal::D**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_displayname) la proprietà.

## <a name="examples"></a>Esempio

Nel codice XML seguente viene definito un oggetto utilizzando un identificatore di gruppo e un nome visualizzato.


```XML
<Principal>
    <GroupId></GroupId>
    <DisplayName></DisplayName>
 </Principal>
```



Il codice XML seguente definisce un'entità usando un identificatore utente e un nome visualizzato.


```XML
<Principal>
    <UserId></UserId>
    <LogonType></LogonType>
    <DisplayName></DisplayName>
 </Principal>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





