---
description: Funzione proxy per il metodo GetPreview.
ms.assetid: 8251af14-68db-4e4a-a501-115e7bbd53cd
title: IWICBitmapDecoder_GetPreview_Proxy funzione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapDecoder_GetPreview_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ffcc09c7721cf56e0b0c799669475da61d8ae3720d98b650f02567fac2130381
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118207222"
---
# <a name="iwicbitmapdecoder_getpreview_proxy-function"></a>Funzione proxy IWICBitmapDecoder \_ GetPreview \_

Funzione proxy per il [**metodo GetPreview.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview)

## <a name="syntax"></a>Sintassi


```C++
HRESULT IWICBitmapDecoder_GetPreview_Proxy(
  _In_  IWICBitmapDecoder *THIS_PTR,
  _Out_ IWICBitmapSource  **ppIBitmapSource
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*QUESTO \_ PTR* \[ in\]
</dt> <dd>

Tipo: **[ **IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)\***

Puntatore a [**questo oggetto IWICBitmapDecoder.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)

</dd> <dt>

*ppIBitmapSource* \[ Cambio\]
</dt> <dd>

Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***

Puntatore che riceve un puntatore alla bitmap di anteprima, se supportato.

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



 

 




