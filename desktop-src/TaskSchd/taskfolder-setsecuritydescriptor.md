---
title: TaskFolder.SetSecurityDescriptor - proprietà
description: Per lo scripting, imposta il descrittore di sicurezza per la cartella.
ms.assetid: 50649100-08f6-4c2e-b084-7cfcf9f78e09
keywords:
- Impostazione della proprietà SetSecurityDescriptor Utilità di pianificazione
- Proprietà SetSecurityDescriptor Utilità di pianificazione, oggetto TaskFolder
- Oggetto TaskFolder Utilità di pianificazione, proprietà SetSecurityDescriptor
topic_type:
- apiref
api_name:
- TaskFolder.SetSecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8416e14a5415de86f8ad3f4a1181ce231ecfbdc875e36e9e3fd14014de8c4935
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033791"
---
# <a name="taskfoldersetsecuritydescriptor-property"></a>TaskFolder.SetSecurityDescriptor - proprietà

Per lo scripting, imposta il descrittore di sicurezza per la cartella.

## <a name="syntax"></a>Sintassi


```VB
TaskFolder.SetSecurityDescriptor( _
  ByVal sddl, _
  ByVal flags _
)
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti

È possibile specificare l'elenco di controllo di accesso (ACL) nel descrittore di sicurezza per una cartella attività per consentire o negare a determinati utenti e gruppi l'accesso a una cartella attività.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RegisteredTask.SetSecurityDescriptor**](registeredtask-setsecuritydescriptor.md)
</dt> <dt>

[**TaskFolder.GetSecurityDescriptor**](taskfolder-getsecuritydescriptor.md)
</dt> </dl>

 

 





