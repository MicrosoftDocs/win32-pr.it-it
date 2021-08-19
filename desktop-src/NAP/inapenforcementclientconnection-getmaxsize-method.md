---
title: Metodo GetMaxSize INapEnforcementClientConnection (NapEnforcementClient.h)
description: Ottiene le dimensioni massime del pacchetto SoH per questo client.
ms.assetid: 054bc783-db5d-4801-8984-6b8a131744a2
keywords:
- Metodo GetMaxSize nap
- Metodo GetMaxSize NAP, interfaccia INapEnforcementClientConnection
- Interfaccia INapEnforcementClientConnection NAP, metodo GetMaxSize
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetMaxSize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cacde01de088739f6e2dc8b8952c81394d82120e278b072189ed1572555740a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117799615"
---
# <a name="inapenforcementclientconnectiongetmaxsize-method"></a>Metodo INapEnforcementClientConnection::GetMaxSize

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo INapEnforcementClientConnection::GetMaxSize** ottiene le dimensioni massime del pacchetto SoH per questo client.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetMaxSize(
  [out] ProtocolMaxSize *maxSize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*maxSize* \[ Cambio\]
</dt> <dd>

Puntatore a [**un oggetto ProtocolMaxSize**](nap-datatypes.md) che indica le dimensioni massime, in byte, del pacchetto SoH.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Possono essere restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Operazione riuscita.<br/>                                    |
| <dl> <dt>**E \_ ACCESSO NEGATO**</dt> </dl> | Errore di autorizzazioni, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite di risorse di sistema: impossibile eseguire l'operazione.<br/> |



 

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

 

 





