---
title: Elemento ComHandler (actionGroup)
description: Specifica un'azione che genera un gestore.
ms.assetid: 18f16873-3879-4a3b-b8f2-17cc84647e25
keywords:
- Elemento ComHandler Utilità di pianificazione
topic_type:
- apiref
api_name:
- ComHandler
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: aba73244c3dc5217bcfe7350462200cd3226f0607c6d68ce5c6bcb8f5574b7df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117943238"
---
# <a name="comhandler-actiongroup-element"></a>Elemento ComHandler (actionGroup)

Specifica un'azione che genera un gestore.

``` syntax
<xs:element name="ComHandler"
    type="comHandlerType"
 />
```

**L'elemento ComHandler** è definito da [**actionGroup**](taskschedulerschema-actiongroup-group.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                         | Derivato da                                                       | Descrizione                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [**Azioni**](taskschedulerschema-actions-tasktype-element.md) | [**actionsType**](taskschedulerschema-actionstype-complextype.md) | Contiene le azioni eseguite dall'attività.<br/> |



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                               | Tipo                                                         | Descrizione                                                       |
|-----------------------------------------------------------------------|--------------------------------------------------------------|-------------------------------------------------------------------|
| [**Classid**](taskschedulerschema-classid-comhandlertype-element.md) | [**guidType**](taskschedulerschema-guidtype-simpletype.md)  | Specifica l'identificatore della classe del gestore.<br/>         |
| [**Dati**](taskschedulerschema-data-comhandlertype-element.md)       | [**dataType**](taskschedulerschema-datatype-complextype.md) | Specifica dati aggiuntivi associati al gestore.<br/> |



## <a name="remarks"></a>Commenti

Le applicazioni definiscono un'azione del gestore COM usando [**l'interfaccia IComHandlerAction.**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction)

### <a name="attributes"></a>Attributi

L'attributo seguente è definito dal [**tipo complesso actionBaseType.**](taskschedulerschema-actionbasetype-complextype.md)

-   ID: identificatore dell'azione eseguita dall'attività.

## <a name="examples"></a>Esempio

Nel codice XML seguente viene definita un'azione del gestore COM.


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
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione di schema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





