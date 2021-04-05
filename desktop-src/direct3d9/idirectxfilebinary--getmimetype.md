---
description: Recupera il tipo di Multipurpose Internet Mail Extensions (MIME) per i dati binari. Deprecato.
ms.assetid: 57c42ace-4313-40d8-9992-eaf12edf3a30
title: 'Metodo IDirectXFileBinary:: GetMimeType (DXFile. h)'
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
ms.openlocfilehash: 965006dc6fbad1176307341a19fd1f186e670104
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969340"
---
# <a name="idirectxfilebinarygetmimetype-method"></a>Metodo IDirectXFileBinary:: GetMimeType

Recupera il tipo di Multipurpose Internet Mail Extensions (MIME) per i dati binari. Deprecato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetMimeType(
  [out] LPCSTR *pszMimeType
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pszMimeType* \[ out\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)\***

Indirizzo di un puntatore per la ricezione della stringa di tipo MIME.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è DXFILE \_ OK. Se il metodo ha esito negativo, il valore restituito può essere DXFILEERR \_ BADVALUE.

## <a name="remarks"></a>Commenti

Quando non è specificato alcun tipo MIME in un file DirectX per un oggetto binario, la funzione imposterà pszMimeType su **null**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IDirectXFileBinary](idirectxfilebinary.md)
</dt> </dl>

 

 
