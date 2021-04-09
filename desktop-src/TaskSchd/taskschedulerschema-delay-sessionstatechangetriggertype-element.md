---
title: Elemento Delay (sessionStateChangeTriggerType)
description: Contiene un valore che indica la lunghezza del ritardo per l'ora di inizio di un'attività, quando viene rilevata una modifica dello stato della sessione Terminal Server.
ms.assetid: 7fb87c4c-0b69-4c5b-b038-d61fb7c4ab9a
keywords:
- Utilità di pianificazione elemento Delay
topic_type:
- apiref
api_name:
- Delay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 03f230465f2e2b49ce83f1af358dfa1f84f21433
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121570"
---
# <a name="delay-sessionstatechangetriggertype-element"></a>Elemento Delay (sessionStateChangeTriggerType)

Contiene un valore che indica la lunghezza del ritardo per l'ora di inizio di un'attività, quando viene rilevata una modifica dello stato della sessione Terminal Server. Il formato di questa stringa è PnYnMnDTnHnMnS, dove nY è il numero di anni, nM è il numero di mesi, nD è il numero di giorni,' t'è il separatore di data/ora, nH è il numero di ore, nM è il numero di minuti e nS è il numero di secondi (ad esempio, PT5M specifica 5 minuti e P1M4DT2H5M specifica un mese, quattro giorni, due ore e cinque minuti). Per ulteriori informazioni sul tipo di durata, vedere <https://go.microsoft.com/fwlink/p/?linkid=106886> .

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

L'elemento **delay** viene definito dal tipo complesso [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                       | Derivato da                                                                                           | Descrizione                                                                                      |
|-------------------------------|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| **SessionStateChangeTrigger** | [**sessionStateChangeTriggerType**](taskschedulerschema-sessionstatechangetriggertype-complextype.md) | Specifica un trigger che avvia un'attività quando una sessione di Terminal Server modifica lo stato. <br/> |



## <a name="remarks"></a>Commenti

Per lo sviluppo di script, il ritardo del trigger di modifica dello stato della sessione viene specificato tramite la proprietà [**SessionStateChangeTrigger. Delay**](sessionstatechangetrigger-delay.md) .

Per lo sviluppo in C++, il ritardo del trigger di modifica dello stato della sessione viene specificato utilizzando la [**Proprietà Delay di ISessionStateChangeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-isessionstatechangetrigger-get_delay).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





