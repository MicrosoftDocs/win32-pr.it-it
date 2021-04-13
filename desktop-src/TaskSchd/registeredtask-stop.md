---
title: Metodo RegisteredTask. Stop
description: Per lo scripting, arresta immediatamente l'attività registrata.
ms.assetid: e4a533d8-5cf0-46ba-a603-f7a9c59ab0fd
keywords:
- Metodo Stop Utilità di pianificazione
- Metodo Stop Utilità di pianificazione, oggetto RegisteredTask
- Oggetto RegisteredTask Utilità di pianificazione, metodo Stop
topic_type:
- apiref
api_name:
- RegisteredTask.Stop
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2d51cf748bb65a9db38c56fded102ddeb5b40fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400888"
---
# <a name="registeredtaskstop-method"></a>Metodo RegisteredTask. Stop

Per lo scripting, arresta immediatamente l'attività registrata.

## <a name="syntax"></a>Sintassi


```VB
RegisteredTask.Stop( _
  ByVal flags _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*flag* \[ in\]
</dt> <dd>

Riservato. Deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

La funzione **RegisteredTask. Stop** arresta tutte le istanze dell'attività.

Gli utenti dell'account di sistema possono arrestare un'attività, gli utenti con privilegi di gruppo amministratori possono arrestare un'attività e se un utente dispone dei diritti per eseguire e leggere un'attività, l'utente può arrestare l'attività. Un utente può arrestare le istanze dell'attività in esecuzione con le stesse credenziali dell'account utente. In tutti gli altri casi, all'utente viene negato l'accesso per arrestare l'attività.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RegisteredTask**](registeredtask.md)
</dt> </dl>

 

 





