---
description: Queste costanti vengono utilizzate in due contesti.
ms.assetid: 5c05a567-cc65-411e-b049-919a442c5c57
title: Costanti LINEPROXYREQUEST_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eba34a3a7f7b1f41f0c32783c4132afcfafef1aa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331252"
---
# <a name="lineproxyrequest_-constants"></a>\_Costanti LINEPROXYREQUEST

Queste costanti vengono utilizzate in due contesti. In primo luogo, possono essere usati in una matrice di valori **DWORD** nella struttura [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) passata con [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) quando \_ viene specificata l'opzione proxy LINEOPENOPTION per indicare le funzioni che l'applicazione è disposti a gestire. In secondo luogo, vengono usati nella [**riga \_ PROXYREQUEST**](line-proxyrequest.md) passata all'applicazione Handler da un messaggio di **riga \_ PROXYREQUEST** per indicare il tipo di richiesta da elaborare e il formato dei dati nel buffer.

<dl> <dt>

<span id="LINEPROXYREQUEST_AGENTSPECIFIC"></span><span id="lineproxyrequest_agentspecific"></span>**\_AGENTSPECIFIC LINEPROXYREQUEST**
</dt> <dd> <dl> <dt>



Associato a [**lineAgentSpecific**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_CREATEAGENT"></span><span id="lineproxyrequest_createagent"></span>**\_CREATEAGENT LINEPROXYREQUEST**
</dt> <dd> <dl> <dt>



Associato a [**lineCreateAgent**](/windows/desktop/api/Tapi/nf-tapi-linecreateagenta).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_CREATEAGENTSESSION"></span><span id="lineproxyrequest_createagentsession"></span>**\_CREATEAGENTSESSION LINEPROXYREQUEST**
</dt> <dd> <dl> <dt>



Associato a [**lineCreateAgentSession**](/windows/desktop/api/Tapi/nf-tapi-linecreateagentsessiona).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_GETAGENTACTIVITYLIST"></span><span id="lineproxyrequest_getagentactivitylist"></span>**\_GETAGENTACTIVITYLIST LINEPROXYREQUEST**
</dt> <dd> <dl> <dt>



Associato a [**lineGetAgentActivityList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentactivitylista).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_GETAGENTCAPS"></span><span id="lineproxyrequest_getagentcaps"></span>**\_GETAGENTCAPS LINEPROXYREQUEST**
</dt> <dd> <dl> <dt>



Associato a [**lineGetAgentCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetagentcapsa).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_GETAGENTGROUPLIST"></span><span id="lineproxyrequest_getagentgrouplist"></span>**\_GETAGENTGROUPLIST LINEPROXYREQUEST**
</dt> <dd> <dl> <dt>



Associato a [**lineGetAgentGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentgrouplista).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_GETAGENTINFO"></span><span id="lineproxyrequest_getagentinfo"></span>**\_GETAGENTINFO LINEPROXYREQUEST**
</dt> <dd> <dl> <dt>



Associato a [**lineGetAgentInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetagentinfo).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_GETAGENTSESSIONINFO"></span><span id="lineproxyrequest_getagentsessioninfo"></span>**\_GETAGENTSESSIONINFO LINEPROXYREQUEST**
</dt> <dd> <dl> <dt>



Associato a [**lineGetAgentSessionInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetagentsessioninfo).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_GETAGENTSESSIONLIST"></span><span id="lineproxyrequest_getagentsessionlist"></span>**\_GETAGENTSESSIONLIST LINEPROXYREQUEST**
</dt> <dd> <dl> <dt>



Associato a [**lineGetAgentSessionList**](/windows/desktop/api/Tapi/nf-tapi-linegetagentsessionlist).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_GETAGENTSTATUS"></span><span id="lineproxyrequest_getagentstatus"></span>**\_GETAGENTSTATUS LINEPROXYREQUEST**
</dt> <dd> <dl> <dt>



Associato a [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_GETGROUPLIST"></span><span id="lineproxyrequest_getgrouplist"></span>**LINEPROXYREQUEST \_ GETgrouping**
</dt> <dd> <dl> <dt>



Associato a [**lineGetGroupList**](/windows/desktop/api/Tapi/nf-tapi-linegetgrouplista).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_GETQUEUEINFO"></span><span id="lineproxyrequest_getqueueinfo"></span>**\_GETQUEUEINFO LINEPROXYREQUEST**
</dt> <dd> <dl> <dt>



Associato a [**lineGetQueueInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetqueueinfo).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_GETQUEUELIST"></span><span id="lineproxyrequest_getqueuelist"></span>**LINEPROXYREQUEST \_ GETqueuein**
</dt> <dd> <dl> <dt>



Associato a [**lineGetQueueList**](/windows/desktop/api/Tapi/nf-tapi-linegetqueuelista).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_SETAGENTACTIVITY"></span><span id="lineproxyrequest_setagentactivity"></span>**\_SETAGENTACTIVITY LINEPROXYREQUEST**
</dt> <dd> <dl> <dt>



Associato a [**lineSetAgentActivity**](/windows/desktop/api/Tapi/nf-tapi-linesetagentactivity).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_SETAGENTGROUP"></span><span id="lineproxyrequest_setagentgroup"></span>**\_SETAGENTGROUP LINEPROXYREQUEST**
</dt> <dd> <dl> <dt>



Associato a [**lineSetAgentGroup**](/windows/desktop/api/Tapi/nf-tapi-linesetagentgroup).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_SETAGENTMEASUREMENTPERIOD"></span><span id="lineproxyrequest_setagentmeasurementperiod"></span>**\_SETAGENTMEASUREMENTPERIOD LINEPROXYREQUEST**
</dt> <dd> <dl> <dt>



Associato a [**lineSetAgentMeasurementPeriod**](/windows/desktop/api/Tapi/nf-tapi-linesetagentmeasurementperiod).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_SETAGENTSESSIONSTATE"></span><span id="lineproxyrequest_setagentsessionstate"></span>**\_SETAGENTSESSIONSTATE LINEPROXYREQUEST**
</dt> <dd> <dl> <dt>



Associato a [**lineSetAgentSessionState**](/windows/desktop/api/Tapi/nf-tapi-linesetagentsessionstate).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_SETAGENTSTATE"></span><span id="lineproxyrequest_setagentstate"></span>**\_SETAGENTSTATE LINEPROXYREQUEST**
</dt> <dd> <dl> <dt>



Associato a [**lineSetAgentState**](/windows/desktop/api/Tapi/nf-tapi-linesetagentstate).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_SETAGENTSTATEEX"></span><span id="lineproxyrequest_setagentstateex"></span>**\_SETAGENTSTATEEX LINEPROXYREQUEST**
</dt> <dd> <dl> <dt>



Associato a [**lineSetAgentStateEx**](/windows/desktop/api/Tapi/nf-tapi-linesetagentstateex).


</dt> </dl> </dd> <dt>

<span id="LINEPROXYREQUEST_SETQUEUEMEASUREMENTPERIOD"></span><span id="lineproxyrequest_setqueuemeasurementperiod"></span>**\_SETQUEUEMEASUREMENTPERIOD LINEPROXYREQUEST**
</dt> <dd> <dl> <dt>



Associato a [**lineSetQueueMeasurementPeriod**](/windows/desktop/api/Tapi/nf-tapi-linesetqueuemeasurementperiod).


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,0 o versione successiva<br/>                                             |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Costanti Call Center](call-center-constants.md)
</dt> <dt>

[Funzioni Call Center](call-center-functions.md)
</dt> </dl>

 

 




