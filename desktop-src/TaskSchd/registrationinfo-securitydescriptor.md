---
title: RegistrationInfo.SecurityDescriptor - proprietà
description: Per lo scripting, ottiene o imposta il descrittore di sicurezza dell'attività.
ms.assetid: e03607f0-c2a0-4aa1-a2b0-915b03aae968
keywords:
- Proprietà SecurityDescriptor Utilità di pianificazione
- Proprietà SecurityDescriptor Utilità di pianificazione, oggetto RegistrationInfo
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
ms.openlocfilehash: c5c3aa83bc05952007d9114ad9812068de5b5b0bd82a4ce9e14e4d5ba1025bb2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117759562"
---
# <a name="registrationinfosecuritydescriptor-property"></a>RegistrationInfo.SecurityDescriptor - proprietà

Per lo scripting, ottiene o imposta il descrittore di sicurezza dell'attività. Se durante la registrazione dell'attività viene fornito un descrittore di sicurezza diverso, questo sostituisce il descrittore di sicurezza impostato con questa proprietà.

## <a name="syntax"></a>Sintassi


```VB
RegistrationInfo.SecurityDescriptor As String
```



## <a name="property-value"></a>Valore proprietà

Descrittore di sicurezza associato all'attività.

## <a name="remarks"></a>Commenti

Durante la lettura o la scrittura di codice XML per un'attività, il descrittore di sicurezza dell'attività viene specificato utilizzando [**l'elemento SecurityDescriptor**](taskschedulerschema-securitydescriptor-registrationinfotype-element.md) dello schema Utilità di pianificazione sicurezza.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Utilità di pianificazione](task-scheduler-start-page.md)
</dt> </dl>

 

 





