---
title: Interfaccia IBackgroundCopyCallback (Deliveryoptimization. h)
description: Implementare l'interfaccia IBackgroundCopyCallback per ricevere una notifica che indica che il processo è stato completato, è stato modificato o è in errore. I client usano questa interfaccia anziché eseguire il polling dello stato del processo.
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
ms.openlocfilehash: 4169acec87e4d1e8a31eecaa4f93b9404aafb714
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301487"
---
# <a name="ibackgroundcopycallback-interface"></a>Interfaccia IBackgroundCopyCallback

Implementare l'interfaccia **IBackgroundCopyCallback** per ricevere una notifica che indica che il processo è stato completato, è stato modificato o è in errore. I client usano questa interfaccia anziché eseguire il polling dello stato del processo.

## <a name="members"></a>Membri

L'interfaccia **IBackgroundCopyCallback** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IBackgroundCopyCallback** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IBackgroundCopyCallback** dispone di questi metodi.



| Metodo                                                                    | Descrizione                                                                       |
|:--------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [**JobError**](ibackgroundcopycallback-joberror-method.md)               | Chiamato quando si verifica un errore.<br/>                                           |
| [**JobModification**](ibackgroundcopycallback-jobmodification-method.md) | Chiamato quando un processo viene modificato.<br/>                                         |
| [**JobTransferred**](ibackgroundcopycallback-jobtransferred.md)          | Chiamato quando tutti i file del processo sono stati trasferiti correttamente.<br/> |



 

## <a name="remarks"></a>Commenti

Per ricevere le notifiche, chiamare il metodo [**Metodo ibackgroundcopyjob:: SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) per specificare il puntatore di interfaccia all'implementazione di **IBackgroundCopyCallback** . Per specificare quali notifiche si desidera ricevere, chiamare il metodo [**Metodo ibackgroundcopyjob:: SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md) .

La funzione chiamerà i callback purché il puntatore all'interfaccia sia valido. L'interfaccia di notifica non è più valida quando l'applicazione termina; DO non rende persistente l'interfaccia Notify. Di conseguenza, il processo di inizializzazione dell'applicazione deve chiamare il metodo [**SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) nei processi esistenti per i quali si desidera ricevere la notifica.

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

[**Metodo ibackgroundcopyjob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**Metodo ibackgroundcopyjob:: SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md)
</dt> <dt>

[**Metodo ibackgroundcopyjob:: SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md)
</dt> </dl>

 

