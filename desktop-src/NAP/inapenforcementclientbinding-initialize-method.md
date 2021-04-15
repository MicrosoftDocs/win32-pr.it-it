---
title: Metodo Initialize INapEnforcementClientBinding (NapEnforcementClient. h)
description: Avvia automaticamente il servizio NapAgent.
ms.assetid: 6b51043d-a8e7-41e4-9da9-e7f18f9bd068
keywords:
- Metodo di inizializzazione NAP
- Metodo Initialize NAP, interfaccia INapEnforcementClientBinding
- Interfaccia NAP di INapEnforcementClientBinding, metodo Initialize
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.Initialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee4d385e47bbbfe2e315d0a93d1f92542e8328e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476000"
---
# <a name="inapenforcementclientbindinginitialize-method"></a>Metodo INapEnforcementClientBinding:: Initialize

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **INapEnforcementClientBinding:: Initialize** avvia automaticamente il servizio napagent.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Initialize(
  [in] EnforcementEntityId           id,
  [in] INapEnforcementClientCallback *callback
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ID* \[ in\]
</dt> <dd>

Un [**EnforcementEntityId**](nap-datatypes.md) che identifica il client di imposizione e la relativa versione.

</dd> <dt>

*callback* \[ di in\]
</dt> <dd>

Puntatore COM a un'interfaccia [**INapEnforcementClientCallback**](inapenforcementclientcallback.md) usata da napagent per richiamare i client di imposizione con Notify/Process. NapAgent include un riferimento all'oggetto associato a questa interfaccia fino a quando non viene chiamato [**INapEnforcementClientBinding:: Uninitialize**](inapenforcementclientbinding-uninitialize-method.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

È possibile che vengano restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                                         | Descrizione                                                                              |
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                               | L'operazione è riuscita.<br/>                                                  |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>                     | Errore delle autorizzazioni, accesso negato.<br/>                                             |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>                      | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/>                       |
| <dl> <dt>**HRESULT (errore \_ già \_ inizializzato)**</dt> </dl> | Se l'applicazione è stata inizializzata in precedenza, viene restituito questo codice di errore.<br/> |
| <dl> <dt>**NAP \_ E \_ non \_ registrato**</dt> </dl>              | Se l'applicazione non è stata registrata in precedenza, viene restituito questo codice di errore.<br/>      |



 

## <a name="remarks"></a>Commenti

Il client di imposizione deve chiamare il metodo **INapEnforcementClientBinding:: Initialize** prima di chiamare qualsiasi altro metodo dell'interfaccia [**INapEnforcementClientBinding**](inapenforcementclientbinding.md) .

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
</dt> <dt>

[**INapEnforcementClientBinding:: Uninitialize**](inapenforcementclientbinding-uninitialize-method.md)
</dt> </dl>

 

 





