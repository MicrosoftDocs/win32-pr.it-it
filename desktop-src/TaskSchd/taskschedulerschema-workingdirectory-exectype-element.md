---
title: Elemento WorkingDirectory (execType)
description: Specifica la directory in cui si trova il file eseguibile o i file utilizzati dal file eseguibile.
ms.assetid: 09e53748-6d21-42df-bbdd-f0fd9693aab0
keywords:
- Elemento WorkingDirectory Utilità di pianificazione
topic_type:
- apiref
api_name:
- WorkingDirectory
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5a91908d5cd774f19f32a182934688dc899179d1abba967b7871a646efcfe042
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513741"
---
# <a name="workingdirectory-exectype-element"></a>Elemento WorkingDirectory (execType)

Specifica la directory in cui si trova il file eseguibile o i file utilizzati dal file eseguibile.

``` syntax
<xs:element name="WorkingDirectory"
    type="pathType"
 />
```

**L'elemento WorkingDirectory** è definito dal [**tipo complesso execType.**](taskschedulerschema-exectype-complextype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                      | Derivato da                                                 | Descrizione                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------|
| [**Exec**](taskschedulerschema-exec-actiongroup-element.md) | [**execType**](taskschedulerschema-exectype-complextype.md) | Specifica un'azione che esegue un'operazione della riga di comando.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo di script, la directory di lavoro viene specificata dalla [**proprietà ExecAction.WorkingDirectory.**](execaction-workingdirectory.md)

Per lo sviluppo in C++, la directory di lavoro viene specificata dalla [**proprietà IExecAction::WorkingDirectory.**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory)

## <a name="examples"></a>Esempio

Nel codice XML seguente viene definita un'azione di esecuzione.


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
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione di schema](task-scheduler-schema-elements.md)
</dt> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





