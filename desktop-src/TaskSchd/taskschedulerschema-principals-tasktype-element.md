---
title: Elemento Principals (taskType)
description: Specifica i contesti di sicurezza che possono essere utilizzati per eseguire l'attività.
ms.assetid: bb46213a-e377-4ed0-9ada-05938fd69c28
keywords:
- Elemento Principals Utilità di pianificazione
topic_type:
- apiref
api_name:
- Principals
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2385d7ff766d72300a402fccfae8eb7338b89f87
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963858"
---
# <a name="principals-tasktype-element"></a>Elemento Principals (taskType)

Specifica i contesti di sicurezza che possono essere utilizzati per eseguire l'attività.

``` syntax
<xs:element name="Principals"
    type="principalsType"
 />
```

L'elemento **Principals** viene definito dal tipo complesso [**TaskType**](taskschedulerschema-tasktype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                          | Derivato da                                                 | Descrizione                                                                  |
|--------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------------|
| [**Attività**](taskschedulerschema-task-element.md) | [**taskType**](taskschedulerschema-tasktype-complextype.md) | Definisce l'attività eseguita dal servizio Utilità di pianificazione.<br/> |



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                  | Tipo                                                                   | Descrizione                                                    |
|--------------------------------------------------------------------------|------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Principale**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Specifica le credenziali di sicurezza per un'entità.<br/> |



## <a name="remarks"></a>Commenti

È possibile specificare fino a 32 entità per un'attività.

Per lo sviluppo di script, le entità di un'attività vengono specificate utilizzando la proprietà [**TaskDefinition. Principal**](taskdefinition-principal.md) .

Per lo sviluppo in C++, le entità di un'attività vengono specificate utilizzando la [**Proprietà Principal di ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_principal).

## <a name="examples"></a>Esempio

Il codice XML seguente definisce due entità: un identificatore utente e un'entità identificatore di gruppo per l'attività.


```XML
<Principals>
    <Principal>
        <UserId></UserId>
        <LogonType><LogonType>
        <DisplayName></DisplayName>
    </Principal>
    <Principal>
        <GroupId></GroupId>
        <DisplayName></DisplayName>
    </Principal>
</Principals>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elementi dello schema Utilità di pianificazione](task-scheduler-schema-elements.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





