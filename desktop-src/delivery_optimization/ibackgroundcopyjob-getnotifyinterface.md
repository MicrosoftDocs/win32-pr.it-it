---
title: Metodo IBackgroundCopyJob GetNotifyInterface (Deliveryoptimization.h)
description: Recupera il puntatore a interfaccia all'implementazione dell'interfaccia IBackgroundCopyCallback.
ms.assetid: 1AA50C03-AC84-4AA9-8EC3-3FBA865C70C0
keywords:
- Metodo GetNotifyInterface
- Metodo GetNotifyInterface, interfaccia IBackgroundCopyJob
- Interfaccia IBackgroundCopyJob, metodo GetNotifyInterface
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetNotifyInterface
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ef8eab6c101cadde2b715c48fe3dae2443e72e93f623b397036e2467bcbf0b5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755381"
---
# <a name="ibackgroundcopyjobgetnotifyinterface-method"></a>Metodo IBackgroundCopyJob::GetNotifyInterface

Recupera il puntatore a interfaccia all'implementazione [**dell'interfaccia IBackgroundCopyCallback.**](ibackgroundcopycallback.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetNotifyInterface(
  [out] IUnknown **ppNotifyInterface
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppNotifyInterface* \[ Cambio\]
</dt> <dd>

Puntatore a interfaccia all'implementazione [**dell'interfaccia IBackgroundCopyCallback.**](ibackgroundcopycallback.md) Al termine, *rilasciare ppNotifyInterface*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce i valori **HRESULT** seguenti, oltre ad altri.



| Codice restituito                                                                              | Descrizione                                                           |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>S_OK****</dt> </dl> | Il puntatore di interfaccia di notifica è stato recuperato correttamente.<br/> |



 

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

[**IBackgroundCopyCallback**](ibackgroundcopycallback.md)
</dt> <dt>

[**IBackgroundCopyJob::GetNotifyFlags**](ibackgroundcopyjob-getnotifyflags.md)
</dt> <dt>

[**IBackgroundCopyJob::SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md)
</dt> </dl>

 

 





