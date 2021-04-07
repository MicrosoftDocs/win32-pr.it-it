---
title: Metodo INapEnforcementClientBinding GetSoHRequest (NapEnforcementClient. h)
description: Viene utilizzato dal client di imposizione per recuperare una richiesta di rapporto di integrità per una determinata connessione.
ms.assetid: 6fce6e84-ce03-48f2-957b-a41efe044fc5
keywords:
- NAP metodo GetSoHRequest
- Metodo GetSoHRequest NAP, interfaccia INapEnforcementClientBinding
- Interfaccia INapEnforcementClientBinding NAP, metodo GetSoHRequest
topic_type:
- apiref
api_name:
- INapEnforcementClientBinding.GetSoHRequest
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9fed4872df7ab328ab241b070a9eeb07907de85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964011"
---
# <a name="inapenforcementclientbindinggetsohrequest-method"></a>Metodo INapEnforcementClientBinding:: GetSoHRequest

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **INapEnforcementClientBinding:: GetSoHRequest** viene usato dal client di imposizione per recuperare una richiesta di rapporto di integrità per una determinata connessione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSoHRequest(
  [in]  INapEnforcementClientConnection *connection,
  [out] BOOL                            *retriggerHint
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*connessione* \[ a in\]
</dt> <dd>

Puntatore COM a un'interfaccia [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) . Il NapAgent non tiene i riferimenti all'oggetto associato a questa interfaccia dopo il completamento del metodo.

</dd> <dt>

*retriggerHint* \[ out\]
</dt> <dd>

Puntatore a un **bool** che indica se la connessione deve essere riattivata. È **true** se [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) è stato modificato dopo l'ultima chiamata a questa funzione o se [**ProbationTime**](nap-datatypes.md) è scaduto. In caso contrario, viene restituito **false** .

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

NapAgent imposta [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) per l'oggetto Connection.

Se una [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) è rimasta in attesa di questa connessione, viene ignorata e il Shas riceve una notifica di **SoHRequests** orfano.

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

 

 





