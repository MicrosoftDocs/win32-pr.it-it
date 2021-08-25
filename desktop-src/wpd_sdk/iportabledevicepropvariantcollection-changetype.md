---
description: Il metodo ChangeType converte tutti gli elementi della raccolta nell'oggetto VARTYPE specificato.
ms.assetid: b01b6205-c900-4b2e-810f-426e1e71a008
title: Metodo IPortableDevicePropVariantCollection::ChangeType (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.ChangeType
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f32670883981abdac56d46424d8ff18d82cf9fbe0e8a3d2222efede797ffb43d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839331"
---
# <a name="iportabledevicepropvariantcollectionchangetype-method"></a>Metodo IPortableDevicePropVariantCollection::ChangeType

Il **metodo ChangeType** converte tutti gli elementi della raccolta nell'oggetto VARTYPE specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ChangeType(
  [in] const VARTYPE vt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*vt* \[ Pollici\]
</dt> <dd>

Specifica **l'oggetto VARTYPE** in cui convertire tutti gli elementi nella raccolta. I tipi di esempio includono VT \_ UI4 e VT \_ UI8.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT.** I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Se questo metodo ha esito negativo, è possibile che la raccolta venga lasciata in uno stato intermedio, con alcuni membri convertiti e altri non convertiti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




