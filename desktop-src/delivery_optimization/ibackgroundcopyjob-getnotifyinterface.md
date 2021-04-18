---
title: Metodo metodo ibackgroundcopyjob GetNotifyInterface (Deliveryoptimization. h)
description: Recupera il puntatore di interfaccia all'implementazione dell'interfaccia IBackgroundCopyCallback.
ms.assetid: 1AA50C03-AC84-4AA9-8EC3-3FBA865C70C0
keywords:
- Metodo GetNotifyInterface
- Metodo GetNotifyInterface, interfaccia metodo ibackgroundcopyjob
- Interfaccia metodo ibackgroundcopyjob, metodo GetNotifyInterface
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
ms.openlocfilehash: 6586a90de5783ceb24e5a7677f699a9cf6dfa60c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302657"
---
# <a name="ibackgroundcopyjobgetnotifyinterface-method"></a>Metodo metodo ibackgroundcopyjob:: GetNotifyInterface

Recupera il puntatore di interfaccia all'implementazione dell'interfaccia [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetNotifyInterface(
  [out] IUnknown **ppNotifyInterface
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppNotifyInterface* \[ out\]
</dt> <dd>

Puntatore di interfaccia all'implementazione dell'interfaccia [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) . Al termine, rilasciare *ppNotifyInterface*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce i valori **HRESULT** seguenti e altri.



| Codice restituito                                                                              | Descrizione                                                           |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl> | Il puntatore all'interfaccia di notifica è stato recuperato.<br/> |



 

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

[**Metodo ibackgroundcopyjob:: GetNotifyFlags**](ibackgroundcopyjob-getnotifyflags.md)
</dt> <dt>

[**Metodo ibackgroundcopyjob:: SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md)
</dt> </dl>

 

 





