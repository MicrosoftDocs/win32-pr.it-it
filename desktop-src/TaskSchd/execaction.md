---
title: Oggetto ExecAction
description: Oggetto di scripting che rappresenta un'azione che esegue un'operazione della riga di comando.
ms.assetid: 51d2746d-3a90-4e8b-ac2b-d73193b3aa74
keywords:
- Esegui Utilità di pianificazione azione, interfaccia
- Utilità di pianificazione oggetto ExecAction
- Oggetto ExecAction Utilità di pianificazione, descritto
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
ms.openlocfilehash: cddd1b9b44612b4ce896fb3ceb99a6deeaa5e3a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121111"
---
# <a name="execaction-object"></a>Oggetto ExecAction

Oggetto di scripting che rappresenta un'azione che esegue un'operazione della riga di comando.

## <a name="members"></a>Membri

L'oggetto **ExecAction** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'oggetto **ExecAction** dispone di queste proprietà.



| Proprietà                                                            | Tipo di accesso           | Descrizione                                                                                                                       |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [**Argomenti**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments)<br/>               | Lettura/Scrittura<br/> | Ottiene o imposta gli argomenti associati all'operazione della riga di comando.<br/>                                                 |
| [**ID**](/windows/desktop/api/taskschd/nf-taskschd-iaction-get_id)<br/>                                 | Lettura/Scrittura<br/> | Ereditato dall'oggetto [**azione**](action.md) . Ottiene o imposta l'identificatore dell'azione.<br/>                         |
| [**Percorso**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_path)<br/>                         | Lettura/Scrittura<br/> | Ottiene o imposta il percorso di un file eseguibile.<br/>                                                                           |
| [**Tipo**](/windows/desktop/api/taskschd/nf-taskschd-iaction-get_type)<br/>                             | Sola lettura<br/>  | Ereditato dall'oggetto [**azione**](action.md) . Ottiene il tipo dell'azione.<br/>                                       |
| [**WorkingDirectory**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory)<br/> | Lettura/Scrittura<br/> | Ottiene o imposta la directory che contiene il file eseguibile o i file utilizzati dal file eseguibile.<br/> |



 

## <a name="remarks"></a>Commenti

Se le variabili di ambiente vengono usate nelle proprietà [**path**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_path), [**arguments**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments)o [**WorkingDirectory**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory) , i valori delle variabili di ambiente vengono memorizzati nella cache e usati quando viene avviata la Taskeng.exe (il motore attività). Le modifiche apportate alle variabili di ambiente che si verificano dopo l'avvio del motore attività non verranno usate dal motore delle attività.

Questa azione esegue un'operazione della riga di comando. Ad esempio, l'azione potrebbe eseguire uno script o avviare un file eseguibile.

Durante la lettura o la scrittura di codice XML, un'azione di esecuzione viene specificata nell'elemento [**Exec**](taskschedulerschema-exec-actiongroup-element.md) dello schema utilità di pianificazione.

## <a name="examples"></a>Esempio

Per ulteriori informazioni e codice di esempio per questo oggetto di scripting, vedere [esempio di trigger di ora (scripting)](time-trigger-example--scripting-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





