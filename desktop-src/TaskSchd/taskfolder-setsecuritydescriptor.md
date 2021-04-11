---
title: Proprietà TaskFolder. SetSecurityDescriptor
description: Per lo scripting, imposta il descrittore di sicurezza per la cartella.
ms.assetid: 50649100-08f6-4c2e-b084-7cfcf9f78e09
keywords:
- Utilità di pianificazione proprietà SetSecurityDescriptor
- Utilità di pianificazione proprietà SetSecurityDescriptor, oggetto TaskFolder
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
ms.openlocfilehash: d0854ee6485007e1465dd0a264c908d67443f248
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963987"
---
# <a name="taskfoldersetsecuritydescriptor-property"></a>Proprietà TaskFolder. SetSecurityDescriptor

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
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**RegisteredTask. SetSecurityDescriptor**](registeredtask-setsecuritydescriptor.md)
</dt> <dt>

[**TaskFolder. GetSecurityDescriptor**](taskfolder-getsecuritydescriptor.md)
</dt> </dl>

 

 





