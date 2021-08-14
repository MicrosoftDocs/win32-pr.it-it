---
description: Funzione proxy per il metodo GetEncoderInfo.
ms.assetid: 759965fd-7bc6-4130-b102-b49d1f0d4bf8
title: IWICBitmapEncoder_GetEncoderInfo_Proxy funzione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_GetEncoderInfo_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 72b423c5efb1dc4db386c5a77b15e5dabc07e05c7c740ccbc4ab411111122f65
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118207212"
---
# <a name="iwicbitmapencoder_getencoderinfo_proxy-function"></a>Funzione proxy IWICBitmapEncoder \_ GetEncoderInfo \_

Funzione proxy per il [**metodo GetEncoderInfo.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getencoderinfo)

## <a name="syntax"></a>Sintassi


```C++
HRESULT IWICBitmapEncoder_GetEncoderInfo_Proxy(
  _In_  IWICBitmapEncoder     *THIS_PTR,
  _Out_ IWICBitmapEncoderInfo **ppIEncoderInfo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*QUESTO \_ PTR* \[ in\]
</dt> <dd>

Tipo: **[ **IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***

Puntatore a [**questo oggetto IWICBitmapEncoder.**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)

</dd> <dt>

*ppIEncoderInfo* \[ Cambio\]
</dt> <dd>

Tipo: **[ **IWICBitmapEncoderInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapencoderinfo)\*\***

Puntatore che riceve un puntatore a [**un oggetto IWICBitmapEncoderInfo.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapencoderinfo)

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



 

 




