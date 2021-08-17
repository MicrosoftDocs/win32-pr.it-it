---
title: Metodo RegisteredTask.SetSecurityDescriptor
description: Per lo scripting, imposta il descrittore di sicurezza usato come credenziali per l'attività registrata.
ms.assetid: 2dc10df0-5827-4199-940e-865a03a694f5
keywords:
- Metodo SetSecurityDescriptor Utilità di pianificazione
- Metodo SetSecurityDescriptor Utilità di pianificazione , oggetto RegisteredTask
- Oggetto RegisteredTask Utilità di pianificazione, metodo SetSecurityDescriptor
topic_type:
- apiref
api_name:
- RegisteredTask.SetSecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7ac6845624ab2032b9b90d742c1346081c3ba4719d0814cfd257d3787c2bf70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117759592"
---
# <a name="registeredtasksetsecuritydescriptor-method"></a>Metodo RegisteredTask.SetSecurityDescriptor

Per lo scripting, imposta il descrittore di sicurezza usato come credenziali per l'attività registrata.

## <a name="syntax"></a>Sintassi


```VB
RegisteredTask.SetSecurityDescriptor( _
  ByVal sddl, _
  ByVal flags _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*sddl* \[ Pollici\]
</dt> <dd>

Descrittore di sicurezza utilizzato come credenziali per l'attività registrata.

> [!Note]  
> Se all'account di sistema locale viene negato l'accesso a un'attività, il servizio Utilità di pianificazione può produrre risultati imprevisti.

 

</dd> <dt>

*flag* \[ Pollici\]
</dt> <dd>

Flag che specificano come impostare il descrittore di sicurezza. È possibile specificare il flag ACE TASK \_ DONT ADD PRINCIPAL \_ \_ \_ (0x10) [**dall'enumerazione TASK \_ CREATION.**](/windows/desktop/api/taskschd/ne-taskschd-task_creation)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

È possibile specificare l'elenco di controllo di accesso (ACL) nel descrittore di sicurezza per un'attività per consentire o negare a determinati utenti e gruppi l'accesso a un'attività.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RegisteredTask**](registeredtask.md)
</dt> <dt>

[**TaskFolder.GetSecurityDescriptor**](taskfolder-getsecuritydescriptor.md)
</dt> <dt>

[**RegisteredTask.SetSecurityDescriptor**](registeredtask-setsecuritydescriptor.md)
</dt> </dl>

 

 





