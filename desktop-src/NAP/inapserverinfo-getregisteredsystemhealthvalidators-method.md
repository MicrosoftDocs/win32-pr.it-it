---
title: Metodo INapServerInfo GetRegisteredSystemHealthValidators (NapServerManagement. h)
description: Recupera un elenco di SHV registrati.
ms.assetid: 029c7d5c-b397-415c-a530-0096de1ef771
keywords:
- NAP metodo GetRegisteredSystemHealthValidators
- Metodo GetRegisteredSystemHealthValidators NAP, interfaccia INapServerInfo
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
ms.openlocfilehash: 16ffdd4d363c994efbecdb57fe4ad7203393fd1f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048631"
---
# <a name="inapserverinfogetregisteredsystemhealthvalidators-method"></a>Metodo INapServerInfo:: GetRegisteredSystemHealthValidators

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **INapServerInfo:: GetRegisteredSystemHealthValidators** recupera un elenco di SHV registrati.

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

*numero* \[ di out\]
</dt> <dd>

Puntatore a un [**SystemHealthEntityCount**](nap-type-constants.md) contenente il numero di SHV registrati.

</dd> <dt>

*validator* \[ out\]
</dt> <dd>

Puntatore a un puntatore a una struttura [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) che contiene le informazioni di registrazione di convalida integrità sistema.

</dd> <dt>

*validatorClsids* \[ out\]
</dt> <dd>

Puntatore a una matrice di ID per il SHV registrato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

È possibile che vengano restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Operazione riuscita.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl> | Errore delle autorizzazioni, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                          |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                               |
| Intestazione<br/>                   | <dl> <dt>NapServerManagement. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapServerManagement. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qsvrmgmt.dll</dt> </dl>            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo)
</dt> <dt>

[**INapServerInfo**](inapserverinfo.md)
</dt> </dl>

 

 





