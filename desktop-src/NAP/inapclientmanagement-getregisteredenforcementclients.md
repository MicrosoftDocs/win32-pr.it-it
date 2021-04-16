---
title: Metodo INapClientManagement GetRegisteredEnforcementClients (NapManagement. h)
description: Recupera le informazioni sui client di imposizione registrati.
ms.assetid: aae7c57c-a7fe-4cb2-94f6-53e501e38054
keywords:
- NAP metodo GetRegisteredEnforcementClients
- Metodo GetRegisteredEnforcementClients NAP, interfaccia INapClientManagement
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
ms.openlocfilehash: 7767f96c9b5410b3de9cfef3695193c0d5572b2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477819"
---
# <a name="inapclientmanagementgetregisteredenforcementclients-method"></a>Metodo INapClientManagement:: GetRegisteredEnforcementClients

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **GetRegisteredEnforcementClients** recupera le informazioni sui client di imposizione registrati.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetRegisteredEnforcementClients(
  [out] EnforcementEntityCount       *count,
  [out] NapComponentRegistrationInfo **enforcers
) const;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*numero* \[ di out\]
</dt> <dd>

Puntatore a un [**EnforcementEntityCount**](nap-datatypes.md) contenente il numero di client di imposizione registrati.

</dd> <dt>

*imposizione* \[ out\]
</dt> <dd>

Puntatore a una matrice di strutture [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) che descrivono i client di imposizione registrati.

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

 

 





