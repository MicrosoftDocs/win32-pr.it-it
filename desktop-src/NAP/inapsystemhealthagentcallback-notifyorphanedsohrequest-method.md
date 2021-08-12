---
title: Metodo INapSystemHealthAgentCallback NotifyOrphanedSoHRequest (NapSystemHealthAgent.h)
description: Viene chiamato se è stata eseguita una query su un oggetto SoHRequest da SHA, ma la risposta non è mai tornati.
ms.assetid: 9e6fac6c-fb23-4725-ae0f-28ef8a6c4ea6
keywords:
- Metodo NotifyOrphanedSoHRequest NAP
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
ms.openlocfilehash: 171191c266ae3fd59ab1ba8f55acd73eb143e9aa220fb3d2989a7ced9f716513
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118621182"
---
# <a name="inapsystemhealthagentcallbacknotifyorphanedsohrequest-method"></a>Metodo INapSystemHealthAgentCallback::NotifyOrphanedSoHRequest

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo INapSystemHealthAgentCallback::NotifyOrphanedSoHRequest** viene chiamato se è stata eseguita una query [**soHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) dall'SHA, ma la risposta non è mai tornati.

## <a name="syntax"></a>Sintassi


```C++
HRESULT NotifyOrphanedSoHRequest(
  [in] const CorrelationId *correlationId
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*correlationId* \[ Pollici\]
</dt> <dd>

Puntatore alla struttura [**CorrelationId univoca**](/windows/win32/api/naptypes/ns-naptypes-correlationid) che identifica l'oggetto [**SoHRequest orfano.**](/windows/win32/api/naptypes/ns-naptypes-soh)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo può restituire uno di questi valori.



| Codice restituito                                                                          | Descrizione                   |
|--------------------------------------------------------------------------------------|-------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Indica l'esito positivo dell'operazione.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo di callback viene dichiarato dal sistema nap e deve essere implementato dal writer SHA.

Questo metodo può essere chiamato dal sistema nei casi seguenti:

-   Non è stato possibile inviare un oggetto [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) in transito.
-   Un [**oggetto SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) è stato inviato in transito, ma non è stato restituito alcun oggetto **SoHResponse,** ad esempio si è timeout o non è presente alcun shv corrispondente sul lato server.
-   La connessione si è erta o un'applicazione è passata offline.

Si tratta solo di una notifica del massimo sforzo, quindi gli account di servizio non devono basarsi su queste informazioni per pulire lo stato. Esistono diverse situazioni in cui un'applicazione SHA non riceverà una notifica:

-   Se un imponitore si comporta in modo non valido, ad esempio non invia una notifica all'SHA quando lo stato della connessione non è attivo.
-   In caso di arresto anomalo di un'applicazione.
-   In condizioni di errore, ad esempio la memoria di NapAgent è insufficiente.

Gli sha possono ricevere alcune notifiche non erre quando si associano per la prima volta a NapAgent, ad esempio, se è in corso uno scambio SoH quando l'sha è associato e quindi si verifica il timeout.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                      |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>NapSystemHealthAgent.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthAgent.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)
</dt> </dl>

 

 





