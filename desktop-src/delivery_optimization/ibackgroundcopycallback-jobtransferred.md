---
title: Metodo IBackgroundCopyCallback JobTransferred (Deliveryoptimization. h)
description: Ottimizzazione recapito chiama l'implementazione del metodo JobTransferred quando tutti i file del processo sono stati trasferiti correttamente.
ms.assetid: D3088279-2D26-4707-9BA2-19D2758EA1CC
keywords:
- Metodo JobTransferred
- Metodo JobTransferred, interfaccia IBackgroundCopyCallback
- Interfaccia IBackgroundCopyCallback, metodo JobTransferred
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback.JobTransferred
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6c5c358978da1731152ca6f7de8c3f7a92a1da86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119619"
---
# <a name="ibackgroundcopycallbackjobtransferred-method"></a>Metodo IBackgroundCopyCallback:: JobTransferred

Ottimizzazione recapito chiama l'implementazione del metodo **JobTransferred** quando tutti i file del processo sono stati trasferiti correttamente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT JobTransferred(
  [in] IBackgroundCopyJob *pJob
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pJob* \[ in\]
</dt> <dd>

Contiene informazioni relative al processo, ad esempio il momento in cui il processo è stato completato, il numero di byte trasferiti e il numero di file trasferiti. Non rilasciare *pJob*; Rilascia l'interfaccia quando il metodo restituisce.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo deve restituire S_OK.

## <a name="remarks"></a>Commenti

In genere, l'implementazione deve chiamare il metodo [**Metodo ibackgroundcopyjob:: complete**](ibackgroundcopyjob-complete.md) per confermare che i file sono stati trasferiti correttamente. Scaricare i file e il file di risposta non sono disponibili nel client fino a quando non viene chiamato il metodo **completo** .

Se non si chiama il metodo [**complete**](ibackgroundcopyjob-complete.md) o il metodo [**Metodo ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md) , Annulla il processo dopo 30 giorni ed Elimina i file incompleti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1709 \[\]<br/>                                           |
| Server minimo supportato<br/> | Windows Server, versione 1709 \[ solo per le app desktop\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyCallback viene definito come 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22<br/>          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IBackgroundCopyCallback**](ibackgroundcopycallback.md)
</dt> <dt>

[**Metodo ibackgroundcopyjob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**Metodo ibackgroundcopyjob:: complete**](ibackgroundcopyjob-complete.md)
</dt> <dt>

[**Metodo ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md)
</dt> </dl>

 

 





