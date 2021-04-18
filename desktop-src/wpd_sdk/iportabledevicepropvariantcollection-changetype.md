---
description: Il metodo ChangeType converte tutti gli elementi della raccolta nel VARTYPE specificato.
ms.assetid: b01b6205-c900-4b2e-810f-426e1e71a008
title: 'Metodo IPortableDevicePropVariantCollection:: ChangeType (PortableDeviceTypes. h)'
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
ms.openlocfilehash: d843b62d273b28f7a694c37358742e4f3365be21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329892"
---
# <a name="iportabledevicepropvariantcollectionchangetype-method"></a>Metodo IPortableDevicePropVariantCollection:: ChangeType

Il metodo **ChangeType** converte tutti gli elementi della raccolta nel VarType specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ChangeType(
  [in] const VARTYPE vt
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*VT* \[ in\]
</dt> <dd>

Specifica il **VarType** in cui si desidera convertire tutti gli elementi della raccolta. I tipi di esempio includono VT \_ UI4 e VT \_ UI8.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                          | Descrizione                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Il metodo è riuscito.<br/> |



 

## <a name="remarks"></a>Commenti

Se questo metodo ha esito negativo, è possibile che la raccolta venga lasciata in uno stato intermedio, con alcuni membri convertiti e non convertiti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




