---
title: Elemento RunLevel (runLevelType)
description: Contiene un valore che specifica il livello di contesto di sicurezza per l'esecuzione dell'attività.
ms.assetid: dc113ffa-8ac9-4dcd-a106-45295da42f46
keywords:
- Utilità di pianificazione elemento RunLevel
topic_type:
- apiref
api_name:
- RunLevel
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d374f5b9ad388f3ad0a626e1b99ecae96eeef1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341303"
---
# <a name="runlevel-runleveltype-element"></a>Elemento RunLevel (runLevelType)

Contiene un valore che specifica il livello di contesto di sicurezza per l'esecuzione dell'attività. È possibile specificare di eseguire un'attività usando privilegi minimi o privilegi elevati. Il valore 0 specifica che per eseguire l'attività con privilegi più bassi e il valore 1 viene specificato di eseguire l'attività con privilegi elevati.

``` syntax
<xs:element name="RunLevel"
    type="runLevelType"
 />
```

L'elemento **runlevel** è definito dal tipo semplice [**runLevelType**](taskschedulerschema-runleveltype-simpletype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                                  | Derivato da                                                           | Descrizione                                                                                                                           |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**Entità (principalType)**](taskschedulerschema-principal-principaltype-element.md) | [**principalType**](taskschedulerschema-principaltype-complextype.md) | Specifica le credenziali di sicurezza per un'entità. Queste credenziali definiscono il contesto di sicurezza in cui viene eseguita un'attività. <br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo in C++, vedere [**Proprietà runlevel di IPrincipal**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel).

Per lo sviluppo di script, vedere [**Principal. runlevel**](principal-runlevel.md).

Se un'attività viene registrata con l'account **\\ Administrator predefinito** o con gli account [LocalSystem](/windows/desktop/Services/localsystem-account) o [LocalService](/windows/desktop/Services/localservice-account) , la proprietà [**runlevel**](principal-runlevel.md) viene ignorata. Il valore dell'attributo verrà ignorato anche se il [controllo dell'account utente](/windows/desktop/SecAuthZ/user-account-control) è disattivato.

Se un'attività viene registrata usando il gruppo **Administrators** per il contesto di sicurezza dell'attività, è necessario impostare anche la proprietà [**runlevel**](principal-runlevel.md) su "highestAvailable" per eseguire l'attività. Per ulteriori informazioni, vedere [contesti di sicurezza per le attività](security-contexts-for-running-tasks.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

