---
title: Metodo GetProperty IBackgroundCopyJob5 (Deliveryoptimization. h)
description: Metodo generico per ottenere le proprietà del processo di ottimizzazione recapito.
ms.assetid: 22BA2FAB-3F24-4801-8FB7-CB6F9E8DFBB3
keywords:
- Metodo GetProperty
- Metodo GetProperty, interfaccia IBackgroundCopyJob5
- Interfaccia IBackgroundCopyJob5, metodo GetProperty
topic_type:
- apiref
api_name:
- IBackgroundCopyJob5.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8200bb63a131db6fcab30b77f35a89fc9c943675
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964309"
---
# <a name="ibackgroundcopyjob5getproperty-method"></a>Metodo IBackgroundCopyJob5:: GetProperty

Metodo generico per ottenere le proprietà del processo di ottimizzazione recapito.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetProperty(
  [in]  BITS_JOB_PROPERTY_ID    PropertyId,
  [out] BITS_JOB_PROPERTY_VALUE *pPropertyValue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PropertyId* \[ in\]
</dt> <dd>

ID della proprietà ottenuta specificata come valore di enumerazione [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) .

</dd> <dt>

*pPropertyValue* \[ out\]
</dt> <dd>

Valore della proprietà restituito come Unione BITS_JOB_PROPERTY_VALUE.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce i valori restituiti seguenti.



| Codice restituito                                                                          | Descrizione        |
|--------------------------------------------------------------------------------------|--------------------|
| <dl> <dt>**S_OK**</dt> </dl> | Operazione riuscita<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows 10 versione 1709 \[\]<br/>                                           |
| Server minimo supportato<br/> | Windows Server, versione 1709 \[ solo per le app desktop\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob5 viene definito come E847030C-BBBA-4657-AF6D-484AA42BF1FE<br/>              |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IBackgroundCopyJob5**](ibackgroundcopyjob5.md)
</dt> <dt>

[**IBackgroundCopyJob5:: SetProperty**](ibackgroundcopyjob5-setproperty.md)
</dt> </dl>

 

 





