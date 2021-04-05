---
title: Metodo INapEnforcementClientConnection SetSoHRequest (NapEnforcementClient. h)
description: Imposta la richiesta di rapporto di integrità.
ms.assetid: 87dbb982-a337-4644-a2fe-970bfdd6c140
keywords:
- NAP metodo SetSoHRequest
- Metodo SetSoHRequest NAP, interfaccia INapEnforcementClientConnection
- Interfaccia INapEnforcementClientConnection NAP, metodo SetSoHRequest
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetSoHRequest
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92559d532e99bfa29d7f62fd29b279db20f2c0a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740911"
---
# <a name="inapenforcementclientconnectionsetsohrequest-method"></a>Metodo INapEnforcementClientConnection:: SetSoHRequest

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **INapEnforcementClientConnection:: SetSoHRequest** imposta la richiesta di rapporto di integrità.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetSoHRequest(
  [in, unique] const NetworkSoHRequest *sohRequest
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*sohRequest* \[ in\]
</dt> <dd>

Puntatore a una struttura [**NetworkSoHRequest**](/windows/win32/api/naptypes/ns-naptypes-networksoh) univoca, ovvero un BLOB di dati opachi per l'applicazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

È possibile che vengano restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Il pacchetto del rapporto di integrità è valido.<br/>                                |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Errore delle autorizzazioni, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/> |



 

## <a name="remarks"></a>Commenti

Questa impostazione è impostata da NapAgent ed è sottoposta a query da Enforcer da inviare in transito.

Il pacchetto di rapporto di integrità con lunghezza zero byte non è valido.

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

 

 





