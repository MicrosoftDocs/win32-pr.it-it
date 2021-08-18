---
title: Interfaccia IBackgroundCopyJob (Deliveryoptimization.h)
description: Usare l'interfaccia IBackgroundCopyJob per aggiungere file al processo, impostare il livello di priorità del processo, determinare lo stato del processo e avviare e arrestare il processo.
ms.assetid: 0D1EAC8D-0013-4FBC-A07F-14CD5D709549
keywords:
- Interfaccia IBackgroundCopyJob
- Interfaccia IBackgroundCopyJob, descritta
topic_type:
- apiref
api_name:
- IBackgroundCopyJob
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 27febd08519a06f7ad452882cf0725fed209e0306182ba336343049936795acf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543027"
---
# <a name="ibackgroundcopyjob-interface"></a>Interfaccia IBackgroundCopyJob

Usare [**l'interfaccia IBackgroundCopyJob**](https://www.bing.com/search?q=**IBackgroundCopyJob**) per aggiungere file al processo, impostare il livello di priorità del processo, determinare lo stato del processo e avviare e arrestare il processo.

Per creare un processo, chiamare il [**metodo IBackgroundCopyManager::CreateJob.**](ibackgroundcopymanager-createjob.md) Per ottenere un [**puntatore a interfaccia IBackgroundCopyJob**](https://www.bing.com/search?q=**IBackgroundCopyJob**) a un processo esistente, chiamare il [**metodo IBackgroundCopyManager::GetJob.**](ibackgroundcopymanager-getjob.md)

## <a name="members"></a>Membri

**L'interfaccia IBackgroundCopyJob** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IBackgroundCopyJob** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IBackgroundCopyJob** include questi metodi.



| Metodo                                                                  | Descrizione                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Annulla**](ibackgroundcopyjob-cancel.md)                             | Annulla il processo e rimuove i file temporanei dal client.<br/>                                                                                                                                                           |
| [**Operazione completata**](ibackgroundcopyjob-complete.md)                         | Termina il processo e salva i file trasferiti nel client.<br/>                                                                                                                                                            |
| [**EnumFiles**](ibackgroundcopyjob-enumfiles.md)                       | Restituisce un puntatore a interfaccia a un oggetto enumeratore utilizzato per enumerare i file nel processo.<br/>                                                                                                                   |
| [**GetDisplayName**](ibackgroundcopyjob-getdisplayname.md)             | Recupera il nome visualizzato che identifica il processo.<br/>                                                                                                                                                                    |
| [**GetError**](ibackgroundcopyjob-geterror.md)                         | Recupera un puntatore a interfaccia all'oggetto errore dopo che si è verificato un errore.<br/>                                                                                                                                              |
| [**GetId**](ibackgroundcopyjob-getid.md)                               | Recupera l'identificatore del processo nella coda.<br/>                                                                                                                                                                      |
| [**GetNoProgressTimeout**](ibackgroundcopyjob-getnoprogresstimeout.md) | Recupera il periodo di tempo durante il quale DO continua a tentare di trasferire il file dopo che si è verificata una condizione di errore temporaneo.<br/>                                                                                             |
| [**GetNotifyFlags**](ibackgroundcopyjob-getnotifyflags.md)             | Recupera i flag di notifica degli eventi (callback) impostati per l'applicazione.<br/>                                                                                                                                   |
| [**GetNotifyInterface**](ibackgroundcopyjob-getnotifyinterface.md)     | Recupera un puntatore all'implementazione [**dell'interfaccia IBackgroundCopyCallback**](ibackgroundcopycallback.md) (callback).<br/>                                                                                    |
| [**GetPriority**](ibackgroundcopyjob-getpriority.md)                   | Recupera il livello di priorità impostato per il processo.<br/>                                                                                                                                                                 |
| [**GetProgress**](ibackgroundcopyjob-getprogress.md)                   | Recupera informazioni sullo stato del processo, ad esempio il numero di byte e file trasferiti al client.<br/>                                                                                                           |
| [**GetState**](ibackgroundcopyjob-getstate.md)                         | Recupera lo stato del processo.<br/>                                                                                                                                                                                        |
| [**GetTimes**](ibackgroundcopyjob-gettimes.md)                         | Recupera i timestamp per le attività correlate al processo, ad esempio l'ora di creazione del processo.<br/>                                                                                                                         |
| [**GetType**](ibackgroundcopyjob-gettype.md)                           | Recupera il tipo di trasferimento eseguito, ad esempio il download di un file.<br/>                                                                                                                                               |
| [**Riprendi**](ibackgroundcopyjob-resume.md)                             | Avvia un nuovo processo o riavvia un processo sospeso.<br/>                                                                                                                                                                          |
| [**SetNoProgressTimeout**](ibackgroundcopyjob-setnoprogresstimeout.md) | Specifica il periodo di tempo durante il quale DO continua a tentare di trasferire il file dopo che si è verificata una condizione di errore temporaneo.<br/>                                                                                             |
| [**SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md)             | Specifica il tipo di notifica degli eventi da ricevere.<br/>                                                                                                                                                                   |
| [**Interfaccia SetNotify**](ibackgroundcopyjob-setnotifyinterface.md)     | Specifica un puntatore all'implementazione [**dell'interfaccia IBackgroundCopyCallback**](ibackgroundcopycallback.md) (callback). L'interfaccia riceve la notifica in base ai flag di notifica degli eventi impostati.<br/> |
| [**SetPriority**](ibackgroundcopyjob-setpriority.md)                   | Specifica la priorità del processo rispetto ad altri processi nella coda di trasferimento.<br/>                                                                                                                                        |
| [**Sospendi**](ibackgroundcopyjob-suspend.md)                           | Sospende il processo.<br/>                                                                                                                                                                                                        |



 

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

[**IBackgroundCopyFile**](ibackgroundcopyfile.md)
</dt> <dt>

[**IBackgroundCopyManager**](ibackgroundcopymanager.md)
</dt> </dl>

 

