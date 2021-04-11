---
title: Metodo getProgress metodo ibackgroundcopyjob (Deliveryoptimization. h)
description: Recupera le informazioni sullo stato di avanzamento correlate al processo, ad esempio il numero di byte e i file trasferiti.
ms.assetid: E23C82E1-3805-4C5D-9F18-0DA17F7C473E
keywords:
- Metodo getProgress
- Metodo getProgress, interfaccia metodo ibackgroundcopyjob
- Interfaccia metodo ibackgroundcopyjob, metodo getProgress
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
ms.openlocfilehash: d49a040bb5656ae6ef6d926a45b31808623e399b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119954"
---
# <a name="ibackgroundcopyjobgetprogress-method"></a>Metodo metodo ibackgroundcopyjob:: getProgress

Recupera le informazioni sullo stato di avanzamento correlate al processo, ad esempio il numero di byte e i file trasferiti.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetProgress(
  [out] BG_JOB_PROGRESS *pProgress
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pProgress* \[ out\]
</dt> <dd>

Contiene i dati che è possibile utilizzare per calcolare la percentuale del processo completato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce i valori **HRESULT** seguenti e altri.



| Codice restituito                                                                              | Descrizione                                                 |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl> | Recupero delle informazioni sullo stato completato.<br/> |



 

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
</dt> </dl>

 

 





