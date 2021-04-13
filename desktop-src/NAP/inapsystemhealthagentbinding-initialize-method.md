---
title: Metodo Initialize INapSystemHealthAgentBinding (NapSystemHealthAgent. h)
description: Inizializza l'agente integrità sistema (SHA) e associa l'SHA al servizio NapAgent.
ms.assetid: abbc942b-0217-4b07-bf43-fab55ca9c411
keywords:
- Metodo di inizializzazione NAP
- Metodo Initialize NAP, interfaccia INapSystemHealthAgentBinding
- Interfaccia NAP di INapSystemHealthAgentBinding, metodo Initialize
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.Initialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ee4d4f602303ca1943e47c04ba30ab8f6e75e72
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340392"
---
# <a name="inapsystemhealthagentbindinginitialize-method"></a>Metodo INapSystemHealthAgentBinding:: Initialize

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **INapSystemHealthAgentBinding:: Initialize** Inizializza l'agente integrità sistema e associa l'Sha al servizio napagent. Questo metodo deve essere chiamato prima di chiamare qualsiasi altro metodo sull'interfaccia [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT Initialize(
  [in] SystemHealthEntityId          id,
  [in] INapSystemHealthAgentCallback *callback
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ID* \[ in\]
</dt> <dd>

[SystemHealthEntityId](nap-datatypes.md) univoco che contiene l'ID dell'SHA associato al servizio napagent.

</dd> <dt>

*callback* \[ di in\]
</dt> <dd>

Puntatore COM a un'interfaccia [**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md) utilizzata da napagent per richiamare l'agente di integrità con una notifica o un processo. NapAgent include un riferimento all'oggetto associato a questa interfaccia fino a quando non viene chiamato [**Uninitialize**](inapsystemhealthagentbinding-uninitialize-method.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

È possibile che vengano restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                                | Descrizione                                                                                                                    |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                      | Operazione riuscita.<br/>                                                                                                |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>            | Errore delle autorizzazioni, accesso negato.<br/>                                                                                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>             | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/>                                                             |
| <dl> <dt>**ERRORE \_ già \_ inizializzato**</dt> </dl> | Se SHA è stato inizializzato in precedenza, viene restituito questo errore.<br/>                                                      |
| <dl> <dt>**NAP \_ E \_ non \_ registrato**</dt> </dl>     | Se SHA non è stato registrato in precedenza, viene restituito questo errore.<br/>                                                      |
| <dl> <dt>**RPC \_ E \_ disconnessa**</dt> </dl>        | Il NapAgent è stato arrestato. Questo oggetto verrà ripristinato automaticamente e riassociato a NapAgent, una volta riavviato.<br/> |



 

## <a name="remarks"></a>Commenti

NapAgent non attiva uno scambio di rapporto di integrità come risultato dell'inizializzazione. Un agente integrità sistema deve chiamare [**NotifySoHChange**](inapsystemhealthagentbinding-notifysohchange-method.md) per richiedere uno scambio di pacchetti SOH dopo l'inizializzazione con napagent.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                      |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>NapSystemHealthAgent. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthAgent. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





