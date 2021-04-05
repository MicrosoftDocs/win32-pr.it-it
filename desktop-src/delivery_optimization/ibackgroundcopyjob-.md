---
title: Interfaccia metodo ibackgroundcopyjob (Deliveryoptimization. h)
description: Usare l'interfaccia metodo ibackgroundcopyjob per aggiungere file al processo, impostare il livello di priorità del processo, determinare lo stato del processo e avviare e arrestare il processo.
ms.assetid: 0D1EAC8D-0013-4FBC-A07F-14CD5D709549
keywords:
- Interfaccia metodo ibackgroundcopyjob
- Interfaccia metodo ibackgroundcopyjob, descritta
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
ms.openlocfilehash: 04572f11afd51c3354c5adabd9950e2a3942287a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048274"
---
# <a name="ibackgroundcopyjob-interface"></a>Interfaccia metodo ibackgroundcopyjob

Usare l'interfaccia [**Metodo ibackgroundcopyjob**](https://www.bing.com/search?q=**IBackgroundCopyJob**) per aggiungere file al processo, impostare il livello di priorità del processo, determinare lo stato del processo e avviare e arrestare il processo.

Per creare un processo, chiamare il metodo [**IBackgroundCopyManager:: CreateJob**](ibackgroundcopymanager-createjob.md) . Per ottenere un puntatore di interfaccia [**Metodo ibackgroundcopyjob**](https://www.bing.com/search?q=**IBackgroundCopyJob**) a un processo esistente, chiamare il metodo [**IBackgroundCopyManager:: GetJob**](ibackgroundcopymanager-getjob.md) .

## <a name="members"></a>Membri

L'interfaccia **Metodo ibackgroundcopyjob** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **Metodo ibackgroundcopyjob** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **Metodo ibackgroundcopyjob** dispone di questi metodi.



| Metodo                                                                  | Descrizione                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Annulla**](ibackgroundcopyjob-cancel.md)                             | Annulla il processo e rimuove i file temporanei dal client.<br/>                                                                                                                                                           |
| [**Operazione completata**](ibackgroundcopyjob-complete.md)                         | Termina il processo e salva i file trasferiti nel client.<br/>                                                                                                                                                            |
| [**EnumFiles**](ibackgroundcopyjob-enumfiles.md)                       | Restituisce un puntatore a interfaccia a un oggetto enumeratore utilizzato per enumerare i file nel processo.<br/>                                                                                                                   |
| [**GetDisplayName**](ibackgroundcopyjob-getdisplayname.md)             | Recupera il nome visualizzato che identifica il processo.<br/>                                                                                                                                                                    |
| [**GetError**](ibackgroundcopyjob-geterror.md)                         | Recupera un puntatore di interfaccia all'oggetto Error dopo che si è verificato un errore.<br/>                                                                                                                                              |
| [**GetId**](ibackgroundcopyjob-getid.md)                               | Recupera l'identificatore del processo nella coda.<br/>                                                                                                                                                                      |
| [**GetNoProgressTimeout**](ibackgroundcopyjob-getnoprogresstimeout.md) | Recupera il periodo di tempo in cui continua a provare a trasferire il file dopo aver riscontrato una condizione di errore temporaneo.<br/>                                                                                             |
| [**GetNotifyFlags**](ibackgroundcopyjob-getnotifyflags.md)             | Recupera i flag di notifica degli eventi (callback) impostati per l'applicazione.<br/>                                                                                                                                   |
| [**GetNotifyInterface**](ibackgroundcopyjob-getnotifyinterface.md)     | Recupera un puntatore all'implementazione dell'interfaccia [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) (callback).<br/>                                                                                    |
| [**GetPriority**](ibackgroundcopyjob-getpriority.md)                   | Recupera il livello di priorità impostato per il processo.<br/>                                                                                                                                                                 |
| [**GetProgress**](ibackgroundcopyjob-getprogress.md)                   | Recupera le informazioni sullo stato di avanzamento correlate al processo, ad esempio il numero di byte e i file trasferiti al client.<br/>                                                                                                           |
| [**GetState**](ibackgroundcopyjob-getstate.md)                         | Recupera lo stato del processo.<br/>                                                                                                                                                                                        |
| [**Gettimes**](ibackgroundcopyjob-gettimes.md)                         | Recupera i timestamp per le attività correlate al processo, ad esempio l'ora di creazione del processo.<br/>                                                                                                                         |
| [**GetType**](ibackgroundcopyjob-gettype.md)                           | Recupera il tipo di trasferimento eseguito, ad esempio il download di un file.<br/>                                                                                                                                               |
| [**Riprendi**](ibackgroundcopyjob-resume.md)                             | Avvia un nuovo processo o riavvia un processo sospeso.<br/>                                                                                                                                                                          |
| [**SetNoProgressTimeout**](ibackgroundcopyjob-setnoprogresstimeout.md) | Specifica il periodo di tempo in cui continua a provare a trasferire il file dopo aver riscontrato una condizione di errore temporaneo.<br/>                                                                                             |
| [**SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md)             | Specifica il tipo di notifica degli eventi da ricevere.<br/>                                                                                                                                                                   |
| [**SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md)     | Specifica un puntatore all'implementazione dell'interfaccia [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) (callback). L'interfaccia riceve la notifica in base ai flag di notifica degli eventi impostati.<br/> |
| [**SetPriority**](ibackgroundcopyjob-setpriority.md)                   | Specifica la priorità del processo rispetto ad altri processi nella coda di trasferimento.<br/>                                                                                                                                        |
| [**Sospendere**](ibackgroundcopyjob-suspend.md)                           | Sospende il processo.<br/>                                                                                                                                                                                                        |



 

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

[**IBackgroundCopyFile**](ibackgroundcopyfile.md)
</dt> <dt>

[**IBackgroundCopyManager**](ibackgroundcopymanager.md)
</dt> </dl>

 

