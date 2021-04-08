---
title: Metodo INapEnforcementClientConnection GetSoHResponse (NapEnforcementClient. h)
description: Ottiene la SoH-Response ricevuta dal client di imposizione.
ms.assetid: fc0084a3-a668-435e-8390-f322941c5cd4
keywords:
- NAP metodo GetSoHResponse
- Metodo GetSoHResponse NAP, interfaccia INapEnforcementClientConnection
- Interfaccia INapEnforcementClientConnection NAP, metodo GetSoHResponse
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetSoHResponse
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67be4d65135d6e4ce606a83eb08fdeed036cc62a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873557"
---
# <a name="inapenforcementclientconnectiongetsohresponse-method"></a>Metodo INapEnforcementClientConnection:: GetSoHResponse

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **INapEnforcementClientConnection:: GetSoHResponse** ottiene la SoH-Response ricevuta dal client di imposizione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSoHResponse(
  [out] NetworkSoHResponse **sohResponse
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*sohResponse* \[ out\]
</dt> <dd>

Puntatore a un puntatore a una struttura [**NetworkSoHResponse**](/windows/win32/api/naptypes/ns-naptypes-networksoh) univoca, ovvero un BLOB di dati opachi per l'applicazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

È possibile che vengano restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Operazione riuscita.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Errore delle autorizzazioni, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/> |



 

## <a name="remarks"></a>Commenti

Un pacchetto di dimensioni pari A zero byte è valido.

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

 

 





