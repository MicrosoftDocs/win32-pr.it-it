---
title: Metodo INapClientManagement GetRegisteredEnforcementClients (NapManagement.h)
description: Recupera informazioni sui client di imposizione registrati.
ms.assetid: aae7c57c-a7fe-4cb2-94f6-53e501e38054
keywords:
- Metodo GetRegisteredEnforcementClients nap
- Metodo GetRegisteredEnforcementClients NAP , interfaccia INapClientManagement
- Interfaccia INapClientManagement NAP, metodo GetRegisteredEnforcementClients
topic_type:
- apiref
api_name:
- INapClientManagement.GetRegisteredEnforcementClients
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae7854a36ffb1d313a1598764c5375a8146471c1b2fd930b4022948f147acc24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940209"
---
# <a name="inapclientmanagementgetregisteredenforcementclients-method"></a>Metodo INapClientManagement::GetRegisteredEnforcementClients

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo GetRegisteredEnforcementClients** recupera informazioni sui client di imposizione registrati.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetRegisteredEnforcementClients(
  [out] EnforcementEntityCount       *count,
  [out] NapComponentRegistrationInfo **enforcers
) const;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*count* \[ Cambio\]
</dt> <dd>

Puntatore a un [**oggetto EnforcementEntityCount**](nap-datatypes.md) che contiene il numero di client di imposizione registrati.

</dd> <dt>

*imponitori* \[ Cambio\]
</dt> <dd>

Puntatore a una matrice di [**strutture NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) che descrivono i client di imposizione registrati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un codice di stato HRESULT che include, ma non solo, uno degli elementi seguenti.



| Codice restituito                                                                                         | Descrizione                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                | Operazione riuscita.<br/>                                   |
| <dl> <dt>**E \_ ACCESSO NEGATO**</dt> </dl>      | Errore di autorizzazioni, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>       | Limite di risorse di sistema: impossibile eseguire l'operazione.<br/> |
| <dl> <dt>**RPC \_ E \_ DISCONNESSO**</dt> </dl> | NapAgent non è in esecuzione.<br/>                            |



 

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

 

 





