---
title: Elemento RandomDelay (calendarTriggerType)
description: Contiene il tempo di ritardo che viene aggiunto in modo casuale all'ora di inizio del trigger. | Elemento RandomDelay (calendarTriggerType)
ms.assetid: 497fab4e-ad63-43e6-a086-2d77b43662d9
keywords:
- Utilità di pianificazione elemento RandomDelay
topic_type:
- apiref
api_name:
- RandomDelay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d71149bfeceeb6c17cafa27f56bb15bb184ead06
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353381"
---
# <a name="randomdelay-calendartriggertype-element"></a>Elemento RandomDelay (calendarTriggerType)

Contiene il tempo di ritardo che viene aggiunto in modo casuale all'ora di inizio del trigger. Il formato di questa stringa è PnYnMnDTnHnMnS, dove nY è il numero di anni, nM è il numero di mesi, nD è il numero di giorni,' t'è il separatore di data/ora, nH è il numero di ore, nM è il numero di minuti e nS è il numero di secondi (ad esempio, PT5M specifica 5 minuti e P1M4DT2H5M specifica un mese, quattro giorni, due ore e cinque minuti). Per ulteriori informazioni sul tipo di durata, vedere <https://go.microsoft.com/fwlink/p/?linkid=106886> .

``` syntax
<xs:element name="RandomDelay"
    type="duration"
    default="PT0M"
    minOccurs="0"
 />
```

L'elemento **RandomDelay** è definito dal tipo complesso [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) .

## <a name="parent-element"></a>Elemento padre



| Elemento                                                                                            | Derivato da                                                                       | Descrizione                                                                                 |
|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**CalendarTrigger (triggerGroup)**](taskschedulerschema-calendartrigger-triggergroup-element.md) | [**calendarTriggerType**](taskschedulerschema-calendartriggertype-complextype.md) | Specifica un trigger giornaliero, settimanale, mensile o mensile (DOW) per il giorno della settimana. <br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





