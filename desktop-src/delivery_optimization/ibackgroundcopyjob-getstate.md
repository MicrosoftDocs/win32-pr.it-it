---
title: Metodo GetState Metodo ibackgroundcopyjob (Deliveryoptimization. h)
description: Recupera lo stato del processo.
ms.assetid: 975AF0FB-37AE-4CE8-9EC1-35A972E422D8
keywords:
- Metodo GetState
- Metodo GetState, interfaccia metodo ibackgroundcopyjob
- Interfaccia metodo ibackgroundcopyjob, metodo GetState
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetState
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5b195377a44cab8f336bae8090bacc5ca5624d7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741719"
---
# <a name="ibackgroundcopyjobgetstate-method"></a>Metodo metodo ibackgroundcopyjob:: GetState

Recupera lo stato del processo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetState(
  [out] BG_JOB_STATE *pJobState
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pJobState* \[ out\]
</dt> <dd>

Stato del processo. Ad esempio, lo stato indica se il processo è in errore, trasferisce i dati o è sospeso. Per un elenco degli Stati del processo, vedere l'enumerazione [**BG_JOB_STATE**](bg-job-state-.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce i valori **HRESULT** seguenti e altri.



| Codice restituito                                                                              | Descrizione                                                 |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl> | Lo stato del processo è stato recuperato correttamente.<br/> |



 

## <a name="remarks"></a>Commenti

Per capire quando un processo è in errore o ha trasferito tutti i file nel processo, è possibile usare questo metodo per eseguire il polling dello stato del processo oppure è possibile registrarsi per ricevere una notifica quando si verificano gli eventi. Per informazioni dettagliate sulla registrazione per ricevere la notifica degli eventi, vedere l'interfaccia [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) .

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

[**BG_JOB_STATE**](bg-job-state-.md)
</dt> <dt>

[**IBackgroundCopyCallback**](ibackgroundcopycallback.md)
</dt> </dl>

 

 





