---
title: Metodo sepriority metodo ibackgroundcopyjob (Deliveryoptimization. h)
description: Specifica il livello di priorità del processo. Il livello di priorità determina quando il processo viene elaborato rispetto ad altri processi nella coda di trasferimento.
ms.assetid: DC943093-CA1D-4840-B7AC-29710764D4E5
keywords:
- Metodo sepriority
- Metodo sepriority, interfaccia metodo ibackgroundcopyjob
- Interfaccia metodo ibackgroundcopyjob, metodo sepriority
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
ms.openlocfilehash: 6fb6407c5d693a2c6e75f8aaf8f7a0544d08cdec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741714"
---
# <a name="ibackgroundcopyjobsetpriority-method"></a>Metodo metodo ibackgroundcopyjob:: sepriority

Specifica il livello di priorità del processo. Il livello di priorità determina quando il processo viene elaborato rispetto ad altri processi nella coda di trasferimento.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetPriority(
  [in] BG_JOB_PRIORITY Priority
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Priorità* \[ di in\]
</dt> <dd>

Specifica il livello di priorità del processo rispetto ad altri processi nella coda di trasferimento. Il valore predefinito è BG_JOB_PRIORITY_NORMAL. Per un elenco di livelli di priorità, vedere l'enumerazione [**BG_JOB_PRIORITY**](bg-job-priority-.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce i valori **HRESULT** seguenti e altri.



| Codice restituito                                                                              | Descrizione                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl> | La priorità del processo è stata impostata correttamente.<br/> |



 

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

[**BG_JOB_PRIORITY**](bg-job-priority-.md)
</dt> <dt>

[**Metodo ibackgroundcopyjob:: GetPriority**](ibackgroundcopyjob-getpriority.md)
</dt> </dl>

 

 





