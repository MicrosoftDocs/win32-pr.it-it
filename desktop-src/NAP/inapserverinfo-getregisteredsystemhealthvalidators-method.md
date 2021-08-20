---
title: Metodo INapServerInfo GetRegisteredSystemHealthValidators (NapServerManagement.h)
description: Recupera un elenco di shv registrati.
ms.assetid: 029c7d5c-b397-415c-a530-0096de1ef771
keywords:
- Metodo GetRegisteredSystemHealthValidators NAP
- Metodo GetRegisteredSystemHealthValidators NAP , interfaccia INapServerInfo
- Interfaccia INapServerInfo NAP, metodo GetRegisteredSystemHealthValidators
topic_type:
- apiref
api_name:
- INapServerInfo.GetRegisteredSystemHealthValidators
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54e096d706107ca812e569e46c980f56cdc7b8eba14f4742530f632570fd3d08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118133946"
---
# <a name="inapserverinfogetregisteredsystemhealthvalidators-method"></a>Metodo INapServerInfo::GetRegisteredSystemHealthValidators

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo INapServerInfo::GetRegisteredSystemHealthValidators** recupera un elenco di shv registrati.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetRegisteredSystemHealthValidators(
  [out] SystemHealthEntityCount      *count,
  [out] NapComponentRegistrationInfo **validators,
  [out] CLSID                        **validatorClsids
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*count* \[ Cambio\]
</dt> <dd>

Puntatore a [**systemHealthEntityCount**](nap-type-constants.md) che contiene il numero di SHV registrati.

</dd> <dt>

*validator* \[ Cambio\]
</dt> <dd>

Puntatore a un puntatore a una [**struttura NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) che contiene le informazioni di registrazione SHV.

</dd> <dt>

*validatorClsids* \[ Cambio\]
</dt> <dd>

Puntatore a una matrice di ID per gli SHV registrati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Possono essere restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Operazione riuscita.<br/>                                    |
| <dl> <dt>**E \_ ACCESSO NEGATO**</dt> </dl> | Errore di autorizzazione, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                          |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                               |
| Intestazione<br/>                   | <dl> <dt>NapServerManagement.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapServerManagement.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qsvrmgmt.dll</dt> </dl>            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo)
</dt> <dt>

[**INapServerInfo**](inapserverinfo.md)
</dt> </dl>

 

 





