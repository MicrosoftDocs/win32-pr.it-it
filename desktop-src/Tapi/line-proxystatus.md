---
description: Il messaggio LINE PROXYSTATUS viene inviato quando i proxy disponibili cambiano in una riga attualmente \_ aperta dall'applicazione.
ms.assetid: e20d4b48-a72a-4a83-ae04-a608791a1a3a
title: LINE_PROXYSTATUS messaggio (Tapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 585feda6194a13ecfbe17292aadb9036784d244c9ee5b7df4361981ab7401f65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682351"
---
# <a name="line_proxystatus-message"></a>MESSAGGIO \_ LINE PROXYSTATUS

Il **messaggio LINE \_ PROXYSTATUS** viene inviato quando i proxy disponibili cambiano in una riga attualmente aperta dall'applicazione.

TAPISRV genera questo messaggio durante una funzione [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen) usando LINEPROXYSTATUS OPEN e \_ LINEPROXYSTATUS \_ ALLOPENFORACD o una funzione [**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose) usando LINEPROXYSTATUS CLOSE (tutte le \_ costanti [**\_ LINEPROXYSTATUS**](lineproxystatus--constants.md)).


```C++
            
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwDevice* 
</dt> <dd>

Handle dell'applicazione per il dispositivo line. Si riferisce al gestore dell'agente.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Istanza di callback fornita all'apertura della riga.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Specifica lo stato della coda modificato. Può essere una o più costanti [**LINEPROXYSTATUS. \_**](lineproxystatus--constants.md)

</dd> <dt>

*dwParam2* 
</dt> <dd>

Se *dwParam1* è impostato su LINEPROXYSTATUS OPEN o \_ LINEPROXYSTATUS \_ CLOSE, *dwParam2* indica il tipo di richiesta proxy correlato, che è uno dei seguenti:

-   LINEPROXYREQUEST \_ SETAGENTGROUP
-   LINEPROXYREQUEST \_ SETAGENTSTATE
-   LINEPROXYREQUEST \_ SETAGENTACTIVITY
-   LINEPROXYREQUEST \_ GETAGENTCAPS
-   LINEPROXYREQUEST \_ GETAGENTSTATUS
-   LINEPROXYREQUEST \_ AGENTSPECIFIC
-   LINEPROXYREQUEST \_ GETAGENTACTIVITYLIST
-   LINEPROXYREQUEST \_ GETAGENTGROUPLIST
-   LINEPROXYREQUEST \_ CREATEAGENT
-   LINEPROXYREQUEST \_ SETAGENTMEASUREMENTPERIOD
-   LINEPROXYREQUEST \_ GETAGENTINFO
-   LINEPROXYREQUEST \_ CREATEAGENTSESSION
-   LINEPROXYREQUEST \_ GETAGENTSESSIONLIST
-   LINEPROXYREQUEST \_ SETAGENTSESSIONSTATE
-   LINEPROXYREQUEST \_ GETAGENTSESSIONINFO
-   LINEPROXYREQUEST \_ GETQUEUELIST
-   LINEPROXYREQUEST \_ SETQUEUEMEASUREMENTPERIOD
-   LINEPROXYREQUEST \_ GETQUEUEINFO
-   LINEPROXYREQUEST \_ GETGROUPLIST
-   LINEPROXYREQUEST \_ SETAGENTSTATEEX

In caso contrario, *dwParam2* viene impostato su zero.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Riservato. Imposta su zero.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------|-----------------------------------------------------------------------------------|
| Versione TAPI<br/> | Richiede TAPI 2.2<br/>                                                      |
| Intestazione<br/>       | <dl> <dt>Tapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)
</dt> <dt>

[**lineClose**](/windows/desktop/api/Tapi/nf-tapi-lineclose)
</dt> <dt>

[**LINE \_ PROXYREQUEST**](line-proxyrequest.md)
</dt> <dt>

[**Costanti \_ LINEPROXYREQUEST**](lineproxyrequest--constants.md)
</dt> </dl>

 

 




