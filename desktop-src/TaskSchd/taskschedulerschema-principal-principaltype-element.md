---
title: Elemento Principal (principalType)
description: Specifica le credenziali di sicurezza per un'entità.
ms.assetid: 4ba65976-98d2-4329-80f0-566fac2e9fda
keywords:
- Utilità di pianificazione elemento principale
topic_type:
- apiref
api_name:
- Principal
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 41d308af651f1aff0ff402c7070adbe631bff9eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301150"
---
# <a name="principal-principaltype-element"></a>Elemento Principal (principalType)

Specifica le credenziali di sicurezza per un'entità. Queste credenziali definiscono il contesto di sicurezza in cui viene eseguita un'attività.

``` syntax
<xs:element name="Principal"
    type="principalType"
 />
```

L'elemento **Principal** è definito dal tipo complesso [**PrincipalType**](taskschedulerschema-principaltype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                               | Derivato da                                                             | Descrizione                                                            |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**Entità**](taskschedulerschema-principals-tasktype-element.md) | [**principalsType**](taskschedulerschema-principalstype-complextype.md) | Specifica le entità di sicurezza associate all'attività.<br/> |



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                      | Tipo                                                          | Descrizione                                                                                                |
|------------------------------------------------------------------------------|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**DisplayName**](taskschedulerschema-displayname-principaltype-element.md) | **string**                                                    | Specifica il nome dell'entità visualizzata nell'interfaccia utente di Utilità di pianificazione.<br/>                 |
| [**GroupId**](taskschedulerschema-groupid-principaltype-element.md)         | **string**                                                    | Specifica l'identificatore del gruppo di utenti necessario per eseguire le attività associate all'entità.<br/> |
| [**LogonType**](taskschedulerschema-logontype-principaltype-element.md)     | [**logonType**](taskschedulerschema-logontype-simpletype.md) | Specifica il metodo di accesso di sicurezza necessario per eseguire le attività associate all'entità.<br/>  |
| [**UserId**](taskschedulerschema-userid-principaltype-element.md)           | **string**                                                    | Specifica l'identificatore utente necessario per eseguire le attività associate all'entità.<br/>              |



## <a name="attributes"></a>Attributi



| Nome | Tipo | Descrizione                                        |
|------|------|----------------------------------------------------|
| Id   | ID   | Identificatore della definizione dell'entità.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo di script, le credenziali di sicurezza per un'entità vengono specificate utilizzando l'oggetto [**Principal**](principal.md) .

Per lo sviluppo in C++, le credenziali di sicurezza per un'entità vengono specificate tramite l'interfaccia [**IPrincipal**](/windows/desktop/api/taskschd/nn-taskschd-iprincipal) .

Gli elementi figlio elencati sopra sono definiti dal tipo complesso [**PrincipalType**](taskschedulerschema-principaltype-complextype.md) . Per informazioni sulla sequenziazione di questi elementi figlio, vedere [**PrincipalType**](taskschedulerschema-principaltype-complextype.md).

## <a name="examples"></a>Esempio

Il codice XML seguente definisce un'entità con un identificatore utente.


```XML
<Principals>
    <Principal>
        <UserId></UserId>
        <LogonType><LogonType>
        <DisplayName></DisplayName>
    </Principal>
</Principals>
```



Il codice XML seguente definisce un'entità con un identificatore di gruppo.


```XML
<Principals>
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

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





