---
title: Metodo IBackgroundCopyCallback JobError (Deliveryoptimization.h)
description: Ottimizzazione recapito (DO) chiama l'implementazione del metodo JobError quando lo stato del processo cambia in BG_JOB_STATE_ERROR.
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
ms.openlocfilehash: 307ab18a0f956e5a2f4f14e9782f90b8ec6bff723da04aa9866566d95c53dca7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543133"
---
# <a name="ibackgroundcopycallbackjoberror-method"></a>Metodo IBackgroundCopyCallback::JobError

Ottimizzazione recapito (DO) chiama l'implementazione del metodo [**JobError**](https://www.bing.com/search?q=**JobError**) quando lo stato del processo cambia in BG_JOB_STATE_ERROR.

## <a name="syntax"></a>Sintassi


```C++
HRESULT JobError(
  [in] IBackgroundCopyJob   *pJob,
  [in] IBackgroundCopyError *pError
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pJob* \[ Pollici\]
</dt> <dd>

Contiene informazioni relative al processo, ad esempio il numero di byte e file trasferiti prima che si sia verificato l'errore. Contiene anche i metodi per riprendere e annullare il processo. Non rilasciare *pJob*; DO rilascia l'interfaccia quando il [**metodo JobError**](https://www.bing.com/search?q=**JobError**) viene restituito.

</dd> <dt>

*pError* \[ Pollici\]
</dt> <dd>

Contiene informazioni sull'errore, ad esempio il file elaborato al momento dell'errore irreversibile e una descrizione dell'errore. Non rilasciare *pError*; DO rilascia l'interfaccia quando il [**metodo JobError**](https://www.bing.com/search?q=**JobError**) viene restituito.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo deve **restituire** S_OK ; In caso contrario, DO continua a chiamare questo metodo finché non **S_OK** restituito. Per motivi di prestazioni, è consigliabile limitare il numero di volte in cui si restituisce un valore diverso da **S_OK** a un numero limitato di volte. In alternativa alla restituzione di un codice di errore, è consigliabile restituire sempre S_OK **e** gestire l'errore internamente. L'intervallo in corrispondenza del quale viene chiamato questo metodo è arbitrario.

## <a name="remarks"></a>Commenti

Dopo aver determinato la causa dell'errore, eseguire una delle opzioni seguenti:

-   Per annullare il processo, chiamare il [**metodo IBackgroundCopyJob::Cancel.**](ibackgroundcopyjob-cancel.md)
-   Per accettare la parte del processo trasferita correttamente prima dell'errore, chiamare il [**metodo IBackgroundCopyJob::Complete.**](ibackgroundcopyjob-complete.md) Questa opzione non si applica ai processi di caricamento. non è possibile completare una parte di un processo di caricamento.
-   Per completare l'elaborazione del processo, risolvere il problema e quindi chiamare il [**metodo IBackgroundCopyJob::Resume.**](ibackgroundcopyjob-resume.md)

Gli errori temporanei non generano chiamate al [**metodo JobError.**](https://www.bing.com/search?q=**JobError**)

DO restituisce BG_ERROR_CONTEXT_REMOTE_FILE se il processo ha raggiunto un errore HTTP 403, BG_ERROR_CONTEXT_NONE in caso contrario.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1709 \[\]<br/>                                           |
| Server minimo supportato<br/> | Windows Server, solo app desktop versione 1709 \[\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyCallback definito come 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22<br/>          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IBackgroundCopyCallback**](ibackgroundcopycallback.md)
</dt> <dt>

[**IBackgroundCopyError**](ibackgroundcopyerror.md)
</dt> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[**IBackgroundCopyJob::Resume**](ibackgroundcopyjob-resume.md)
</dt> </dl>

 

 





