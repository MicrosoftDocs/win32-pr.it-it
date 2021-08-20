---
description: Funzione proxy per il metodo CreateBitmapFromMemory.
ms.assetid: 5aa455d5-23e3-4738-b028-b84da0fb0c50
title: IWICImagingFactory_CreateBitmapFromMemory_Proxy funzione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapFromMemory_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e7f5567f2ead2b68440e448a9a03f36fdedceb5d31ecfc579f7df956988dfc01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118033914"
---
# <a name="iwicimagingfactory_createbitmapfrommemory_proxy-function"></a>Funzione proxy IWICImagingFactory \_ CreateBitmapFromMemory \_

Funzione proxy per [**il metodo CreateBitmapFromMemory.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfrommemory)

## <a name="syntax"></a>Sintassi


```C++
HRESULT IWICImagingFactory_CreateBitmapFromMemory_Proxy(
  _In_  IWICImagingFactory    *pFactory,
  _In_  UINT                  uiWidth,
  _In_  UINT                  uiHeight,
  _In_  REFWICPixelFormatGUID pixelFormat,
  _In_  UINT                  cbStride,
  _In_  UINT                  cbBufferSize,
  _In_  BYTE                  *pbBuffer,
  _Out_ IWICBitmap            **ppIBitmap
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pFactory* \[ Pollici\]
</dt> <dd>

Tipo: **[ **IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\***

</dd> <dt>

*uiWidth* \[ Pollici\]
</dt> <dd>

Tipo: **UINT**

Larghezza della nuova bitmap.

</dd> <dt>

*uiHeight* \[ Pollici\]
</dt> <dd>

Tipo: **UINT**

Altezza della nuova bitmap.

</dd> <dt>

*pixelFormat* \[ Pollici\]
</dt> <dd>

Tipo: **REFWICPixelFormatGUID**

Formato pixel della nuova bitmap.

</dd> <dt>

*cbStride* \[ Pollici\]
</dt> <dd>

Tipo: **UINT**

Stride [*dei*](/windows) dati pixel specificato.

</dd> <dt>

*cbBufferSize* \[ Pollici\]
</dt> <dd>

Tipo: **UINT**

Dimensioni di *pbBuffer*.

</dd> <dt>

*pbBuffer* \[ Pollici\]
</dt> <dd>

Tipo: **\* BYTE**

Buffer utilizzato per creare la bitmap.

</dd> <dt>

*ppIBitmap* \[ Cambio\]
</dt> <dd>

Tipo: **[ **IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***

Puntatore che riceve un puntatore alla nuova bitmap.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questa funzione ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Osservazioni

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP con SP2, Windows solo app desktop di Vista \[\]<br/>                                                                                              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 

