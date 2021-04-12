---
title: Command (execType)-elemento
description: Specifica il file eseguibile o il documento da eseguire.
ms.assetid: dedf8627-926c-43c6-8add-21ff298d697a
keywords:
- Utilità di pianificazione dell'elemento Command
topic_type:
- apiref
api_name:
- Command
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c9d27eb5b40d652035882efc311d9735bcbdd23e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400833"
---
# <a name="command-exectype-element"></a>Command (execType)-elemento

Specifica il file eseguibile o il documento da eseguire.

``` syntax
<xs:element name="Command"
    type="pathType"
 />
```

L'elemento **Command** è definito dal tipo complesso [**execType**](taskschedulerschema-exectype-complextype.md) .

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

 

 





