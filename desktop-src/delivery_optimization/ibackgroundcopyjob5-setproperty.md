---
title: Metodo SetProperty IBackgroundCopyJob5 (Deliveryoptimization. h)
description: Metodo generico per l'impostazione delle proprietà del processo di ottimizzazione recapito.
ms.assetid: 9A8CCE04-B3EB-43CC-A135-7054EC40ABEC
keywords:
- Metodo SetProperty
- Metodo SetProperty, interfaccia IBackgroundCopyJob5
- Interfaccia IBackgroundCopyJob5, metodo SetProperty
topic_type:
- apiref
api_name:
- IBackgroundCopyJob5.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a3dbd1e7c66592ea959c9b1ff4f4864340c504d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742858"
---
# <a name="ibackgroundcopyjob5setproperty-method"></a>Metodo IBackgroundCopyJob5:: SetProperty

Metodo generico per l'impostazione delle proprietà del processo di ottimizzazione recapito.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetProperty(
  [in] BITS_JOB_PROPERTY_ID    PropertyId,
  [in] BITS_JOB_PROPERTY_VALUE PropertyValue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PropertyId* \[ in\]
</dt> <dd>

ID della proprietà che viene impostata come valore di enumerazione [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) .

</dd> <dt>

*PropertyValue* \[ in\]
</dt> <dd>

Valore della proprietà da impostare. Per mantenere un valore il cui tipo è appropriato per la proprietà, questo valore viene specificato tramite il [**BITS_JOB_PROPERTY_VALUE**](bits-job-property-value-.md) Unione costituito da tutti i tipi di proprietà noti.

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

[**IBackgroundCopyJob5:: GetProperty**](ibackgroundcopyjob5-getproperty.md)
</dt> </dl>

 

 





