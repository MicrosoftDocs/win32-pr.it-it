---
title: Elemento Exec (actionGroup)
description: Specifica un'azione che esegue un'operazione della riga di comando.
ms.assetid: 84bdd1ec-4279-4282-b44a-4b5ad30503eb
keywords:
- Utilità di pianificazione elemento Exec
topic_type:
- apiref
api_name:
- Exec
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b29ba66be8f2d3aefaec4f437359f2af5275d2f0
ms.sourcegitcommit: 628fda3e63fd1d513ce9a5f55be8bbc4af4b2a4b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320835"
---
# <a name="exec-actiongroup-element"></a>Elemento Exec (actionGroup)

Specifica un'azione che esegue un'operazione della riga di comando.

``` syntax
<xs:element name="Exec"
    type="execType"
 />
```

L'elemento **Exec** è definito da [**actionGroup**](taskschedulerschema-actiongroup-group.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                         | Derivato da                                                       | Descrizione                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [**Azioni**](taskschedulerschema-actions-tasktype-element.md) | [**actionsType**](taskschedulerschema-actionstype-complextype.md) | Contiene le azioni eseguite dall'attività.<br/> |



## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                           | Tipo       | Descrizione                                                                                                  |
|-----------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------|
| [**Argomenti**](taskschedulerschema-arguments-exectype-element.md)               | **string** | Specifica gli argomenti associati all'operazione della riga di comando.<br/>                               |
| [**Comando**](taskschedulerschema-command-exectype-element.md)                   | **string** | Specifica il file eseguibile o il documento da eseguire.<br/>                                              |
| [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) | string     | Specifica la directory in cui si trova il file eseguibile o i file utilizzati dall'eseguibile.<br/> |



## <a name="attributes"></a>Attributi



| Nome | Tipo       | Descrizione                                                    |
|------|------------|----------------------------------------------------------------|
| id   | **string** | Identificatore dell'azione eseguita dall'attività.<br/> |



## <a name="remarks"></a>Commenti

Gli elementi figlio elencati sopra sono definiti dal tipo complesso [**execType**](taskschedulerschema-exectype-complextype.md) .

Per lo sviluppo di script, un'azione di esecuzione viene definita dall'oggetto [**ExecAction**](execaction.md) .

Per lo sviluppo in C++, un'azione di esecuzione viene definita dall'interfaccia [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) .

Se le variabili di ambiente vengono usate negli elementi [**Command**](taskschedulerschema-command-exectype-element.md), [**arguments**](taskschedulerschema-arguments-exectype-element.md)o [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) , i valori delle variabili di ambiente vengono memorizzati nella cache e usati quando viene avviata la Taskeng.exe (il motore attività). Le modifiche apportate alle variabili di ambiente che si verificano dopo l'avvio del motore attività non verranno usate dal motore delle attività.

## <a name="examples"></a>Esempio

Per un esempio completo del codice XML per un'attività che usa un trigger di evento, vedere [esempio di trigger di ora (XML)](time-trigger-example--xml-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elementi dello schema Utilità di pianificazione](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





