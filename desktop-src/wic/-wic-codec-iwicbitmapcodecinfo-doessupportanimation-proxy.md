---
description: Funzione proxy per il metodo DoesSupportAnimation.
ms.assetid: dd7ed856-14b5-4215-96da-8f5db19a7796
title: Funzione IWICBitmapCodecInfo_DoesSupportAnimation_Proxy
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
ms.openlocfilehash: 443a8ec7871af6161de2efbb6d4f21d65e5ae9d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306684"
---
# <a name="iwicbitmapcodecinfo_doessupportanimation_proxy-function"></a>IWICBitmapCodecInfo \_ DoesSupportAnimation- \_ funzione proxy

Funzione proxy per il metodo [**DoesSupportAnimation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapcodecinfo-doessupportanimation) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT IWICBitmapCodecInfo_DoesSupportAnimation_Proxy(
  _In_  IWICBitmapCodecInfo *THIS_PTR,
  _Out_ BOOL                *pfSupportAnimation
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Questa \_ PTR* \[ in\]
</dt> <dd>

Tipo: **[**IWICBitmapCodecInfo**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) \** _

Puntatore a questo oggetto [_ *IWICBitmapCodecInfo* *](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecinfo) .

</dd> <dt>

*pfSupportAnimation* \[ out\]
</dt> <dd>

Tipo: **bool \** _

Puntatore che riceve _ *true** se il codec supporta immagini con informazioni sull'intervallo; in caso contrario, **false**.

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



 

 




