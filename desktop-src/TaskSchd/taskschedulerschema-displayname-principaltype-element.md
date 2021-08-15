---
title: Elemento DisplayName (principalType)
description: Specifica il nome dell'entità visualizzata nell'interfaccia Utilità di pianificazione interfaccia utente.
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
ms.openlocfilehash: 0ff653a2b2991622b2446bcc0fc74d7063319c2bb6b45556313034a3afb42480
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118356914"
---
# <a name="displayname-principaltype-element"></a>Elemento DisplayName (principalType)

Specifica il nome dell'entità visualizzata nell'interfaccia Utilità di pianificazione interfaccia utente.

``` syntax
<xs:element name="DisplayName"
    type="string"
 />
```

**L'elemento DisplayName** è definito dal [**tipo complesso principalType.**](taskschedulerschema-principaltype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                  | Derivato da                                                           | Descrizione                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Principale**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Specifica le credenziali di sicurezza per un'entità.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo di script, il nome visualizzato dell'entità viene specificato tramite la [**proprietà Principal.DisplayName.**](principal-displayname.md)

Per lo sviluppo C++, il nome visualizzato dell'entità viene specificato usando la proprietà [**IPrincipal::D isplayName.**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_displayname)

## <a name="examples"></a>Esempio

Il codice XML seguente definisce un oggetto usando un identificatore di gruppo e un nome visualizzato.


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
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





