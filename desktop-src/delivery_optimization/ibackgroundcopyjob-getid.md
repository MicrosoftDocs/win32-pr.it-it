---
title: Metodo GetId IBackgroundCopyJob (Deliveryoptimization.h)
description: Recupera l'identificatore utilizzato per identificare il processo nella coda.
ms.assetid: 05CE5420-22F8-4CFE-BC40-3A29C775854B
keywords:
- GetId (metodo)
- Metodo GetId, interfaccia IBackgroundCopyJob
- Interfaccia IBackgroundCopyJob, metodo GetId
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetId
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 01c696985b4b632223318675fd63f842b85ed6e27297ff1befebbac1b3fa9bce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755501"
---
# <a name="ibackgroundcopyjobgetid-method"></a>Metodo IBackgroundCopyJob::GetId

Recupera l'identificatore utilizzato per identificare il processo nella coda.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetId(
  [out] GUID *pJobID
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pJobID* \[ Cambio\]
</dt> <dd>

GUID che identifica il processo all'interno della coda DO.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo **restituisce** S_OK esito positivo o uno dei valori **HRESULT** COM standard in caso di errore.

## <a name="remarks"></a>Commenti

Il servizio genera l'identificatore quando si [crea](ibackgroundcopymanager-createjob.md) il processo. Per usare l'identificatore per recuperare un puntatore a interfaccia [**IBackgroundCopyJob**](ibackgroundcopyjob-.md) per il processo, chiamare il [**metodo IBackgroundCopyManager::GetJob.**](ibackgroundcopymanager-getjob.md)

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

[**IBackgroundCopyManager::CreateJob**](ibackgroundcopymanager-createjob.md)
</dt> <dt>

[**IBackgroundCopyManager::GetJob**](ibackgroundcopymanager-getjob.md)
</dt> </dl>

 

 





