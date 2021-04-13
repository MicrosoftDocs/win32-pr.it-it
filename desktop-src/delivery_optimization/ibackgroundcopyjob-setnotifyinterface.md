---
title: Metodo metodo ibackgroundcopyjob SetNotifyInterface (Deliveryoptimization. h)
description: Identifica l'implementazione dell'interfaccia IBackgroundCopyCallback da eseguire. Usare l'interfaccia IBackgroundCopyCallback per ricevere notifiche di eventi correlati al processo.
ms.assetid: 792211FC-440E-4D2C-A6C7-CE9EFB86571C
keywords:
- Metodo SetNotifyInterface
- Metodo SetNotifyInterface, interfaccia metodo ibackgroundcopyjob
- Interfaccia metodo ibackgroundcopyjob, metodo SetNotifyInterface
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
ms.openlocfilehash: f3b6e8205eb60cbd2ca645cd484e41f8f242619d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340622"
---
# <a name="ibackgroundcopyjobsetnotifyinterface-method"></a>Metodo metodo ibackgroundcopyjob:: SetNotifyInterface

Identifica l'implementazione dell'interfaccia [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) da eseguire. Usare l'interfaccia **IBackgroundCopyCallback** per ricevere notifiche di eventi correlati al processo.

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

Puntatore di interfaccia [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) . Per rimuovere il puntatore all'interfaccia di callback corrente, impostare questo parametro su **null**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce i valori **HRESULT** seguenti e altri.



| Codice restituito                                                                              | Descrizione                                                     |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl> | Il puntatore all'interfaccia di notifica è stato impostato correttamente.<br/> |



 

## <a name="remarks"></a>Commenti

Chiamare questo metodo solo se si implementa l'interfaccia [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) . Utilizzare il metodo **SetNotifyInterface** insieme al metodo [**SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md) per specificare il tipo di notifica che si desidera ricevere.

L'interfaccia di notifica diventa non valida al termine dell'applicazione; DO non rende persistente l'interfaccia Notify. Di conseguenza, il processo di inizializzazione dell'applicazione deve chiamare il metodo **SetNotifyInterface** nei processi esistenti per i quali si desidera ricevere la notifica. Se è necessario acquisire informazioni sullo stato e sullo stato di avanzamento dopo l'ultima esecuzione dell'applicazione, eseguire il polling delle informazioni sullo stato e sullo stato durante l'inizializzazione dell'applicazione.

Solo il proprietario/autore del processo o un amministratore può registrarsi per le notifiche.

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

[**IBackgroundCopyCallback**](ibackgroundcopycallback.md)
</dt> <dt>

[**Metodo ibackgroundcopyjob:: GetNotifyInterface**](ibackgroundcopyjob-getnotifyinterface.md)
</dt> <dt>

[**Metodo ibackgroundcopyjob:: SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md)
</dt> </dl>

 

 





