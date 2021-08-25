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
ms.openlocfilehash: 955dcc93b826b4f86bffd3371ab9907e56dfe7f35649aee603cb18716868f535
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959531"
---
# <a name="userid-principaltype-element"></a>Elemento UserId (principalType)

Specifica l'identificatore utente necessario per eseguire le attività associate all'entità.

``` syntax
<xs:element name="UserId"
    type="nonEmptyString"
 />
```

**L'elemento UserId** è definito dal [**tipo complesso principalType.**](taskschedulerschema-principaltype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                  | Derivato da                                                           | Descrizione                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Principale**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Specifica le credenziali di sicurezza per un'entità.<br/> |



## <a name="remarks"></a>Commenti

**L'elemento UserId** e [**l'elemento LogonType**](taskschedulerschema-logontype-principaltype-element.md) vengono usati insieme per definire l'utente necessario per eseguire le attività che usano questa entità.

Non è possibile specificare contemporaneamente un identificatore utente e un identificatore di gruppo. Specificare **l'elemento UserId** o [**GroupId,**](taskschedulerschema-groupid-principaltype-element.md) ma non entrambi.

Per lo sviluppo di script, l'identificatore utente viene specificato usando la [**proprietà Principal.UserId.**](principal-userid.md)

Per lo sviluppo in C++, l'identificatore utente viene specificato usando la [**proprietà IPrincipal::UserId.**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_userid)

## <a name="examples"></a>Esempio

Nel codice XML seguente viene definito un principio utilizzando un identificatore utente.


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
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





