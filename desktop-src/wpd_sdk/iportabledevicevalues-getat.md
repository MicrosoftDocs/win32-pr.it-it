---
description: Il metodo GetA recupera un valore dalla raccolta utilizzando l'indice in base zero fornito.
ms.assetid: d52675f0-55b4-43ef-bb1d-ff6aa8a70647
title: 'Metodo IPortableDeviceValues:: GetA (PortableDeviceTypes. h)'
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
ms.openlocfilehash: 44126b69dc4e8720fde687d47dc70dd97e104c72
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329050"
---
# <a name="iportabledevicevaluesgetat-method"></a>IPortableDeviceValues:: GetA (metodo)

Il metodo **Geta** recupera un valore dalla raccolta utilizzando l'indice in base zero fornito.

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

*Indice* \[ di in\]
</dt> <dd>

**DWORD** che specifica un indice in base zero nella raccolta.

</dd> <dt>

*pKey* \[ in uscita\]
</dt> <dd>

Puntatore **PropertyKey** facoltativo che recupera la chiave dell'elemento specificato.

</dd> <dt>

*pValue* \[ in uscita\]
</dt> <dd>

**PROPVARIANT** facoltativo che recupera il valore dell'elemento specificato. Il chiamante deve liberare la memoria chiamando **PropVariantClear** al termine di tale operazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                  | Descrizione                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>         | Il metodo è riuscito.<br/>                  |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | È stato specificato un numero di indice non valido.<br/> |



 

## <a name="remarks"></a>Commenti

Se una proprietà indica un valore di tipo VT \_ Unknown, la proprietà sarà uno dei dispositivi portatili Windows ([**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md), [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md), [**IPortableDeviceValues**](iportabledevicevalues.md) o [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)). Non è possibile restituire altre interfacce da dispositivi portatili Windows.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues:: GetStringValue**](iportabledevicevalues-getstringvalue.md)
</dt> </dl>

 

 




