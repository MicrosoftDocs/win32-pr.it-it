---
title: Metodo IBackgroundCopyJob GetProgress (Deliveryoptimization.h)
description: Recupera informazioni sullo stato di avanzamento relative al processo, ad esempio il numero di byte e file trasferiti.
ms.assetid: E23C82E1-3805-4C5D-9F18-0DA17F7C473E
keywords:
- Metodo GetProgress
- Metodo GetProgress, interfaccia IBackgroundCopyJob
- Interfaccia IBackgroundCopyJob, metodo GetProgress
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetProgress
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 07a498aef2a9dcfd108733b45526bd876817d8d5075323d0edd95c7cbf3de8df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755321"
---
# <a name="ibackgroundcopyjobgetprogress-method"></a>Metodo IBackgroundCopyJob::GetProgress

Recupera informazioni sullo stato di avanzamento relative al processo, ad esempio il numero di byte e file trasferiti.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetProgress(
  [out] BG_JOB_PROGRESS *pProgress
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pProgress* \[ Cambio\]
</dt> <dd>

Contiene dati che è possibile utilizzare per calcolare la percentuale di completamento del processo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce i valori **HRESULT** seguenti, oltre ad altri.



| Codice restituito                                                                              | Descrizione                                                 |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>S_OK****</dt> </dl> | Le informazioni sullo stato di avanzamento sono state recuperate correttamente.<br/> |



 

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
</dt> </dl>

 

 





