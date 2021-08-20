---
title: Metodo IBackgroundCopyCallback JobTransferred (Deliveryoptimization.h)
description: Ottimizzazione recapito chiama l'implementazione del metodo JobTransferred quando tutti i file nel processo sono stati trasferiti correttamente.
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
ms.openlocfilehash: 69cf1a739e15bc7341769bdc01549ad439a1c93877f653f0689e686eb8bac1f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047099"
---
# <a name="ibackgroundcopycallbackjobtransferred-method"></a>Metodo IBackgroundCopyCallback::JobTransferred

Ottimizzazione recapito chiama l'implementazione del metodo **JobTransferred** quando tutti i file nel processo sono stati trasferiti correttamente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT JobTransferred(
  [in] IBackgroundCopyJob *pJob
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pJob* \[ Pollici\]
</dt> <dd>

Contiene informazioni relative al processo, ad esempio l'ora di completamento del processo, il numero di byte trasferiti e il numero di file trasferiti. Non rilasciare *pJob*; DO rilascia l'interfaccia quando il metodo viene restituito.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo deve restituire S_OK.

## <a name="remarks"></a>Commenti

In genere, l'implementazione deve chiamare il [**metodo IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md) per confermare che DO ha trasferito correttamente i file. I file di download e il file di risposta non sono disponibili nel client fino a quando non si chiama il **metodo** Complete.

Se non si chiama il metodo [**Complete**](ibackgroundcopyjob-complete.md) o il metodo [**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md) DO annulla il processo dopo 30 giorni ed elimina i file incompleti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1709 \[\]<br/>                                           |
| Server minimo supportato<br/> | Windows Server, solo app desktop versione 1709 \[\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyCallback è definito come 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22<br/>          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IBackgroundCopyCallback**](ibackgroundcopycallback.md)
</dt> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md)
</dt> <dt>

[**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md)
</dt> </dl>

 

 





