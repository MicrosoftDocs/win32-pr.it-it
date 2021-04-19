---
description: Il metodo WriteIPortableDeviceValuesToBuffer serializza un'interfaccia IPortableDeviceValues in una matrice di byte allocata dal chiamante.
ms.assetid: 4d0108f1-563e-42df-897b-7cc0e9ff5b3a
title: 'Metodo IWpdSerializer:: WriteIPortableDeviceValuesToBuffer (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer.WriteIPortableDeviceValuesToBuffer
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f2a8f8b374f967f7231881d9e0eca6434e9c57e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324045"
---
# <a name="iwpdserializerwriteiportabledevicevaluestobuffer-method"></a>Metodo IWpdSerializer:: WriteIPortableDeviceValuesToBuffer

Il metodo **WriteIPortableDeviceValuesToBuffer** serializza un'interfaccia **IPortableDeviceValues** in una matrice di byte allocata dal chiamante.

## <a name="syntax"></a>Sintassi


```C++
HRESULT WriteIPortableDeviceValuesToBuffer(
  [in]  DWORD                 dwOutputBufferLength,
  [in]  IPortableDeviceValues *pResults,
  [out] BYTE                  *pBuffer,
  [out] DWORD                 *pdwBytesWritten
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwOutputBufferLength* \[ in\]
</dt> <dd>

**DWORD** che specifica la dimensione di *pbuffer* in byte.

</dd> <dt>

*pResults* \[ in\]
</dt> <dd>

Puntatore a un'interfaccia [**IPortableDeviceValues**](iportabledevicevalues.md) da serializzare.

</dd> <dt>

*pbuffer* \[ out\]
</dt> <dd>

Puntatore a un buffer allocato dal chiamante. Per informazioni sulle dimensioni del buffer necessario, chiamare **GetSerializedSize**.

</dd> <dt>

*pdwBytesWritten* \[ out\]
</dt> <dd>

Puntatore a un **valore DWORD** che indica il numero di byte effettivamente scritti nel buffer allocato dal chiamante.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                   | Descrizione                                               |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Il metodo è riuscito.<br/>                          |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | Un argomento obbligatorio del puntatore è **null**.<br/>      |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | Il buffer fornito dal chiamante non era sufficientemente grande.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo copia un'interfaccia **IPortableDeviceValues** in un buffer esistente. Se si desidera allocare un nuovo buffer, utilizzare [**GetBufferFromIPortableDeviceValues**](iwpdserializer-getbufferfromiportabledevicevalues.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWpdSerializer**](iwpdserializer.md)
</dt> </dl>

 

 




