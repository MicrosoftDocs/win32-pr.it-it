---
title: Metodo INapEnforcementClientConnection SetFlags (NapEnforcementClient.h)
description: Viene usato per distinguere le risposte per la prima volta dalle risposte a causa delle richieste SoHRequest memorizzate nella cache dagli imponitori. | Metodo INapEnforcementClientConnection SetFlags (NapEnforcementClient.h)
ms.assetid: 2f35bcdf-662c-431f-a39e-a7c758f35603
keywords:
- Metodo SetFlags NAP
- Metodo SetFlags NAP, interfaccia INapEnforcementClientConnection
- Interfaccia INapEnforcementClientConnection NAP, metodo SetFlags
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetFlags
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 306ab4312138136dc00aec701d322ed82e95a731c8c4f418fb2cfaddd921ed50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118133993"
---
# <a name="inapenforcementclientconnectionsetflags-method"></a>Metodo INapEnforcementClientConnection::SetFlags

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo INapEnforcementClientConnection::SetFlags** viene usato per distinguere le risposte per la prima volta dalle risposte a causa delle richieste SoHRequest memorizzate nella cache dagli imponitori.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetFlags(
  [in] UINT8 flags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*flag* \[ Pollici\]
</dt> <dd>

Flag che determinano se [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) è dovuto a un oggetto **SoHRequest memorizzato nella** cache. Se *flags* ha un valore [**freshSoHRequest**](nap-type-constants.md), si tratta di una nuova richiesta. in caso contrario, si tratta di una richiesta memorizzata nella cache.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Possono essere restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Operazione riuscita.<br/>                                    |
| <dl> <dt>**E \_ ACCESSO NEGATO**</dt> </dl> | Errore di autorizzazione, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/> |



 

## <a name="remarks"></a>Commenti

Questo valore viene impostato da NapAgent.

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

 

 





