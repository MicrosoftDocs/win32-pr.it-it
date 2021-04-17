---
title: Metodo IBackgroundCopyCallback JobError (Deliveryoptimization. h)
description: Ottimizzazione recapito chiama l'implementazione del metodo JobError quando lo stato del processo viene modificato in BG_JOB_STATE_ERROR.
ms.assetid: 121712A5-98EB-4B2F-A004-A3BDF9C1332B
keywords:
- Metodo JobError
- Metodo JobError, interfaccia IBackgroundCopyCallback
- Interfaccia IBackgroundCopyCallback, metodo JobError
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback.JobError
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0122f5777303506be5fd81d0966b00f828bf2073
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400553"
---
# <a name="ibackgroundcopycallbackjoberror-method"></a>Metodo IBackgroundCopyCallback:: JobError

Ottimizzazione recapito chiama l'implementazione del metodo [**JobError**](https://www.bing.com/search?q=**JobError**) quando lo stato del processo viene modificato in BG_JOB_STATE_ERROR.

## <a name="syntax"></a>Sintassi


```C++
HRESULT JobError(
  [in] IBackgroundCopyJob   *pJob,
  [in] IBackgroundCopyError *pError
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pJob* \[ in\]
</dt> <dd>

Contiene informazioni relative al processo, ad esempio il numero di byte e i file trasferiti prima che si verifichi l'errore. Contiene inoltre i metodi per riprendere e annullare il processo. Non rilasciare *pJob*; Rilascia l'interfaccia quando il metodo [**JobError**](https://www.bing.com/search?q=**JobError**) restituisce.

</dd> <dt>

*perror* \[ in\]
</dt> <dd>

Contiene informazioni sull'errore, ad esempio il file elaborato al momento in cui si è verificato l'errore irreversibile e una descrizione dell'errore. Non rilasciare *perror*; Rilascia l'interfaccia quando il metodo [**JobError**](https://www.bing.com/search?q=**JobError**) restituisce.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo deve restituire **S_OK**; in caso contrario, continuare a chiamare questo metodo fino a quando non viene restituito **S_OK** . Per motivi di prestazioni, è consigliabile limitare il numero di volte in cui viene restituito un valore diverso da **S_OK** per alcune volte. In alternativa alla restituzione di un codice di errore, è consigliabile restituire sempre **S_OK** e gestire l'errore internamente. L'intervallo in cui viene chiamato questo metodo è arbitrario.

## <a name="remarks"></a>Commenti

Dopo aver determinato la cause dell'errore, eseguire una delle seguenti opzioni:

-   Per annullare il processo, chiamare il metodo [**Metodo ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md) .
-   Per accettare la parte del processo che è stata trasferita correttamente prima dell'errore, chiamare il metodo [**Metodo ibackgroundcopyjob:: complete**](ibackgroundcopyjob-complete.md) . Questa opzione non è applicabile ai processi di caricamento. non è possibile completare una parte di un processo di caricamento.
-   Per completare l'elaborazione del processo, risolvere il problema e quindi chiamare il metodo [**Metodo ibackgroundcopyjob:: Resume**](ibackgroundcopyjob-resume.md) .

Gli errori temporanei non generano chiamate al metodo [**JobError**](https://www.bing.com/search?q=**JobError**) .

Restituisce BG_ERROR_CONTEXT_REMOTE_FILE se il processo ha raggiunto un errore HTTP 403. in caso contrario, BG_ERROR_CONTEXT_NONE.

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

[**IBackgroundCopyError**](ibackgroundcopyerror.md)
</dt> <dt>

[**Metodo ibackgroundcopyjob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**Metodo ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[**Metodo ibackgroundcopyjob:: Resume**](ibackgroundcopyjob-resume.md)
</dt> </dl>

 

 





