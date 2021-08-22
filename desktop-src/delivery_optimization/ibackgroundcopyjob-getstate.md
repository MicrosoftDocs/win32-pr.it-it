---
title: Metodo GetState IBackgroundCopyJob (Deliveryoptimization.h)
description: Recupera lo stato del processo.
ms.assetid: 975AF0FB-37AE-4CE8-9EC1-35A972E422D8
keywords:
- Metodo GetState
- Metodo GetState, interfaccia IBackgroundCopyJob
- Interfaccia IBackgroundCopyJob, metodo GetState
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
ms.openlocfilehash: 64a26d1cc301230a9bb8330b9a2b2daf3178b1538ec95f593cd5e3f4d3099d7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755301"
---
# <a name="ibackgroundcopyjobgetstate-method"></a>Metodo IBackgroundCopyJob::GetState

Recupera lo stato del processo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetState(
  [out] BG_JOB_STATE *pJobState
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pJobState* \[ Cambio\]
</dt> <dd>

Stato del processo. Ad esempio, lo stato riflette se il processo è in errore, trasferisce i dati o è sospeso. Per un elenco degli stati del processo, vedere [**l'enumerazione BG_JOB_STATE**](bg-job-state-.md) processo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce i **valori HRESULT** seguenti, oltre ad altri.



| Codice restituito                                                                              | Descrizione                                                 |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>S_OK****</dt> </dl> | Lo stato del processo è stato recuperato correttamente.<br/> |



 

## <a name="remarks"></a>Commenti

Se si vuole sapere quando un processo è in errore o ha trasferito tutti i file nel processo, è possibile usare questo metodo per eseguire il polling dello stato del processo oppure è possibile registrarsi per ricevere una notifica quando si verificano eventi. Per informazioni dettagliate sulla registrazione per ricevere la notifica degli eventi, vedere [**l'interfaccia IBackgroundCopyCallback.**](ibackgroundcopycallback.md)

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

[**BG_JOB_STATE**](bg-job-state-.md)
</dt> <dt>

[**IBackgroundCopyCallback**](ibackgroundcopycallback.md)
</dt> </dl>

 

 





