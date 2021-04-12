---
title: Metodo INapSystemHealthAgentCallback NotifyOrphanedSoHRequest (NapSystemHealthAgent. h)
description: Viene chiamato se un SoHRequest è stato sottoposto a query dall'SHA, ma la risposta non è mai stata restituita.
ms.assetid: 9e6fac6c-fb23-4725-ae0f-28ef8a6c4ea6
keywords:
- NAP metodo NotifyOrphanedSoHRequest
- Metodo NotifyOrphanedSoHRequest NAP, interfaccia INapSystemHealthAgentCallback
- Interfaccia INapSystemHealthAgentCallback NAP, metodo NotifyOrphanedSoHRequest
topic_type:
- apiref
api_name:
- INapSystemHealthAgentCallback.NotifyOrphanedSoHRequest
api_location:
- NapSystemHealthAgent.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 676b67b61a9375f4fd44ecc41f9e56e92a97b693
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400890"
---
# <a name="inapsystemhealthagentcallbacknotifyorphanedsohrequest-method"></a>Metodo INapSystemHealthAgentCallback:: NotifyOrphanedSoHRequest

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **INapSystemHealthAgentCallback:: NotifyOrphanedSoHRequest** viene chiamato se un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) è stato sottoposto a query dall'SHA, ma la risposta non è mai stata restituita.

## <a name="syntax"></a>Sintassi


```C++
HRESULT NotifyOrphanedSoHRequest(
  [in] const CorrelationId *correlationId
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

ID correlazione  \[ in\]
</dt> <dd>

Puntatore alla struttura univoca [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) che identifica il [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh)orfano.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                          | Descrizione                   |
|--------------------------------------------------------------------------------------|-------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Indica l'esito positivo dell'operazione.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo di callback viene dichiarato dal sistema NAP e deve essere implementato dal writer SHA.

Questo metodo può essere chiamato dal sistema nei casi seguenti:

-   Non è stato possibile inviare un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) in rete.
-   Un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) è stato inviato in rete, ma non è stato restituito alcun **SoHResponse** , ovvero si è verificato il timeout dell'applicazione o non è presente alcun servizio di convalida dell'integrità corrispondente sul lato server.
-   La connessione è stata interrotta o un Enforcer è andato offline.

Si tratta solo di una notifica di massimo sforzo, quindi SHAs non deve basarsi su queste informazioni per pulire lo stato. Esistono diverse situazioni in cui un SHA non riceve alcuna notifica:

-   Se un Enforcer si comporta in modo improprio, ovvero non invia una notifica all'SHA quando lo stato della connessione non è attivo.
-   Se un'applicazione si arresta in modo anomalo.
-   In condizioni di errore, ad esempio, il NapAgent ha esaurito la memoria.

SHAs può ricevere alcune notifiche non corrette quando vengono prima associate al NapAgent, ad esempio se è in corso uno scambio di rapporto di integrità quando si verifica un binding SHA e si verifica il timeout.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                      |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>NapSystemHealthAgent. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthAgent. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





