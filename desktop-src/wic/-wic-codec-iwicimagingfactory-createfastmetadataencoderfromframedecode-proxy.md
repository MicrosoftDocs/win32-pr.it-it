---
description: Funzione proxy per il metodo CreateFastMetadataEncoderFromFrameDecode.
ms.assetid: 0edc3387-47e9-401c-9153-76c8c32b52de
title: IWICImagingFactory_CreateFastMetadataEncoderFromFrameDecode_Proxy funzione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateFastMetadataEncoderFromFrameDecode_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 0c877343b317057f4a94d7313d768fa2260b518f438f4db54fd6ff0bfa108c46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118033634"
---
# <a name="iwicimagingfactory_createfastmetadataencoderfromframedecode_proxy-function"></a>Funzione proxy IWICImagingFactory \_ CreateFastMetadataEncoderFromFrameDecode \_

Funzione proxy per [**il metodo CreateFastMetadataEncoderFromFrameDecode.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createfastmetadataencoderfromframedecode)

## <a name="syntax"></a>Sintassi


```C++
HRESULT IWICImagingFactory_CreateFastMetadataEncoderFromFrameDecode_Proxy(
  _In_  IWICImagingFactory      *pFactory,
  _In_  IWICBitmapFrameDecode   *pIFrameDecoder,
  _Out_ IWICFastMetadataEncoder **ppIFME
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pFactory* \[ Pollici\]
</dt> <dd>

Tipo: **[ **IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\***

</dd> <dt>

*pIFrameDecoder* \[ Pollici\]
</dt> <dd>

Tipo: **[ **IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\***

[**IWICBitmapFrameDecode da**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) cui creare [**IWICFastMetadataEncoder.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)

</dd> <dt>

*ppIFME* \[ Cambio\]
</dt> <dd>

Tipo: **[ **IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)\*\***

Puntatore che riceve un puntatore a un [**nuovo oggetto IWICFastMetadataEncoder.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questa funzione ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Osservazioni

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP con SP2, Windows solo \[ app desktop vista\]<br/>                                                                                              |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 

 




