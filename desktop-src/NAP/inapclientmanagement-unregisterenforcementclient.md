---
title: Metodo INapClientManagement UnregisterEnforcementClient (NapManagement. h)
description: Annulla la registrazione di un client di imposizione con il sistema NAP.
ms.assetid: 549683de-7f2c-4da6-9616-862e0e99d21f
keywords:
- NAP metodo UnregisterEnforcementClient
- Metodo UnregisterEnforcementClient NAP, interfaccia INapClientManagement
- Interfaccia INapClientManagement NAP, metodo UnregisterEnforcementClient
topic_type:
- apiref
api_name:
- INapClientManagement.UnregisterEnforcementClient
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea318cf632ac00d54451b11428907c88159809df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120446"
---
# <a name="inapclientmanagementunregisterenforcementclient-method"></a>Metodo INapClientManagement:: UnregisterEnforcementClient

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **UnregisterEnforcementClient** Annulla la registrazione di un client di imposizione con il sistema NAP.

## <a name="syntax"></a>Sintassi


```C++
HRESULT UnregisterEnforcementClient(
  [in] EnforcementEntityId id
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ID* \[ in\]
</dt> <dd>

Valore [**EnforcementEntityId**](nap-datatypes.md) che identifica il client di imposizione di cui annullare la registrazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un codice di stato HRESULT incluso ma non limitato a uno dei valori seguenti.



| Codice restituito                                                                                         | Descrizione                                                                    |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                | Operazione riuscita.<br/>                                               |
| <dl> <dt>**E \_ AccessDenied**</dt> </dl>      | Errore delle autorizzazioni, accesso negato.<br/>                                   |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl>       | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/>             |
| <dl> <dt>**NAP \_ E \_ ancora \_ associato**</dt> </dl> | Impossibile annullare la registrazione del client di imposizione e rimanere associato.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                               |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                         |
| Intestazione<br/>                   | <dl> <dt>NapManagement. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapManagement. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapClientManagement**](inapclientmanagement.md)
</dt> </dl>

 

 





