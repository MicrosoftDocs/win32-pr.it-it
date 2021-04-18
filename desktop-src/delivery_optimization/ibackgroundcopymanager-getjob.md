---
title: Metodo IBackgroundCopyManager GetJob (Deliveryoptimization. h)
description: Recupera un processo specificato dalla coda di trasferimento. In genere, l'applicazione salva in modo permanente l'identificatore del processo, quindi è possibile recuperare il processo dalla coda in un secondo momento.
ms.assetid: ED551A6B-66C7-47E9-93DA-E231BD637522
keywords:
- Metodo GetJob
- Metodo GetJob, interfaccia IBackgroundCopyManager
- Interfaccia IBackgroundCopyManager, metodo GetJob
topic_type:
- apiref
api_name:
- IBackgroundCopyManager.GetJob
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a59956e68b5b656e7182e62969b3212c2ef6732c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301726"
---
# <a name="ibackgroundcopymanagergetjob-method"></a>Metodo IBackgroundCopyManager:: GetJob

Recupera un processo specificato dalla coda di trasferimento. In genere, l'applicazione salva in modo permanente l'identificatore del processo, quindi è possibile recuperare il processo dalla coda in un secondo momento.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetJob(
  [in]  REFGUID            JobID,
  [out] IBackgroundCopyJob **ppJob
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*JobID* \[ in\]
</dt> <dd>

Identifica il processo da recuperare dalla coda di trasferimento. Il metodo [**CreateJob**](ibackgroundcopymanager-createjob.md) restituisce l'identificatore di processo.

</dd> <dt>

*ppJob* \[ out\]
</dt> <dd>

Puntatore all'interfaccia [**Metodo ibackgroundcopyjob**](ibackgroundcopyjob-.md) per il processo specificato da *JobID*. Al termine, rilasciare *ppJob*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce i valori **HRESULT** seguenti e altri.



| Codice restituito                                                                                      | Descrizione                                                        |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl>         | Il processo è stato recuperato dalla coda di trasferimento.<br/> |
| <dl> <dt>**DO_E_NOT_FOUND**</dt> </dl> | Il processo non è stato trovato nella coda.<br/>                     |
| <dl> <dt>**E_ACCESSDENIED**</dt> </dl>   | L'utente non dispone delle autorizzazioni necessarie per recuperare il processo.<br/>      |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1709 \[\]<br/>                                           |
| Server minimo supportato<br/> | Windows Server, versione 1709 \[ solo per le app desktop\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyManager viene definito come 5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C<br/>           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IBackgroundCopyManager**](ibackgroundcopymanager.md)
</dt> <dt>

[**Metodo ibackgroundcopyjob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**Metodo ibackgroundcopyjob:: GetId**](ibackgroundcopyjob-getid.md)
</dt> <dt>

[**IBackgroundCopyManager:: CreateJob**](ibackgroundcopymanager-createjob.md)
</dt> </dl>

 

 





