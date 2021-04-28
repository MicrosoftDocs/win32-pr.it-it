---
description: IWICFastMetadataEncoder_GetMetadataQueryWriter_Proxy funzione proxy per il metodo GetMetadataQueryWriter.
ms.assetid: 64d2c6d8-f1dd-4397-8487-4d23c69aea82
title: IWICFastMetadataEncoder_GetMetadataQueryWriter_Proxy funzione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICFastMetadataEncoder_GetMetadataQueryWriter_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: b06bc6fbcdc65c9d1163ccb4a862d6046b455c9a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097169"
---
# <a name="iwicfastmetadataencoder_getmetadataquerywriter_proxy-function"></a>Funzione proxy IWICFastMetadataEncoder \_ GetMetadataQueryWriter \_

Funzione proxy per il [**metodo GetMetadataQueryWriter.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicfastmetadataencoder-getmetadataquerywriter)

## <a name="syntax"></a>Sintassi


```C++
HRESULT IWICFastMetadataEncoder_GetMetadataQueryWriter_Proxy(
  _In_  IWICBitmapFrameDecode   *THIS_PTR,
  _Out_ IWICMetadataQueryWriter **ppIMetadataQueryWriter
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*QUESTO \_ PTR* \[ in\]
</dt> <dd>

Tipo: **[ **IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)\***

Puntatore a [**questo oggetto IWICBitmapFrameDecode.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)

</dd> <dt>

*ppIMetadataQueryWriter* \[ Cambio\]
</dt> <dd>

Tipo: **[ **IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter)\*\***

Puntatore che riceve un puntatore al writer di query dei metadati del codificatore.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **HRESULT**

Se questa funzione ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="remarks"></a>Osservazioni

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows XP con SP2, solo app desktop di Windows Vista \[\]<br/>                                                                                              |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2008 \[\]<br/>                                                                                                             |
| DLL<br/>                      | <dl> <dt>Windowscodecs.dll; </dt> <dt>Wincodec.lib</dt> </dl> |



 

 




