---
title: Metodo CreateJob IBackgroundCopyManager (Deliveryoptimization.h)
description: Crea un processo.
ms.assetid: BDE5BE4D-9AE9-463D-B900-850D255EAB58
keywords:
- Metodo CreateJob
- Metodo CreateJob, interfaccia IBackgroundCopyManager
- Interfaccia IBackgroundCopyManager, metodo CreateJob
topic_type:
- apiref
api_name:
- IBackgroundCopyManager.CreateJob
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 165b0a74f71ee5267fb3bd300baec4e48c51662b33c83203ebae1ba462f10a0b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953561"
---
# <a name="ibackgroundcopymanagercreatejob-method"></a>Metodo IBackgroundCopyManager::CreateJob

Crea un processo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateJob(
  [in]  LPCWSTR            pDisplayName,
  [in]  BG_JOB_TYPE        Type,
  [out] GUID               *pJobID,
  [out] IBackgroundCopyJob **ppJob
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pDisplayName* \[ Pollici\]
</dt> <dd>

Stringa con terminazione Null che contiene un nome visualizzato per il processo. In genere, il nome visualizzato viene usato per identificare il processo in un'interfaccia utente. Si noti che più processi possono avere lo stesso nome visualizzato. Non deve essere **NULL.** Il nome è limitato a 256 caratteri, senza includere il carattere di terminazione Null.

</dd> <dt>

*Tipo* \[ Pollici\]
</dt> <dd>

Tipo di processo di trasferimento, ad esempio BG_JOB_TYPE_DOWNLOAD. Per un elenco dei tipi di trasferimento, vedere [**l'enumerazione BG_JOB_TYPE**](bg-job-type.md) di trasferimento.

</dd> <dt>

*pJobID* \[ Cambio\]
</dt> <dd>

Identifica in modo univoco il processo nella coda. Usare questo identificatore quando si chiama il [**metodo IBackgroundCopyManager::GetJob**](ibackgroundcopymanager-getjob.md) per ottenere un processo dalla coda.

</dd> <dt>

*ppJob* \[ Cambio\]
</dt> <dd>

Puntatore a interfaccia [**IBackgroundCopyJob**](ibackgroundcopyjob-.md) che viene utilizzato per modificare le proprietà del processo e specificare i file da trasferire. Per attivare il processo nella coda, chiamare il [**metodo IBackgroundCopyJob::Resume.**](ibackgroundcopyjob-resume.md) Al *termine, rilasciare ppJob.*

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce i **valori HRESULT** seguenti, oltre ad altri.



| Codice restituito                                                                              | Descrizione                                    |
|------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>S_OK****</dt> </dl> | Generazione del nuovo processo completata.<br/> |



 

## <a name="remarks"></a>Commenti

Solo l'utente che crea il processo o [](https://www.bing.com/search?q=add+files+to+the+job) un utente con privilegi di amministratore può aggiungere file al processo e modificare le [proprietà del processo.](https://www.bing.com/search?q=change+the+job's+properties)

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

[**IBackgroundCopyJob::Resume**](ibackgroundcopyjob-resume.md)
</dt> </dl>
