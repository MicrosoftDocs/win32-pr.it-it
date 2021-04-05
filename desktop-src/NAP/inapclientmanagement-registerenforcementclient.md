---
title: Metodo INapClientManagement RegisterEnforcementClient (NapManagement. h)
description: Registra un client di imposizione con il sistema NAP.
ms.assetid: 26ea45ea-a366-4162-91dc-06bcd0261c56
keywords:
- NAP metodo RegisterEnforcementClient
- Metodo RegisterEnforcementClient NAP, interfaccia INapClientManagement
- Interfaccia INapClientManagement NAP, metodo RegisterEnforcementClient
topic_type:
- apiref
api_name:
- INapClientManagement.RegisterEnforcementClient
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc8ed4b5fe5a97d60b764341f21f25628c3c3434
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120447"
---
# <a name="inapclientmanagementregisterenforcementclient-method"></a>Metodo INapClientManagement:: RegisterEnforcementClient

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **RegisterEnforcementClient** registra un client di imposizione con il sistema NAP.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RegisterEnforcementClient(
  [in] const NapComponentRegistrationInfo *enforcer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*applicazione* \[ in\]
</dt> <dd>

Puntatore a una struttura di dati [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) che contiene le informazioni di registrazione associate al client di imposizione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un codice di stato HRESULT incluso ma non limitato a uno dei valori seguenti.



| Codice restituito                                                                                            | Descrizione                                                                       |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                   | Operazione riuscita.<br/>                                                  |
| <dl> <dt>**E \_ AccessDenied**</dt> </dl>         | Errore delle autorizzazioni, accesso negato.<br/>                                      |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl>          | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/>                |
| <dl> <dt>**protezione accesso alla rete \_ E \_ ID in conflitto \_**</dt> </dl> | Un agente di imposizione che usa l'identificatore specificato è già registrato.<br/> |



 

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

 

 





