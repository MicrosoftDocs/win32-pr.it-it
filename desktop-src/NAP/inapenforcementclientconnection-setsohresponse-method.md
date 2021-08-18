---
title: Metodo INapEnforcementClientConnection SetSoHResponse (NapEnforcementClient.h)
description: Imposta il SoH-Response e viene utilizzato dal client di imposizione alla ricezione di un pacchetto.
ms.assetid: 718669c7-73cf-44f4-8463-c59fdbe215cc
keywords:
- Metodo SetSoHResponse nap
- Metodo SetSoHResponse NAP , interfaccia INapEnforcementClientConnection
- Interfaccia INapEnforcementClientConnection nap , metodo SetSoHResponse
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetSoHResponse
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97a86c1a0fc86fcef9189f9d575063cee9abdf627e1cf3c58e68d669358142f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626231"
---
# <a name="inapenforcementclientconnectionsetsohresponse-method"></a>Metodo INapEnforcementClientConnection::SetSoHResponse

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo INapEnforcementClientConnection::SetSoHResponse** imposta il SoH-Response e viene usato dal client di imposizione alla ricezione di un pacchetto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetSoHResponse(
  [in] const NetworkSoHResponse *sohResponse
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*sohResponse* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura NetworkSoHResponse**](/windows/win32/api/naptypes/ns-naptypes-networksoh) univoca, ovvero un BLOB di dati opaco per l'applicatore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Possono essere restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Il pacchetto SoH è valido.<br/>                                |
| <dl> <dt>**E \_ ACCESSO NEGATO**</dt> </dl> | Errore di autorizzazioni, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite di risorse di sistema: impossibile eseguire l'operazione.<br/> |



 

## <a name="remarks"></a>Commenti

Un pacchetto di dimensioni zero è valido.

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

 

 





