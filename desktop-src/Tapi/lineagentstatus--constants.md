---
description: Le costanti LINEAGENTSTATUS \_ elencano lo stato di aggiornamento dei membri della struttura LINEAGENTSTATUS per un agente.
ms.assetid: 068a2b24-a430-4cf5-b70d-5574e981a899
title: LINEAGENTSTATUS_ costanti (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1d792fc31c1d56afaa483a9aa6890db1f52398d7107ef944cf53352734044b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682041"
---
# <a name="lineagentstatus_-constants"></a>Costanti \_ LINEAGENTSTATUS

Le **costanti LINEAGENTSTATUS \_ elencano** lo stato di aggiornamento dei membri della [**struttura LINEAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus) per un agente.

<dl> <dt>

<span id="LINEAGENTSTATUS_ACTIVITY"></span><span id="lineagentstatus_activity"></span>**ATTIVITÀ \_ LINEAGENTSTATUS**
</dt> <dd> <dl> <dt>



Il **membro dwActivityID**, **dwActivitySize** o **dwActivityOffset** in [**LINEAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus) è stato aggiornato.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATUS_ACTIVITYLIST"></span><span id="lineagentstatus_activitylist"></span>**LINEAGENTSTATUS \_ ACTIVITYLIST**
</dt> <dd> <dl> <dt>



[**LINEAGENTACTIVITYLIST**](/windows/desktop/api/Tapi/ns-tapi-lineagentactivitylist) è stato aggiornato. L'applicazione può chiamare [**lineGetAgentActivityList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentactivitylista) per ottenere l'elenco aggiornato.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATUS_CAPSCHANGE"></span><span id="lineagentstatus_capschange"></span>**LINEAGENTSTATUS \_ CAPSCHANGE**
</dt> <dd> <dl> <dt>



Le funzionalità di [**LINEAGENTCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineagentcaps) sono state aggiornate. L'applicazione può chiamare [**lineGetAgentCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetagentcapsa) per ottenere l'elenco aggiornato.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATUS_GROUP"></span><span id="lineagentstatus_group"></span>**GRUPPO \_ LINEAGENTSTATUS**
</dt> <dd> <dl> <dt>



[**LINEAGENTSTATUS è**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus) stato aggiornato.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATUS_GROUPLIST"></span><span id="lineagentstatus_grouplist"></span>**LINEAGENTSTATUS \_ GROUPLIST**
</dt> <dd> <dl> <dt>



[**LINEAGENTGROUPLIST**](/windows/desktop/api/Tapi/ns-tapi-lineagentgrouplist) è stato aggiornato. L'applicazione può chiamare [**lineGetAgentGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentgrouplista) per ottenere l'elenco aggiornato.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATUS_NEXTSTATE"></span><span id="lineagentstatus_nextstate"></span>**LINEAGENTSTATUS \_ NEXTSTATE**
</dt> <dd> <dl> <dt>



Il **membro dwNextState** in [**LINEAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus) è stato aggiornato.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATUS_STATE"></span><span id="lineagentstatus_state"></span>**STATO \_ LINEAGENTSTATUS**
</dt> <dd> <dl> <dt>



Il **membro dwState** in [**LINEAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus) è stato aggiornato.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATUS_VALIDNEXTSTATES"></span><span id="lineagentstatus_validnextstates"></span>**LINEAGENTSTATUS \_ VALIDNEXTSTATES**
</dt> <dd> <dl> <dt>



Il **membro dwValidNextStates** in [**LINEAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus) è stato aggiornato.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATUS_VALIDSTATES"></span><span id="lineagentstatus_validstates"></span>**LINEAGENTSTATUS \_ VALIDSTATES**
</dt> <dd> <dl> <dt>



Il **membro dwValidStates** in [**LINEAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus) è stato aggiornato.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**LINEAGENTACTIVITYLIST**](/windows/desktop/api/Tapi/ns-tapi-lineagentactivitylist)
</dt> <dt>

[**LINEAGENTCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineagentcaps)
</dt> <dt>

[**LINEAGENTGROUPLIST**](/windows/desktop/api/Tapi/ns-tapi-lineagentgrouplist)
</dt> <dt>

[**LINEAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus)
</dt> <dt>

[**lineGetAgentActivityList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentactivitylista)
</dt> <dt>

[**lineGetAgentCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetagentcapsa)
</dt> <dt>

[**lineGetAgentGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentgrouplista)
</dt> </dl>

 

 




