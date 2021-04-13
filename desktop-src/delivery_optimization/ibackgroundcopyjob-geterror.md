---
title: Metodo GetError metodo ibackgroundcopyjob (Deliveryoptimization. h)
description: Recupera l'interfaccia di errore dopo che si è verificato un errore.
ms.assetid: 66891557-C118-4C66-AEFC-D8FD70976B9A
keywords:
- Metodo GetError
- Metodo GetError, interfaccia metodo ibackgroundcopyjob
- Interfaccia metodo ibackgroundcopyjob, metodo getError
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
ms.openlocfilehash: 1f2da994da83a786b89adb5ae63104dbaa6e2ef9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400624"
---
# <a name="ibackgroundcopyjobgeterror-method"></a>Metodo metodo ibackgroundcopyjob:: GetError

Recupera l'interfaccia di errore dopo che si è verificato un errore.

L'ottimizzazione recapito genera un oggetto Error quando lo stato del processo è BG_JOB_STATE_ERROR o BG_JOB_STATE_TRANSIENT_ERROR. Il servizio non crea un oggetto Error quando una chiamata a un metodo di interfaccia **IBackgroundCopyXXXX** ha esito negativo. L'oggetto Error è disponibile fino a quando non inizia il trasferimento dei dati (lo stato del processo viene modificato in BG_JOB_STATE_TRANSFERRING) per il processo o fino alla chiusura dell'applicazione.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetError(
  [out] IBackgroundCopyError **ppError
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppError* \[ out\]
</dt> <dd>

Interfaccia di errore che fornisce il codice di errore, una descrizione dell'errore e il contesto in cui si è verificato l'errore. Questo parametro identifica anche il file da trasferire nel momento in cui si è verificato l'errore. Rilasciare *ppError* al termine.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce i valori **HRESULT** seguenti e altri.



| Codice restituito                                                                                                           | Descrizione                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl>                              | Generazione dell'oggetto Error completata.<br/>                                                                                                                                                       |
| <dl> <dt>**DO_E_ERROR_INFORMATION_UNAVAILABLE**</dt> </dl> | L'interfaccia di errore è disponibile solo dopo che si è verificato un errore (BG_JOB_STATE_ERROR o BG_JOB_STATE_TRANSIENT_ERROR) e prima che inizi il trasferimento dei dati (BG_JOB_STATE_TRANSFERRING).<br/> |



 

## <a name="remarks"></a>Commenti

Il processo viene inserito in uno stato di errore in presenza di errori irreversibili. Per determinare se il processo è in errore, utilizzare una delle opzioni seguenti:

-   Per eseguire il polling dello stato del processo, chiamare il metodo [**Metodo ibackgroundcopyjob:: GetState**](ibackgroundcopyjob-getstate.md) . Il processo è in errore se lo stato è BG_JOB_STATE_ERROR.
-   Per ricevere una notifica quando si verifica un errore, implementare l'interfaccia [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) (in particolare il metodo [**JobError**](https://www.bing.com/search?q=**JobError**) ). Chiamare quindi il metodo [**Metodo ibackgroundcopyjob:: SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) per registrare il callback e il metodo [**Metodo ibackgroundcopyjob:: SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md) per impostare il flag BG_NOTIFY_JOB_ERROR.

L'interfaccia [**IBackgroundCopyError**](ibackgroundcopyerror.md) contiene le informazioni utilizzate per determinare la motivo dell'errore e se il processo di trasferimento può proseguire. Dopo aver determinato la cause dell'errore, eseguire una delle seguenti opzioni:

-   Per annullare il processo, chiamare il metodo [**Metodo ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md) .
-   Per salvare i file che sono stati trasferiti correttamente prima dell'errore, chiamare il metodo [**Metodo ibackgroundcopyjob:: complete**](ibackgroundcopyjob-complete.md) .
-   Per completare l'elaborazione del processo, risolvere il problema e quindi chiamare il metodo [**Metodo ibackgroundcopyjob:: Resume**](ibackgroundcopyjob-resume.md) .

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

[**IBackgroundCopyCallback::JobError**](ibackgroundcopycallback-joberror-method.md)
</dt> <dt>

[**IBackgroundCopyError**](ibackgroundcopyerror.md)
</dt> <dt>

[**Metodo ibackgroundcopyjob:: GetState**](ibackgroundcopyjob-getstate.md)
</dt> </dl>

 

 





