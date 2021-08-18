---
title: Metodo GetProperty IBackgroundCopyJob5 (Deliveryoptimization.h)
description: Metodo generico per ottenere Ottimizzazione recapito di processo (DO).
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
ms.openlocfilehash: 2141afba2d2f58a08c62d609b9029c07ae07923e35f43e985f61a13a02aa68d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118542800"
---
# <a name="ibackgroundcopyjob5getproperty-method"></a>Metodo IBackgroundCopyJob5::GetProperty

Metodo generico per ottenere Ottimizzazione recapito di processo (DO).

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetProperty(
  [in]  BITS_JOB_PROPERTY_ID    PropertyId,
  [out] BITS_JOB_PROPERTY_VALUE *pPropertyValue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PropertyId* \[ Pollici\]
</dt> <dd>

ID della proprietà ottenuta specificato come [](bits-job-property-id.md) valore BITS_JOB_PROPERTY_ID enum.

</dd> <dt>

*pPropertyValue* \[ Cambio\]
</dt> <dd>

Valore della proprietà restituito come BITS_JOB_PROPERTY_VALUE unione.

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
| IID<br/>                      | IID_IBackgroundCopyJob5 definito come E847030C-BBBA-4657-AF6D-484AA42BF1FE<br/>              |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IBackgroundCopyJob5**](ibackgroundcopyjob5.md)
</dt> <dt>

[**IBackgroundCopyJob5::SetProperty**](ibackgroundcopyjob5-setproperty.md)
</dt> </dl>

 

 





