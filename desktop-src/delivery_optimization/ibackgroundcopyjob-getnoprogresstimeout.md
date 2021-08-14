---
title: Metodo IBackgroundCopyJob GetNoProgressTimeout (Deliveryoptimization.h)
description: Recupera il periodo di tempo durante il quale il servizio tenta di trasferire il file dopo che si verifica una condizione di errore temporaneo. Se lo stato è in corso, il timer viene reimpostato.
ms.assetid: 3C31A15B-62EF-4807-8EC3-78BAEA3E23AE
keywords:
- Metodo GetNoProgressTimeout
- Metodo GetNoProgressTimeout, interfaccia IBackgroundCopyJob
- Interfaccia IBackgroundCopyJob, metodo GetNoProgressTimeout
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
ms.openlocfilehash: 9a80e4d89c510885372a92d2c373d5fb73e9bd8375dd712ec07c5f98be51f791
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755431"
---
# <a name="ibackgroundcopyjobgetnoprogresstimeout-method"></a>Metodo IBackgroundCopyJob::GetNoProgressTimeout

Recupera il periodo di tempo durante il quale il servizio tenta di trasferire il file dopo che si verifica una condizione di errore temporaneo. Se lo stato è in corso, il timer viene reimpostato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetNoProgressTimeout(
  [in] ULONG *pRetryPeriod
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pRetryPeriod* \[ Pollici\]
</dt> <dd>

Periodo di tempo, in secondi, in cui il servizio tenta di trasferire il file dopo che si è verificato un errore temporaneo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce i valori **HRESULT** seguenti, oltre ad altri.



| Codice restituito                                                                              | Descrizione                                     |
|------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>S_OK****</dt> </dl> | Il timeout è stato recuperato correttamente.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1709 \[\]<br/>                                           |
| Server minimo supportato<br/> | Windows Server, solo app desktop versione 1709 \[\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob definito come 37668D37-507E-4160-9316-26306D150B12<br/>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**IBackgroundCopyJob::SetNoProgressTimeout**](ibackgroundcopyjob-setnoprogresstimeout.md)
</dt> </dl>

 

 





