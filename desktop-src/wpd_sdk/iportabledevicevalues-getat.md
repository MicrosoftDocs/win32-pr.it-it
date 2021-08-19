---
description: Il metodo GetAt recupera un valore dalla raccolta usando l'indice in base zero fornito.
ms.assetid: d52675f0-55b4-43ef-bb1d-ff6aa8a70647
title: Metodo IPortableDeviceValues::GetAt (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 4e234d0fe24eec947b388b5da798c55e7478ffa6bda69a9b9fe57c279af6d96e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843024"
---
# <a name="iportabledevicevaluesgetat-method"></a>Metodo IPortableDeviceValues::GetAt

Il **metodo GetAt** recupera un valore dalla raccolta usando l'indice in base zero fornito.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetAt(
  [in]      const DWORD       index,
  [in, out]       PROPERTYKEY *pKey,
  [in, out]       PROPVARIANT *pValue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*index* \[ Pollici\]
</dt> <dd>

Valore **DWORD** che specifica un indice in base zero nella raccolta.

</dd> <dt>

*pKey* \[ in, out\]
</dt> <dd>

Puntatore **PROPERTYKEY facoltativo** che recupera la chiave dell'elemento specificato.

</dd> <dt>

*pValue* \[ in, out\]
</dt> <dd>

Valore **PROPVARIANT facoltativo** che recupera il valore dell'elemento specificato. Al termine, il chiamante deve liberare la memoria chiamando **PropVariantClear.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **valore HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                  | Descrizione                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Il metodo è riuscito.<br/>                  |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | È stato specificato un numero di indice non valido.<br/> |



 

## <a name="remarks"></a>Commenti

Se una proprietà indica un valore di tipo VT UNKNOWN, la proprietà sarà uno dei dispositivi portabili \_ Windows ([**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md), [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md), [**IPortableDeviceValues**](iportabledevicevalues.md) o [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)). Nessun'altra interfaccia può essere restituita Windows dispositivi portatili.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::GetStringValue**](iportabledevicevalues-getstringvalue.md)
</dt> </dl>

 

 




