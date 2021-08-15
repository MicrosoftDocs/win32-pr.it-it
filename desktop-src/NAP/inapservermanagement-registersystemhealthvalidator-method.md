---
title: Metodo INapServerManagement RegisterSystemHealthValidator (NapServerManagement.h)
description: Registra un shv.
ms.assetid: 23f147d5-3c4e-48ca-940a-c4350ad6ecb3
keywords:
- Metodo RegisterSystemHealthValidator NAP
- Metodo RegisterSystemHealthValidator NAP , interfaccia INapServerManagement
- Interfaccia INapServerManagement NAP, metodo RegisterSystemHealthValidator
topic_type:
- apiref
api_name:
- INapServerManagement.RegisterSystemHealthValidator
api_location:
- qsvrmgmt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdb5dc93c5bb927ffb25df20f37e5b2c30560153efb006f3c91bf7e97efec360
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012569"
---
# <a name="inapservermanagementregistersystemhealthvalidator-method"></a>Metodo INapServerManagement::RegisterSystemHealthValidator

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo INapServerManagement::RegisterSystemHealthValidator** registra un shv.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RegisterSystemHealthValidator(
  [in] const NapComponentRegistrationInfo *validator,
  [in] const CLSID                        *validatorClsid
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*validator* \[ Pollici\]
</dt> <dd>

Puntatore a una [**struttura NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) che contiene le informazioni di registrazione SHV.

</dd> <dt>

*validatorClsid* \[ Pollici\]
</dt> <dd>

Puntatore al CLSID della classe COM che implementa [**l'interfaccia INapSystemHealthValidator.**](inapsystemhealthvalidator.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Possono essere restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                            | Descrizione                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Operazione riuscita.<br/>                                    |
| <dl> <dt>**E \_ ACCESSO NEGATO**</dt> </dl>        | Errore di autorizzazione, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>         | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/> |
| <dl> <dt>**ID \_ IN CONFLITTO DI PROTEZIONE ACCESSO ALLA RETE \_ \_ E**</dt> </dl> | L'ID SHV è già registrato.<br/>                           |



 

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

 

 





