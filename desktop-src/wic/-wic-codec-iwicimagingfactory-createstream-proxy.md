---
description: Funzione proxy per il metodo CreateStream.
ms.assetid: c827e1aa-13ae-459e-a1dc-5ff8c31a54bc
title: IWICImagingFactory_CreateStream_Proxy funzione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICImagingFactory_CreateStream_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: ec69a5cb9fe03fe6ebb1e9c31ac27fe2a81ab8df69ed5595c877ba5064e17953
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119088223"
---
# <a name="iwicimagingfactory_createstream_proxy-function"></a>Funzione proxy IWICImagingFactory \_ \_ CreateStream

Funzione proxy per il [**metodo CreateStream.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createstream)

## <a name="syntax"></a>Sintassi


```C++
HRESULT IWICImagingFactory_CreateStream_Proxy(
  _In_  IWICImagingFactory *pFactory,
  _Out_ IWICStream         **ppIWICStream
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pFactory* \[ Pollici\]
</dt> <dd>

Tipo: **[ **IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory)\***

</dd> <dt>

*ppIWICStream* \[ Cambio\]
</dt> <dd>

Tipo: **[ **IWICStream**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)\*\***

Puntatore che riceve un puntatore a un nuovo [**IWICStream.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicstream)

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



 

 




