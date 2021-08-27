---
title: Metodo INapServerManagement UnregisterSystemHealthValidator (NapServerManagement.h)
description: Viene usato per annullare la registrazione di una shv con il server protezione accesso alla rete.
ms.assetid: f4148df1-a230-4845-ac8b-9e04be9e0d6c
keywords:
- Metodo UnregisterSystemHealthValidator NAP
- Metodo UnregisterSystemHealthValidator NAP , interfaccia INapServerManagement
- Interfaccia INapServerManagement NAP, metodo UnregisterSystemHealthValidator
topic_type:
- apiref
api_name:
- INapServerManagement.UnregisterSystemHealthValidator
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 116bcf2d2eec17389cf230bf0a1ad24ba386d2a6e35872570efda092e5992869
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037831"
---
# <a name="inapservermanagementunregistersystemhealthvalidator-method"></a>Metodo INapServerManagement::UnregisterSystemHealthValidator

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo INapServerManagement::UnregisterSystemHealthValidator** viene usato per annullare la registrazione di un shv con il server protezione accesso alla rete.

## <a name="syntax"></a>Sintassi


```C++
HRESULT UnregisterSystemHealthValidator(
  [in] SystemHealthEntityId id
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*id* \[ in\]
</dt> <dd>

[**SystemHealthEntityId che**](nap-type-constants.md) contiene l'identificatore univoco dell'istanza SHV di cui annullare la registrazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Possono essere restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                     | Descrizione                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Operazione riuscita.<br/>                                    |
| <dl> <dt>**E \_ ACCESSO NEGATO**</dt> </dl> | Errore di autorizzazione, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>  | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/> |



 

## <a name="remarks"></a>Commenti

Se sono presenti chiamate asincrone in sospeso in SHV, verranno completate in un secondo momento e verranno rimosse.

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

[**INapServerManagement**](inapservermanagement.md)
</dt> </dl>

 

 





