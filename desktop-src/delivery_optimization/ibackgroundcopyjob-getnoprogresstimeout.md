---
title: Metodo metodo ibackgroundcopyjob GetNoProgressTimeout (Deliveryoptimization. h)
description: Recupera il periodo di tempo durante il quale il servizio tenta di trasferire il file dopo che si è verificata una condizione di errore temporaneo. Se è presente lo stato di avanzamento, il timer viene reimpostato.
ms.assetid: 3C31A15B-62EF-4807-8EC3-78BAEA3E23AE
keywords:
- Metodo GetNoProgressTimeout
- Metodo GetNoProgressTimeout, interfaccia metodo ibackgroundcopyjob
- Interfaccia metodo ibackgroundcopyjob, metodo GetNoProgressTimeout
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetNoProgressTimeout
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3ccd236c17612aa03a28e07a08d087454f8db6f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477033"
---
# <a name="ibackgroundcopyjobgetnoprogresstimeout-method"></a>Metodo metodo ibackgroundcopyjob:: GetNoProgressTimeout

Recupera il periodo di tempo durante il quale il servizio tenta di trasferire il file dopo che si è verificata una condizione di errore temporaneo. Se è presente lo stato di avanzamento, il timer viene reimpostato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetNoProgressTimeout(
  [in] ULONG *pRetryPeriod
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pRetryPeriod* \[ in\]
</dt> <dd>

Periodo di tempo, espresso in secondi, durante il quale il servizio tenta di trasferire il file dopo che si è verificato un errore temporaneo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce i valori **HRESULT** seguenti e altri.



| Codice restituito                                                                              | Descrizione                                     |
|------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl> | Timeout recuperato.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1709 \[\]<br/>                                           |
| Server minimo supportato<br/> | Windows Server, versione 1709 \[ solo per le app desktop\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob viene definito come 37668D37-507E-4160-9316-26306D150B12<br/>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Metodo ibackgroundcopyjob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**Metodo ibackgroundcopyjob:: SetNoProgressTimeout**](ibackgroundcopyjob-setnoprogresstimeout.md)
</dt> </dl>

 

 





