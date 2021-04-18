---
title: Metodo GetFlags INapEnforcementClientConnection (NapEnforcementClient. h)
description: Viene usato per distinguere le risposte per la prima volta da risposte dovute a SoHRequests memorizzate nella cache dalle forze di esecuzione. | Metodo GetFlags INapEnforcementClientConnection (NapEnforcementClient. h)
ms.assetid: e8399615-5190-46f7-a3bf-3070de548953
keywords:
- Metodo GetFlags NAP
- Metodo GetFlags NAP, interfaccia INapEnforcementClientConnection
- Interfaccia NAP di INapEnforcementClientConnection, Metodo GetFlags
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetFlags
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a35e183b5d4f606d21f4afce8cca68135732a35c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321310"
---
# <a name="inapenforcementclientconnectiongetflags-method"></a>Metodo INapEnforcementClientConnection:: GetFlags

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **INapEnforcementClientConnection:: GetFlags** viene usato per distinguere le risposte per la prima volta da risposte dovute alla memorizzazione nella cache di SoHRequests da parte degli Enforcer.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetFlags(
  [out] UINT8 *flags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*flag* \[ out\]
</dt> <dd>

Puntatore a un flag che determina se [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) è dovuto a un **SoHRequest** memorizzato nella cache. Se *Flags* ha un valore [**freshSoHRequest**](nap-type-constants.md), si tratta di una nuova richiesta; in caso contrario, è una richiesta memorizzata nella cache.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

È possibile che vengano restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Operazione riuscita.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Errore delle autorizzazioni, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/> |



 

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

[**INapEnforcementClientConnection**](inapenforcementclientconnection.md)
</dt> </dl>

 

 





