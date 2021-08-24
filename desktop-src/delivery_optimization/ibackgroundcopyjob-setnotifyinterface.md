---
title: Metodo IBackgroundCopyJob SetNotifyInterface (Deliveryoptimization.h)
description: Identifica l'implementazione dell'interfaccia IBackgroundCopyCallback da eseguire. Usare l'interfaccia IBackgroundCopyCallback per ricevere la notifica degli eventi correlati al processo.
ms.assetid: 792211FC-440E-4D2C-A6C7-CE9EFB86571C
keywords:
- Metodo SetNotifyInterface
- Metodo SetNotifyInterface, interfaccia IBackgroundCopyJob
- Interfaccia IBackgroundCopyJob, metodo SetNotifyInterface
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.SetNotifyInterface
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bd54255d87ee3f15f87d692e06b7a503e773634ab4ec30c3f388388233aab2b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793410"
---
# <a name="ibackgroundcopyjobsetnotifyinterface-method"></a>Metodo IBackgroundCopyJob::SetNotifyInterface

Identifica l'implementazione [**dell'interfaccia IBackgroundCopyCallback**](ibackgroundcopycallback.md) da eseguire. Usare **l'interfaccia IBackgroundCopyCallback** per ricevere la notifica degli eventi correlati al processo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetNotifyInterface(
   IUnknown *pNotifyInterface
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pNotifyInterface* 
</dt> <dd>

Puntatore [**a interfaccia IBackgroundCopyCallback.**](ibackgroundcopycallback.md) Per rimuovere il puntatore all'interfaccia di callback corrente, impostare questo parametro su **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce i valori **HRESULT** seguenti, oltre ad altri.



| Codice restituito                                                                              | Descrizione                                                     |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>S_OK****</dt> </dl> | Il puntatore dell'interfaccia di notifica è stato impostato correttamente.<br/> |



 

## <a name="remarks"></a>Commenti

Chiamare questo metodo solo se si implementa [**l'interfaccia IBackgroundCopyCallback.**](ibackgroundcopycallback.md) Usare il **metodo SetNotifyInterface** insieme al [**metodo SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md) per specificare il tipo di notifica che si vuole ricevere.

L'interfaccia di notifica non è più valida al termine dell'applicazione. DO non rende persistente l'interfaccia di notifica. Di conseguenza, il processo di inizializzazione dell'applicazione deve chiamare il metodo **SetNotifyInterface** sui processi esistenti per cui si vuole ricevere la notifica. Se è necessario acquisire informazioni sullo stato e sull'avanzamento dell'esecuzione dall'ultima esecuzione dell'applicazione, eseguire il polling delle informazioni sullo stato e sullo stato durante l'inizializzazione dell'applicazione.

Solo il proprietario o l'autore del processo o un amministratore può registrarsi per le notifiche.

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

[**IBackgroundCopyCallback**](ibackgroundcopycallback.md)
</dt> <dt>

[**IBackgroundCopyJob::GetNotifyInterface**](ibackgroundcopyjob-getnotifyinterface.md)
</dt> <dt>

[**IBackgroundCopyJob::SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md)
</dt> </dl>

 

 





