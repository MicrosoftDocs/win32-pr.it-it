---
description: Funzione proxy per il metodo GetSize.
ms.assetid: a9b7d01c-78d9-47b8-a373-a7c49f7bccfd
title: Funzione IWICBitmapSource_GetSize_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapSource_GetSize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 978748125b7c7f643027077182b9136b577cb00c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313432"
---
# <a name="iwicbitmapsource_getsize_proxy-function"></a>\_Funzione proxy IWICBitmapSource GetSize \_

Funzione proxy per il metodo [**GetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT IWICBitmapSource_GetSize_Proxy(
  _In_  IWICBitmapSource *THIS_PTR,
  _Out_ UINT             *puiWidth,
  _Out_ UINT             *puiHeight
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Questa \_ PTR* \[ in\]
</dt> <dd>

Tipo: **[**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) \** _

Puntatore a questo oggetto [_ *IWICBitmapSource* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) .

</dd> <dt>

*puiWidth* \[ out\]
</dt> <dd>

Tipo: **uint \** _

Puntatore che riceve la larghezza in pixel della bitmap.

</dd> <dt>

_puiHeight * \[ out\]
</dt> <dd>

Tipo: **uint \** _

Puntatore che riceve l'altezza in pixel della bitmap

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



 

 




