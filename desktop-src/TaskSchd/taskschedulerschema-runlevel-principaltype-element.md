---
title: Elemento RunLevel (runLevelType)
description: Contiene un valore che specifica il livello del contesto di sicurezza per l'esecuzione dell'attività.
ms.assetid: dc113ffa-8ac9-4dcd-a106-45295da42f46
keywords:
- Elemento RunLevel Utilità di pianificazione
topic_type:
- apiref
api_name:
- RunLevel
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 143db96de30e647c67abadc2a9fb4384ae9784604b9c679efd9de5fd2157f923
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991091"
---
# <a name="runlevel-runleveltype-element"></a>Elemento RunLevel (runLevelType)

Contiene un valore che specifica il livello del contesto di sicurezza per l'esecuzione dell'attività. È possibile specificare di eseguire un'attività usando privilegi minimi o privilegi elevati. Il valore 0 specifica di eseguire l'attività con privilegi minimi e il valore 1 specifica di eseguire l'attività con privilegi elevati.

``` syntax
<xs:element name="RunLevel"
    type="runLevelType"
 />
```

**L'elemento RunLevel** è definito dal tipo semplice [**runLevelType.**](taskschedulerschema-runleveltype-simpletype.md)

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                                  | Derivato da                                                           | Descrizione                                                                                                                           |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**Principal (principalType)**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Specifica le credenziali di sicurezza per un'entità. Queste credenziali definiscono il contesto di sicurezza in cui viene eseguita un'attività. <br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo in C++, [**vedere Proprietà RunLevel di IPrincipal.**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel)

Per lo sviluppo di script, [**vedere Principal.RunLevel.**](principal-runlevel.md)

Se un'attività viene registrata usando **l'account Amministratore \\** predefinito o gli account [LocalSystem](/windows/desktop/Services/localsystem-account) o [LocalService,](/windows/desktop/Services/localservice-account) la [**proprietà RunLevel**](principal-runlevel.md) viene ignorata. Il valore dell'attributo verrà ignorato anche se [controllo dell'account utente](/windows/desktop/SecAuthZ/user-account-control) è disattivato.

Se un'attività viene registrata usando il gruppo **Administrators** per il contesto di sicurezza dell'attività, è necessario impostare anche la [**proprietà RunLevel**](principal-runlevel.md) su "HighestAvailable" per eseguire l'attività. Per altre informazioni, vedere [Contesti di sicurezza per le attività.](security-contexts-for-running-tasks.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



 

