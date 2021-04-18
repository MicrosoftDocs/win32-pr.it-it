---
description: Il messaggio di riga \_ PROXYSTATUS viene inviato quando i proxy disponibili cambiano in una riga attualmente aperta dall'applicazione.
ms.assetid: e20d4b48-a72a-4a83-ae04-a608791a1a3a
title: Messaggio di LINE_PROXYSTATUS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb00c5df4f531309bdd1311fb7c34c3e9967a8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328424"
---
# <a name="line_proxystatus-message"></a>\_Messaggio linea PROXYSTATUS

Il messaggio di **riga \_ PROXYSTATUS** viene inviato quando i proxy disponibili cambiano in una riga attualmente aperta dall'applicazione.

TAPISRV genera questo messaggio durante una funzione [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) usando LINEPROXYSTATUS \_ Open e LINEPROXYSTATUS \_ ALLOPENFORACD o una funzione [**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose) usando LINEPROXYSTATUS \_ Close (tutte le [**\_ costanti LINEPROXYSTATUS**](lineproxystatus--constants.md)).


```C++
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwDevice* 
</dt> <dd>

Handle dell'applicazione per il dispositivo linea. Questo si riferisce al gestore agenti.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Istanza di callback fornita all'apertura della riga.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Specifica lo stato della coda che è stato modificato. Può essere una o più delle [**\_ costanti LINEPROXYSTATUS**](lineproxystatus--constants.md).

</dd> <dt>

*dwParam2* 
</dt> <dd>

Se *dwParam1* è impostato su LINEPROXYSTATUS \_ Open o LINEPROXYSTATUS \_ Close, *dwParam2* indica il tipo di richiesta proxy correlato, che è uno dei seguenti:

-   \_SETAGENTGROUP LINEPROXYREQUEST
-   \_SETAGENTSTATE LINEPROXYREQUEST
-   \_SETAGENTACTIVITY LINEPROXYREQUEST
-   \_GETAGENTCAPS LINEPROXYREQUEST
-   \_GETAGENTSTATUS LINEPROXYREQUEST
-   \_AGENTSPECIFIC LINEPROXYREQUEST
-   \_GETAGENTACTIVITYLIST LINEPROXYREQUEST
-   \_GETAGENTGROUPLIST LINEPROXYREQUEST
-   \_CREATEAGENT LINEPROXYREQUEST
-   \_SETAGENTMEASUREMENTPERIOD LINEPROXYREQUEST
-   \_GETAGENTINFO LINEPROXYREQUEST
-   \_CREATEAGENTSESSION LINEPROXYREQUEST
-   \_GETAGENTSESSIONLIST LINEPROXYREQUEST
-   \_SETAGENTSESSIONSTATE LINEPROXYREQUEST
-   \_GETAGENTSESSIONINFO LINEPROXYREQUEST
-   LINEPROXYREQUEST \_ GETqueuein
-   \_SETQUEUEMEASUREMENTPERIOD LINEPROXYREQUEST
-   \_GETQUEUEINFO LINEPROXYREQUEST
-   LINEPROXYREQUEST \_ GETgrouping
-   \_SETAGENTSTATEEX LINEPROXYREQUEST

In caso contrario, *dwParam2* è impostato su zero.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Riservato. Imposta su zero.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2,2<br/>                                                      |
| Intestazione<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose)
</dt> <dt>

[**LINEA \_ PROXYREQUEST**](line-proxyrequest.md)
</dt> <dt>

[**\_Costanti LINEPROXYREQUEST**](lineproxyrequest--constants.md)
</dt> </dl>

 

 




