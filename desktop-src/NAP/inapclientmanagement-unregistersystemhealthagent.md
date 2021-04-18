---
title: Metodo INapClientManagement UnregisterSystemHealthAgent (NapManagement. h)
description: Annulla la registrazione di un SHA con il sistema NAP.
ms.assetid: c3ad6f2a-c39a-4590-8487-24c802433845
keywords:
- NAP metodo UnregisterSystemHealthAgent
- Metodo UnregisterSystemHealthAgent NAP, interfaccia INapClientManagement
- Interfaccia INapClientManagement NAP, metodo UnregisterSystemHealthAgent
topic_type:
- apiref
api_name:
- INapClientManagement.UnregisterSystemHealthAgent
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbff7af1c279090d12883d2a4e06ee9bcc364438
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302022"
---
# <a name="inapclientmanagementunregistersystemhealthagent-method"></a>Metodo INapClientManagement:: UnregisterSystemHealthAgent

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **UnregisterSystemHealthAgent** Annulla la registrazione di un Sha con il sistema NAP.

## <a name="syntax"></a>Sintassi


```C++
HRESULT UnregisterSystemHealthAgent(
  [in] SystemHealthEntityId id
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ID* \[ in\]
</dt> <dd>

[**SystemHealthEntityId**](nap-datatypes.md) che identifica l'agente integrità sistema di cui annullare la registrazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un codice di stato HRESULT incluso ma non limitato a uno dei valori seguenti.



| Codice restituito                                                                                         | Descrizione                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                | Operazione riuscita.<br/>                                   |
| <dl> <dt>**E \_ AccessDenied**</dt> </dl>      | Errore delle autorizzazioni, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl>       | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/> |
| <dl> <dt>**NAP \_ E \_ ancora \_ associato**</dt> </dl> | SHA rimane associato e non è possibile annullare la registrazione.<br/>    |



 

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

 

 





