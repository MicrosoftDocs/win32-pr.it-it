---
title: Metodo RegisteredTask.Stop
description: Per lo scripting, arresta immediatamente l'attività registrata.
ms.assetid: e4a533d8-5cf0-46ba-a603-f7a9c59ab0fd
keywords:
- Arrestare l'Utilità di pianificazione
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
ms.openlocfilehash: 0496a3b9c8adad0ad4095b6c8aed3888940fd699750350117f4bf503c442f4c8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681661"
---
# <a name="registeredtaskstop-method"></a>Metodo RegisteredTask.Stop

Per lo scripting, arresta immediatamente l'attività registrata.

## <a name="syntax"></a>Sintassi


```VB
RegisteredTask.Stop( _
  ByVal flags _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*flag* \[ Pollici\]
</dt> <dd>

Riservato. Deve essere zero.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

La **funzione RegisteredTask.Stop** arresta tutte le istanze dell'attività.

Gli utenti dell'account di sistema possono arrestare un'attività, gli utenti con privilegi di gruppo Amministratore possono arrestare un'attività e, se un utente dispone dei diritti per eseguire e leggere un'attività, l'utente può arrestare l'attività. Un utente può arrestare le istanze dell'attività in esecuzione con le stesse credenziali dell'account utente. In tutti gli altri casi, all'utente viene negato l'accesso per arrestare l'attività.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RegisteredTask**](registeredtask.md)
</dt> </dl>

 

 





