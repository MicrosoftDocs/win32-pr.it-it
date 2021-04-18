---
description: Funzione proxy per il metodo CreateBitmapFromHBITMAP.
ms.assetid: e4e9a6b4-00d9-4f87-aeec-f2c02c3f44ab
title: Funzione IWICImagingFactory_CreateBitmapFromHBITMAP_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmapFromHBITMAP_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 6599a9699e6fb83c1678cd0360f906cc8e0668c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316808"
---
# <a name="iwicimagingfactory_createbitmapfromhbitmap_proxy-function"></a>IWICImagingFactory \_ CreateBitmapFromHBITMAP- \_ funzione proxy

Funzione proxy per il metodo [**CreateBitmapFromHBITMAP**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmapfromhbitmap) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT IWICImagingFactory_CreateBitmapFromHBITMAP_Proxy(
  _In_  IWICImagingFactory          *pFactory,
  _In_  HBITMAP                     hBitmap,
  _In_  HPALETTE                    hPalette,
  _In_  WICBitmapAlphaChannelOption options,
  _Out_ IWICBitmap                  **ppIBitmap
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pFactory* \[ in\]
</dt> <dd>

Tipo: **[**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory) \** _

</dd> <dt>

_hBitmap * \[ in\]
</dt> <dd>

Tipo: **HBITMAP**

Handle bitmap da cui creare la bitmap.

</dd> <dt>

*hPalette* \[ in\]
</dt> <dd>

Tipo: **HPALETTE**

Handle della tavolozza utilizzato per creare la bitmap.

</dd> <dt>

*Opzioni* \[ di in\]
</dt> <dd>

Tipo: **[ **WICBitmapAlphaChannelOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapalphachanneloption)**

Opzioni del canale alfa per creare la bitmap.

</dd> <dt>

*ppIBitmap* \[ out\]
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



 

 




