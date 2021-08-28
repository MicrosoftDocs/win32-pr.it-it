---
title: Elemento LogonType (principalType)
description: Specifica il metodo di accesso di sicurezza necessario per eseguire le attività associate all'entità.
ms.assetid: e36a1755-96f3-45dc-8779-8bd0cfde886c
keywords:
- Elemento LogonType Utilità di pianificazione
topic_type:
- apiref
api_name:
- LogonType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9121179b744857d5e7d0bec5a2ae814c603c6b1c
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885844"
---
# <a name="logontype-principaltype-element"></a>Elemento LogonType (principalType)

Specifica il metodo di accesso di sicurezza necessario per eseguire le attività associate all'entità.

``` syntax
<xs:element name="LogonType"
    type="logonType"
 />
```

**L'elemento LogonType** è definito dal [**tipo complesso principalType.**](taskschedulerschema-principaltype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                  | Derivato da                                                           | Descrizione                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Principale**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Specifica le credenziali di sicurezza per un'entità.<br/> |



## <a name="remarks"></a>Commenti

**L'elemento LogonType** e [**l'elemento UserId**](taskschedulerschema-userid-principaltype-element.md) vengono usati insieme per definire l'utente necessario per eseguire le attività che usano questa entità.

Per lo sviluppo di script, il tipo di accesso per l'entità viene specificato dalla [**proprietà Principal.LogonType.**](principal-logontype.md)

Per lo sviluppo in C++, il tipo di accesso per l'entità viene specificato dalla [**proprietà IPrincipal::LogonType.**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_logontype)

Questo elemento (definito dal tipo [**semplice logonType)**](taskschedulerschema-logontype-simpletype.md) deve avere uno dei valori seguenti.

-   S4U: l'utente deve accedere usando un servizio per l'accesso utente (S4U). Quando si usa un accesso S4U, non viene archiviata alcuna password dal sistema e non è possibile accedere alla rete o ai file crittografati.
-   Password: l'utente deve accedere usando una password.
-   InteractiveToken: l'utente deve essere già connesso. L'attività verrà eseguita solo in una sessione interattiva esistente.

Per un'attività che contiene un'azione della finestra di messaggio, la finestra di messaggio verrà visualizzata se l'attività è attivata e l'attività ha un tipo di accesso interattivo. Per impostare il tipo di accesso dell'attività come interattivo, specificare **InteractiveToken** **&lt; nell'elemento LogonType &gt;** dell'entità attività.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





