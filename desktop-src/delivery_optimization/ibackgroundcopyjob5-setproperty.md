---
title: Metodo SetProperty IBackgroundCopyJob5 (Deliveryoptimization.h)
description: Metodo generico per l'impostazione Ottimizzazione recapito proprietà del processo.
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
ms.openlocfilehash: f9b7dab17780572a59e12dde9905c3d8db23895e6564aac47cb6eb2d984bfaf3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118542684"
---
# <a name="ibackgroundcopyjob5setproperty-method"></a>Metodo IBackgroundCopyJob5::SetProperty

Metodo generico per l'impostazione Ottimizzazione recapito proprietà del processo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetProperty(
  [in] BITS_JOB_PROPERTY_ID    PropertyId,
  [in] BITS_JOB_PROPERTY_VALUE PropertyValue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PropertyId* \[ Pollici\]
</dt> <dd>

ID della proprietà che viene impostata specificato come valore [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) enum.

</dd> <dt>

*PropertyValue* \[ Pollici\]
</dt> <dd>

Valore della proprietà che viene impostata. Per contenere un valore il cui tipo è appropriato per la proprietà , [**questo**](bits-job-property-value-.md) valore viene specificato tramite l'unione BITS_JOB_PROPERTY_VALUE costituita da tutti i tipi di proprietà noti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce i valori restituiti seguenti.



| Codice restituito                                                                          | Descrizione        |
|--------------------------------------------------------------------------------------|--------------------|
| <dl> <dt>**S_OK**</dt> </dl> | Operazione riuscita<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1709 \[\]<br/>                                           |
| Server minimo supportato<br/> | Windows Server, solo app desktop versione 1709 \[\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob5 è definito come E847030C-BBBA-4657-AF6D-484AA42BF1FE<br/>              |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IBackgroundCopyJob5**](ibackgroundcopyjob5.md)
</dt> <dt>

[**IBackgroundCopyJob5::GetProperty**](ibackgroundcopyjob5-getproperty.md)
</dt> </dl>

 

 





