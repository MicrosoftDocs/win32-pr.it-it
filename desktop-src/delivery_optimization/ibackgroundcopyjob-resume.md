---
title: Metodo IBackgroundCopyJob Resume (Deliveryoptimization.h)
description: Attiva un nuovo processo o riavvia un processo sospeso.
ms.assetid: B745BDA6-36B9-41FD-9737-61D14150A9E4
keywords:
- Metodo Resume
- Metodo Resume, interfaccia IBackgroundCopyJob
- Interfaccia IBackgroundCopyJob, metodo Resume
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.Resume
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fa4bd9a98626b7f26fc4ac9968d27d54604b5db56539eb383bb8aff696b2a561
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118543007"
---
# <a name="ibackgroundcopyjobresume-method"></a>Metodo IBackgroundCopyJob::Resume

Attiva un nuovo processo o riavvia un processo sospeso.

## <a name="syntax"></a>Sintassi


```C++
HRESULT Resume();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce i valori **HRESULT** seguenti, oltre ad altri.



| Codice restituito                                                                                          | Descrizione                                                                                          |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK****</dt> </dl>             | Il processo è stato riavviato correttamente.<br/>                                                           |
| <dl> <dt>**DO_E_EMPTY**</dt> </dl>          | Nessun file da trasferire.<br/>                                                           |
| <dl> <dt>**DO_E_INVALID_STATE**</dt> </dl> | Lo stato del processo non può essere BG_JOB_STATE_CANCELLED o BG_JOB_STATE_ACKNOWLEDGED.<br/> |



 

## <a name="remarks"></a>Commenti

Quando si crea un processo, il processo viene inizialmente sospeso. Se **si chiama Resume,** il processo viene spostato nello stato Trasferimento. Si noti che il processo deve contenere uno o più file prima di chiamare questo metodo.

Se un processo nello stato BG_JOB_STATE_TRANSIENT_ERROR o BG_JOB_STATE_ERROR, chiamare il metodo **Resume** per riavviare il processo dopo aver corretto l'errore.

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

[**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[**IBackgroundCopyJob::Suspend**](ibackgroundcopyjob-suspend.md)
</dt> </dl>

 

 





