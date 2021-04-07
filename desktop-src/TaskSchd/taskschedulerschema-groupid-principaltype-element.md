---
title: Elemento GroupId (principalType)
description: Specifica l'identificatore del gruppo di utenti necessario per eseguire le attività associate all'entità.
ms.assetid: 1e576c31-79a9-42d4-b497-74412e464d60
keywords:
- Utilità di pianificazione elemento GroupId
topic_type:
- apiref
api_name:
- GroupId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 080a408f65ac7a36ada1751bbd5cb95395cf0b35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048627"
---
# <a name="groupid-principaltype-element"></a>Elemento GroupId (principalType)

Specifica l'identificatore del gruppo di utenti necessario per eseguire le attività associate all'entità.

``` syntax
<xs:element name="GroupId"
    type="nonEmptyString"
 />
```

L'elemento **GroupID** è definito dal tipo complesso [**PrincipalType**](taskschedulerschema-principaltype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                  | Derivato da                                                           | Descrizione                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Principale**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Specifica le credenziali di sicurezza per un'entità.<br/> |



## <a name="remarks"></a>Commenti

Non è possibile specificare contemporaneamente un identificatore di gruppo e un identificatore utente. Specificare gli elementi [**userid**](taskschedulerschema-userid-principaltype-element.md) o **GroupID** , ma non entrambi.

Per lo sviluppo di script, l'identificatore di gruppo dell'entità viene specificato utilizzando la proprietà [**Principal. GroupID**](principal-groupid.md) .

Per lo sviluppo in C++, l'identificatore di gruppo dell'entità viene specificato tramite la proprietà [**IPrincipal:: GroupID**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_groupid) .

## <a name="examples"></a>Esempio

Per un esempio completo del codice XML per un'attività che usa questo elemento, vedere [esempio di trigger LOGON (XML)](logon-trigger-example--xml-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





