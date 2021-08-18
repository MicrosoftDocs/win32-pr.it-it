---
title: Metodo GetError IBackgroundCopyJob (Deliveryoptimization.h)
description: Recupera l'interfaccia degli errori dopo che si è verificato un errore.
ms.assetid: 66891557-C118-4C66-AEFC-D8FD70976B9A
keywords:
- Metodo GetError
- Metodo GetError, interfaccia IBackgroundCopyJob
- Interfaccia IBackgroundCopyJob, metodo GetError
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetError
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 016f11023d50d7ea1fa9024e270a7ebce0597e07d5c33a915facae47773759c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755511"
---
# <a name="ibackgroundcopyjobgeterror-method"></a>Metodo IBackgroundCopyJob::GetError

Recupera l'interfaccia degli errori dopo che si è verificato un errore.

Ottimizzazione recapito (DO) genera un oggetto errore quando lo stato del processo è BG_JOB_STATE_ERROR o BG_JOB_STATE_TRANSIENT_ERROR. Il servizio non crea un oggetto errore quando una chiamata a un metodo di interfaccia **IBackgroundCopyXXXX** ha esito negativo. L'oggetto errore è disponibile fino a quando DO non inizia il trasferimento dei dati (lo stato del processo cambia in BG_JOB_STATE_TRANSFERRING) per il processo o fino alla chiusura dell'applicazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetError(
  [out] IBackgroundCopyError **ppError
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppError* \[ Cambio\]
</dt> <dd>

Interfaccia di errore che fornisce il codice di errore, una descrizione dell'errore e il contesto in cui si è verificato l'errore. Questo parametro identifica anche il file trasferito nel momento in cui si è verificato l'errore. Al *termine, rilasciare ppError.*

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce i valori **HRESULT** seguenti, oltre ad altri.



| Codice restituito                                                                                                           | Descrizione                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK****</dt> </dl>                              | L'oggetto errore è stato generato correttamente.<br/>                                                                                                                                                       |
| <dl> <dt>**DO_E_ERROR_INFORMATION_UNAVAILABLE**</dt> </dl> | L'interfaccia degli errori è disponibile solo dopo che si è verificato un errore (BG_JOB_STATE_ERROR o BG_JOB_STATE_TRANSIENT_ERROR) e prima che DO inizi a trasferire i dati (BG_JOB_STATE_TRANSFERRING).<br/> |



 

## <a name="remarks"></a>Commenti

Il processo viene inserito in uno stato di errore in caso di errori irreversibili. Usare una delle opzioni seguenti per determinare se il processo è in errore:

-   Per eseguire il polling dello stato del processo, chiamare il [**metodo IBackgroundCopyJob::GetState.**](ibackgroundcopyjob-getstate.md) Il processo è in errore se lo stato è BG_JOB_STATE_ERROR.
-   Per ricevere una notifica quando si verifica un errore, implementare [**l'interfaccia IBackgroundCopyCallback**](ibackgroundcopycallback.md) ,in particolare il [**metodo JobError.**](https://www.bing.com/search?q=**JobError**) Chiamare quindi il [**metodo IBackgroundCopyJob::SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) per registrare il callback e il metodo [**IBackgroundCopyJob::SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md) per impostare il flag BG_NOTIFY_JOB_ERROR.

[**L'interfaccia IBackgroundCopyError**](ibackgroundcopyerror.md) contiene informazioni che consentono di determinare la causa dell'errore e se il processo di trasferimento può continuare. Dopo aver determinato la causa dell'errore, eseguire una delle opzioni seguenti:

-   Per annullare il processo, chiamare il [**metodo IBackgroundCopyJob::Cancel.**](ibackgroundcopyjob-cancel.md)
-   Per salvare i file trasferiti correttamente prima che si sia verificato l'errore, chiamare il [**metodo IBackgroundCopyJob::Complete.**](ibackgroundcopyjob-complete.md)
-   Per completare l'elaborazione del processo, risolvere il problema e quindi chiamare il [**metodo IBackgroundCopyJob::Resume.**](ibackgroundcopyjob-resume.md)

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

[**IBackgroundCopyCallback::JobError**](ibackgroundcopycallback-joberror-method.md)
</dt> <dt>

[**IBackgroundCopyError**](ibackgroundcopyerror.md)
</dt> <dt>

[**IBackgroundCopyJob::GetState**](ibackgroundcopyjob-getstate.md)
</dt> </dl>

 

 





