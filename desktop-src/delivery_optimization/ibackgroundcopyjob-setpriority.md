---
title: Metodo IBackgroundCopyJob SetPriority (Deliveryoptimization.h)
description: Specifica il livello di priorità del processo. Il livello di priorità determina quando il processo viene elaborato rispetto ad altri processi nella coda di trasferimento.
ms.assetid: DC943093-CA1D-4840-B7AC-29710764D4E5
keywords:
- Metodo SetPriority
- Metodo SetPriority, interfaccia IBackgroundCopyJob
- Interfaccia IBackgroundCopyJob, metodo SetPriority
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.SetPriority
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4ed1852d6990b94a000ac6affcec6020d266aaac5fae4611c3985a6f5c203aca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118542872"
---
# <a name="ibackgroundcopyjobsetpriority-method"></a>Metodo IBackgroundCopyJob::SetPriority

Specifica il livello di priorità del processo. Il livello di priorità determina quando il processo viene elaborato rispetto ad altri processi nella coda di trasferimento.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetPriority(
  [in] BG_JOB_PRIORITY Priority
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Priorità* \[ Pollici\]
</dt> <dd>

Specifica il livello di priorità del processo rispetto ad altri processi nella coda di trasferimento. Il valore predefinito è BG_JOB_PRIORITY_NORMAL. Per un elenco dei livelli di priorità, vedere [**l'BG_JOB_PRIORITY**](bg-job-priority-.md) predefinita.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce i valori **HRESULT** seguenti, oltre ad altri.



| Codice restituito                                                                              | Descrizione                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>S_OK****</dt> </dl> | La priorità del processo è stata impostata correttamente.<br/> |



 

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

[**BG_JOB_PRIORITY**](bg-job-priority-.md)
</dt> <dt>

[**IBackgroundCopyJob::GetPriority**](ibackgroundcopyjob-getpriority.md)
</dt> </dl>

 

 





