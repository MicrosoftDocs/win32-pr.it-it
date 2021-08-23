---
title: Metodo INapEnforcementClientConnection GetStringCorrelationId (NapEnforcementClient.h)
description: Ottiene la versione stringa dell'ID utilizzato per correlare richieste e risposte.
ms.assetid: d744fa4e-5e30-429e-810d-7326047bb3f8
keywords:
- Metodo GetStringCorrelationId nap
- Metodo GetStringCorrelationId NAP, interfaccia INapEnforcementClientConnection
- Metodo GetStringCorrelationId dell'interfaccia INapEnforcementClientConnection nap
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetStringCorrelationId
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c7a7729873958d830e40a1979abb5fbcb3135ec4f08ae75af8396244ef35537
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119781011"
---
# <a name="inapenforcementclientconnectiongetstringcorrelationid-method"></a>Metodo INapEnforcementClientConnection::GetStringCorrelationId

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo INapEnforcementClientConnection::GetStringCorrelationId** ottiene la versione stringa dell'ID usato per correlare richieste e risposte.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetStringCorrelationId(
  [out] CountedString **correlationId
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*correlationId* \[ Cambio\]
</dt> <dd>

Puntatore a una [**struttura CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) che contiene la versione stringa di [**CorrelationId della connessione.**](/windows/win32/api/naptypes/ns-naptypes-correlationid)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Possono essere restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Operazione riuscita.<br/>                                    |
| <dl> <dt>**E \_ ACCESSO NEGATO**</dt> </dl> | Errore di autorizzazioni, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite risorse di sistema: impossibile eseguire l'operazione.<br/> |



 

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

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





