---
title: Metodo INapSystemHealthValidationRequest2 GetConfigID (NapSystemHealthValidator. h)
description: Utilizzato dai validator di integrità del sistema (SHV) per recuperare l'ID configurazione in una richiesta di convalida.
ms.assetid: 6d5564e4-8386-444b-a859-f0c855e4ee30
keywords:
- NAP metodo GetConfigID
- Metodo GetConfigID NAP, interfaccia INapSystemHealthValidationRequest2
- Interfaccia INapSystemHealthValidationRequest2 NAP, metodo GetConfigID
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
ms.openlocfilehash: 0f3b41d2f08dc117fd28e704d607c628ec73e6ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302580"
---
# <a name="inapsystemhealthvalidationrequest2getconfigid-method"></a>Metodo INapSystemHealthValidationRequest2:: GetConfigID

> [!Note]  
> La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10

 

Il metodo **INapSystemHealthValidationRequest2:: GetConfigId** viene usato da convalida integrità sistema (SHV) per recuperare l'ID configurazione in una richiesta di convalida.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetConfigID(
  [out] UINT32 *configID
) const;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*configID* \[ out\]
</dt> <dd>

Al ritorno, un puntatore a UINT32 che contiene un ID di configurazione di convalida integrità di sistema.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei seguenti codici di errore in base al risultato di questa operazione.



| Codice restituito                                                                                  | Descrizione                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Operazione riuscita.<br/>                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Il parametro configID è **null**.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                               |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                                 |
| Intestazione<br/>                   | <dl> <dt>NapSystemHealthValidator. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthValidator. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**INapSystemHealthValidationRequest2**](inapsystemhealthvalidationrequest2.md)
</dt> </dl>

 

 





