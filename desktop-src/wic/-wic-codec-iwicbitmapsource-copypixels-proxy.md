---
description: Funzione proxy per il metodo CopyPixels.
ms.assetid: 020c11e9-0847-468e-b240-20529f6460cd
title: IWICBitmapSource_CopyPixels_Proxy funzione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_CopyPixels_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: e9c847680a93cb245b0e5d4247cb60b82629ea82eba12313dbcff7303dcce707
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119772341"
---
# <a name="iwicbitmapsource_copypixels_proxy-function"></a>Funzione proxy IWICBitmapSource \_ CopyPixels \_

Funzione proxy per [**il metodo CopyPixels.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels)

## <a name="syntax"></a>Sintassi


```C++
HRESULT IWICBitmapSource_CopyPixels_Proxy(
  _In_        IWICBitmapSource *THIS_PTR,
  _In_  const WICRect          *prc,
  _In_        UINT             cbStride,
  _In_        UINT             cbBufferSize,
  _Out_       BYTE             *pbBuffer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*QUESTO \_ PTR* \[ in\]
</dt> <dd>

Tipo: **[ **IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)\***

Puntatore a [**questo oggetto IWICBitmapSource.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource)

</dd> <dt>

*prc* \[ Pollici\]
</dt> <dd>

Tipo: **const [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect) \***

Rettangolo da copiare. Un valore NULL specifica l'intera bitmap.

</dd> <dt>

*cbStride* \[ Pollici\]
</dt> <dd>

Tipo: **UINT**

Stride della bitmap

</dd> <dt>

*cbBufferSize* \[ Pollici\]
</dt> <dd>

Tipo: **UINT**

Dimensione del buffer.

</dd> <dt>

*pbBuffer* \[ Cambio\]
</dt> <dd>

Tipo: **\* BYTE**

Puntatore al buffer.

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



 

 




