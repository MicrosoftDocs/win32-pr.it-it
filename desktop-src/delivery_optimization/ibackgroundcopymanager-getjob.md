---
title: Metodo GetJob IBackgroundCopyManager (Deliveryoptimization.h)
description: Recupera un processo specificato dalla coda di trasferimento. In genere, l'applicazione rende persistente l'identificatore del processo, quindi è possibile recuperare il processo dalla coda in un secondo momento.
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
ms.openlocfilehash: d8d05b496eaa0d6f1520f22efeed8a39af5eb8e4c338457e18c65a7913489472
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118542289"
---
# <a name="ibackgroundcopymanagergetjob-method"></a>Metodo IBackgroundCopyManager::GetJob

Recupera un processo specificato dalla coda di trasferimento. In genere, l'applicazione rende persistente l'identificatore del processo, quindi è possibile recuperare il processo dalla coda in un secondo momento.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetJob(
  [in]  REFGUID            JobID,
  [out] IBackgroundCopyJob **ppJob
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Id processo* \[ Pollici\]
</dt> <dd>

Identifica il processo da recuperare dalla coda di trasferimento. Il [**metodo CreateJob**](ibackgroundcopymanager-createjob.md) restituisce l'identificatore del processo.

</dd> <dt>

*ppJob* \[ Cambio\]
</dt> <dd>

Puntatore [**a interfaccia IBackgroundCopyJob**](ibackgroundcopyjob-.md) al processo specificato da *JobID*. Al termine, *rilasciare ppJob*.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce i valori **HRESULT** seguenti, oltre ad altri.



| Codice restituito                                                                                      | Descrizione                                                        |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>S_OK****</dt> </dl>         | Il processo è stato recuperato correttamente dalla coda di trasferimento.<br/> |
| <dl> <dt>**DO_E_NOT_FOUND**</dt> </dl> | Il processo non è stato trovato nella coda.<br/>                     |
| <dl> <dt>**E_ACCESSDENIED**</dt> </dl>   | L'utente non dispone dell'autorizzazione per recuperare il processo.<br/>      |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1709 \[\]<br/>                                           |
| Server minimo supportato<br/> | Windows Server, solo app desktop versione 1709 \[\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyManager definito come 5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C<br/>           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IBackgroundCopyManager**](ibackgroundcopymanager.md)
</dt> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**IBackgroundCopyJob::GetId**](ibackgroundcopyjob-getid.md)
</dt> <dt>

[**IBackgroundCopyManager::CreateJob**](ibackgroundcopymanager-createjob.md)
</dt> </dl>

 

 





