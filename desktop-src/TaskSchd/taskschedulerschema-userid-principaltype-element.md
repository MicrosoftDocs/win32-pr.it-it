---
title: Elemento UserId (principalType)
description: Specifica l'identificatore utente necessario per eseguire le attività associate all'entità.
ms.assetid: 7f3c92bf-c982-4155-9391-862f674a3665
keywords:
- Elemento UserId Utilità di pianificazione
topic_type:
- apiref
api_name:
- UserId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fe12f76c35238251e2ecc60f848e2f7eb4eaa681
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400932"
---
# <a name="userid-principaltype-element"></a>Elemento UserId (principalType)

Specifica l'identificatore utente necessario per eseguire le attività associate all'entità.

``` syntax
<xs:element name="UserId"
    type="nonEmptyString"
 />
```

L'elemento **userid** è definito dal tipo complesso [**PrincipalType**](taskschedulerschema-principaltype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                  | Derivato da                                                           | Descrizione                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Principale**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Specifica le credenziali di sicurezza per un'entità.<br/> |



## <a name="remarks"></a>Commenti

L'elemento **userid** e l'elemento [**LogonType**](taskschedulerschema-logontype-principaltype-element.md) vengono utilizzati insieme per definire l'utente necessario per eseguire le attività che utilizzano questa entità.

Non è possibile specificare contemporaneamente un identificatore utente e un identificatore di gruppo. Specificare l' **ID utente** o l'elemento [**GroupID**](taskschedulerschema-groupid-principaltype-element.md) , ma non entrambi.

Per lo sviluppo di script, l'identificatore utente viene specificato utilizzando la proprietà [**Principal. UserID**](principal-userid.md) .

Per lo sviluppo in C++, l'identificatore utente viene specificato tramite la proprietà [**IPrincipal:: UserID**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_userid) .

## <a name="examples"></a>Esempio

Il codice XML seguente definisce un principio usando un identificatore utente.


```XML
<Principal>
    <UserId></UserId>
    <LogonType><LogonType>
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

 

 





