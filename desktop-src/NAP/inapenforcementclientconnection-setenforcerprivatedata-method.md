---
title: Metodo INapEnforcementClientConnection SetEnforcerPrivateData (NapEnforcementClient.h)
description: Viene usato dall'imponitore per impostare i dati privati.
ms.assetid: 56f6fec7-47ec-4b2c-b8c8-a4d519ba0f91
keywords:
- Metodo SetEnforcerPrivateData NAP
- Metodo SetEnforcerPrivateData NAP, interfaccia INapEnforcementClientConnection
- Metodo SetEnforcerPrivateData dell'interfaccia INapEnforcementClientConnection NAP
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetEnforcerPrivateData
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ebf42212d55f059286aa7b3d67f965b3b861755cc0291e57f339465291e5099
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118368100"
---
# <a name="inapenforcementclientconnectionsetenforcerprivatedata-method"></a>Metodo INapEnforcementClientConnection::SetEnforcerPrivateData

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo INapEnforcementClientConnection::SetEnforcerPrivateData** viene usato dall'applicazione per impostare i dati privati.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetEnforcerPrivateData(
  [in] const PrivateData *privateData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*privateData* \[ Pollici\]
</dt> <dd>

Puntatore a un BLOB di dati opaco [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) che solo l'applicatore può interpretare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Possono essere restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Operazione riuscita.<br/>                                    |
| <dl> <dt>**E \_ ACCESSO NEGATO**</dt> </dl> | Errore di autorizzazione, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/> |



 

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

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





