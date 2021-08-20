---
title: Metodo INapClientManagement UnregisterEnforcementClient (NapManagement.h)
description: Annulla la registrazione di un client di imposizione con il sistema di Protezione accesso alla rete.
ms.assetid: 549683de-7f2c-4da6-9616-862e0e99d21f
keywords:
- Metodo UnregisterEnforcementClient nap
- Metodo UnregisterEnforcementClient NAP , interfaccia INapClientManagement
- Metodo UnregisterEnforcementClient dell'interfaccia INapClientManagement nap
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
ms.openlocfilehash: e0298b55a5552f2a3ce7a40e048874076729f7e506475c8626de9e9e343da3b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134553"
---
# <a name="inapclientmanagementunregisterenforcementclient-method"></a>Metodo INapClientManagement::UnregisterEnforcementClient

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo UnregisterEnforcementClient** annulla la registrazione di un client di imposizione con il sistema di Protezione accesso alla rete.

## <a name="syntax"></a>Sintassi


```C++
HRESULT UnregisterEnforcementClient(
  [in] EnforcementEntityId id
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*id* \[ in\]
</dt> <dd>

Valore [**EnforcementEntityId**](nap-datatypes.md) che identifica il client di imposizione di cui annullare la registrazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un codice di stato HRESULT che include, ma non solo, uno degli elementi seguenti.



| Codice restituito                                                                                         | Descrizione                                                                    |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                | Operazione riuscita.<br/>                                               |
| <dl> <dt>**E \_ ACCESSO NEGATO**</dt> </dl>      | Errore di autorizzazioni, accesso negato.<br/>                                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>       | Limite di risorse di sistema: impossibile eseguire l'operazione.<br/>             |
| <dl> <dt>**NAP \_ E \_ ANCORA \_ ASSOCIATO**</dt> </dl> | Non è stato possibile annullare la registrazione del client di imposizione e rimane associato.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                               |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                         |
| Intestazione<br/>                   | <dl> <dt>NapManagement.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapManagement.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qagent.dll</dt> </dl>        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapClientManagement**](inapclientmanagement.md)
</dt> </dl>

 

 





