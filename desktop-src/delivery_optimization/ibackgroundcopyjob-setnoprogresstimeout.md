---
title: Metodo metodo ibackgroundcopyjob SetNoProgressTimeout (Deliveryoptimization. h)
description: Imposta il periodo di tempo durante il quale l'ottimizzazione del recapito tenta di trasferire il file dopo che si è verificata una condizione di errore temporaneo. Se è presente lo stato di avanzamento, il timer viene reimpostato.
ms.assetid: DC86F74F-8429-4D78-B425-CAF19867B05E
keywords:
- Metodo SetNoProgressTimeout
- Metodo SetNoProgressTimeout, interfaccia metodo ibackgroundcopyjob
- Interfaccia metodo ibackgroundcopyjob, metodo SetNoProgressTimeout
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
ms.openlocfilehash: 276c8c44d2b2b034543aae25361c5f5c94046f5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048430"
---
# <a name="ibackgroundcopyjobsetnoprogresstimeout-method"></a>Metodo metodo ibackgroundcopyjob:: SetNoProgressTimeout

Imposta il periodo di tempo durante il quale l'ottimizzazione del recapito tenta di trasferire il file dopo che si è verificata una condizione di errore temporaneo. Se è presente lo stato di avanzamento, il timer viene reimpostato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetNoProgressTimeout(
  [in] ULONG RetryPeriod
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*RetryPeriod* \[ in\]
</dt> <dd>

Periodo di tempo, in secondi, che tenta di trasferire il file dopo che non è stato eseguito alcun avanzamento. Il periodo di ripetizione predefinito per il processo con priorità alta è 3600 secondi (1 ora) e per il processo con priorità bassa è 86400 secondi (24 ore).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce i valori **HRESULT** seguenti e altri.



| Codice restituito                                                                                          | Descrizione                                                                                          |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl>             | Il periodo di ripetizione dei tentativi è stato impostato.<br/>                                                            |
| <dl> <dt>**DO_E_INVALID_STATE**</dt> </dl> | Lo stato del processo non può essere BG_JOB_STATE_CANCELLED o BG_JOB_STATE_ACKNOWLEDGED.<br/> |



 

## <a name="remarks"></a>Commenti

Se DO non avanza durante il periodo di ripetizione dei tentativi, sposta lo stato del processo da BG_JOB_STATE_TRANSIENT_ERROR a BG_JOB_STATE_ERROR. Se si richiede la notifica di errore, chiamare il callback [**JobError**](https://www.bing.com/search?q=**JobError**) .

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

[**Metodo ibackgroundcopyjob:: GetNoProgressTimeout**](ibackgroundcopyjob-getnoprogresstimeout.md)
</dt> </dl>

 

 





