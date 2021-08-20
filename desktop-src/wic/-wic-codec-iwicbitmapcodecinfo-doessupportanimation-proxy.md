---
description: Funzione proxy per il metodo DoesSupportAnimation.
ms.assetid: dd7ed856-14b5-4215-96da-8f5db19a7796
title: IWICBitmapCodecInfo_DoesSupportAnimation_Proxy funzione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapCodecInfo_DoesSupportAnimation_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: fb67ac0a55b37b680e3d16fac26bb0303a4c2d79bd63c74f162860f47d5a9318
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118034733"
---
# <a name="iwicbitmapcodecinfo_doessupportanimation_proxy-function"></a>Funzione \_ proxy DoesSupportAnimation IWICBitmapCodecInfo \_

Funzione proxy per [**il metodo DoesSupportAnimation.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-doessupportanimation)

## <a name="syntax"></a>Sintassi


```C++
HRESULT IWICBitmapCodecInfo_DoesSupportAnimation_Proxy(
  _In_  IWICBitmapCodecInfo *THIS_PTR,
  _Out_ BOOL                *pfSupportAnimation
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*QUESTO \_ PTR* \[ in\]
</dt> <dd>

Tipo: **[ **IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)\***

Puntatore a [**questo oggetto IWICBitmapCodecInfo.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo)

</dd> <dt>

*pfSupportAnimation* \[ Cambio\]
</dt> <dd>

Tipo: **BOOL \***

Puntatore che riceve **TRUE** se il codec supporta immagini con informazioni di intervallo; in caso contrario, **FALSE.**

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



 

 




