---
title: Metodo Complete metodo ibackgroundcopyjob (Deliveryoptimization. h)
description: Termina il processo e salva i file trasferiti nel client.
ms.assetid: A3706DBA-C44E-4F7A-A787-62FB436706FC
keywords:
- Metodo complete
- Metodo complete, interfaccia metodo ibackgroundcopyjob
- Interfaccia metodo ibackgroundcopyjob, metodo complete
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
ms.openlocfilehash: 72383bb235d31043f781998324891b6df134e6ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119755"
---
# <a name="ibackgroundcopyjobcomplete-method"></a>Metodo metodo ibackgroundcopyjob:: complete

Termina il processo e salva i file trasferiti nel client.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Complete();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce i valori **HRESULT** seguenti. Il metodo può inoltre restituire errori correlati alla ridenominazione delle copie temporanee dei file trasferiti nei nomi specificati.



| Codice restituito                                                                                          | Descrizione                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl>             | Tutti i file sono stati trasferiti.<br/>                                                                                                                                                         |
| <dl> <dt>**DO_E_INVALID_STATE**</dt> </dl> | Per i download, lo stato del processo non può essere BG_JOB_STATE_CANCELLED o BG_JOB_STATE_ACKNOWLEDGED. <br/> Per i caricamenti, lo stato del processo deve essere BG_JOB_STATE_TRANSFERRED.<br/> |



 

## <a name="remarks"></a>Commenti

Tutti i file sono stati trasferiti se lo stato del processo è **BG_JOB_STATE_TRANSFERRED**. Per controllare lo stato del processo, chiamare il metodo [**Metodo ibackgroundcopyjob:: GetState**](ibackgroundcopyjob-getstate.md) . È anche possibile implementare l'interfaccia [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) per ricevere una notifica quando tutti i file sono stati trasferiti al client.

Mantiene i processi che sono solo di meno di 30 giorni. Tutti i processi meno recenti verranno rimossi. DO non supporta il Criteri di gruppo [JobInactivityTimeout](https://www.bing.com/search?q=JobInactivityTimeout) .

Per i processi di download, è possibile chiamare il metodo **completo** in qualsiasi momento durante il processo di trasferimento. Tuttavia, vengono salvati solo i file che sono stati trasferiti correttamente al client prima di chiamare questo metodo. Se, ad esempio, si chiama il metodo **complete** mentre si elabora il terzo di cinque file, vengono salvati solo i primi due file. Per determinare quali file sono stati trasferiti, chiamare il metodo [**IBackgroundCopyFile:: getProgress**](ibackgroundcopyfile-getprogress-method.md) e confrontare il membro **byte trasferiti** con il membro **bytesTotal** della struttura [**BG_FILE_PROGRESS**](bg-file-progress.md) .

Per i processi di caricamento, è possibile chiamare il metodo **complete** solo quando lo stato del processo è **BG_JOB_STATE_TRANSFERRED**.

Il proprietario del file è l'utente che ha effettuato la chiamata. Se, ad esempio, un amministratore completa il processo di un altro utente, l'amministratore non è proprietario del processo.

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

[**Metodo ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[**Metodo ibackgroundcopyjob:: GetState**](ibackgroundcopyjob-getstate.md)
</dt> </dl>

 

 





