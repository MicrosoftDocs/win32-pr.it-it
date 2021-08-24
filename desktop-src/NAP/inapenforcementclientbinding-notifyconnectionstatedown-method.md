---
title: Metodo INapEnforcementClientBinding NotifyConnectionStateDown (NapEnforcementClient.h)
description: Viene usato per informare NapAgent che una connessione a un client di imposizione è stata erta.
ms.assetid: 504c61c1-c8f9-46b8-87cd-c1f04846f0b3
keywords:
- Metodo NotifyConnectionStateDown nap
- Metodo NotifyConnectionStateDown NAP , interfaccia INapEnforcementClientBinding
- Metodo NotifyConnectionStateDown dell'interfaccia INapEnforcementClientBinding nap
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.NotifyConnectionStateDown
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e0e40d3b46e8c970287f49d983d89733d4858e38671ac93fb75d482c0259a73
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803051"
---
# <a name="inapenforcementclientbindingnotifyconnectionstatedown-method"></a>Metodo INapEnforcementClientBinding::NotifyConnectionStateDown

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo INapEnforcementClientBinding::NotifyConnectionStateDown** viene usato per informare NapAgent che una connessione a un client di imposizione è stata nessa.

## <a name="syntax"></a>Sintassi


```C++
HRESULT NotifyConnectionStateDown(
  [in] INapEnforcementClientConnection *downCxn
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*downCxn* \[ Pollici\]
</dt> <dd>

Puntatore COM [**all'interfaccia INapEnforcementClientConnection**](inapenforcementclientconnection.md) della connessione in corso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Possono essere restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                             | Descrizione                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | L'operazione è riuscita.<br/>                            |
| <dl> <dt>**E \_ ACCESSO NEGATO**</dt> </dl>         | Errore di autorizzazioni, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | Limite di risorse di sistema: impossibile eseguire l'operazione.<br/> |
| <dl> <dt>**PROTEZIONE \_ ACCESSO ALLA RETE NON \_ \_ INIZIALIZZATA**</dt> </dl> | L'applicazione non è stata inizializzata in precedenza.<br/>       |



 

## <a name="remarks"></a>Commenti

Quando una delle connessioni stabilite da un client di imposizione non è più attiva, il client di imposizione deve rimuovere la connessione dall'elenco attivo e informare NapAgent usando questo metodo. Non appena questa chiamata viene restituita, l'oggetto connessione può essere rilasciato e liberato. NapAgent non contenerà riferimenti all'oggetto connessione.

Come risultato di questa notifica, NapAgent aggiorna lo stato di Protezione accesso alla rete di sistema in base alle esigenze.

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
</dt> </dl>

 

 





