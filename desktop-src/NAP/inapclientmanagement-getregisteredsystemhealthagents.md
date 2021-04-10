---
title: Metodo INapClientManagement GetRegisteredSystemHealthAgents (NapManagement. h)
description: Recupera le informazioni sul SHAs registrato.
ms.assetid: c38d2d23-62d4-49f0-81a3-52394866f0c4
keywords:
- NAP metodo GetRegisteredSystemHealthAgents
- Metodo GetRegisteredSystemHealthAgents NAP, interfaccia INapClientManagement
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
ms.openlocfilehash: a4852e2d4c1ffa08b1a7ea7b3d8395c1b116cca6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964522"
---
# <a name="inapclientmanagementgetregisteredsystemhealthagents-method"></a>Metodo INapClientManagement:: GetRegisteredSystemHealthAgents

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **GetRegisteredSystemHealthAgents** recupera le informazioni relative al Shas registrato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetRegisteredSystemHealthAgents(
  [out] SystemHealthEntityCount      *count,
  [out] NapComponentRegistrationInfo **agents
) const;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*numero* \[ di out\]
</dt> <dd>

Puntatore a un [**SystemHealthEntityCount**](nap-datatypes.md) che descrive il numero di Shas registrati.

</dd> <dt>

*agenti* \[ di out\]
</dt> <dd>

Puntatore a una matrice di strutture [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) che descrivono il Shas registrato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un codice di stato HRESULT incluso ma non limitato a uno dei valori seguenti.



| Codice restituito                                                                                         | Descrizione                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                | Operazione riuscita.<br/>                                   |
| <dl> <dt>**E \_ AccessDenied**</dt> </dl>      | Errore delle autorizzazioni, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl>       | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/> |
| <dl> <dt>**RPC \_ E \_ disconnessa**</dt> </dl> | NapAgent non è in esecuzione.<br/>                            |



 

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

 

 





