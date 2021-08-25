---
description: Il metodo GetSerializedSize calcola le dimensioni del buffer necessarie per contenere un'interfaccia IPortableDeviceValues serializzata.
ms.assetid: 12fa6ed1-ce3b-4c5d-920a-87ff693fe0ea
title: Metodo IWpdSerializer::GetSerializedSize (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer.GetSerializedSize
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: ae6b8381928c64b7d16e9f5daa4dd9fd85acd9b61c13531365d871563ef6afe0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119704521"
---
# <a name="iwpdserializergetserializedsize-method"></a>Metodo IWpdSerializer::GetSerializedSize

Il **metodo GetSerializedSize** calcola le dimensioni del buffer necessarie per contenere un'interfaccia [**IPortableDeviceValues serializzata.**](iportabledevicevalues.md)

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetSerializedSize(
  [in]  IPortableDeviceValues *pSource,
  [out] DWORD                 *pdwSize
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSource* \[ Pollici\]
</dt> <dd>

Puntatore a [**un'interfaccia IPortableDeviceValues**](iportabledevicevalues.md) di cui si desidera richiedere le dimensioni.

</dd> <dt>

*pdwSize* \[ Cambio\]
</dt> <dd>

Puntatore a **un valore DWORD** che indica le dimensioni del buffer necessarie per serializzare *pSource,* in byte.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                   | Descrizione                                                            |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Il metodo è riuscito.<br/>                                       |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>     | Un argomento del puntatore obbligatorio era **NULL.**<br/>                   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria disponibile insufficiente per creare il buffer.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWpdSerializer**](iwpdserializer.md)
</dt> </dl>

 

 




