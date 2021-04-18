---
title: Elemento LogonType (principalType)
description: Specifica il metodo di accesso di sicurezza necessario per eseguire le attività associate all'entità.
ms.assetid: e36a1755-96f3-45dc-8779-8bd0cfde886c
keywords:
- Utilità di pianificazione elemento LogonType
topic_type:
- apiref
api_name:
- LogonType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4a382225f526f18731b8b9f0541e617cb31dfb4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301239"
---
# <a name="logontype-principaltype-element"></a>Elemento LogonType (principalType)

Specifica il metodo di accesso di sicurezza necessario per eseguire le attività associate all'entità.

``` syntax
<xs:element name="LogonType"
    type="logonType"
 />
```

L'elemento **LogonType** è definito dal tipo complesso [**PrincipalType**](taskschedulerschema-principaltype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                  | Derivato da                                                           | Descrizione                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Principale**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Specifica le credenziali di sicurezza per un'entità.<br/> |



## <a name="remarks"></a>Commenti

L'elemento **LogonType** e l'elemento [**userid**](taskschedulerschema-userid-principaltype-element.md) vengono utilizzati insieme per definire l'utente necessario per eseguire le attività che utilizzano questa entità.

Per lo sviluppo di script, il tipo di accesso per l'entità viene specificato dalla proprietà [**Principal. LogonType**](principal-logontype.md) .

Per lo sviluppo in C++, il tipo di accesso per l'entità viene specificato dalla proprietà [**IPrincipal:: LogonType**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_logontype) .

Questo elemento (definito dal tipo semplice [**LogonType**](taskschedulerschema-logontype-simpletype.md) ) deve avere uno dei valori seguenti.

-   S4U: l'utente deve accedere utilizzando un servizio per l'accesso utente (S4U). Quando si usa un accesso S4U, nessuna password viene archiviata dal sistema e non è possibile accedere alla rete o ai file crittografati.
-   Password: l'utente deve accedere usando una password.
-   InteractiveToken: l'utente deve essere già connesso. L'attività verrà eseguita solo in una sessione interattiva esistente.

Per un'attività che contiene un'azione della finestra di messaggio, la finestra di messaggio verrà visualizzata se l'attività è attivata e l'attività dispone di un tipo di accesso interattivo. Per impostare il tipo di accesso dell'attività in modo che sia interattivo, specificare **InteractiveToken** nell' **<LogonType>** elemento dell'entità attività.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





