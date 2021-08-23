---
title: Metodo Initialize INapSystemHealthAgentBinding (NapSystemHealthAgent.h)
description: Inizializza l'agente di integrità del sistema (SHA) e associa l'SHA al servizio NapAgent.
ms.assetid: abbc942b-0217-4b07-bf43-fab55ca9c411
keywords:
- Inizializzare il metodo NAP
- Inizializzare il metodo NAP, interfaccia INapSystemHealthAgentBinding
- Interfaccia INapSystemHealthAgentBinding NAP , metodo Initialize
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
ms.openlocfilehash: 7dbe764d477c5f176fcaebc0825bbbcd02495ec70ee669a02c59258173cfbdd3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119802711"
---
# <a name="inapsystemhealthagentbindinginitialize-method"></a>Metodo INapSystemHealthAgentBinding::Initialize

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo INapSystemHealthAgentBinding::Initialize** inizializza l'agente di integrità del sistema (SHA) e associa l'SHA al servizio NapAgent. Questo metodo deve essere chiamato prima di chiamare qualsiasi altro metodo [**sull'interfaccia INapSystemHealthAgentBinding2.**](inapsystemhealthagentbinding2.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT Initialize(
  [in] SystemHealthEntityId          id,
  [in] INapSystemHealthAgentCallback *callback
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*id* \[ in\]
</dt> <dd>

[SystemHealthEntityId univoco](nap-datatypes.md) che contiene l'ID dell'SHA associato al servizio NapAgent.

</dd> <dt>

*callback* \[ Pollici\]
</dt> <dd>

Puntatore COM a [**un'interfaccia INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md) usata da NapAgent per eseguire il callback dell'agente integrità con una notifica o un processo. NapAgent contiene un riferimento all'oggetto associato a questa interfaccia fino a quando non [**viene chiamato Uninitialize.**](inapsystemhealthagentbinding-uninitialize-method.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Possono essere restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                                | Descrizione                                                                                                                    |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                      | Operazione riuscita.<br/>                                                                                                |
| <dl> <dt>**E \_ ACCESSO NEGATO**</dt> </dl>            | Errore di autorizzazione, accesso negato.<br/>                                                                                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>             | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/>                                                             |
| <dl> <dt>**ERRORE \_ GIÀ \_ INIZIALIZZATO**</dt> </dl> | Se l'sha è stato inizializzato in precedenza, viene restituito questo errore.<br/>                                                      |
| <dl> <dt>**PROTEZIONE \_ ACCESSO ALLA RETE E NON \_ \_ REGISTRATO**</dt> </dl>     | Se l'SHA non è stato registrato in precedenza, viene restituito questo errore.<br/>                                                      |
| <dl> <dt>**RPC \_ E \_ DISCONNESSO**</dt> </dl>        | NapAgent è stato arrestato. Questo oggetto verrà ripristinato automaticamente e riassociato a NapAgent, dopo il riavvio.<br/> |



 

## <a name="remarks"></a>Commenti

NapAgent non attiva uno scambio soh come risultato dell'inizializzazione. Un agente integrità sistema deve chiamare [**NotifySoHChange**](inapsystemhealthagentbinding-notifysohchange-method.md) per richiedere uno scambio di pacchetti SoH dopo l'inizializzazione con NapAgent.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                      |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>NapSystemHealthAgent.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthAgent.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





