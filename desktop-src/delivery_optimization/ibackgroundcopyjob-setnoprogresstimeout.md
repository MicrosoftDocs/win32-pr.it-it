---
title: Metodo IBackgroundCopyJob SetNoProgressTimeout (Deliveryoptimization.h)
description: Imposta il periodo di tempo durante il Ottimizzazione recapito (DO) tenta di trasferire il file dopo che si verifica una condizione di errore temporaneo. Se lo stato è in corso, il timer viene reimpostato.
ms.assetid: DC86F74F-8429-4D78-B425-CAF19867B05E
keywords:
- Metodo SetNoProgressTimeout
- Metodo SetNoProgressTimeout, interfaccia IBackgroundCopyJob
- Interfaccia IBackgroundCopyJob, metodo SetNoProgressTimeout
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.SetNoProgressTimeout
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dcf6905388d54103aaac34ae934c89e2fd8ccc16ce32a384eb730376606351b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118542928"
---
# <a name="ibackgroundcopyjobsetnoprogresstimeout-method"></a>Metodo IBackgroundCopyJob::SetNoProgressTimeout

Imposta il periodo di tempo durante il Ottimizzazione recapito (DO) tenta di trasferire il file dopo che si verifica una condizione di errore temporaneo. Se lo stato è in corso, il timer viene reimpostato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetNoProgressTimeout(
  [in] ULONG RetryPeriod
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*RetryPeriod* \[ Pollici\]
</dt> <dd>

Periodo di tempo, in secondi, in cui DO tenta di trasferire il file dopo che non è stato effettuato alcun avanzamento. Il periodo di ripetizione dei tentativi predefinito per il processo con priorità alta è 3600 secondi (1 ora) e per il processo con priorità bassa è 86400 secondi (24 ore).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce i valori **HRESULT** seguenti, oltre ad altri.



| Codice restituito                                                                                          | Descrizione                                                                                          |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK****</dt> </dl>             | Periodo di ripetizione dei tentativi impostato correttamente.<br/>                                                            |
| <dl> <dt>**DO_E_INVALID_STATE**</dt> </dl> | Lo stato del processo non può essere BG_JOB_STATE_CANCELLED o BG_JOB_STATE_ACKNOWLEDGED.<br/> |



 

## <a name="remarks"></a>Commenti

Se DO non procede durante il periodo di ripetizione dei tentativi, sposta lo stato del processo da BG_JOB_STATE_TRANSIENT_ERROR a BG_JOB_STATE_ERROR. Se si richiede la notifica di errore, DO chiama il callback [**JobError.**](https://www.bing.com/search?q=**JobError**)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1709 \[\]<br/>                                           |
| Server minimo supportato<br/> | Windows Server, solo app desktop versione 1709 \[\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob è definito come 37668D37-507E-4160-9316-26306D150B12<br/>               |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**IBackgroundCopyJob::GetNoProgressTimeout**](ibackgroundcopyjob-getnoprogresstimeout.md)
</dt> </dl>

 

 





