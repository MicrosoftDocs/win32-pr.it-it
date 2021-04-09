---
title: RegisteredTask. GetSecurityDescriptor, metodo
description: Per gli script, ottiene il descrittore di sicurezza utilizzato come credenziali per l'attività registrata.
ms.assetid: 9b5985c5-c01a-4104-940f-1e0e79f18bb7
keywords:
- Utilità di pianificazione del metodo GetSecurityDescriptor
- Metodo GetSecurityDescriptor Utilità di pianificazione, oggetto RegisteredTask
- Oggetto RegisteredTask Utilità di pianificazione, metodo GetSecurityDescriptor
topic_type:
- apiref
api_name:
- RegisteredTask.GetSecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85c7c0e6125bc848b361e4cc2d4515c32d797c57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964680"
---
# <a name="registeredtaskgetsecuritydescriptor-method"></a>RegisteredTask. GetSecurityDescriptor, metodo

Per gli script, ottiene il descrittore di sicurezza utilizzato come credenziali per l'attività registrata.

## <a name="syntax"></a>Sintassi


```VB
sddl = .GetSecurityDescriptor( _
  ByVal securityInformation _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*securityInformation* 
</dt> <dd>

Informazioni di sicurezza da [**\_ informazioni di sicurezza**](/windows/desktop/SecAuthZ/security-information).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Descrittore di sicurezza per l'attività registrata.

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

 

