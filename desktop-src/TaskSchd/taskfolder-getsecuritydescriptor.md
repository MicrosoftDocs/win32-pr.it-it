---
title: Proprietà TaskFolder. GetSecurityDescriptor
description: Per la creazione di script, ottiene il descrittore di sicurezza per la cartella.
ms.assetid: ebf8dc7f-32b7-45bf-9ee5-36df674a1530
keywords:
- Utilità di pianificazione proprietà GetSecurityDescriptor
- Utilità di pianificazione proprietà GetSecurityDescriptor, oggetto TaskFolder
- Oggetto TaskFolder Utilità di pianificazione, proprietà GetSecurityDescriptor
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
ms.openlocfilehash: 81fdb3a301ba3238a699a5ed814057be53c3062d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302173"
---
# <a name="taskfoldergetsecuritydescriptor-property"></a>Proprietà TaskFolder. GetSecurityDescriptor

Per la creazione di script, ottiene il descrittore di sicurezza per la cartella.

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
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**TaskFolder. SetSecurityDescriptor**](taskfolder-setsecuritydescriptor.md)
</dt> <dt>

[**RegisteredTask. SetSecurityDescriptor**](registeredtask-setsecuritydescriptor.md)
</dt> </dl>

 

 





