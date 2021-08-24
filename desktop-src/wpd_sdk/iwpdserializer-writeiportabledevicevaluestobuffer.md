---
description: Il metodo WriteIPortableDeviceValuesToBuffer serializza un'interfaccia IPortableDeviceValues in una matrice di byte allocata dal chiamante.
ms.assetid: 4d0108f1-563e-42df-897b-7cc0e9ff5b3a
title: Metodo IWpdSerializer::WriteIPortableDeviceValuesToBuffer (PortableDeviceTypes.h)
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
ms.openlocfilehash: db86953e2e08c0a66f6e497c1fcd2350cc726be8852803cf8f4d64bfff523500
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657741"
---
# <a name="iwpdserializerwriteiportabledevicevaluestobuffer-method"></a>Metodo IWpdSerializer::WriteIPortableDeviceValuesToBuffer

Il **metodo WriteIPortableDeviceValuesToBuffer** serializza **un'interfaccia IPortableDeviceValues** in una matrice di byte allocata dal chiamante.

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

*dwOutputBufferLength* \[ Pollici\]
</dt> <dd>

**DWORD** che specifica le dimensioni di *pBuffer*, in byte.

</dd> <dt>

*pResults* \[ Pollici\]
</dt> <dd>

Puntatore a [**un'interfaccia IPortableDeviceValues**](iportabledevicevalues.md) da serializzare.

</dd> <dt>

*pBuffer* \[ Cambio\]
</dt> <dd>

Puntatore a un buffer allocato dal chiamante. Per informazioni sulle dimensioni del buffer richiesto, chiamare **GetSerializedSize**.

</dd> <dt>

*pdwBytesWritten* \[ Cambio\]
</dt> <dd>

Puntatore a **un valore DWORD** che indica il numero di byte effettivamente scritti nel buffer allocato dal chiamante.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                   | Descrizione                                               |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Il metodo è riuscito.<br/>                          |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>     | Un argomento del puntatore obbligatorio era **NULL.**<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Il buffer fornito dal chiamante non era sufficientemente grande.<br/> |



 

## <a name="remarks"></a>Commenti

Questo metodo copia **un'interfaccia IPortableDeviceValues** in un buffer esistente. Se si vuole allocare un nuovo buffer, usare [**GetBufferFromIPortableDeviceValues**](iwpdserializer-getbufferfromiportabledevicevalues.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|----------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IWpdSerializer**](iwpdserializer.md)
</dt> </dl>

 

 




