---
title: Metodo INapClientManagement GetRegisteredSystemHealthAgents (NapManagement.h)
description: Recupera informazioni sugli sha registrati.
ms.assetid: c38d2d23-62d4-49f0-81a3-52394866f0c4
keywords:
- Metodo GetRegisteredSystemHealthAgents nap
- Metodo GetRegisteredSystemHealthAgents NAP , interfaccia INapClientManagement
- Interfaccia INapClientManagement NAP, metodo GetRegisteredSystemHealthAgents
topic_type:
- apiref
api_name:
- INapClientManagement.GetRegisteredSystemHealthAgents
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57d9c2792282245ad4903d77700f5413bef0d2f769a65753aed60f50ba759707
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117800111"
---
# <a name="inapclientmanagementgetregisteredsystemhealthagents-method"></a>Metodo INapClientManagement::GetRegisteredSystemHealthAgents

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo GetRegisteredSystemHealthAgents** recupera informazioni sugli SHA registrati.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetRegisteredSystemHealthAgents(
  [out] SystemHealthEntityCount      *count,
  [out] NapComponentRegistrationInfo **agents
) const;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*count* \[ Cambio\]
</dt> <dd>

Puntatore a un [**oggetto SystemHealthEntityCount**](nap-datatypes.md) che descrive il numero di sha registrati.

</dd> <dt>

*agenti* \[ Cambio\]
</dt> <dd>

Puntatore a una matrice di [**strutture NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) che descrivono gli SHA registrati.

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

 

 





