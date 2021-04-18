---
title: Metodo metodo ibackgroundcopyjob GetId (Deliveryoptimization. h)
description: Recupera l'identificatore utilizzato per identificare il processo nella coda.
ms.assetid: 05CE5420-22F8-4CFE-BC40-3A29C775854B
keywords:
- GetId (metodo)
- Metodo GetId, interfaccia metodo ibackgroundcopyjob
- Interfaccia metodo ibackgroundcopyjob, Metodo GetId
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
ms.openlocfilehash: ade12d72d68b43df7d9ae3d1f33010bb95b7052a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301593"
---
# <a name="ibackgroundcopyjobgetid-method"></a>Metodo metodo ibackgroundcopyjob:: GetId

Recupera l'identificatore utilizzato per identificare il processo nella coda.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetId(
  [out] GUID *pJobID
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pJobID* \[ out\]
</dt> <dd>

GUID che identifica il processo all'interno della coda di esecuzione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce **S_OK** in esito positivo o uno dei valori **HRESULT** com standard in errore.

## <a name="remarks"></a>Commenti

Il servizio genera l'identificatore quando si [Crea](ibackgroundcopymanager-createjob.md) il processo. Per usare l'identificatore per recuperare un puntatore di interfaccia [**Metodo ibackgroundcopyjob**](ibackgroundcopyjob-.md) per il processo, chiamare il metodo [**IBackgroundCopyManager:: GetJob**](ibackgroundcopymanager-getjob.md) .

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

[**IBackgroundCopyManager:: CreateJob**](ibackgroundcopymanager-createjob.md)
</dt> <dt>

[**IBackgroundCopyManager:: GetJob**](ibackgroundcopymanager-getjob.md)
</dt> </dl>

 

 





