---
title: Metodo GetProperty IBackgroundCopyFile5 (Deliveryoptimization.h)
description: Ottiene una proprietà generica di un Ottimizzazione recapito (DO).
ms.assetid: E2E96A0F-5670-4DE7-9DF8-A215AFAD0E8A
keywords:
- Metodo GetProperty
- Metodo GetProperty, interfaccia IBackgroundCopyFile5
- Interfaccia IBackgroundCopyFile5, metodo GetProperty
topic_type:
- apiref
api_name:
- IBackgroundCopyFile5.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0a664c752bd28b176189cdd77e955684236cfa23c6b384378610336335651fad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635951"
---
# <a name="ibackgroundcopyfile5getproperty-method"></a>Metodo IBackgroundCopyFile5::GetProperty

Ottiene una proprietà generica di un Ottimizzazione recapito (DO).

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetProperty(
  [in]  BITS_FILE_PROPERTY_ID    PropertyId,
  [out] BITS_FILE_PROPERTY_VALUE *PropertyValue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PropertyId* \[ Pollici\]
</dt> <dd>

Specifica la proprietà del file di cui recuperare il valore.

</dd> <dt>

*PropertyValue* \[ Cambio\]
</dt> <dd>

Valore della proprietà, restituito come puntatore a un'BITS_FILE_PROPERTY_VALUE unione. Usare il campo union appropriato per il valore ID proprietà passato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, **restituisce** S_OK . In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 10, solo app desktop versione 1709 \[\]<br/>                                           |
| Server minimo supportato<br/> | Windows Server, solo app desktop versione 1709 \[\]<br/>                                       |
| Intestazione<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Libreria<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile5 è definito come 85C1657F-DAFC-40E8-8834-DF18EA25717E<br/>             |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IBackgroundCopyFile5**](ibackgroundcopyfile5.md)
</dt> <dt>

[**IBackgroundCopyFile5.SetProperty**](ibackgroundcopyfile5-setproperty.md)
</dt> </dl>

 

 





