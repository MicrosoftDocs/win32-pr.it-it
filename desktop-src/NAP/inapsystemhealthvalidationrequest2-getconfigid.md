---
title: Metodo INapSystemHealthValidationRequest2 GetConfigID (NapSystemHealthValidator.h)
description: Usato dai validator di integrità del sistema per recuperare l'ID configurazione in una richiesta di convalida.
ms.assetid: 6d5564e4-8386-444b-a859-f0c855e4ee30
keywords:
- Metodo GetConfigID NAP
- Metodo GetConfigID NAP, interfaccia INapSystemHealthValidationRequest2
- Interfaccia INapSystemHealthValidationRequest2 Nap , metodo GetConfigID
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest2.GetConfigID
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72acdd170726d2d94e4fbc46864a7e5aab6b902d7b1ee25b63ee0fa9e376c75e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119625981"
---
# <a name="inapsystemhealthvalidationrequest2getconfigid-method"></a>Metodo INapSystemHealthValidationRequest2::GetConfigID

> [!Note]  
> La piattaforma Protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il **metodo INapSystemHealthValidationRequest2::GetConfigId** viene usato dai validator di integrità del sistema per recuperare l'ID configurazione in una richiesta di convalida.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetConfigID(
  [out] UINT32 *configID
) const;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*configID* \[ Cambio\]
</dt> <dd>

In caso di restituzione, puntatore a UINT32 che contiene un ID di configurazione dell'shv.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei codici di errore seguenti in base al risultato di questa operazione.



| Codice restituito                                                                                  | Descrizione                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Operazione riuscita.<br/>                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Il parametro configID è **NULL.**<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                               |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                                 |
| Intestazione<br/>                   | <dl> <dt>NapSystemHealthValidator.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthValidator.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapSystemHealthValidationRequest2**](inapsystemhealthvalidationrequest2.md)
</dt> </dl>

 

 





