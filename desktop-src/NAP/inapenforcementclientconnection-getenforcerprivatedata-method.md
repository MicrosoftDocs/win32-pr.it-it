---
title: Metodo INapEnforcementClientConnection GetEnforcerPrivateData (NapEnforcementClient.h)
description: Viene usato dall'esecutore per ottenere dati privati.
ms.assetid: a1f5b5a7-c862-4e5b-bf9c-b137f99f6165
keywords:
- Metodo GetEnforcerPrivateData nap
- Metodo GetEnforcerPrivateData NAP , interfaccia INapEnforcementClientConnection
- Metodo GetEnforcerPrivateData dell'interfaccia INapEnforcementClientConnection nap
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetEnforcerPrivateData
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60765a6cfd90ae1ea244b9b521e58bb5aeb3c4afd4217d5e39c51c94de02c324
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940064"
---
# <a name="inapenforcementclientconnectiongetenforcerprivatedata-method"></a>Metodo INapEnforcementClientConnection::GetEnforcerPrivateData

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo INapEnforcementClientConnection::GetEnforcerPrivateData** viene usato dall'applicazione per ottenere dati privati.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetEnforcerPrivateData(
  [out] PrivateData **privateData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*privateData* \[ Cambio\]
</dt> <dd>

Puntatore a un puntatore a un BLOB di dati opaco [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) che solo l'applicatore può interpretare.

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

 

 





