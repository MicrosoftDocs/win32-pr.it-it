---
title: Metodo INapEnforcementClientCallback NotifySoHChange (NapEnforcementClient. h)
description: Viene usato da NapAgent per informare il client di imposizione delle modifiche del rapporto di integrità.
ms.assetid: da8b9238-6371-4a6a-a9e7-ab791391ffc2
keywords:
- NAP metodo NotifySoHChange
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
ms.openlocfilehash: 6b405bca5ae27a68eea780dfcb922d1f986f475c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121606"
---
# <a name="inapenforcementclientcallbacknotifysohchange-method"></a>Metodo INapEnforcementClientCallback:: NotifySoHChange

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo di callback **INapEnforcementClientCallback:: NotifySoHChange** viene usato da napagent per informare il client di imposizione delle modifiche del rapporto di integrità.

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
| <dl> <dt>**\_OK**</dt> </dl>                       | Restituisce questo valore se l'operazione ha esito positivo.<br/>                                                                                                                                                              |
| <dl> <dt>**\_server RPC \_ non \_ disponibile**</dt> </dl> | Se si restituisce questo valore, l'imposizione viene rimossa dall'elenco associato-SHA e viene scaricata la voce della cache NapAgent corrispondente. L'SHA in errore può quindi reinizializzarsi con NapAgent.<br/> |



 

## <a name="remarks"></a>Commenti

Il completamento della correzione del sistema è un evento di modifica dell'integrità di sistema. Ciò significa che è necessario chiamare **NotifySoHChange** quando una notifica [**INapSystemHealthAgentCallback:: GetFixupInfo**](inapsystemhealthagentcallback-getfixupinfo-method.md) indica che il client è fisso. Quando un client viene risolto, il membro di **stato** della struttura [**FixupInfo**](/windows/win32/api/naptypes/ns-naptypes-fixupinfo) restituito da **GetFixupInfo** ha il valore **fixupStateSuccess**.

Dopo essere stato chiamato da NapAgent tramite questo callback, l'agente di imposizione deve quindi chiamare [**INapEnforcementClientBinding:: GetSoHRequest**](inapenforcementclientbinding-getsohrequest-method.md) per recuperare la nuova richiesta. Questa chiamata può essere eseguita sullo stesso thread di **INapEnforcementClientCallback:: NotifySoHChange**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                      |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>NapEnforcementClient. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapEnforcementClient. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapEnforcementClientCallback**](inapenforcementclientcallback.md)
</dt> </dl>

 

 





