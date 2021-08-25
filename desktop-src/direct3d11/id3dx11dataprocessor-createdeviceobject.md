---
title: Metodo ID3DX11DataProcessor CreateDeviceObject (D3DX11core.h)
description: Nota La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Crea un oggetto dispositivo.
ms.assetid: 797d216b-2f54-4d24-aa97-04be0c71f909
keywords:
- Metodo CreateDeviceObject Direct3D 11
- Metodo CreateDeviceObject Direct3D 11, interfaccia ID3DX11DataProcessor
- Id3DX11DataProcessor interface Direct3D 11 , CreateDeviceObject method
topic_type:
- apiref
api_name:
- ID3DX11DataProcessor.CreateDeviceObject
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15627fc823de8a46a1299607f74694a0f93236082423910adf395b2b00ad57f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894931"
---
# <a name="id3dx11dataprocessorcreatedeviceobject-method"></a>Metodo ID3DX11DataProcessor::CreateDeviceObject

> [!Note]  
> La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app Windows Store.

 

Crea un oggetto dispositivo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateDeviceObject(
  [out] void **ppDataObject
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppDataObject* \[ Cambio\]
</dt> <dd>

Tipo: **\* \* void**

Indirizzo di un puntatore all'oggetto dispositivo creato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Il valore restituito è uno dei valori elencati in [Codici restituiti Direct3D 11.](d3d11-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Commenti

Questo metodo viene usato da [**un'interfaccia ID3DX11ThreadPump.**](id3dx11threadpump.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX11core.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3DX11.lib</dt> </dl>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DX11DataProcessor](id3dx11dataprocessor.md)
</dt> <dt>

[Interfacce D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





