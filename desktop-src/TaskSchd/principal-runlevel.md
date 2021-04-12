---
title: Proprietà Principal. RunLevel
description: Per gli script, ottiene o imposta l'identificatore utilizzato per specificare il livello di privilegio necessario per eseguire le attività associate all'entità.
ms.assetid: 2ec3d93e-9eef-4590-842c-edfc9232bcdf
keywords:
- Utilità di pianificazione proprietà RunLevel
- Utilità di pianificazione proprietà RunLevel, oggetto Principal
- Utilità di pianificazione oggetto principale, proprietà RunLevel
topic_type:
- apiref
api_name:
- Principal.RunLevel
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9acb6c4c86215312b2df73f7bf85847ef61a4b96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517907"
---
# <a name="principalrunlevel-property"></a>Proprietà Principal. RunLevel

Per gli script, ottiene o imposta l'identificatore utilizzato per specificare il livello di privilegio necessario per eseguire le attività associate all'entità.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
Principal.RunLevel As Integer
```



## <a name="property-value"></a>Valore proprietà

Identificatore utilizzato per specificare il livello di privilegio necessario per eseguire le attività associate all'entità.



| Valore                                                                                                                                                                                                                                         | Significato                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="TASK_RUNLEVEL_LUA"></span><span id="task_runlevel_lua"></span><dl> <dt>**Attività \_ RUNLEVEL \_ LUA**</dt> <dt>0</dt> </dl>             | Le attività verranno eseguite con i privilegi minimi (LUA).<br/> |
| <span id="TASK_RUNLEVEL_HIGHEST"></span><span id="task_runlevel_highest"></span><dl> <dt>**Attività \_ RUNLEVEL \_ più alto**</dt> <dt>1</dt> </dl> | Le attività verranno eseguite con i privilegi più elevati.<br/>     |



 

## <a name="remarks"></a>Commenti

Se un'attività viene registrata utilizzando l' \\ account Administrator predefinito o gli account del sistema locale o del servizio locale, la proprietà **runlevel** verrà ignorata. Il valore della proprietà verrà ignorato anche se il controllo dell'account utente è disattivato.

Se un'attività viene registrata usando il gruppo Administrators per il contesto di sicurezza dell'attività, è necessario impostare anche la proprietà [**runlevel**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) su **attività \_ runlevel \_ più alta** se si vuole eseguire l'attività. Per ulteriori informazioni, vedere [contesti di sicurezza per le attività](security-contexts-for-running-tasks.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Principale**](principal.md)
</dt> </dl>

 

 





