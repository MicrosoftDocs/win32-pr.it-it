---
title: Metodo GetMachineName INapSystemHealthValidationRequest (NapSystemHealthValidator. h)
description: Viene utilizzato da convalida integrità sistema (SHV) per recuperare il nome del computer del client di protezione accesso alla rete. Il servizio di convalida dell'integrità registra quindi queste informazioni.
ms.assetid: 2ea6a65d-1579-4a05-b5bc-aebf6421e46a
keywords:
- Metodo GetMachineName NAP
- Metodo GetMachineName NAP, interfaccia INapSystemHealthValidationRequest
- Interfaccia INapSystemHealthValidationRequest NAP, metodo GetMachineName
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetMachineName
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be1c3e264d7d2d6e4d93e3ad71d7f3adc92ff8d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121655"
---
# <a name="inapsystemhealthvalidationrequestgetmachinename-method"></a>Metodo INapSystemHealthValidationRequest:: GetMachineName

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **INapSystemHealthValidationRequest:: GetMachineName** viene usato da convalida integrità sistema (SHV) per recuperare il nome del computer del client di protezione accesso alla rete. Il servizio di convalida dell'integrità registra quindi queste informazioni.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetMachineName(
  [out] CountedString **machineName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*nomecomputer* \[ out\]
</dt> <dd>

Puntatore a un puntatore a una struttura [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) contenente il nome del computer del client di protezione accesso alla rete.

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
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                               |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                    |
| Intestazione<br/>                   | <dl> <dt>NapSystemHealthValidator. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthValidator. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





