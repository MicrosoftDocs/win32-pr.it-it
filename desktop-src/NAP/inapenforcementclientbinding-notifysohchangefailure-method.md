---
title: Metodo INapEnforcementClientBinding NotifySoHChangeFailure (NapEnforcementClient.h)
description: Viene usato dal client di imposizione per informare NapAgent che non è stato possibile elaborare un oggetto INapEnforcementClientCallback NotifySoHChange precedente.
ms.assetid: 2de1626c-ffda-4191-90c4-72d0275965d9
keywords:
- Metodo NotifySoHChangeFailure NAP
- Metodo NotifySoHChangeFailure NAP , interfaccia INapEnforcementClientBinding
- Metodo NotifySoHChangeFailure dell'interfaccia INapEnforcementClientBinding NAP
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.NotifySoHChangeFailure
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f91ae79656ec8909a8bff041e3ddc2714f1cbd17a65362e08731e9ca411d57f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134219"
---
# <a name="inapenforcementclientbindingnotifysohchangefailure-method"></a>Metodo INapEnforcementClientBinding::NotifySoHChangeFailure

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **INapEnforcementClientBinding::NotifySoHChangeFailure** viene usato dal client di imposizione per informare NapAgent che non è stato possibile elaborare un [**oggetto INapEnforcementClientCallback::NotifySoHChange precedente.**](inapenforcementclientcallback-notifysohchange-method.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT NotifySoHChangeFailure();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Possono essere restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                             | Descrizione                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | L'operazione è riuscita.<br/>                            |
| <dl> <dt>**E \_ ACCESSO NEGATO**</dt> </dl>         | Errore di autorizzazione, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/> |
| <dl> <dt>**PROTEZIONE \_ ACCESSO ALLA RETE E NON \_ \_ INIZIALIZZATA**</dt> </dl> | L'applicazione non è stata inizializzata in precedenza.<br/>       |



 

## <a name="remarks"></a>Commenti

Come risultato di questo metodo, i tentativi di NapAgent di applicare la modifica SoH in un secondo momento chiamando di nuovo [**INapEnforcementClientCallback::NotifySoHChange.**](inapenforcementclientcallback-notifysohchange-method.md) Dopo che il client di imposizione ha chiamato [**INapEnforcementClientBinding::GetSoHRequest,**](inapenforcementclientbinding-getsohrequest-method.md)deve applicare la modifica, ad esempio nessun errore viene gestito da NapAgent dopo questo punto.

Il client di imposizione deve chiamare il metodo [**INapEnforcementClientBinding::Initialize**](inapenforcementclientbinding-initialize-method.md) prima di chiamare questo o qualsiasi altro metodo [**dell'interfaccia INapEnforcementClientBinding.**](inapenforcementclientbinding.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                                      |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>NapEnforcementClient.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapEnforcementClient.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>


</dt> <dt>

[**INapEnforcementClientBinding**](inapenforcementclientbinding.md)
</dt> <dt>

[**INapEnforcementClientBinding::GetSoHRequest**](inapenforcementclientbinding-getsohrequest-method.md)
</dt> <dt>

[**INapEnforcementClientCallback::NotifySoHChange**](inapenforcementclientcallback-notifysohchange-method.md)
</dt> </dl>

 

 





