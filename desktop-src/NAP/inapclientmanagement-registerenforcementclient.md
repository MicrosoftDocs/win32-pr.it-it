---
title: Metodo INapClientManagement RegisterEnforcementClient (NapManagement.h)
description: Registra un client di imposizione con il sistema protezione accesso alla rete.
ms.assetid: 26ea45ea-a366-4162-91dc-06bcd0261c56
keywords:
- Metodo RegisterEnforcementClient NAP
- Metodo RegisterEnforcementClient NAP , interfaccia INapClientManagement
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
ms.openlocfilehash: 1e22deffb8f144e8f7176bd78fb18978228a26251be5591df61a322e5da17d3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134563"
---
# <a name="inapclientmanagementregisterenforcementclient-method"></a>Metodo INapClientManagement::RegisterEnforcementClient

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo RegisterEnforcementClient** registra un client di imposizione con il sistema nap.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RegisterEnforcementClient(
  [in] const NapComponentRegistrationInfo *enforcer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*enforcer* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura di dati NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) che contiene le informazioni di registrazione associate al client di imposizione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un codice di stato HRESULT che include, a sua volta, uno degli elementi seguenti.



| Codice restituito                                                                                            | Descrizione                                                                       |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Operazione riuscita.<br/>                                                  |
| <dl> <dt>**E \_ ACCESSO NEGATO**</dt> </dl>         | Errore di autorizzazione, accesso negato.<br/>                                      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/>                |
| <dl> <dt>**ID \_ IN CONFLITTO DI PROTEZIONE ACCESSO ALLA RETE \_ \_ E**</dt> </dl> | Un agente di imposizione che usa l'identificatore specificato è già registrato.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                               |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                         |
| Intestazione<br/>                   | <dl> <dt>NapManagement.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapManagement.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapClientManagement**](inapclientmanagement.md)
</dt> </dl>

 

 





