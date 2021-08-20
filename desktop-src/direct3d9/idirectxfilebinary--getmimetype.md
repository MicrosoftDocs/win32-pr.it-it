---
description: Recupera il Multipurpose Internet Mail Extensions (MIME) per i dati binari. Deprecato.
ms.assetid: 57c42ace-4313-40d8-9992-eaf12edf3a30
title: Metodo IDirectXFileBinary::GetMimeType (DXFile.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileBinary.GetMimeType
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 1a3443577a8d7b837ce43ef468d28d01ebde7b265b4e27dd72c481329b7003e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118093476"
---
# <a name="idirectxfilebinarygetmimetype-method"></a>Metodo IDirectXFileBinary::GetMimeType

Recupera il Multipurpose Internet Mail Extensions (MIME) per i dati binari. Deprecato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetMimeType(
  [out] LPCSTR *pszMimeType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pszMimeType* \[ Cambio\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)\***

Indirizzo di un puntatore per ricevere la stringa di tipo MIME.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è DXFILE \_ OK. Se il metodo ha esito negativo, il valore restituito può essere DXFILEERR \_ BADVALUE.

## <a name="remarks"></a>Commenti

Quando non è specificato alcun tipo MIME in un file DirectX per un oggetto binario, la funzione imposta pszMimeType su **NULL.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IDirectXFileBinary](idirectxfilebinary.md)
</dt> </dl>

 

 
