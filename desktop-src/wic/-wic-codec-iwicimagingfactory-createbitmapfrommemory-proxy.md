---
description: Funzione proxy per il metodo CreateBitmapFromMemory.
ms.assetid: 5aa455d5-23e3-4738-b028-b84da0fb0c50
title: Funzione IWICImagingFactory_CreateBitmapFromMemory_Proxy
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
ms.openlocfilehash: 79893952bb6dcdbab6c4a1cea4f57355831d31c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316806"
---
# <a name="iwicimagingfactory_createbitmapfrommemory_proxy-function"></a>IWICImagingFactory \_ CreateBitmapFromMemory- \_ funzione proxy

Funzione proxy per il metodo [**CreateBitmapFromMemory**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfrommemory) .

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

*pFactory* \[ in\]
</dt> <dd>

Tipo: **[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _

</dd> <dt>

_uiWidth * \[ in\]
</dt> <dd>

Tipo: **uint**

Larghezza della nuova bitmap.

</dd> <dt>

*uiHeight* \[ in\]
</dt> <dd>

Tipo: **uint**

Altezza della nuova bitmap.

</dd> <dt>

*PixelFormat* \[ in\]
</dt> <dd>

Tipo: **REFWICPixelFormatGUID**

Formato pixel della nuova bitmap.

</dd> <dt>

*cbStride* \[ in\]
</dt> <dd>

Tipo: **uint**

[*Stride*](/windows) dei dati pixel specificati.

</dd> <dt>

*cbBufferSize* \[ in\]
</dt> <dd>

Tipo: **uint**

Dimensioni di *pbBuffer*.

</dd> <dt>

*pbBuffer* \[ in\]
</dt> <dd>

Tipo: **byte \** _

Buffer utilizzato per creare la bitmap.

</dd> <dt>

_ppIBitmap * \[ out\]
</dt> <dd>

Tipo: **[ **IWICBitmap**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmap)\*\***

Puntatore che riceve un puntatore alla nuova bitmap.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questa funzione ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Osservazioni

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP con SP2, \[ solo app desktop di Windows Vista\]<br/>                                                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt> </dl> |



 

