---
description: IWICBitmapEncoder_Initialize_Proxy funzione proxy per il metodo Initialize.
ms.assetid: 0db79eb4-dcb2-491a-9bea-a0dec418f80f
title: IWICBitmapEncoder_Initialize_Proxy funzione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICBitmapEncoder_Initialize_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ef1c51ac9693d81eb7c6cdc88c28431eacda3137a5ad73e4fa20c08c16d32509
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119812651"
---
# <a name="iwicbitmapencoder_initialize_proxy-function"></a>Funzione del proxy di inizializzazione IWICBitmapEncoder \_ \_

Funzione proxy per il [**metodo Initialize.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize)

## <a name="syntax"></a>Sintassi


```C++
HRESULT IWICBitmapEncoder_Initialize_Proxy(
  _In_ IWICBitmapEncoder           *THIS_PTR,
  _In_ IStream                     *pIStream,
  _In_ WICBitmapEncoderCacheOption cacheOption
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*QUESTO \_ PTR* \[ in\]
</dt> <dd>

Tipo: **[ **IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)\***

Puntatore a [**questo oggetto IWICBitmapEncoder.**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)

</dd> <dt>

*pIStream* \[ Pollici\]
</dt> <dd>

Tipo: **[IStream](/windows/desktop/api/objidl/nn-objidl-istream)\***

Flusso di output.

</dd> <dt>

*cacheOption* \[ Pollici\]
</dt> <dd>

Tipo: **[ **WICBitmapEncoderCacheOption**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption)**

[**WiCBitmapEncoderCacheOption usato**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmapencodercacheoption) durante l'inizializzazione.

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



 

