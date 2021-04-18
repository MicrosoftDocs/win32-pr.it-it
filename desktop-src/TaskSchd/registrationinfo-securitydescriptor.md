---
title: Proprietà RegistrationInfo. SecurityDescriptor
description: Per lo scripting, ottiene o imposta il descrittore di sicurezza dell'attività.
ms.assetid: e03607f0-c2a0-4aa1-a2b0-915b03aae968
keywords:
- Utilità di pianificazione proprietà SecurityDescriptor
- Utilità di pianificazione proprietà SecurityDescriptor, oggetto RegistrationInfo
- Oggetto RegistrationInfo Utilità di pianificazione, proprietà SecurityDescriptor
topic_type:
- apiref
api_name:
- RegistrationInfo.SecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 379e42f41387a40b160a73ec3457d3d5b9feaf59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106300938"
---
# <a name="registrationinfosecuritydescriptor-property"></a>Proprietà RegistrationInfo. SecurityDescriptor

Per lo scripting, ottiene o imposta il descrittore di sicurezza dell'attività. Se durante la registrazione dell'attività viene fornito un descrittore di sicurezza diverso, il descrittore di sicurezza impostato con questa proprietà verrà sostituito.

## <a name="syntax"></a>Sintassi


```VB
RegistrationInfo.SecurityDescriptor As String
```



## <a name="property-value"></a>Valore proprietà

Descrittore di sicurezza associato all'attività.

## <a name="remarks"></a>Commenti

Durante la lettura o la scrittura di codice XML per un'attività, il descrittore di sicurezza dell'attività viene specificato utilizzando l'elemento [**securityDescriptor**](taskschedulerschema-securitydescriptor-registrationinfotype-element.md) dello schema utilità di pianificazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





