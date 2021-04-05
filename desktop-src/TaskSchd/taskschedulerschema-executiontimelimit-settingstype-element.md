---
title: Elemento ExecutionTimeLimit (settingsType)
description: Quantità di tempo consentita per completare l'attività.
ms.assetid: c42d0f42-4571-44ab-90b1-948fd7ea991b
keywords:
- Utilità di pianificazione elemento ExecutionTimeLimit
topic_type:
- apiref
api_name:
- ExecutionTimeLimit
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dd86f7ae4988211fdf100f69ac82e747e9ea0f49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873457"
---
# <a name="executiontimelimit-settingstype-element"></a>Elemento ExecutionTimeLimit (settingsType)

Quantità di tempo consentita per completare l'attività. Il formato di questa stringa è PnYnMnDTnHnMnS, dove nY è il numero di anni, nM è il numero di mesi, nD è il numero di giorni,' t'è il separatore di data/ora, nH è il numero di ore, nM è il numero di minuti e nS è il numero di secondi (ad esempio, PT5M specifica 5 minuti e P1M4DT2H5M specifica un mese, quattro giorni, due ore e cinque minuti). Per ulteriori informazioni sul tipo di durata, vedere <https://go.microsoft.com/fwlink/p/?linkid=106886> . Il valore PT0S consentirà l'esecuzione illimitata dell'attività.

``` syntax
<xs:element name="ExecutionTimeLimit"
    type="duration"
    minOccurs="0"
 />
```

L'elemento **ExecutionTimeLimit** è definito dal tipo complesso [**settingsType**](taskschedulerschema-settingstype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                           | Derivato da                                                         | Descrizione                                                                        |
|-------------------------------------------------------------------|----------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Impostazioni**](taskschedulerschema-settings-tasktype-element.md) | [**settingsType**](taskschedulerschema-settingstype-complextype.md) | Contiene le impostazioni utilizzate dal Utilità di pianificazione per eseguire l'attività.<br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo in C++, vedere [**la proprietà ExecutionTimeLimit di ITaskSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_executiontimelimit).

Per lo sviluppo di script, vedere [**TaskSettings.ExecutionTimeLimit**](tasksettings-executiontimelimit.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Elementi dello schema Utilità di pianificazione](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





