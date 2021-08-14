---
title: Elemento Arguments (execType)
description: Specifica gli argomenti associati all'operazione della riga di comando.
ms.assetid: 37207c4f-941c-4cbf-9a81-5876b224a7c1
keywords:
- Elemento Arguments Utilità di pianificazione
topic_type:
- apiref
api_name:
- Arguments
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: edf76f7073e62aac10c85dc035d3b441a90a4e0ee1fae90b4decf5cffc4568df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118132076"
---
# <a name="arguments-exectype-element"></a>Elemento Arguments (execType)

Specifica gli argomenti associati all'operazione della riga di comando.

``` syntax
<xs:element name="Arguments"
    type="string"
 />
```

**L'elemento** Arguments è definito dal [**tipo complesso execType.**](taskschedulerschema-exectype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                      | Derivato da                                                 | Descrizione                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------|
| [**Exec**](taskschedulerschema-exec-actiongroup-element.md) | [**execType**](taskschedulerschema-exectype-complextype.md) | Specifica un'azione che esegue un'operazione della riga di comando.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo C++, vedere la [**proprietà Arguments di IExecAction**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments).

Per lo sviluppo di script, [**vedere ExecAction.Arguments**](execaction-arguments.md).

## <a name="examples"></a>Esempio

Per un esempio completo del codice XML per un'attività che usa un'azione eseguibile, vedere [Esempio di trigger temporale (XML).](time-trigger-example--xml-.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione schema](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





