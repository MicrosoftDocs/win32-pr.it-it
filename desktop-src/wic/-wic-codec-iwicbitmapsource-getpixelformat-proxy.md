---
description: Funzione proxy per il metodo GetPixelFormat.
ms.assetid: 0879bfb7-0175-4275-a093-a69b39c66a41
title: Funzione IWICBitmapSource_GetPixelFormat_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_GetPixelFormat_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ff795dd028c8d8f1e18a944df60a87f1e7cee670
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313431"
---
# <a name="iwicbitmapsource_getpixelformat_proxy-function"></a>IWICBitmapSource \_ GetPixelFormat- \_ funzione proxy

Funzione proxy per il metodo [**GetPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT IWICBitmapSource_GetPixelFormat_Proxy(
  _In_  IWICBitmapSource   *THIS_PTR,
  _Out_ WICPixelFormatGUID *pPixelFormat
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Questa \_ PTR* \[ in\]
</dt> <dd>

Tipo: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _

Puntatore a questo oggetto [_ *IWICBitmapSource* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) .

</dd> <dt>

*pPixelFormat* \[ out\]
</dt> <dd>

Tipo: **WICPixelFormatGUID \** _

Puntatore che riceve il GUID del formato pixel in cui è archiviata la bitmap.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: _ *HRESULT**

Se questa funzione ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="remarks"></a>Osservazioni

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP con SP2, \[ solo app desktop di Windows Vista\]<br/>                                                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec. lib</dt> </dl> |



 

 




