---
title: TaskFolder.GetSecurityDescriptor - proprietà
description: Per lo scripting, ottiene il descrittore di sicurezza per la cartella.
ms.assetid: ebf8dc7f-32b7-45bf-9ee5-36df674a1530
keywords:
- Proprietà GetSecurityDescriptor Utilità di pianificazione
- Proprietà GetSecurityDescriptor Utilità di pianificazione , oggetto TaskFolder
- Oggetto TaskFolder Utilità di pianificazione proprietà , GetSecurityDescriptor
topic_type:
- apiref
api_name:
- TaskFolder.GetSecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 851565299b7e6d1c29e2e53d87fb27aa30297921cc194f3cce753fc8d22a6bc6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080321"
---
# <a name="taskfoldergetsecuritydescriptor-property"></a>TaskFolder.GetSecurityDescriptor - proprietà

Per lo scripting, ottiene il descrittore di sicurezza per la cartella.

## <a name="syntax"></a>Sintassi


```VB
TaskFolder.GetSecurityDescriptor( _
  ByVal securityInformation, _
  ByRef pSddl _
)
```



## <a name="property-value"></a>Valore proprietà

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TaskFolder.SetSecurityDescriptor**](taskfolder-setsecuritydescriptor.md)
</dt> <dt>

[**RegisteredTask.SetSecurityDescriptor**](registeredtask-setsecuritydescriptor.md)
</dt> </dl>

 

 





