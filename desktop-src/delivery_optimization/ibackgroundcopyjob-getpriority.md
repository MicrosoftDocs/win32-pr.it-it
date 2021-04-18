---
title: Metodo GetPriority metodo ibackgroundcopyjob (Deliveryoptimization. h)
description: Recupera il livello di priorità per il processo. Il livello di priorità determina quando il processo viene elaborato rispetto ad altri processi nella coda di trasferimento.
ms.assetid: 2F778B35-8DBB-4540-88C2-A2E18EBB0D89
keywords:
- GetPriority (metodo)
- Metodo GetPriority, interfaccia metodo ibackgroundcopyjob
- Interfaccia metodo ibackgroundcopyjob, metodo GetPriority
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetPriority
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7ae9a865045ee1264a0598a3d3c1db8cc3c3b8bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301727"
---
# <a name="ibackgroundcopyjobgetpriority-method"></a>Metodo metodo ibackgroundcopyjob:: GetPriority

Recupera il livello di priorità per il processo. Il livello di priorità determina quando il processo viene elaborato rispetto ad altri processi nella coda di trasferimento.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetPriority(
  [out] BG_JOB_PRIORITY *pPriority
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pPriority* \[ out\]
</dt> <dd>

Priorità del processo rispetto ad altri processi nella coda di trasferimento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce i valori **HRESULT** seguenti e altri.



| Codice restituito                                                                              | Descrizione                                           |
|------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl> | Il livello di priorità è stato recuperato.<br/> |



 

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

[**Metodo ibackgroundcopyjob:: sepriority**](ibackgroundcopyjob-setpriority.md)
</dt> </dl>

 

 





