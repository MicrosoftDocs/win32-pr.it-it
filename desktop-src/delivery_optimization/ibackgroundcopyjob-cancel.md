---
title: Metodo Cancel metodo ibackgroundcopyjob (Deliveryoptimization. h)
description: Elimina il processo dalla coda di trasferimento e rimuove i file temporanei correlati dal client (download) e dal server (caricamenti).
ms.assetid: DC502DC2-1335-476F-A1B8-FDB6BA595FF1
keywords:
- Metodo Cancel
- Metodo Cancel, interfaccia metodo ibackgroundcopyjob
- Interfaccia metodo ibackgroundcopyjob, metodo Cancel
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.Cancel
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f72cdcea82ef7db30de141af295bb74594a7a630
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873685"
---
# <a name="ibackgroundcopyjobcancel-method"></a>Metodo metodo ibackgroundcopyjob:: Cancel

Elimina il processo dalla coda di trasferimento e rimuove i file temporanei correlati dal client (download) e dal server (caricamenti).

## <a name="syntax"></a>Sintassi


```C++
HRESULT Cancel();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce i valori **HRESULT** seguenti e altri.



| Codice restituito                                                                                          | Descrizione                                                                                              |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl>             | Il processo è stato annullato.<br/>                                                                |
| <dl> <dt>**DO_E_INVALID_STATE**</dt> </dl> | Non è possibile annullare un processo il cui stato è BG_JOB_STATE_CANCELLED o BG_JOB_STATE_ACKNOWLEDGED.<br/> |



 

## <a name="remarks"></a>Commenti

È possibile annullare un processo in qualsiasi momento; Tuttavia, non è possibile recuperare il processo dopo che è stato annullato.

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

[**Metodo ibackgroundcopyjob:: complete**](ibackgroundcopyjob-complete.md)
</dt> <dt>

[**Metodo ibackgroundcopyjob:: Resume**](ibackgroundcopyjob-resume.md)
</dt> <dt>

[**Metodo ibackgroundcopyjob:: Suspend**](ibackgroundcopyjob-suspend.md)
</dt> </dl>

 

 





