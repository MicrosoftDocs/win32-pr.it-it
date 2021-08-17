---
title: Metodo IBackgroundCopyJob SetNotifyFlags (Deliveryoptimization.h)
description: Specifica il tipo di notifica degli eventi che si vuole ricevere, ad esempio gli eventi trasferiti dal processo.
ms.assetid: 19E626A5-6B6E-44E0-BD6F-43F132F32890
keywords:
- Metodo SetNotifyFlags
- Metodo SetNotifyFlags, interfaccia IBackgroundCopyJob
- Interfaccia IBackgroundCopyJob, metodo SetNotifyFlags
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.SetNotifyFlags
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cdb1750391027163a7ac8fb9ba8cc20085a06d187de0d7f05850641a5a774b18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118542918"
---
# <a name="ibackgroundcopyjobsetnotifyflags-method"></a>Metodo IBackgroundCopyJob::SetNotifyFlags

Specifica il tipo di notifica degli eventi che si vuole ricevere, ad esempio gli eventi trasferiti dal processo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetNotifyFlags(
  [in] ULONG NotifyFlags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*NotifyFlags* \[ Pollici\]
</dt> <dd>

Impostare uno o più flag seguenti per identificare gli eventi che si desidera ricevere.



| Valore                                                                                                                                                                                                                                                                                    | Significato                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BG_NOTIFY_JOB_TRANSFERRED"></span><span id="bg_notify_job_transferred"></span><dl> <dt>**BG_NOTIFY_JOB_TRANSFERRED**</dt> <dt>0x0001</dt> </dl>                          | Tutti i file nel processo sono stati trasferiti.<br/>                                                                                                                                                          |
| <span id="BG_NOTIFY_JOB_ERROR"></span><span id="bg_notify_job_error"></span><dl> <dt>**BG_NOTIFY_JOB_ERROR**</dt> <dt>0x0002</dt> </dl>                                            | un errore.<br/>                                                                                                                                                                                      |
| <span id="BG_NOTIFY_DISABLE"></span><span id="bg_notify_disable"></span><dl> <dt>**BG_NOTIFY_DISABLE**</dt> <dt>0x0004</dt> </dl>                                                   | Non supportata.<br/>                                                                                                                                                                                              |
| <span id="BG_NOTIFY_JOB_MODIFICATION"></span><span id="bg_notify_job_modification"></span><dl> <dt>**BG_NOTIFY_JOB_MODIFICATION**</dt> <dt>0x0008</dt> </dl>                       | Il processo è stato modificato. Ad esempio, un valore di proprietà modificato, lo stato del processo modificato o lo stato di avanzamento viene effettuato il trasferimento dei file. Questo flag viene ignorato se viene specificata la notifica della riga di comando.<br/> |
| <span id="BG_NOTIFY_FILE_TRANSFERRED"></span><span id="bg_notify_file_transferred"></span><dl> <dt>**BG_NOTIFY_FILE_TRANSFERRED**</dt> <dt>0x0010</dt> </dl>                       | È stato trasferito un file nel processo. Questo flag viene ignorato se viene specificata la notifica della riga di comando.<br/>                                                                                                     |
| <span id="BG_NOTIFY_FILE_RANGES_TRANSFERRED"></span><span id="bg_notify_file_ranges_transferred"></span><dl> <dt>**BG_NOTIFY_FILE_RANGES_TRANSFERRED**</dt> <dt>0x0020</dt> </dl> | Non supportata.<br/>                                                                                                                                                                                              |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce i valori **HRESULT** seguenti, oltre ad altri.



| Codice restituito                                                                                          | Descrizione                                                                                          |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK****</dt> </dl>             | Il tipo di notifica degli eventi è stato impostato correttamente.<br/>                                          |
| <dl> <dt>**DO_E_INVALID_STATE**</dt> </dl> | Lo stato del processo non può essere BG_JOB_STATE_CANCELLED o BG_JOB_STATE_ACKNOWLEDGED.<br/> |



 

## <a name="remarks"></a>Commenti

Usare il **metodo SetNotifyFlags** insieme a [**IBackgroundCopyJob::SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md).

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

 

 





