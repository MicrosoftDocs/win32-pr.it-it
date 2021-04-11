---
description: Funzione proxy per il metodo GetFileExtensions.
ms.assetid: 1c9232c5-54f3-4186-a1c8-4531e8357d06
title: Funzione IWICBitmapCodecInfo_GetFileExtensions_Proxy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_GetFileExtensions_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: 7dc44622bb7d576bfe4dc8a70e69779a72c1c07b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343231"
---
# <a name="iwicbitmapcodecinfo_getfileextensions_proxy-function"></a>IWICBitmapCodecInfo \_ GetFileExtensions- \_ funzione proxy

Funzione proxy per il metodo [**GetFileExtensions**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-getfileextensions) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT IWICBitmapCodecInfo_GetFileExtensions_Proxy(
  _In_    IWICBitmapCodecInfo *THIS_PTR,
  _In_    UINT                cchFileExtensions,
  _Inout_ WCHAR               *wzFileExtensions,
  _Inout_ UINT                *pcchActual
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Questa \_ PTR* \[ in\]
</dt> <dd>

Tipo: **[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _

Puntatore a questo oggetto [_ *IWICBitmapCodecInfo* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) .

</dd> <dt>

*cchFileExtensions* \[ in\]
</dt> <dd>

Tipo: **uint**

Dimensioni del buffer dell'estensione del nome file.

</dd> <dt>

*wzFileExtensions* \[ in uscita\]
</dt> <dd>

Tipo: **WCHAR \** _

Puntatore che riceve le estensioni dei nomi di file associate al codec.

</dd> <dt>

_pcchActual * \[ in uscita\]
</dt> <dd>

Tipo: **uint \** _

Dimensioni effettive del buffer necessarie per recuperare tutte le estensioni dei nomi di file associate al codec.

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



 

 




