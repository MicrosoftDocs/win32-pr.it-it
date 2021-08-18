---
title: Metodo INapEnforcementClientCallback NotifySoHChange (NapEnforcementClient.h)
description: Viene usato da NapAgent per informare il client di imposizione delle modifiche SoH.
ms.assetid: da8b9238-6371-4a6a-a9e7-ab791391ffc2
keywords:
- Metodo NotifySoHChange NAP
- Metodo NotifySoHChange NAP, interfaccia INapEnforcementClientCallback
- Interfaccia INapEnforcementClientCallback NAP, metodo NotifySoHChange
topic_type:
- apiref
api_name:
- INapEnforcementClientCallback.NotifySoHChange
api_location:
- NapEnforcementClient.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9011db09b698f886bd10ad19298a104668d038cc2bb11136b6e4ac58035e3425
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940135"
---
# <a name="inapenforcementclientcallbacknotifysohchange-method"></a>Metodo INapEnforcementClientCallback::NotifySoHChange

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo di callback **INapEnforcementClientCallback::NotifySoHChange** viene usato da NapAgent per informare il client di imposizione delle modifiche soH.

## <a name="syntax"></a>Sintassi


```C++
HRESULT NotifySoHChange();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo di callback deve restituire uno dei codici di errore seguenti.



| Codice restituito                                                                                                | Descrizione                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | Restituisce questo valore se l'operazione ha avuto esito positivo.<br/>                                                                                                                                                              |
| <dl> <dt>**RPC \_ S \_ SERVER \_ UNAVAILABLE**</dt> </dl> | Se si restituisce questo valore, l'applicazione viene rimossa dall'elenco bound-SHA e la voce della cache NapAgent corrispondente viene scaricata. L'sha con errori può quindi inizializzarsi nuovamente con NapAgent.<br/> |



 

## <a name="remarks"></a>Commenti

Il completamento della correzione del sistema è un evento di modifica dell'integrità del sistema. Ciò significa che è necessario chiamare **NotifySoHChange** quando una notifica [**INapSystemHealthAgentCallback::GetFixupInfo**](inapsystemhealthagentcallback-getfixupinfo-method.md) indica che il client è fisso. Quando un client è  fisso, il membro di stato della struttura [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) restituito da **GetFixupInfo** ha il valore **fixupStateSuccess**.

Dopo essere stato chiamato da NapAgent tramite questo callback, l'agente di imposizione deve chiamare [**INapEnforcementClientBinding::GetSoHRequest**](inapenforcementclientbinding-getsohrequest-method.md) per recuperare la nuova richiesta. Questa chiamata può essere effettuata sullo stesso thread di **INapEnforcementClientCallback::NotifySoHChange.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                      |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>NapEnforcementClient.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient.idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapEnforcementClientCallback**](inapenforcementclientcallback.md)
</dt> </dl>

 

 





