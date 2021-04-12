---
title: Metodo INapServerManagement RegisterSystemHealthValidator (NapServerManagement. h)
description: Registra un servizio di convalida dell'integrità.
ms.assetid: 23f147d5-3c4e-48ca-940a-c4350ad6ecb3
keywords:
- NAP metodo RegisterSystemHealthValidator
- Metodo RegisterSystemHealthValidator NAP, interfaccia INapServerManagement
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
ms.openlocfilehash: 2abd8d42da196caa804a8919c6425fda9fcb950c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104225247"
---
# <a name="inapservermanagementregistersystemhealthvalidator-method"></a>Metodo INapServerManagement:: RegisterSystemHealthValidator

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **INapServerManagement:: RegisterSystemHealthValidator** registra un servizio di convalida dell'integrità.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RegisterSystemHealthValidator(
  [in] const NapComponentRegistrationInfo *validator,
  [in] const CLSID                        *validatorClsid
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*validator* \[ di in\]
</dt> <dd>

Puntatore a una struttura [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) che contiene le informazioni di registrazione di convalida integrità sistema.

</dd> <dt>

*validatorClsid* \[ in\]
</dt> <dd>

Puntatore al CLSID della classe COM che implementa l'interfaccia [**INapSystemHealthValidator**](inapsystemhealthvalidator.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

È possibile che vengano restituiti anche altri codici di errore specifici di COM.



| Codice restituito                                                                                            | Descrizione                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Operazione riuscita.<br/>                                    |
| <dl> <dt>**E \_ ACCESSDENIED**</dt> </dl>        | Errore delle autorizzazioni, accesso negato.<br/>                       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>         | Limite di risorse di sistema. Impossibile eseguire l'operazione.<br/> |
| <dl> <dt>**protezione accesso alla rete \_ E \_ ID in conflitto \_**</dt> </dl> | L'ID di convalida integrità sistema è già registrato.<br/>                           |



 

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

[**INapServerManagement**](inapservermanagement.md)
</dt> </dl>

 

 





