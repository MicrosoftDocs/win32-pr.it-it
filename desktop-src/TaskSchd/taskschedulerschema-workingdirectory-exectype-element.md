---
title: Elemento WorkingDirectory (execType)
description: Specifica la directory in cui si trova il file eseguibile o i file utilizzati dall'eseguibile.
ms.assetid: 09e53748-6d21-42df-bbdd-f0fd9693aab0
keywords:
- Utilità di pianificazione elemento WorkingDirectory
topic_type:
- apiref
api_name:
- WorkingDirectory
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e8c382d0e60b16d85fbc86f7579a0e700d3dd30b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302674"
---
# <a name="workingdirectory-exectype-element"></a>Elemento WorkingDirectory (execType)

Specifica la directory in cui si trova il file eseguibile o i file utilizzati dall'eseguibile.

``` syntax
<xs:element name="WorkingDirectory"
    type="pathType"
 />
```

L'elemento **WorkingDirectory** è definito dal tipo complesso [**execType**](taskschedulerschema-exectype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                      | Derivato da                                                 | Descrizione                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------|
| [**Exec**](taskschedulerschema-exec-actiongroup-element.md) | [**execType**](taskschedulerschema-exectype-complextype.md) | Specifica un'azione che esegue un'operazione della riga di comando.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo di script, la directory di lavoro viene specificata dalla proprietà [**ExecAction. WorkingDirectory**](execaction-workingdirectory.md) .

Per lo sviluppo in C++, la directory di lavoro viene specificata dalla proprietà [**IExecAction:: WorkingDirectory**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory) .

## <a name="examples"></a>Esempio

Il codice XML seguente definisce un'azione di esecuzione.


```XML
<Exec>
    <Command></Command>
    <Arguments></Arguments>
    <WorkingDirectory></WorkingDirectory>
</ServiceResume>
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

 

 





