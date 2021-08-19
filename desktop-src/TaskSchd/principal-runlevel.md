---
title: Principal.RunLevel - proprietà
description: Per lo scripting, ottiene o imposta l'identificatore utilizzato per specificare il livello di privilegio necessario per eseguire le attività associate all'entità.
ms.assetid: 2ec3d93e-9eef-4590-842c-edfc9232bcdf
keywords:
- Proprietà RunLevel Utilità di pianificazione
- Proprietà RunLevel Utilità di pianificazione , oggetto Principal
- Oggetto Principal Utilità di pianificazione proprietà RunLevel
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
ms.openlocfilehash: 8be2bc9552ac8650bb2cf9ca40944a480683f2ef6dc6cccecfc5ed34eb544ca6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126131"
---
# <a name="principalrunlevel-property"></a>Principal.RunLevel - proprietà

Per lo scripting, ottiene o imposta l'identificatore utilizzato per specificare il livello di privilegio necessario per eseguire le attività associate all'entità.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
Principal.RunLevel As Integer
```



## <a name="property-value"></a>Valore proprietà

Identificatore utilizzato per specificare il livello di privilegio necessario per eseguire le attività associate all'entità.



| Valore                                                                                                                                                                                                                                         | Significato                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="TASK_RUNLEVEL_LUA"></span><span id="task_runlevel_lua"></span><dl> <dt>**ATTIVITÀ \_ RUNLEVEL \_ LUA**</dt> <dt>0</dt> </dl>             | Le attività verranno eseguite con i privilegi minimi (LUA).<br/> |
| <span id="TASK_RUNLEVEL_HIGHEST"></span><span id="task_runlevel_highest"></span><dl> <dt>**ATTIVITÀ \_ RUNLEVEL \_ PIÙ ALTO**</dt> <dt>1</dt> </dl> | Le attività verranno eseguite con i privilegi più elevati.<br/>     |



 

## <a name="remarks"></a>Commenti

Se un'attività viene registrata usando l'account amministratore predefinito o gli account del sistema locale o del servizio locale, la \\ **proprietà RunLevel** verrà ignorata. Il valore della proprietà verrà ignorato anche se il controllo dell'account utente è disattivato.

Se un'attività viene registrata usando il gruppo Administrators per il contesto di sicurezza dell'attività, è necessario impostare anche la [**proprietà RunLevel**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) su **TASK \_ RUNLEVEL \_ HIGHEST** se si vuole eseguire l'attività. Per altre informazioni, vedere [Contesti di sicurezza per le attività](security-contexts-for-running-tasks.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                          |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                    |
| Libreria dei tipi<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Principale**](principal.md)
</dt> </dl>

 

 





