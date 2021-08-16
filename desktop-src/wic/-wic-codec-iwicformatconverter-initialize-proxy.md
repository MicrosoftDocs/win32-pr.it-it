---
description: IWICFormatConverter_Initialize_Proxy funzione proxy per il metodo Initialize.
ms.assetid: 26112d52-95e2-4c67-83fc-cf5e28712730
title: IWICFormatConverter_Initialize_Proxy funzione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICFormatConverter_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ade363204d9edca08003d5bfef1295c4dabf52aafed037cd2e9ca69b56d02a07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118206530"
---
# <a name="iwicformatconverter_initialize_proxy-function"></a>Funzione IWICFormatConverter \_ Initialize \_ Proxy

Funzione proxy per il [**metodo Initialize.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicformatconverter-initialize)

## <a name="syntax"></a>Sintassi


```C++
HRESULT IWICFormatConverter_Initialize_Proxy(
  _In_ IWICFormatConverter   *THIS_PTR,
  _In_ IWICBitmapSource      *pISource,
  _In_ REFWICPixelFormatGUID dstFormat,
  _In_ WICBitmapDitherType   dither,
  _In_ IWICPalette           *pIPalette,
  _In_ double                alphaThresholdPercent,
  _In_ WICBitmapPaletteType  paletteTranslate
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*QUESTO \_ PTR* \[ in\]
</dt> <dd>

Tipo: **[ **IWICFormatConverter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)\***

Puntatore a [**questo oggetto IWICFormatConverter.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicformatconverter)

</dd> <dt>

*pISource* \[ Pollici\]
</dt> <dd>

Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***

Bitmap di input da convertire

</dd> <dt>

*dstFormat* \[ Pollici\]
</dt> <dd>

Tipo: **REFWICPixelFormatGUID**

GUID del formato pixel di destinazione.

</dd> <dt>

*dithering* \[ Pollici\]
</dt> <dd>

Tipo: **[ **WICBitmapDitherType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdithertype)**

[**WICBitmapDitherType usato**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapdithertype) per la conversione.

</dd> <dt>

*pIPalette* \[ Pollici\]
</dt> <dd>

Tipo: **[ **IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***

Riquadro da utilizzare per la conversione.

</dd> <dt>

*alphaThresholdPercent* \[ Pollici\]
</dt> <dd>

Tipo: **double**

Soglia alfa da usare per la conversione.

</dd> <dt>

*paletteTranslate* \[ Pollici\]
</dt> <dd>

Tipo: **[ **WICBitmapPaletteType**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmappalettetype)**

Tipo di conversione del riquadro da utilizzare per la conversione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questa funzione ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Osservazioni

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP con SP2, Windows solo \[ app desktop di Vista\]<br/>                                                                                              |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 

 




