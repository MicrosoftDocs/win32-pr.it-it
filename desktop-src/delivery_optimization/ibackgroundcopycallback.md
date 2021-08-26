---
title: Interfaccia IBackgroundCopyCallback (Deliveryoptimization.h)
description: Implementare l'interfaccia IBackgroundCopyCallback per ricevere la notifica che un processo è stato completato, modificato o è in errore. I client usano questa interfaccia anziché il polling per lo stato del processo.
ms.assetid: CF85D852-1B4E-4BC2-B6A6-0035ED3C439C
keywords:
- Interfaccia IBackgroundCopyCallback
- Interfaccia IBackgroundCopyCallback, descritta
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 165a1edcdb6bd70de8fad379fcc89d5afc36776348fd7751277614229a23377e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953641"
---
# <a name="ibackgroundcopycallback-interface"></a>Interfaccia IBackgroundCopyCallback

Implementare **l'interfaccia IBackgroundCopyCallback** per ricevere la notifica che un processo è stato completato, modificato o è in errore. I client usano questa interfaccia anziché il polling per lo stato del processo.

## <a name="members"></a>Membri

**L'interfaccia IBackgroundCopyCallback** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IBackgroundCopyCallback** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia IBackgroundCopyCallback** include questi metodi.



| Metodo                                                                    | Descrizione                                                                       |
|:--------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [**JobError**](ibackgroundcopycallback-joberror-method.md)               | Chiamato quando si verifica un errore.<br/>                                           |
| [**JobModification**](ibackgroundcopycallback-jobmodification-method.md) | Chiamato quando un processo viene modificato.<br/>                                         |
| [**JobTransferred**](ibackgroundcopycallback-jobtransferred.md)          | Chiamato quando tutti i file nel processo sono stati trasferiti correttamente.<br/> |



 

## <a name="remarks"></a>Commenti

Per ricevere notifiche, chiamare il metodo [**IBackgroundCopyJob::SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) per specificare il puntatore a interfaccia **all'implementazione di IBackgroundCopyCallback.** Per specificare le notifiche da ricevere, chiamare il [**metodo IBackgroundCopyJob::SetNotifyFlags.**](ibackgroundcopyjob-setnotifyflags.md)

DO chiamerà i callback purché il puntatore a interfaccia sia valido. L'interfaccia di notifica non è più valida al termine dell'applicazione. DO non rende persistente l'interfaccia di notifica. Di conseguenza, il processo di inizializzazione dell'applicazione deve chiamare il [**metodo SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) sui processi esistenti per cui si vuole ricevere la notifica.

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

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**IBackgroundCopyJob::SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md)
</dt> <dt>

[**IBackgroundCopyJob::SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md)
</dt> </dl>

 

