---
title: Metodo IBackgroundCopyJob Complete (Deliveryoptimization.h)
description: Termina il processo e salva i file trasferiti nel client.
ms.assetid: A3706DBA-C44E-4F7A-A787-62FB436706FC
keywords:
- Metodo Complete
- Metodo Complete, interfaccia IBackgroundCopyJob
- Interfaccia IBackgroundCopyJob, metodo Complete
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.Complete
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 72ace8890e724e529e96c5292a439042f13bc2bfad77e6d990a6dbb2fa18f5d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736226"
---
# <a name="ibackgroundcopyjobcomplete-method"></a>Metodo IBackgroundCopyJob::Complete

Termina il processo e salva i file trasferiti nel client.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Complete();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce i valori **HRESULT** seguenti. Il metodo può anche restituire errori correlati alla ridenominazione delle copie temporanee dei file trasferiti nei nomi specificati.



| Codice restituito                                                                                          | Descrizione                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK****</dt> </dl>             | Tutti i file trasferiti correttamente.<br/>                                                                                                                                                         |
| <dl> <dt>**DO_E_INVALID_STATE**</dt> </dl> | Per i download, lo stato del processo non può essere BG_JOB_STATE_CANCELLED o BG_JOB_STATE_ACKNOWLEDGED. <br/> Per i caricamenti, lo stato del processo deve essere BG_JOB_STATE_TRANSFERRED.<br/> |



 

## <a name="remarks"></a>Commenti

Tutti i file sono stati trasferiti correttamente se lo stato del processo è **BG_JOB_STATE_TRANSFERRED**. Per controllare lo stato del processo, chiamare il [**metodo IBackgroundCopyJob::GetState.**](ibackgroundcopyjob-getstate.md) È anche possibile implementare [**l'interfaccia IBackgroundCopyCallback**](ibackgroundcopycallback.md) per ricevere una notifica quando tutti i file sono stati trasferiti al client.

DO mantiene solo i processi inferiori a 30 giorni. Tutti i processi meno recenti verranno rimossi. DO non supporta [l'Criteri di gruppo JobInactivityTimeout.](https://www.bing.com/search?q=JobInactivityTimeout)

Per i processi di download, è possibile chiamare il **metodo Complete** in qualsiasi momento durante il processo di trasferimento. Tuttavia, vengono salvati solo i file che sono stati trasferiti correttamente al client prima di chiamare questo metodo. Ad esempio, se si chiama il **metodo Complete** mentre DO elabora il terzo di cinque file, vengono salvati solo i primi due file. Per determinare quali file sono stati trasferiti, chiamare il metodo [**IBackgroundCopyFile::GetProgress**](ibackgroundcopyfile-getprogress-method.md) e confrontare il membro **BytesTransferred** con il membro **BytesTotal** della [**struttura**](bg-file-progress.md) BG_FILE_PROGRESS.

Per i processi di caricamento, è possibile chiamare il **metodo Complete** solo quando lo stato del processo è **BG_JOB_STATE_TRANSFERRED**.

Il proprietario del file è l'utente che ha effettuato la chiamata. Ad esempio, se un amministratore completa il processo di un altro utente, l'amministratore non il proprietario del processo è proprietario del file.

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

[**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[**IBackgroundCopyJob::GetState**](ibackgroundcopyjob-getstate.md)
</dt> </dl>

 

 





