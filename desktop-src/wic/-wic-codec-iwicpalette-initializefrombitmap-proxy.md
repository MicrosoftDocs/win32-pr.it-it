---
description: Funzione proxy per il metodo InitializeFromBitmap.
ms.assetid: 9559a56d-7201-4b39-a3cd-9c0e4eac611a
title: IWICPalette_InitializeFromBitmap_Proxy funzione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICPalette_InitializeFromBitmap_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 5c807e95b980a564096216727315f4a1534e8cd011cc78aa7322f670fff0876c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119088183"
---
# <a name="iwicpalette_initializefrombitmap_proxy-function"></a>Funzione proxy IWICPalette \_ InitializeFromBitmap \_

Funzione proxy per il [**metodo InitializeFromBitmap.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicpalette-initializefrombitmap)

## <a name="syntax"></a>Sintassi


```C++
HRESULT IWICPalette_InitializeFromBitmap_Proxy(
  _In_ IWICPalette      *THIS_PTR,
  _In_ IWICBitmapSource *pISurface,
  _In_ UINT             colorCount,
  _In_ BOOL             fAddTransparentColor
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*QUESTO \_ PTR* \[ in\]
</dt> <dd>

Tipo: **[ **IWICPalette**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)\***

Puntatore a [**questo oggetto IWICPalette.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicpalette)

</dd> <dt>

*pISurface* \[ Pollici\]
</dt> <dd>

Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***

Puntatore alla bitmap di origine.

</dd> <dt>

*colorCount* \[ Pollici\]
</dt> <dd>

Tipo: **UINT**

Numero di colori con cui inizializzare la tavolozza.

</dd> <dt>

*fAddTransparentColor* \[ Pollici\]
</dt> <dd>

Tipo: **BOOL**

Valore che indica se aggiungere un colore trasparente.

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



 

 




