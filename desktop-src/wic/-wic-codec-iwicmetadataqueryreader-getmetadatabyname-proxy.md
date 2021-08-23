---
description: Funzione proxy per il metodo GetMetadataByName.
ms.assetid: 5685e282-637e-4db0-8654-fee12ae25112
title: IWICMetadataQueryReader_GetMetadataByName_Proxy funzione
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWICMetadataQueryReader_GetMetadataByName_Proxy
api_type:
- DllExport
api_location:
- Windowscodecs.dll
- Wincodec.lib
ms.openlocfilehash: c84d8d6e93c3f5edf223811844937fd1d223a1a3df991e9d62dd24c2fa445ce9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119088233"
---
# <a name="iwicmetadataqueryreader_getmetadatabyname_proxy-function"></a>Funzione proxy IWICMetadataQueryReader \_ GetMetadataByName \_

Funzione proxy per il [**metodo GetMetadataByName.**](/windows/desktop/api/Wincodec/nf-wincodec-iwicmetadataqueryreader-getmetadatabyname)

## <a name="syntax"></a>Sintassi


```C++
HRESULT IWICMetadataQueryReader_GetMetadataByName_Proxy(
  _In_    IWICMetadataQueryReader *THIS_PTR,
  _In_    LPCWSTR                 wzName,
  _Inout_ PROPVARIANT             *pvarValue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*QUESTO \_ PTR* \[ in\]
</dt> <dd>

Tipo: **[ **IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)\***

Puntatore a [**questo oggetto IWICMetadataQueryReader.**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader)

</dd> <dt>

*wzName* \[ Pollici\]
</dt> <dd>

Tipo: **LPCWSTR**

Nome dell'elemento di metadati richiesto.

</dd> <dt>

*pvarValue* \[ in, out\]
</dt> <dd>

Tipo: **[PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)\***

Puntatore che riceve la proprietà dei metadati.

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



 

