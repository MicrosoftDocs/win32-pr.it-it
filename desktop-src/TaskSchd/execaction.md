---
title: Oggetto ExecAction
description: Oggetto di scripting che rappresenta un'azione che esegue un'operazione della riga di comando.
ms.assetid: 51d2746d-3a90-4e8b-ac2b-d73193b3aa74
keywords:
- eseguire l'azione Utilità di pianificazione , interfaccia
- Oggetto ExecAction Utilità di pianificazione
- Oggetto ExecAction Utilità di pianificazione , descritto
topic_type:
- apiref
api_name:
- ExecAction
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 140ff991bd26f779beee7407666572d8649bd9f1a2718b719713770745157656
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072661"
---
# <a name="execaction-object"></a>Oggetto ExecAction

Oggetto di scripting che rappresenta un'azione che esegue un'operazione della riga di comando.

## <a name="members"></a>Membri

**L'oggetto ExecAction** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

**L'oggetto ExecAction** ha queste proprietà.



| Proprietà                                                            | Tipo di accesso           | Descrizione                                                                                                                       |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [**Argomenti**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments)<br/>               | Lettura/Scrittura<br/> | Ottiene o imposta gli argomenti associati all'operazione della riga di comando.<br/>                                                 |
| [**Id**](/windows/desktop/api/taskschd/nf-taskschd-iaction-get_id)<br/>                                 | Lettura/Scrittura<br/> | Ereditato [**dall'oggetto**](action.md) Action. Ottiene o imposta l'identificatore dell'azione.<br/>                         |
| [**Percorso**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_path)<br/>                         | Lettura/Scrittura<br/> | Ottiene o imposta il percorso di un file eseguibile.<br/>                                                                           |
| [**Tipo**](/windows/desktop/api/taskschd/nf-taskschd-iaction-get_type)<br/>                             | Sola lettura<br/>  | Ereditato [**dall'oggetto**](action.md) Action. Ottiene il tipo dell'azione.<br/>                                       |
| [**WorkingDirectory**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta la directory che contiene il file eseguibile o i file utilizzati dal file eseguibile.<br/> |



 

## <a name="remarks"></a>Commenti

Se le variabili di ambiente vengono usate nelle proprietà [**Path**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_path), [**Arguments**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments)o [**WorkingDirectory,**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory) i valori delle variabili di ambiente vengono memorizzati nella cache e usati all'avvio del Taskeng.exe (il motore attività). Le modifiche alle variabili di ambiente che si verificano dopo l'avvio del motore attività non verranno usate dal motore attività.

Questa azione esegue un'operazione della riga di comando. Ad esempio, l'azione potrebbe eseguire uno script o avviare un eseguibile.

Durante la lettura o la scrittura di codice XML, viene specificata un'azione di esecuzione [**nell'elemento Exec**](taskschedulerschema-exec-actiongroup-element.md) dello schema Utilità di pianificazione.

## <a name="examples"></a>Esempio

Per altre informazioni e codice di esempio per questo oggetto di scripting, vedere [Time Trigger Example (Scripting) .](time-trigger-example--scripting-.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





