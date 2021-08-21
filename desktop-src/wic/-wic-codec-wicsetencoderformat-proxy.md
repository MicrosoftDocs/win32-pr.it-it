---
description: Funzione proxy per negoziare il formato pixel e la tavolozza per il codificatore.
ms.assetid: 01179598-ba40-4aed-a7c4-888cb4e851f4
title: WICSetEncoderFormat_Proxy funzione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WICSetEncoderFormat_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 3343e6f80193a4cb37dba98ffa3320bd8d56ee8bb9f14159adbf2474c767ed03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119812061"
---
# <a name="wicsetencoderformat_proxy-function"></a>Funzione proxy WICSetEncoderFormat \_

Funzione proxy per negoziare il formato pixel e la tavolozza per il codificatore.

## <a name="syntax"></a>Sintassi


```C++
HRESULT WICSetEncoderFormat_Proxy(
  _In_  IWICBitmapSource      *pSourceIn,
  _In_  IWICPalette           *pIPalette,
  _In_  IWICBitmapFrameEncode *pIFrameEncode,
  _Out_ IWICBitmapSource      **ppSourceOut
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pSourceIn* \[ Pollici\]
</dt> <dd>

Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***

Puntatore alla bitmap di origine.

</dd> <dt>

*pIPalette* \[ Pollici\]
</dt> <dd>

Tipo: **[ **IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***

Puntatore alla tavolozza da utilizzare per la codifica.

</dd> <dt>

*pIFrameEncode* \[ Pollici\]
</dt> <dd>

Tipo: **[ **IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)\***

Puntatore all'oggetto di codifica del frame.

</dd> <dt>

*ppSourceOut* \[ Cambio\]
</dt> <dd>

Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\*\***

Puntatore che riceve un puntatore all'origine di output.

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



 

 




