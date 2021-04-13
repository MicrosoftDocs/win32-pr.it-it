---
title: Arguments (execType)-elemento
description: Specifica gli argomenti associati all'operazione della riga di comando.
ms.assetid: 37207c4f-941c-4cbf-9a81-5876b224a7c1
keywords:
- Elemento arguments Utilità di pianificazione
topic_type:
- apiref
api_name:
- Arguments
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ff35465fbad1de82d096b583499ea6cdafe93ca7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518195"
---
# <a name="arguments-exectype-element"></a>Arguments (execType)-elemento

Specifica gli argomenti associati all'operazione della riga di comando.

``` syntax
<xs:element name="Arguments"
    type="string"
 />
```

L'elemento **arguments** è definito dal tipo complesso [**execType**](taskschedulerschema-exectype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                      | Derivato da                                                 | Descrizione                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------|
| [**Exec**](taskschedulerschema-exec-actiongroup-element.md) | [**execType**](taskschedulerschema-exectype-complextype.md) | Specifica un'azione che esegue un'operazione della riga di comando.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo in C++, vedere la [**proprietà Arguments di IExecAction**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments).

Per lo sviluppo di script, vedere [**ExecAction. Arguments**](execaction-arguments.md).

## <a name="examples"></a>Esempio

Per un esempio completo del codice XML per un'attività che usa un'azione eseguibile, vedere [esempio di trigger temporale (XML)](time-trigger-example--xml-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elementi dello schema Utilità di pianificazione](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





