---
title: Metodo INapEnforcementClientBinding NotifyConnectionStateDown (NapEnforcementClient. h)
description: Viene usato per indicare al NapAgent che una connessione a un client di imposizione è diminuita.
ms.assetid: 504c61c1-c8f9-46b8-87cd-c1f04846f0b3
keywords:
- NAP metodo NotifyConnectionStateDown
- Metodo NotifyConnectionStateDown NAP, interfaccia INapEnforcementClientBinding
- Interfaccia INapEnforcementClientBinding NAP, metodo NotifyConnectionStateDown
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
ms.openlocfilehash: 3129883342f493fd56a4cc81513910e8789ca4f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519278"
---
# <a name="inapenforcementclientbindingnotifyconnectionstatedown-method"></a>Metodo INapEnforcementClientBinding:: NotifyConnectionStateDown

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **INapEnforcementClientBinding:: NotifyConnectionStateDown** viene usato per indicare al napagent che una connessione a un client di imposizione è diminuita.

## <a name="syntax"></a>Sintassi


```C++
HRESULT NotifyConnectionStateDown(
  [in] INapEnforcementClientConnection *downCxn
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*downCxn* \[ in\]
</dt> <dd>

Puntatore COM all'interfaccia [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) della connessione in basso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

È possibile che vengano restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                             | Descrizione                                                        |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | L'operazione è riuscita.<br/>                            |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>         | Errore delle autorizzazioni, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/> |
| <dl> <dt>**NAP \_ E \_ non \_ inizializzato**</dt> </dl> | L'applicazione non è stata inizializzata in precedenza.<br/>       |



 

## <a name="remarks"></a>Commenti

Quando una delle connessioni stabilite da un client di imposizione si arresta, il client di imposizione deve rimuovere la connessione dall'elenco attivo e informare il NapAgent usando questo metodo. Non appena la chiamata restituisce, l'oggetto connessione può essere rilasciato e liberato. NapAgent non conterrà riferimenti all'oggetto Connection.

In seguito a questa notifica, il NapAgent aggiorna lo stato di protezione accesso alla rete del sistema in base alle esigenze.

Il client di imposizione deve chiamare il metodo [**INapEnforcementClientBinding:: Initialize**](inapenforcementclientbinding-initialize-method.md) prima di chiamare questo o qualsiasi altro metodo dell'interfaccia [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                                      |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                |
| Intestazione<br/>                   | <dl> <dt>NapEnforcementClient. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapEnforcementClient. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>


</dt> <dt>

[**INapEnforcementClientBinding**](inapenforcementclientbinding.md)
</dt> </dl>

 

 





