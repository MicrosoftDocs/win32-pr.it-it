---
description: Funzione proxy per il metodo CreateBitmap.
ms.assetid: 5647521b-231d-4819-97ab-4dfb5f796211
title: IWICImagingFactory_CreateBitmap_Proxy funzione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateBitmap_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 978946b5c22d8e4cb3427dbf27e5bb745efde259b48811a2b2a82e3721108184
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965200"
---
# <a name="iwicimagingfactory_createbitmap_proxy-function"></a>Funzione proxy IWICImagingFactory \_ CreateBitmap \_

Funzione proxy per il [**metodo CreateBitmap.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmap)

## <a name="syntax"></a>Sintassi


```C++
HRESULT IWICImagingFactory_CreateBitmap_Proxy(
  _In_  IWICImagingFactory         *pFactory,
  _In_  UINT                       uiWidth,
  _In_  UINT                       uiHeight,
  _In_  REFWICPixelFormatGUID      pixelFormat,
  _In_  WICBitmapCreateCacheOption option,
  _Out_ IWICBitmap                 **ppIBitmap
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

*opzione* \[ Pollici\]
</dt> <dd>

Tipo: **[ **WICBitmapCreateCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapcreatecacheoption)**

Opzioni di creazione della cache della nuova bitmap.

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
| Client minimo supportato<br/> | Windows XP con SP2, Windows solo \[ app desktop vista\]<br/>                                                                                              |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 

 




