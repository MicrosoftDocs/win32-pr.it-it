---
description: Funzione proxy per il metodo CreateBitmap.
ms.assetid: 5647521b-231d-4819-97ab-4dfb5f796211
title: Funzione IWICImagingFactory_CreateBitmap_Proxy
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
ms.openlocfilehash: 56684de0280ae27bf2ec1e900bd718faec4733fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316810"
---
# <a name="iwicimagingfactory_createbitmap_proxy-function"></a>IWICImagingFactory \_ CreateBitmap- \_ funzione proxy

Funzione proxy per il metodo [**CreateBitmap**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createbitmap) .

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

*opzione* \[ in\]
</dt> <dd>

Tipo: **[ **WICBitmapCreateCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapcreatecacheoption)**

Opzioni di creazione della cache della nuova bitmap.

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



 

 




