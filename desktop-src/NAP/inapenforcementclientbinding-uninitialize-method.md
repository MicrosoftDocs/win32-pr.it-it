---
title: Metodo INapEnforcementClientBinding Uninitialize (NapEnforcementClient.h)
description: Conclude il servizio NapAgent.
ms.assetid: 792600e5-586f-4858-8439-75761c928745
keywords:
- Annullare l'inizializzazione del metodo NAP
- Metodo Uninitialize NAP , interfaccia INapEnforcementClientBinding
- Interfaccia INapEnforcementClientBinding nap , metodo Uninitialize
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.Uninitialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 613646eb169ab12c788cc294ab012962606a77b5f9fe5dfc8c041e6a4ad6fa35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940145"
---
# <a name="inapenforcementclientbindinguninitialize-method"></a>Metodo INapEnforcementClientBinding::Uninitialize

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo INapEnforcementClientBinding::Uninitialize** termina il servizio NapAgent.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Uninitialize();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Possono essere restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | L'operazione è riuscita.<br/>                            |
| <dl> <dt>**E \_ ACCESSO NEGATO**</dt> </dl> | Errore di autorizzazioni, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite di risorse di sistema: impossibile eseguire l'operazione.<br/> |



 

## <a name="remarks"></a>Commenti

NapAgent blocca l'ulteriore elaborazione fino al completamento di tutte le chiamate esistenti sulle interfacce [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) e [**INapEnforcementClientCallback.**](inapenforcementclientcallback.md) Al termine di questa chiamata, NapAgent rilascia tutti i relativi riferimenti sui puntatori COM del client di imposizione.

Prima di chiamare questa funzione, l'applicatore deve chiamare [**INapEnforcementClientBinding::NotifyConnectionStateDown**](inapenforcementclientbinding-notifyconnectionstatedown-method.md) su tutte le connessioni attive, in modo che gli SHA possano ricevere una notifica se una delle relative SoH-Requests è orfana.

Il client di imposizione deve chiamare il metodo [**INapEnforcementClientBinding::Initialize**](inapenforcementclientbinding-initialize-method.md) prima di chiamare questo o qualsiasi altro metodo [**dell'interfaccia INapEnforcementClientBinding.**](inapenforcementclientbinding.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                                      |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>NapEnforcementClient.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>


</dt> <dt>

[**INapEnforcementClientBinding**](inapenforcementclientbinding.md)
</dt> <dt>

[**INapEnforcementClientBinding::NotifyConnectionStateDown**](inapenforcementclientbinding-notifyconnectionstatedown-method.md)
</dt> <dt>

[**INapEnforcementClientCallback**](inapenforcementclientcallback.md)
</dt> </dl>

 

 





