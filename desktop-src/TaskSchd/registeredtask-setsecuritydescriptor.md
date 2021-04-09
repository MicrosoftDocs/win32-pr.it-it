---
title: RegisteredTask. SetSecurityDescriptor, metodo
description: Per lo scripting, imposta il descrittore di sicurezza utilizzato come credenziali per l'attività registrata.
ms.assetid: 2dc10df0-5827-4199-940e-865a03a694f5
keywords:
- Utilità di pianificazione del metodo SetSecurityDescriptor
- Metodo SetSecurityDescriptor Utilità di pianificazione, oggetto RegisteredTask
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
ms.openlocfilehash: 386c97c470b94686c0a1f654313c6ef1e0bca5a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121107"
---
# <a name="registeredtasksetsecuritydescriptor-method"></a>RegisteredTask. SetSecurityDescriptor, metodo

Per lo scripting, imposta il descrittore di sicurezza utilizzato come credenziali per l'attività registrata.

## <a name="syntax"></a>Sintassi


```VB
RegisteredTask.SetSecurityDescriptor( _
  ByVal sddl, _
  ByVal flags _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*SDDL* \[ in\]
</dt> <dd>

Descrittore di sicurezza utilizzato come credenziali per l'attività registrata.

> [!Note]  
> Se all'account di sistema locale viene negato l'accesso a un'attività, il servizio Utilità di pianificazione può produrre risultati imprevisti.

 

</dd> <dt>

*flag* \[ in\]
</dt> <dd>

Flag che specificano come impostare il descrittore di sicurezza. \_ \_ È possibile specificare l'attività non aggiungere il \_ \_ flag ACE principale (0x10) dell'enumerazione per la [**\_ creazione di attività**](/windows/desktop/api/taskschd/ne-taskschd-task_creation) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

È possibile specificare l'elenco di controllo di accesso (ACL) nel descrittore di sicurezza per un'attività per consentire o negare a determinati utenti e gruppi l'accesso a un'attività.

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
</dt> <dt>

[**TaskFolder. GetSecurityDescriptor**](taskfolder-getsecuritydescriptor.md)
</dt> <dt>

[**RegisteredTask. SetSecurityDescriptor**](registeredtask-setsecuritydescriptor.md)
</dt> </dl>

 

 





