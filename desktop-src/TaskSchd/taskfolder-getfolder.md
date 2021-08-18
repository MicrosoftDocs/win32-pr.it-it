---
title: TaskFolder.GetFolder - proprietà
description: Per lo scripting, ottiene una cartella che contiene attività in un percorso specificato.
ms.assetid: 73e60b10-7a8c-4b07-9f8c-be7715f4e032
keywords:
- Proprietà GetFolder Utilità di pianificazione
- Proprietà GetFolder Utilità di pianificazione , oggetto TaskFolder
- Oggetto TaskFolder Utilità di pianificazione proprietà , GetFolder
topic_type:
- apiref
api_name:
- TaskFolder.GetFolder
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7668b2486a316fe2bf799762401459ec7da2602ff52a4d5d3dc9ddb4dd888e61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117758984"
---
# <a name="taskfoldergetfolder-property"></a>TaskFolder.GetFolder - proprietà

Per lo scripting, ottiene una cartella che contiene attività in un percorso specificato.

## <a name="syntax"></a>Sintassi


```VB
TaskFolder.GetFolder( _
  ByVal path _
)
```



## <a name="property-value"></a>Valore proprietà

Percorso (percorso) della cartella. Non usare una barra rovesciata dopo l'ultimo nome di cartella nel percorso. La cartella dell'attività radice viene specificata con una barra rovesciata ( \\ ). Un esempio di percorso di cartella di attività, nella cartella dell'attività radice, è \\ MyTaskFolder. Il carattere '.' non può essere usato per specificare la cartella dell'attività corrente e '.'. Non è possibile usare caratteri per specificare la cartella dell'attività padre nel percorso.

## <a name="error-codes"></a>Codici di errore

Cartella nel percorso specificato. La cartella è un [**oggetto TaskFolder.**](taskfolder.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





