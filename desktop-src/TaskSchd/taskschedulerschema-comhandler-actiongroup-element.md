---
title: Elemento comhandler (actionGroup)
description: Specifica un'azione che attiva un gestore.
ms.assetid: 18f16873-3879-4a3b-b8f2-17cc84647e25
keywords:
- Elemento comhandler Utilità di pianificazione
topic_type:
- apiref
api_name:
- ComHandler
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2269464efb09e8c513ab2bdebb24744a6b32a671
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964675"
---
# <a name="comhandler-actiongroup-element"></a>Elemento comhandler (actionGroup)

Specifica un'azione che attiva un gestore.

``` syntax
<xs:element name="ComHandler"
    type="comHandlerType"
 />
```

L'elemento **Comhandler** è definito da [**actionGroup**](taskschedulerschema-actiongroup-group.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                         | Derivato da                                                       | Descrizione                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [**Azioni**](taskschedulerschema-actions-tasktype-element.md) | [**actionsType**](taskschedulerschema-actionstype-complextype.md) | Contiene le azioni eseguite dall'attività.<br/> |



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                               | Tipo                                                         | Descrizione                                                       |
|-----------------------------------------------------------------------|--------------------------------------------------------------|-------------------------------------------------------------------|
| [**ClassId**](taskschedulerschema-classid-comhandlertype-element.md) | [**guidType**](taskschedulerschema-guidtype-simpletype.md)  | Specifica l'identificatore della classe del gestore.<br/>         |
| [**Data**](taskschedulerschema-data-comhandlertype-element.md)       | [**dataType**](taskschedulerschema-datatype-complextype.md) | Specifica i dati aggiuntivi associati al gestore.<br/> |



## <a name="remarks"></a>Commenti

Le applicazioni definiscono un'azione del gestore COM usando l'interfaccia [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) .

### <a name="attributes"></a>Attributi

L'attributo seguente viene definito dal tipo complesso [**actionBaseType**](taskschedulerschema-actionbasetype-complextype.md) .

-   ID: identificatore dell'azione eseguita dall'attività.

## <a name="examples"></a>Esempio

Il codice XML seguente definisce un'azione del gestore COM.


```XML
<Actions>
    <ComHandler>
        <ClassId></ClassId>
        <Data></Data>
    </ComHandler>
</Actions>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elementi dello schema Utilità di pianificazione](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





